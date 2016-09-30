# react-tabbar-navigator
React Native Tabbar Navigation

("https://github.com/mdnahian/react-tabbar-navigator/blob/master/screenshot.png")

### Install
```
npm i react-tabbar-navigator
```

### Usage
```javascript
import React, { Component } from 'react';

var Tabbar = require('react-tabbar-navigator');

var Settings = require('../pages/settings');
var Home = require('../pages/home');
var Contact = require('../pages/contact');

module.exports = React.createClass({
	getInitialState: function () {
		return	{
			initialRoute: 'home',
			views: {
				settings: Settings,
				home: Home,
				contact: Contact
			},
			images: [
				[require('../img/home.png'), 'home'],
				[require('../img/settings.png'), 'settings'],
				[require('../img/contact.png'), 'contact']
			],
			underlayColor: '#dedede'
		}
	},
	render: function () {
		return <Tabbar config={this.state} />
	}
});
```
