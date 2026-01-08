# 1.关于useMemo和jotai的atom的组合
```
// 首页组件，每次调用都会渲染
function IndexComponent() {
// 读取关注的数据源
const focusSources = useAtomValue(focusSourcesAtom)
// eslint-disable-next-line react-hooks/exhaustive-deps
// 如果存在关注数据源， 则选择关注列，否则选择最热列，useMemo中选择[]表示只执行一次，后续都不判断， 假如写成[focusSources.length]则每次读取都会判断这个值
// 其中因为首次调用后页面停留在"focus" : "hottest"， 所以即使点了关注也不会切换列， 需要手动刷新页面才能切换列
const id = useMemo(() => focusSources.length ? "focus" : "hottest", [focusSources.length])
// 渲染Column组件
return <Column id={id} />

}
```
情况1：userMemo的参数为空数组， 则focusSourcesAtom发生变化时，组件重新渲染， 但是Column都是使用上次的值，useMemo上次调用的值，所以页面不会发生变化
情况2：userMemo的参数为focusSources.length，则focusSourcesAtom发生变化时，组件重新渲染， 此时会重新计算id， 得到新的渲染页面。