

FlatList性能明显优于ListView

```
<FlatList
    data={this.state.articles}
    extraData={this.state}
    keyExtractor={(article)=>{return article.id;}}
    renderItem={this._renderItem}
    onRefresh={()=>{this._refresh(1)}}
    refreshing={false}
    onEndReached={this._end_next_page}
    onEndReachedThreshold={0.1}
    initialNumToRender={7}
    ListFooterComponent={this._footerComponent}
    getItemLayout={this._itemLayout}
    />
```

最佳实践是添加getItemLayout，这个方法可以明显优化列表渲染效率

另外一点是，当列表为空时，同样会触发onRefresh

Item组件尽量继承PureComponent





