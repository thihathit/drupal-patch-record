# Adding patch history folder
Folder name: `patches`

Location: `root directory of Drupal`

## Folder structure

    patches/
    --------/README.md
    --------/README.html
    --------/records.yml
    --------/bugfix.patch
    --------/drupal.org/bugfix.patch

## records.yml Format
```yaml
# global restoration procedure [optional]
RESTORATION_PROCEDURE:
	description: how all the patches should be restored.

# patched module/theme/file info
module_name_or_relevant_name:
	description: What this patch does.
	patch_file_location: http://drupal.org/files/issues/bugfix.patch [live url of patch file if exists]
	local_patch_file_location: local/bugfix.patch [custom_patches/unknown_source_patches that is applied will stored under "patches/local" folder]
	type: core/module ["core/theme" or "contrib/module" or "contrib/theme"]
	version: 8.x.x [version of the issue last found]
	restoration_procedure: How this patch should be restored. [does not required if global RESTORATION_PROCEDURE is set.]
```
