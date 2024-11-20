# Open Refine Template for Daily Beacon Page Titles


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
{{if(isBlank(cells['mods.physicalDescriptionextent'].value), '<mods><identifier type="pid">' + cells["filename"].value + '</identifier>', '')}}

{{if(isBlank(cells['mods.physicalDescriptionextent'].value), '<titleInfo><title>' + cells['pageTitle'].value + '</title></titleInfo></mods>', '')}}


```

#### Suffix

```
</modsCollection>
```