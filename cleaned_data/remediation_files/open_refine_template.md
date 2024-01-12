# Open Refine Template Daily Beacon / Orange and White


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells["Image prefix"].value}}</identifier>

{{if(isBlank(cells['title'].value), '', '<titleInfo supplied="yes"><title>' + cells["title"].value + '</title></titleInfo>')}} 
{{if(isBlank(cells['alternative_title'].value), '', '<titleInfo type="alternative"><title>' + cells["alternative_title"].value + '</title></titleInfo>')}}

{{if(isBlank(cells['abstract'].value), '', '<abstract>' + cells["abstract"].value + '</abstract>')}}

<originInfo>
{{if(isBlank(cells['Issue Date'].value), '', '<dateIssued>' + cells['Issue Date'].value + '</dateIssued><dateIssued encoding="edtf">' + cells['Issue Date EDTF'].value + '</dateIssued>')}}
{{if(isBlank(cells['place_of_publication'].value), '', '<place><placeTerm valueURI="' + cells['place_of_publication_URI'].value + '">' + cells['place_of_publication'].value + '</placeTerm></place>')}}
</originInfo>

<physicalDescription>
{{if(isBlank(cells['form'].value), '', '<form authority="aat" valueURI="' + cells['form_URI'].value + '">' + cells['form'].value + '</form>')}}
{{if(isBlank(cells['Pages'].value), '', '<extent>' + cells["Pages"].value + '</extent>')}}
</physicalDescription>

{{if(isBlank(cells['subject 1'].value), '', '<subject valueURI="' + cells['subject_URI 1'].value + '"><topic>' + cells['subject 1'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject 2'].value), '', '<subject valueURI="' + cells['subject_URI 2'].value + '"><topic>' + cells['subject 2'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject 3'].value), '', '<subject valueURI="' + cells['subject_URI 3'].value + '"><topic>' + cells['subject 3'].value + '</topic></subject>')}}

<subject authority="naf" valueURI="http://id.loc.gov/authorities/names/n79109786"><name><namePart>Knoxville (Tenn.)</namePart></name></subject>

<typeOfResource>{{cells['typeOfResource'].value}}</typeOfResource>

{{if(isBlank(cells['language'].value), '', '<language><languageTerm type="text" authority="iso639-2b">' + cells['language'].value + '</languageTerm></language>')}}

<relatedItem displayLabel="Project" type="host"><titleInfo><title>The Daily Beacon</title></titleInfo></relatedItem>

<classification authority="lcc">{{cells['classification'].value}}</classification>

<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>

<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>

<accessCondition type="use and reproduction" xlink:href="{{cells['rights_statement_URI'].value}}">{{cells['rights_statement'].value}}</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```