<script lang="ts">
    import { AppBar, AppShell, LightSwitch } from '@skeletonlabs/skeleton';
    import { popup } from '@skeletonlabs/skeleton';

    let isMenuOpen = false;
    
    function toggleMenu() {
        isMenuOpen = !isMenuOpen;
    }
</script>

<AppShell>
    <svelte:fragment slot="header">
        <AppBar class="flex justify-between px-4">
            <!-- Center-aligned Navigation -->
            <svelte:fragment slot="lead"></svelte:fragment>
            
            <!-- Center content -->
            <div class="flex justify-center w-full">
                <div class="flex gap-8">
                    <a href="/" class="btn btn-sm !bg-transparent">Home</a>
                    <a href="/resume" class="btn btn-sm !bg-transparent">Resume</a>
                    <a href="/projects" class="btn btn-sm !bg-transparent">Projects</a>
                    <a href="/projects" class="btn btn-sm !bg-transparent">Contact</a>
                </div>
            </div>
            
            <!-- Right side content -->
            <svelte:fragment slot="trail">
                <div class="ml-auto">
                    <LightSwitch />
                </div>
            </svelte:fragment>
        </AppBar>
    </svelte:fragment>
    
    <!-- Page content goes here -->
    <slot />
</AppShell>