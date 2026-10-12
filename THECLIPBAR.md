# TheClipBar: source footage retrieval

This is TheClipBar's source fork of [yt-dlp/yt-dlp](https://github.com/yt-dlp/yt-dlp). It supports collecting permitted source footage and metadata for manual clip selection, video analysis, and editing.

## Copy and review record

- Review date: 2026-10-12.
- Reviewed upstream commit: `897341241f2bfb2439fe0367f4c7c9ccd29a3828`.
- The fork's initial default-branch commit was verified to match that commit.
- GitHub Actions was disabled for this fork and read back as `enabled: false`.
- Upstream code and license were preserved. This note is a TheClipBar addition.
- This was a focused static review, not a complete security audit or a runtime test. Nothing from this fork was installed on the user's computer during the review.

## What was checked

The review covered the package manifest, license, documented installation and verification options, update code, command-execution postprocessor, and published security advisories. The reviewed commit was verified to be 80 commits ahead and zero commits behind the security-fixed release `2026.07.04`.

Relevant evidence:

- [Package manifest](https://github.com/yt-dlp/yt-dlp/blob/897341241f2bfb2439fe0367f4c7c9ccd29a3828/pyproject.toml)
- [Source license](https://github.com/yt-dlp/yt-dlp/blob/897341241f2bfb2439fe0367f4c7c9ccd29a3828/LICENSE)
- [Security-fix ancestry](https://github.com/yt-dlp/yt-dlp/compare/2026.07.04...897341241f2bfb2439fe0367f4c7c9ccd29a3828)
- [Command-template security advisory](https://github.com/yt-dlp/yt-dlp/security/advisories/GHSA-69qj-pvh9-c5wg)
- [Shortcut-output security advisory](https://github.com/yt-dlp/yt-dlp/security/advisories/GHSA-6v4j-43gg-vj32)
- [External-downloader cookie advisory](https://github.com/yt-dlp/yt-dlp/security/advisories/GHSA-f7j3-774f-rfhj)

The source repository uses the Unlicense. Packaged binaries and optional dependencies can have additional licenses; retain their notices when redistributing them.

## Intended setup and use

Install in an isolated environment with reviewed, current dependencies. Full YouTube support can require FFmpeg, FFprobe, yt-dlp-ejs, and a supported JavaScript runtime. Verify official release checksums and signatures when using binaries. The source fork alone does not install these dependencies.

Use direct public media URLs or files supplied for the edit. Use site-specific authentication only when explicitly needed and authorized. Keep browser cookies, API keys, downloaded private footage, and credentials out of Git.

Example invocation after a separately validated installation:

```bash
yt-dlp --ignore-config --no-plugin-dirs --no-cookies --no-cookies-from-browser --no-exec --no-playlist --restrict-filenames -P ./source -o '%(id)s.%(ext)s' -- 'PASTE_THE_SOURCE_VIDEO_URL_HERE'
```

This starts without inherited configuration, extra plugins, browser cookies, or shell hooks. It does not bypass site access controls. Site changes can still prevent a download. Fetching a video does not establish permission to republish it.

Save the original source URL and timecodes alongside the editing project. The next stage is visual inspection and transcription, then selecting a coherent moment and creating the branded edit. Downloading alone does not identify the best moment or locate every shot in a reference video.

## TheClipBar production requirements

Create a distinctive streamer/reaction edit with readable portrait framing, the approved logo, pink/cyan/yellow graphics, large captions, and sound cues that follow the dialogue. Preserve context and meaningful reactions. Review the final video before publishing. Publishing remains through Metricool with the user's authorization.

Before updating this fork, review upstream changes from the recorded commit and recheck dependency and security advisories.
