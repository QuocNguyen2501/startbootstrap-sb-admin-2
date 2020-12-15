<script>
    export let level='';
    export let exClass='';
    export let size='';

    const _level = level ? `btn-${level}` : '';
    const _exClass = exClass ? `btn-${exClass}` : '';
</script>

<button class="btn {_level} {_exClass} {size}" on:click>
    <slot></slot>
</button>