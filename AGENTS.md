<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

## Application architecture
- Keep the invitation at the index route and isolate canvas and countdown behavior into focused components; the single invitation is the primary experience.
- Read guest personalization after hydration and keep opening state in memory; every shared invitation starts sealed without browser-storage dependencies.
- Keep the curtain layer mounted across opening and replay phases so closing can transition from its off-screen position; hide and disable it when the invitation is open.
- Use asset pointers for uploaded media and bundled imports for generated decoration; preserve user imagery without storing duplicate binaries.
