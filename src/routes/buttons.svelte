<script>
    import CircleButton from "../components/CircleButton.svelte";
    import SplitButton from "../components/SplitButton.svelte";
    import Footer from "../components/Footer.svelte";
    import PageHeading from "../components/PageHeading.svelte";
    import Topbar from "../components/Topbar.svelte";

    let title = 'Buttons';
</script>

<div id="content-wrapper" class="d-flex flex-column">

    <!-- Main Content -->
    <div id="content">

       <Topbar />

        <!-- Begin Page Content -->
        <div class="container-fluid">

            <PageHeading {title} />

            <div class="row">

                <div class="col-lg-6">

                    <!-- Circle Buttons -->
                    <div class="card shadow mb-4">
                        <div class="card-header py-3">
                            <h6 class="m-0 font-weight-bold text-primary">Circle Buttons</h6>
                        </div>
                        <div class="card-body">
                            <p>Use Font Awesome Icons (included with this theme package) along with the circle
                                buttons as shown in the examples below!</p>
                            <!-- Circle Buttons (Default) -->
                            <div class="mb-2">
                                <code>.btn-circle</code>
                            </div>
                            <CircleButton level='primary' on:click={()=>alert("I'm fa-facebook Circle button!")}>
                                <i class="fab fa-facebook-f"></i>
                            </CircleButton>
                            <CircleButton level='success' on:click={()=>alert("I'm fa-check Circle button!")}>
                                <i class="fas fa-check"></i>
                            </CircleButton>
                            <CircleButton level='info' on:click={()=>alert("I'm fa-info Circle button!")}>
                                <i class="fas fa-info-circle"></i>
                            </CircleButton>
                            <CircleButton level='warning' on:click={()=>alert("I'm fa-exclamation-triangle Circle button!")}>
                                <i class="fas fa-exclamation-triangle"></i>
                            </CircleButton>
                            <CircleButton level='danger' on:click={()=>alert("I'm fa-trash Circle button!")}>
                                <i class="fas fa-trash"></i>
                            </CircleButton>
                           
                            <!-- Circle Buttons (Small) -->
                            <div class="mt-4 mb-2">
                                <code>.btn-circle .btn-sm</code>
                            </div>
                            <CircleButton size='small' level='primary' on:click={()=>alert("I'm fa-facebook Circle button!")}>
                                <i class="fab fa-facebook-f"></i>
                            </CircleButton>
                            <CircleButton size='small' level='success' on:click={()=>alert("I'm fa-check Circle button!")}>
                                <i class="fas fa-check"></i>
                            </CircleButton>
                            <CircleButton size='small' level='info' on:click={()=>alert("I'm fa-info Circle button!")}>
                                <i class="fas fa-info-circle"></i>
                            </CircleButton>
                            <CircleButton size='small' level='warning' on:click={()=>alert("I'm fa-exclamation-triangle Circle button!")}>
                                <i class="fas fa-exclamation-triangle"></i>
                            </CircleButton>
                            <CircleButton size='small' level='danger' on:click={()=>alert("I'm fa-trash Circle button!")}>
                                <i class="fas fa-trash"></i>
                            </CircleButton>
                            
                            <!-- Circle Buttons (Large) -->
                            <div class="mt-4 mb-2">
                                <code>.btn-circle .btn-lg</code>
                            </div>
                            <CircleButton size='large' level='primary' on:click={()=>alert("I'm fa-facebook Circle button!")}>
                                <i class="fab fa-facebook-f"></i>
                            </CircleButton>
                            <CircleButton size='large' level='success' on:click={()=>alert("I'm fa-check Circle button!")}>
                                <i class="fas fa-check"></i>
                            </CircleButton>
                            <CircleButton size='large' level='info' on:click={()=>alert("I'm fa-info Circle button!")}>
                                <i class="fas fa-info-circle"></i>
                            </CircleButton>
                            <CircleButton size='large' level='warning' on:click={()=>alert("I'm fa-exclamation-triangle Circle button!")}>
                                <i class="fas fa-exclamation-triangle"></i>
                            </CircleButton>
                            <CircleButton size='large' level='danger' on:click={()=>alert("I'm fa-trash Circle button!")}>
                                <i class="fas fa-trash"></i>
                            </CircleButton>
                        </div>
                    </div>

                    <!-- Brand Buttons -->
                    <div class="card shadow mb-4">
                        <div class="card-header py-3">
                            <h6 class="m-0 font-weight-bold text-primary">Brand Buttons</h6>
                        </div>
                        <div class="card-body">
                            <p>Google and Facebook buttons are available featuring each company's respective
                                brand color. They are used on the user login and registration pages.</p>
                            <p>You can create more custom buttons by adding a new color variable in the
                                <code>_variables.scss</code> file and then using the Bootstrap button variant
                                mixin to create a new style, as demonstrated in the <code>_buttons.scss</code>
                                file.</p>
                            <button class="btn btn-google btn-block"><i class="fab fa-google fa-fw"></i>
                                .btn-google</button>
                            <button class="btn btn-facebook btn-block"><i
                                    class="fab fa-facebook-f fa-fw"></i> .btn-facebook</button>

                        </div>
                    </div>

                </div>

                <div class="col-lg-6">

                    <div class="card shadow mb-4">
                        <div class="card-header py-3">
                            <h6 class="m-0 font-weight-bold text-primary">Split Buttons with Icon</h6>
                        </div>
                        <div class="card-body">
                            <p>Works with any button colors, just use the <code>.btn-icon-split</code> class and
                                the markup in the examples below. The examples below also use the
                                <code>.text-white-50</code> helper class on the icons for additional styling,
                                but it is not required.</p>
                            <SplitButton level="primary" title="Split Button Primary" on:click={()=>alert("I'm Split Button Primary!")}>
                                <i class="fas fa-flag"></i>
                            </SplitButton>
                            <div class="my-2"></div>
                            <SplitButton level="success" title="Split Button Success" on:click={()=>alert("I'm Split Button Success!")}>
                                <i class="fas fa-check"></i>
                            </SplitButton>
                            <div class="my-2"></div>
                            <SplitButton level="info" title="Split Button Info" on:click={()=>alert("I'm Split Button Info!")}>
                                <i class="fas fa-info-circle"></i>
                            </SplitButton>
                            <div class="my-2"></div>
                            <SplitButton level="warning" title="Split Button Warning" on:click={()=>alert("I'm Split Button Warning!")}>
                                <i class="fas fa-exclamation-triangle"></i>
                            </SplitButton>
                            <div class="my-2"></div>
                            <SplitButton level="danger" title="Split Button Danger" on:click={()=>alert("I'm Split Button Danger!")}>
                                <i class="fas fa-trash"></i>
                            </SplitButton>
                            <div class="my-2"></div>
                            <SplitButton level="secondary" title="Split Button Secondary" on:click={()=>alert("I'm Split Button Secondary!")}>
                                <i class="fas fa-arrow-right"></i>
                            </SplitButton>
                            <div class="mb-4"></div>
                            <p>Also works with small and large button classes!</p>
                            
                            <SplitButton level="primary" size="small" title="Split Button Small" on:click={()=>alert("I'm Split Button Small!")}>
                                <i class="fas fa-flag"></i>
                            </SplitButton>
                            <div class="my-2"></div>
                            <SplitButton level="primary" size="large" title="Split Button Large" on:click={()=>alert("I'm Split Button Large!")}>
                                <i class="fas fa-flag"></i>
                            </SplitButton>
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