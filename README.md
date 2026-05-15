# ruich
<p align="center">
  <img src="./Ruich.png" />
</p>
A small svelte ui lib

# Dark/Light mode
Use `mode-watcher`

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
