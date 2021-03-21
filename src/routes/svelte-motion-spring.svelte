<script>
  import { spring } from 'svelte/motion';

  let coords = spring(
    { x: 50, y: 50 },
    {
      stiffness: 0.4,
      damping: 0.1,
    },
  );

  let size = spring(10);
</script>

<svg
  on:mousemove={(e) => coords.set({ x: e.clientX, y: e.clientY })}
  on:mousedown={() => size.set(30)}
  on:mouseup={() => size.set(10)}
>
  <circle cx={$coords.x} cy={$coords.y} r={$size} />
</svg>

<style>
  * {
    cursor: none;
  }

  svg {
    width: 100%;
    height: 100%;
    position: absolute;
    left: 0;
    top: 0;
  }

  circle {
    fill: #ff3e00;
  }
</style>
