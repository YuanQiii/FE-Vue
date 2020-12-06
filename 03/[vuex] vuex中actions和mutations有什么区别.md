# vuex中actions和mutations有什么区别

## mutations

- mutations可以直接修改state，但只能包含同步操作
- 只能通过提交commit调用(尽量通过Action或mapMutation调用而非直接在组件中通过this.$store.commit()提交)

## actions

- actions是用来触发mutations的
- 它无法直接改变state，它可以包含异步操作