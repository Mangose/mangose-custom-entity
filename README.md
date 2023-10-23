<p align="center">
  <img src="https://cdn.mangose.app/assets/mangose.png" width="200" alt="Mangose Logo" />
</p>

# Mangose Custom View Tutorial
You can create your own views and share them with other users.

## Requirements:
- You need to upload your custom view to github as a public repo
- Use our tag system to keep it looking similar to mangose
- Have fun.

## Required files on the repo:
- script.js
- manifest.json
- index.html

## Example manifest.json
```json
{
  "name": "custom-view-name",
  "version": "1.0",
  "author": "Your name",
  "manifest_version": 1,
  "view": "index.html",
  "script": "script.js"
}
```

## Example index.html
```html
<view>
  <label>This label show text</label>
  <container border='true' type='column' gap='4'>
    <header>Header show bigger text</header>
    <container gap='4'>
      <button type='primary'>Button 1</button>
      <button type='primary'>Button 2</button>
    </container>
  </container>
</view>
```

Each view should be in a ```<view>``` tag

```<label>``` displays text
  Props: 
  - margin - 1...4
  
```container``` displays several items
  Props: 
  - border - true/false - container border
  - type - column/row - how to display items
  - gap - 1..4 - elements distance

```button``` displays the button
 Props: 
  - type - default/primary

## Example script.html
```js
window.mounted = () => {
  console.log('Hello world')
}
```


## JS API
```js
mangose.isDarkMode // return true or false
mangose.user // user info
mangose.addTask: (taskName, sectionId)
mangose.addProp: (propName, propType)
mangose.openTask: (taskId)
mangose.trigger: (triggerId)
```
