Requirements
===
You need to have NPM and Bower installed.

```
 npm install && bower install
```

Then - obvious - GunUi needs Gun, so you do have to install that.

```
 nmp install gun
```

> GunUi tries to stay up to date with new Gun releases...right now it works with <b>gun version 7.x</b>

Include gun in your main file

```
 <script src="../node_modules/gun/gun.min.js"></script>
```

<b>Important!</b><br>
Do not instantiate Gun...aka <b>DO NOT</b> do `var gun = Gun()` <br>
This will be handled by a supporting element `<gun-ui-mixin`>.

Gun options
===
If you need to set Gun options you will have to put this in your main file to
```
<script>
	let gun_options = {
		<!-- options like you would normally set -->
		peers:['http://my-gun-server/gun']
	}
</script>
```

`gun_options` will be implemented by `<gun-ui-mixin>` 
>  `<gun-ui-mixin>` is a <i>supporting</i> element.<br>you never have to install 'supporting' elements yourself, this will be handled by GunUi.