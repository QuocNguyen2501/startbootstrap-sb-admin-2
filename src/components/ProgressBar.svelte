<script>
    export let title='';
    export let percent = 0;
    export let minVal;
    export let maxVal;
    export let mode='';
    export let isCompleted = false;

    import { spring } from 'svelte/motion';

	let width = spring(0, {
		stiffness: 0.1,
		damping: 0.25
	});

    let _mode = ''
    switch (mode) {
        case 'danger':
            _mode = 'bg-danger';
            break;
        case 'warning':
            _mode = 'bg-warning';
            break;
        case 'info':
            _mode = 'bg-info';
            break;
        case 'success':
            _mode = 'bg-success';
            break;
        default:
            _mode =''
            break;
    }
    $: width = percent+"%";
</script>

{#if title.length > 0}
    <h4 class="small font-weight-bold">{title}
        {#if isCompleted == false}
            <span class="float-right">{percent}%</span>
        {:else}
            <span class="float-right">Complete!</span>
        {/if}
    </h4>
{/if}
<div class="progress mb-4">
<div class="progress-bar {_mode}" role="progressbar" width={width}
    aria-valuenow="{percent}" aria-valuemin="{minVal}" aria-valuemax="{maxVal}"></div>
</div>