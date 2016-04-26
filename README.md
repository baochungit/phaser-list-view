# List View classes for Phaser

## Install
`npm install phaser-list-view --save`

## API
- Scroller : A pure logic scroller built for scrolling on the x and y axis.
- ListView : An iOS-like ListView class. Uses Scroller for the input and outputs a ListView. Performance is good because we cull off-screen items.
Perfect for high scoreboards.
- SwipeCarousel : An iOS-like SwipeCarousel. Uses Scroller for the input and outputs a SwipeCarousel. Perfect for instructions screens, or a photo gallery.

## ListView Usage
```
import {ListView} from 'phaser-list-view'

let parent = this.world
let bounds = Phaser.Rectangle(0, 0, 300, 400)
let options = {
  direction: 'y',
  overflow: 100,
  padding: 10
}

let listView = new ListView(this.game, parent, bounds, options)
let items = this.createSomeDisplayObjectsAndReturnAnArray() // [Graphics, Image, Sprite]
listView.addMultiple(...items)
```

## SwipeCarousel Usage
```
import {SwipeCarousel} from 'phaser-list-view'

let parent = this.world
let bounds = Phaser.Rectangle(0, 0, 300, 400)
let options = {
  direction: 'x',
  overflow: 100,
  padding: 10
}

let swipeCarousel = new SwipeCarousel(this.game, parent, bounds, options)
let photos = this.getAnArrayOfImages() // [Image, Image, Image, Image]
swipeCarousel.addMultiple(...photos)
```

## Scroller Usage
// TODO