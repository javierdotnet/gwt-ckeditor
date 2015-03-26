#How to handle the save event

# Introduction #

It is interresting to handle the save element (i.e. When the user clicks on the Save button) because it allows the interface to be more user friendly.


# Details #

To handle the save event, you just have to proceed like any other event in GWT :
```
CKEditor ckEditor = new CKEditor(CKConfig.full);

ckEditor.addSaveHandler(new SaveHandler<CKEditor>() {
    @Override
    public void onSave(SaveEvent<CKEditor> event) {
        CKEditor target = event.getTarget();//The CKEditor which generates the save event
        String content = event.getText();//The content to save (also available in target)
    }
});
```