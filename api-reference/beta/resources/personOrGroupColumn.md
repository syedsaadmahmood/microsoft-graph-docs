# PersonOrGroupColumn resource type

The **personOrGroupColumn** on a [columnDefinition](columnDefinition.md) resource indicates that the column's values represent a person or group chosen from the directory.

## JSON representation

Here is a JSON representation of a **personOrGroupColumn** resource.
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.personOrGroupColumn" } -->

```json
{
  "allowMultipleSelection": true,
  "displayAs": "account | contentType | created | department | ...",
  "chooseFrom": "peopleAndGroups | peopleOnly"
}
```

## Properties

| Property name              | Type    | Description
|:---------------------------|:--------|:--------------------------------------
| **allowMultipleSelection** | boolean | Indicates whether multiple values can be selected from the source.
| **displayAs**              | string  | How to display the information about the person or group chosen. See below.
| **chooseFrom**             | string  | Whether to allow selection of people only, or people and groups. Must be one of `peopleAndGroups` or `peopleOnly`.

## DisplayAs values

| DisplayAs value               | Description
|:------------------------------|:-----------------------
| **account**                   | The raw SharePoint encoded claim string for the person or group (eg. i:0#.f|membership|jane@contoso.com).
| **department**                | The person or group's department.
| **firstName**                 | The person's first name.
| **id**                        | The id of the person or group in the directory.
| **lastName**                  | The person's last name.
| **mobilePhone**               | The person's mobile phone number.
| **name**                      | The person's name.
| **nameWithPictureAndDetails** | The person's name along with their picture and additional details.
| **nameWithPresence**          | Default. The person's name with a presence indicator icon (available/busy/etc.)
| **office**                    | The person's office number.
| **pictureOnly36x36**          | The person's picture, bounded by a 36x36 px square.
| **pictureOnly48x48**          | The person's picture, bounded by a 48x48 px square.
| **pictureOnly72x72**          | The person's picture, bounded by a 72x72 px square.
| **sipAddress**                | The person's sip address.
| **title**                     | The person's title in the organization.
| **userName**                  | The person or group's user name.
| **workEmail**                 | The person or group's email address.
| **workPhone**                 | The person's work phone number.

Note: Additional DisplayAs types may be returned.

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/PersonOrGroupColumn"
} -->