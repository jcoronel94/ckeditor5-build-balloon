CKEditor 5 balloon editor build
==============================================

[![Join the chat at https://gitter.im/ckeditor/ckeditor5](https://badges.gitter.im/ckeditor/ckeditor5.svg)](https://gitter.im/ckeditor/ckeditor5?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![npm version](https://badge.fury.io/js/%40ckeditor%2Fckeditor5-build-balloon.svg)](https://www.npmjs.com/package/@ckeditor/ckeditor5-build-balloon)
[![Dependency Status](https://david-dm.org/ckeditor/ckeditor5-build-balloon/status.svg)](https://david-dm.org/ckeditor/ckeditor5-build-balloon)
[![devDependency Status](https://david-dm.org/ckeditor/ckeditor5-build-balloon/dev-status.svg)](https://david-dm.org/ckeditor/ckeditor5-build-balloon?type=dev)

The balloon editor build. Read more in the [balloon editor](https://ckeditor5.github.io/docs/nightly/ckeditor5/latest/builds/guides/overview.html#Balloon-editor) and see the [demo](https://ckeditor5.github.io/docs/nightly/ckeditor5/latest/examples/builds/balloon-editor.html).

## Documentation

See:

* [Installation](https://ckeditor5.github.io/docs/nightly/ckeditor5/latest/builds/guides/integration/installation.html) for how to install this package and what it contains.
* [Basic API](https://ckeditor5.github.io/docs/nightly/ckeditor5/latest/builds/guides/integration/basic-api.html) for how to create an editor and interact with it.
* [Configuration](https://ckeditor5.github.io/docs/nightly/ckeditor5/latest/builds/guides/integration/configuration.html) for how to configure the editor.
* [Creating custom builds](https://ckeditor5.github.io/docs/nightly/ckeditor5/latest/builds/guides/development/custom-builds.html) for how to customize the build (configure and rebuild the editor bundle).

## Quick start

First, install the build from npm:

```
npm install --save @ckeditor/ckeditor5-build-balloon
```

And use it in your website:

```html
<div id="editor">
	<p>This is the editor content.</p>
</div>
<script src="./node_modules/@ckeditor/ckeditor5-build-balloon/build/ckeditor.js"></script>
<script>
	BalloonEditor
		.create( document.querySelector( '#editor' ) )
		.then( editor => {
			window.editor = editor;
		} )
		.catch( err => {
			console.error( err.stack );
		} );
</script>
```

Or in your JavaScript application:

```js
import BalloonEditor from '@ckeditor/ckeditor5-build-balloon/build/ckeditor';

// Or using CommonJS verion:
// const BalloonEditor = require( '@ckeditor/ckeditor5-build-balloon/build/ckeditor' );

BalloonEditor
	.create( document.querySelector( '#editor' ) )
	.then( editor => {
		window.editor = editor;
	} )
	.catch( err => {
		console.error( err.stack );
	} );
```

**Note:** If you are planning to integrate CKEditor 5 deep into your application it is actually more convenient and recommended to install and import the source modules directly (like it happens in `ckeditor.js`). Read more in the [Bundling guide](https://ckeditor5.github.io/docs/nightly/ckeditor5/latest/builds/guides/integration/bundling.html).

## License

Licensed under the GPL, LGPL and MPL licenses, at your choice. For full details about the license, please check the `LICENSE.md` file.