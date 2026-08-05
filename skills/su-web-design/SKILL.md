---
name: su-web-design
description: Design and refine SU Navigation web interfaces with restrained maritime visual language, Emil Kowalski-inspired interaction polish, accessible motion, and GitHub Pages-safe implementation. Use when building, reviewing, or animating the SU Navigation website.
---

# SU Navigation Web Design

## Direction

- Preserve the maritime identity: deep navy, ocean blue, paper-white surfaces, restrained cyan accents, and strong editorial typography.
- Keep the hero composition readable: the vessel must remain visible on the right, with copy anchored on the left.
- Prefer hierarchy and whitespace over decorative density.
- Keep official company facts, fleet data, offices, safety policy, and contact details intact when redesigning.

## Motion rules

- Animate only when motion explains hierarchy, state, feedback, or spatial continuity.
- Use custom easing: cubic-bezier(.23,1,.32,1) for responsive exits and cubic-bezier(.77,0,.175,1) for deliberate movement.
- Keep frequent interaction feedback under 180ms; use 220–280ms for cards and 500–900ms only for hero or ambient motion.
- Use transform and opacity; avoid animating layout properties.
- Pressable controls use transform: scale(.97) for 100–160ms.
- Hover motion stays subtle: 4–8px translation or 1.01–1.03 scale.
- Decorative route lines may drift slowly, but must stop or become effectively instant under prefers-reduced-motion: reduce.
- Never let a hover transform obscure text, clip a vessel, or move content out of its reading order.
- Include visible :focus-visible states for keyboard users.

## Implementation checklist

1. Check the hero image at desktop, tablet, and narrow mobile widths; verify the boat remains visible.
2. Verify asset URLs include the GitHub Pages base path.
3. Test navigation, service rows, fleet rows, contact links, and reduced-motion behavior.
4. Run the Pages build before claiming completion.
5. Compare the deployed result, not only local source.

## Review format

When reviewing motion, use a table with Before, After, and Why columns. Flag generic transition: all, slow UI transitions, ease-in for entrances, missing press feedback, missing reduced-motion handling, and motion that competes with the vessel or headline.
