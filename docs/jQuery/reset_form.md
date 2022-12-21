## 表格
```HTML
<form id="form_id">
    <label>测试输入框:</label>
    <input type="text" name="test_input">
    <label>测试下拉框:</label>
    <select id="test_select" name="test_select">
        <option value="1">1</option>
        <option value="2">2</option>
    </select>
</form>
```

## JavaScript
```JS
// 清空表单
$('#form_id')[0].reset()
// 清空下拉框
$('#test_select').val(null).trigger("change");
```