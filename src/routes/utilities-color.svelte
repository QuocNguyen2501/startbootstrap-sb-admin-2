<script>
    import Footer from "../components/Footer.svelte";
    import Topbar from "../components/Topbar.svelte";
    import PageHeading from "../components/PageHeading.svelte";
    
    let title = 'Color Utilities';
    let description = 'Bootstrap\'s default utility classes can be found on the official <a href="https://getbootstrap.com/docs">Bootstrap Documentation</a> page. The custom utilities below were created to extend this theme past the default utility classes built into Bootstrap\'s framework.';

    const colorArr = [
        'text-gray-100',
        'text-gray-200',
        'text-gray-300',
        'text-gray-400',
        'text-gray-500',
        'text-gray-600',
        'text-gray-700',
        'text-gray-800',
        'text-gray-900',
    ];

    const bgGradientArr = [
        'bg-gradient-primary',
        'bg-gradient-secondary',
        'bg-gradient-success',
        'bg-gradient-info',
        'bg-gradient-warning',
        'bg-gradient-danger',
        'bg-gradient-light',
        'bg-gradient-dark'
    ];

    const bgGrayArr = [
        'bg-gray-100',
        'bg-gray-200',
        'bg-gray-300',
        'bg-gray-400',
        'bg-gray-500',
        'bg-gray-600',
        'bg-gray-700',
        'bg-gray-800',
        'bg-gray-900',
    ];

</script>

<div id="content-wrapper" class="d-flex flex-column">

    <!-- Main Content -->
    <div id="content">

       <Topbar />

        <!-- Begin Page Content -->
        <div class="container-fluid">

        <PageHeading {title} {description}/>

            <!-- Content Row -->
            <div class="row">

                <!-- First Column -->
                <div class="col-lg-4">

                    <!-- Custom Text Color Utilities -->
                    <div class="card shadow mb-4">
                        <div class="card-header py-3">
                            <h6 class="m-0 font-weight-bold text-primary">Custom Text Color Utilities</h6>
                        </div>
                        <div class="card-body">
                            {#each colorArr as color, index}
                                {#if index < 4 }
                                <p class="{color} p-3 bg-dark m-0">.{color}</p>
                                {:else}
                                <p class="{color} p-3 m-0">.{color}</p>
                                {/if}
                            {/each}
                        </div>
                    </div>

                    <!-- Custom Font Size Utilities -->
                    <div class="card shadow mb-4">
                        <div class="card-header py-3">
                            <h6 class="m-0 font-weight-bold text-primary">Custom Font Size Utilities</h6>
                        </div>
                        <div class="card-body">
                            <p class="text-xs">.text-xs</p>
                            <p class="text-lg mb-0">.text-lg</p>
                        </div>
                    </div>

                </div>

                <!-- Second Column -->
                <div class="col-lg-4">

                    <!-- Background Gradient Utilities -->
                    <div class="card shadow mb-4">
                        <div class="card-header py-3">
                            <h6 class="m-0 font-weight-bold text-primary">Custom Background Gradient Utilities
                            </h6>
                        </div>
                        <div class="card-body">
                            {#each bgGradientArr as bgGradien}
                            <div class="px-3 py-5 {bgGradien} text-white">.{bgGradien}</div>
                            {/each}
                        </div>
                    </div>

                </div>

                <!-- Third Column -->
                <div class="col-lg-4">

                    <!-- Grayscale Utilities -->
                    <div class="card shadow mb-4">
                        <div class="card-header py-3">
                            <h6 class="m-0 font-weight-bold text-primary">Custom Grayscale Background Utilities
                            </h6>
                        </div>
                        <div class="card-body">
                            {#each bgGrayArr as bgGray, index}
                                {#if index < 4}
                                    <div class="p-3 {bgGray}">.{bgGray}</div>
                                {:else}
                                    <div class="p-3 {bgGray} text-white">.{bgGray}</div>
                                {/if}
                            {/each}
                        </div>
                    </div>
                </div>

            </div>

        </div>
        <!-- /.container-fluid -->

    </div>
    <!-- End of Main Content -->

    <Footer/>

</div>