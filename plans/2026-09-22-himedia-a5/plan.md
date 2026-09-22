# HiMedia A5 Armbian target

## Outcome

Add a conservative Meson GXM board target for the HiMedia A5 using Armbian's
existing `oldlts`/6.12 Meson64 path, with Panfrost and raw IR enabled.

## Constraints

- Preserve the vendor bootloader path; do not add guessed regulators, keymaps,
  peripheral nodes, or eMMC flashing steps.
- Reuse existing Meson64 family and kernel configuration.

## Acceptance criteria

- Board config and DT source pass shell/Python validation.
- Meson64 Xorg modesetting case includes `himedia-a5`.
- Required oldlts kernel symbols are present.
- Kernel build is attempted; full image build is attempted only if kernel build succeeds.
