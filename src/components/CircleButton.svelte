<script>
    import Button from './Button.svelte';
    export let level='success';
    export let size='';

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

<Button size={_size} {level} exClass='circle' on:click>
    <slot></slot>
</Button>