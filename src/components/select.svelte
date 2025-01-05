<script>
 export let value = '';
 export let onSelect;
</script>

<style>
 select {
  display: flex;
  flex-grow: 1;
  padding: 0 10px;
  border: 0;
  outline: 0;
  font-family: inherit;
  font-size: inherit;
  border: 1px solid #888;
  border-radius: 10px;
  text-align: center;
  cursor: pointer;
 }
</style>

<select {value} on:select={() => onSelect({ value })}>
 <slot></slot>
</select>
