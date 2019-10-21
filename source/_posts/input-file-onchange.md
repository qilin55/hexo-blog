# `input onchange`事件触发问题

### input在上传图片时，如果上传的图片跟之前最后一张上传的是同一张，就触发不了`onchange`事件

```javascript
<input ref='fileUpload' onChange={this.getFile} id="fileUpload" type="file" className="upload"/>
```

### 这是因为`input`的value值没有改变，需要我们手动清空一下,需要注意的是清空value需要在图片上传完成后再清空，不然会上传失败
```javascript
this.refs.fileUpload.value = null
```
