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
    # global restoration procedure [optional]
    RESTORATION_PROCEDURE:
	    description: how all the patches should be restored.

	# patched module/theme/file info
	module_name_or_relevant_name:
		description: What this patch does.
		patch_file_location: http://drupal.org/files/issues/bugfix.patch [live url of patch file if exists]
		patch_file_location: /bugfix.patch [custom patch file location inside "patches/" folder]
		local_patch_file_location: bugfix.patch [a copy of patch file downloaded/stored locally inside "patches/" folder]
		type: core/module ["core/theme" or "contrib/module" or "contrib/theme"]
		restoration_procedure: How this patch should be restored. [does not required if global RESTORATION_PROCEDURE is set.]
