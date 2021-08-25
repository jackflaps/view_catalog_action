# View Catalog Action Button

Adds a button to resource views in the ArchivesSpace public site so that a user may click through the library catalog, where they can view holdings and determine availability of collection materials.

This plugin assumes catalog keys are kept in `string_1` in the User Defined fields in ArchivesSpace. Currently, to update this you will need to edit the plugin code directly. Ideally it would be configurable.

Because the button displays conditionally based on a user-defined string value, it must be activated with a partial. To activate it, add the following code to your `config/config.rb` file:

```
AppConfig[:pui_page_custom_actions] = {
  'record_type' => ['resource'],
  'erb_partial' => 'shared/view_catalog_action',
}
```
