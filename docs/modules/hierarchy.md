# Hierarchy

The [Hierarchy module](https://omeka.org/s/modules/Hierarchy){target=_blank} adds the ability to organize your Omeka S item sets into trees. This module is similar to [Collection Tree](https://omeka.org/classic/plugins/CollectionTree/){target=_blank} for Omeka Classic - you can create ordered or multi-level organizational systems.

![A hierarchy in action on a public page.](modulesfiles/hierarchy_public.png)

Any number of groupings can be created in the module; a parent can have any number of children. You can choose to have higher-level groupings reflect the total number of items in all the item sets included at lower levels. 

Hierarchies are displayed on each site with [resource page blocks](../sites/site_theme.md#configure-resource-pages) for items and item sets, and with a ["Hierarchy" page block](../sites/site_pages.md#page-blocks). Hierarchies can be added to individual sites for display, and can be configured on a site-by-site basis.

Hierarchies can be created by users at the Supervisor and Global Administrator levels. Hierarchies are displayed [on individual sites by users with permission](../sites/site_users.md) to modify the resource page blocks, and the permission to edit pages. 

## Plan your groupings

An Omeka S item can be in many item sets, according to your needs. But item sets cannot contain other item sets. Hierarchies do not change this - rather, they are a supplemental way of indicating a relationship between item sets. 

For example, if you organize your items by creator (in a "Shakespeare, William" item set, a "Marlowe, Christopher" item set, and so on) these item sets might be considered "siblings" to one another: equivalent concepts, but unordered. You can use a hierarchy to order these item sets chronologically by the creators' lifetimes, or by most to least items, or alphabetically, or any other system you choose. 

You could also organize them in groupings by country of origin, the language used in their works, or other categories. If you have a "Works in German" item set, containing miscellaneous items as well as items also in the "Mann, Thomas" item set, you could nest the item sets of German authors under the "Works in German" item set as a way to indicate that relationship.  

Another example might be organizing items by artifact type: paintings, sculptures, archaeological finds, documents, photographs. These item sets will not be modified but can be supplemented by adding larger categories such as "Artworks" and "Paper Items" and "Three-Dimensional Objects" to group the relevant item sets together. One hierarchy can contain the same item set more than once, so you can have a hierarchy as follows:

- Artworks
	- Paintings
	- Sculptures
	- Photographs
- Three-Dimensional Objects
	- Sculptures
	- Archaeological Finds
- Paper Items
	- Documents
	- Photographs.

Remember that item sets, resource classes, and templates can also help you provide multiple points of organization and context for your items. 

## Create a hierarchy

In the "Modules" section of the sidebar, find the "Hierarchy" page. Click the "Add Hierarchy" button to start your first hierarchy.

![Adding a new hierarchy on the Hierarchy page.](modulesfiles/hierarchy_add.png)

You can optionally give your new hierarchy a label, or leave it blank. 

Hierarchies are made by creating and rearranging groupings into trees. Click the "Add grouping" button to add your first grouping. You can optionally give it a label or leave it blank. You can also optionally set your grouping to be equivalent to an existing item set. 

If you leave the grouping label blank, the item set's name will be displayed. If you fill in the label, that will be displayed instead, wherever the hierarchy appears. 

!!! note
	If you neither fill in the label nor choose an item set, the grouping will appear in the tree as "[Untitled]". We recommend you employ at least one of the two options. 

Then, drag and drop your groupings into your desired order or tree structure. Groupings can be dragged to become children of other groupings, or ordered to be siblings of each other. When a grouping is being dragged, look for small arrows that indicate where to drop it - to be a sibling of another grouping (an arrow underneath), or to be a child of the grouping (an arrow in the center). 

Add as many groupings as you need, filling out labels and selecting item sets where necessary. Combine this with creating new item sets and adding items to them as needed. 

For example, you may wish to create a five-level archival organizational system as follows:

- A Collection [the hierarchy]
	- Series 1
	- Series 2
	- Series 3
		- Sub-series 3.1
			-  Folder 3.1.1 [set to an item set]
				- [Items]

Every entry in the list above is a grouping with a label but no item set, except for the bottom-most level, which is set to the item set containing the relevant items in Omeka. 

![An example Hierarchy screen is filled out](modulesfiles/hierarchy_admin.png)

You can create as many hierarchies as you wish, with as many levels as needed, and reuse your item sets wherever you wish. In this way you can create multiple points of access to your collections, according to different topics or browse methods. 

If you delete a grouping (the trash can icon to the right), its children will not be deleted with it. Instead, they will be promoted up to the level of the deleted grouping. 

Remember to save your changes before navigating away from the module page. 

## Add a hierarchy to a site

From the Sites tab of the left-hand navigation, pick a site and then choose "Hierarchy" in the list.

![Adding hierarchies by name to one site.](modulesfiles/hierarchy_site.png)

All of your hierarchies are listed on the right. Add them to each site as desired. The order that hierarchies are arranged on this page is the order they will display on this site; you can drag and drop them once added. Then save the page. 

## Site configuration

From the Site Admin page, select the "Settings" tab, and scroll down to the "Hierarchy" section. 

![An example configuration screen is filled out](modulesfiles/hierarchy_config.png)

The Hierarchy module has three configuration options for each site:

- **Show hierarchy label**: If checked, the hierarchy's assigned label will display as the hierarchy header on public pages. If unchecked, the hierarchy will display without a label. You can also leave individual hierarchy labels blank. 
- **Show hierarchy resource counts**: If checked, hierarchy groupings will show the number of resources within currently assigned item set.
- **Combine hierarchy resources**: If checked, groupings will display resources of all child groupings in resource counts and on hierarchy grouping browse pages.

If you show resource counts for each level of your hierarchy, and if you also combine those counts, you will see the total number of items, regardless of whether those items are in more than one included item set (that is, items will not be counted twice). 

## Display hierarchies on a site

Public pages will display the hierarchy as a tree. Groupings with items in them will be links; groupings without any items will be displayed in plain text. 

The links in the hierarchy will point to a custom public page, in the form `yourinstallation.org/s/your-site/hierarchy/01`. This will display the chosen hierarchy at left, and all the items contained in the given grouping at right (either all the items in the attached item set, or including all the children items as per your site settings). 

Underneath the hierarchy on these pages will be a list of all the item sets that are included in the full hierarchy, so that users can navigate to those if needed. (See the image at the top of this page for an example.) On site page blocks and on resources (items and item sets), this section will not display. 

!!! note
	Public display will depend on whether the applicable item sets are added to the site as a resource. Note that item sets with visibility set to "private" will not be available to logged-out users; their place in hierarchies will not be linked and their items will not be included in counts.

You can display hierarchies in two ways on your sites: 

- By adding resource page blocks to item and item set view pages
- By adding page blocks to site pages. 

### Resource blocks

Select a site, then select the "Theme" tab in the left sidebar. Click the "Configure resource pages" button next to "Edit theme settings". 

![The items view page settings in the admin side, with the Hierarchy block included.](modulesfiles/hierarchy_resource.png)

On the Items view page, you can add the "Hierarchy" resource block to any region offered by your theme. This will display all the hierarchies that apply to the item. If an item is in more than one item set, all of the item sets' hierarchies will be displayed (according to which hierarchies and which item sets are added to the site as resources). 

![The item set view page settings in the admin side, with the Hierarchy block included.](modulesfiles/hierarchy_resource2.png)

On the Item set view page, you can add the "Hierarchy" resource block to any region offered by your theme. This will display all the hierarchies that apply to the item set (if the hierarchies are added to the site). 

![An item view page with the hierarchy at top.](modulesfiles/hierarchy_publicItem.png)

### Page blocks

![The Hierarchy page block on the admin side.](modulesfiles/hierarchy_pageBlock.png)

When adding the Hierarchy page block to a page, you can select one hierarchy at a time to display. You can add multiple page blocks. 

![An example configuration screen is filled out](modulesfiles/hierarchy_public2.png)