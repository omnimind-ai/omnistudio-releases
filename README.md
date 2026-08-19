# OmniStudio Releases

Public distribution mirror and stable update manifest for [OmniStudio](https://github.com/omnimind-ai/OmniStudio).

## Downloads

Download the current Windows and macOS installers from the [latest GitHub Release](https://github.com/omnimind-ai/omnistudio-releases/releases/latest). Each Release records the exact filename, byte size, SHA-256 digest, and platform signing status.

The primary production downloads are also served from `https://studio.omnimind.com.cn/`. GitHub Release assets provide a public mirror of the same verified files.

## Update manifest

[`latest.json`](./latest.json) is the machine-readable stable-channel manifest consumed by the OmniStudio website and other download clients. It includes:

- the current source Release and target version;
- per-platform filenames, sizes, and SHA-256 digests;
- the primary object-storage URL and GitHub Release mirror;
- the previous reachable platform entry as a fallback when available.

The manifest is updated atomically only after the source Release and both platform artifacts are published and reachable from object storage and GitHub.

## Security notes

- Windows installers are currently unsigned.
- macOS installers are Developer ID signed. A Release note states whether that version is notarized.
- Verify downloaded files against the SHA-256 digest in the corresponding GitHub Release before installation.

Source code, changelogs, and issue tracking remain in the [OmniStudio repository](https://github.com/omnimind-ai/OmniStudio).
