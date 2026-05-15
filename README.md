# Ruich Ui
<p align="center">
  <img src="./Ruich.png" />
</p>
A small svelte ui lib

## Dark/Light mode
Use ![mode-watcher](https://github.com/svecosystem/mode-watcher) [![npm](https://img.shields.io/badge/npm-CB3837?logo=npm&logoColor=fff)]([#](https://www.npmjs.com/package/mode-watcher))

### Install ModeWatcher:
  `npm install mode-watcher`
### Add ModeWatcher to layout
```svelte title="+layout.svelte"
<script>
  import { ModeWatcher } from "mode-watcher";
  // ...
</script>

<ModeWatcher/>
/ ...
```
### Theme swith
```svelte
<script>
  import { toggleMode } from 'mode-watcher';
</script>

<button onclick={toggleMode}>
  Swith mode
</button>
```
## ToDo

- [ ] Button
- [x] Flex
- [ ] Field
- [ ] Kbd
- [ ] Badge
- [ ] Avatar
- [ ] Alert dialog
- [ ] Spinner
