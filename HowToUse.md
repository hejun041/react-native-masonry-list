```javascript
<Masonry
    sorted
    containerWidth={super.getWidth()}
    columns={2} // optional - Default: 2
    initialColToRender={2}
    initialNumInColsToRender={3}
    spacing={0}
    images={this.images}
    contentContainerStyle={{
        flexWrap: 'wrap',
        flexDirection: "row",
    }}
    completeCustomComponent={(props) => <CustomMasonryItem {...props} hasHeader />}
    masonryFlatListColProps={{
        onEndReachedThreshold: 0.2,
        onEndReached: this._onEndReached,
        ListHeaderComponent: this._renderHeader.bind(this),
        ListFooterComponent: this.images.length != 0 && (this.loadEnd ?this._renderNoMore: this._renderLoading)
    }}
/>
```
![react-native-masonry-list](https://github.com/hejun041/react-native-masonry-list/blob/master/src/assets/test.gif?raw=true)
