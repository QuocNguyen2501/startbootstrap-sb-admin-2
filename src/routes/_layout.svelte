<script>
    import Sidebar from '../components/Sidebar.svelte';
    import { scrollto } from "svelte-scrollto";
    import { fade, fly } from 'svelte/transition';
    
	export let segment;
    export let isLogin = false;
    
    let visible = false;
    let y;

    $: visible = y > 100 ? true: false;

</script>

<style>
	
</style>


<svelte:window bind:scrollY={y}/>

{#if segment === 'login' || segment === 'register' || segment === 'forgotPassword'}
	<main>
		<slot></slot>
	</main>
{:else}
	<div id="wrapper">
		<Sidebar {segment}/>
		<slot></slot>
	</div>

    {#if visible}
        <a class="scroll-to-top rounded" in:fly="{{ duration: 2000 }}" out:fade use:scrollto={'#sapper',{duration: 2000}}>
            <i class="fas fa-angle-up"></i>
        </a>
    {/if}
	<!-- Logout Modal-->
    <div class="modal fade" id="logoutModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel"
        aria-hidden="true">
        <div class="modal-dialog" role="document">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="exampleModalLabel">Ready to Leave?</h5>
                    <button class="close" type="button" data-dismiss="modal" aria-label="Close">
                        <span aria-hidden="true">×</span>
                    </button>
                </div>
                <div class="modal-body">Select "Logout" below if you are ready to end your current session.</div>
                <div class="modal-footer">
                    <button class="btn btn-secondary" type="button" data-dismiss="modal">Cancel</button>
                    <a class="btn btn-primary" href="/login">Logout</a>
                </div>
            </div>
        </div>
    </div>
{/if}
