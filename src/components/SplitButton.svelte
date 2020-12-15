<script>
    export let level='';
    export let size='';
    export let title='';

    const _level = level ? `btn-${level}` : '';
    let _size ='';
    switch (size){
        case 'small':
            _size = 'btn-'+'sm';
            break;
        case 'large':
            _size = 'btn-'+'lg';
            break;
        default:
            break;
    }
</script>

<button class="btn {_level} btn-icon-split {_size}" on:click>
    <span class="icon text-white-50">
        <slot/>
    </span>
    <span class="text">{title}</span>
</button>