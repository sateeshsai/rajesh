<script>
  export let iconBackgroundColor;
  export let iconColor;
  export let itemIconOpacity;
  export let iconStrokeWidth;
</script>

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 412 412" xml:space="preserve"
  ><circle cx="206" cy="206" r="206" fill={iconBackgroundColor} fill-opacity={itemIconOpacity} /><path
    fill="none"
    stroke={iconColor}
    stroke-width={iconStrokeWidth}
    stroke-linecap="round"
    stroke-linejoin="round"
    stroke-miterlimit={iconStrokeWidth + iconStrokeWidth / 2}
    d="M248 309.9 120.6 203.6l122.7-101.5"
  /></svg
>

<style>
  svg {
    transform: rotate(180deg);
  }
</style>
