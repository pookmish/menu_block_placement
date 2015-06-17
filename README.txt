-- SUMMARY --
Allows content to be used similar to blocks placed into regions. Provides the selection of menu items to place the piece of content and allows individual pages or cascading pages.

-- USE --
1. Add the Menu Block Placement field to a content type.
2. Create a view for that type. Add a contextual filter for that field (field_name:mlid).
3. Provide a default value for the filter
  a. 'Active Menu Item - Menu Block Placement Per Path' - Will apply the content to the chosen pages from the field.
  b. 'Active Menu Item - Menu Block Placement' - Will apply the content to the chosen page and all children under that menu item.
4. Place the Block in the desired region.

Restrictions to the region portion of the field can be changed on the theme level. In the desired theme .info file include the following to declare the region as available in the select list:
settings[menu_block_placement][region_key] = 1

If no regions are designated, all regions will be available in the dropdown. If the theme changes and the regions do not adjust in the field, simply clear the site cache.

-- SUBMODULES --

Menu Block Placement Defaults
-----------------------------
This module will automatically generate the views and context to place the blocks in the necessary region (if the region setting for the field is selected). It uses Draggableviews and Quicktabs to give a convienent interface to reorder the content within the block.

To Use:
1. Enable 'Menu Block Placement Defaults'
2. Add the Menu Block Placement Field to a content type.
  a. If the desired content is allowed to be in various regions, check the 'Include Region Select List'.
  b. If it is desired to have that content in only a single region, do not include regions list.
  c. If you would like the content to be able to cascade, check "Include 'Individual Pages' checkbox".
3. If the region list is not included, place the generated block into the desired region. If region list is included, no further work is required.
4. Create content.

Menu Block Placement Roles
--------------------------
This allows for roles to be designated with a menu item and are only allowed to place content on those pages. This is similar to what workbench access does, but takes it a step further by removing the menu items the user is not given permission to.

To Use:
1. Enable 'Menu Block Placement Roles'
2. Go to admin/config/content/mbp/roles
3. Choose the desired parent menu items for each role. That menu item and all children of the item will be available in the dropdown for the Menu Block Placement Fields.
