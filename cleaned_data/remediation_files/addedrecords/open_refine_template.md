# Open Refine Template Daily Beacon / Orange and White - Added Records


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells["Identifier"].value}}</identifier>

{{if(isBlank(cells['title'].value), '', '<titleInfo supplied="yes"><title>' + cells["title"].value + '</title></titleInfo>')}} 
{{if(isBlank(cells['alternative_title'].value), '', '<titleInfo type="alternative"><title>' + cells["alternative_title"].value + '</title></titleInfo>')}}

<originInfo>
{{if(isBlank(cells['date_issued_hr 1'].value), '', '<dateIssued>' + cells['date_issued_hr 1'].value + '</dateIssued><dateIssued encoding="edtf">' + cells['Issue date'].value + '</dateIssued>')}}
<place><placeTerm valueURI="http://id.loc.gov/authorities/names/n79109786">Knoxville (Tenn.)</placeTerm></place>
</originInfo>

<physicalDescription>
<form authority="aat" valueURI="http://vocab.getty.edu/aat/300026656">newspapers</form>
{{if(isBlank(cells['Pages'].value), '', '<extent>' + cells["Pages"].value + '</extent>')}}
</physicalDescription>

   <subject valueURI="http://id.loc.gov/authorities/subjects/sh85028351">
      <topic>College student newspapers and periodicals</topic>
   </subject>
   <subject valueURI="http://id.loc.gov/authorities/names/n80003887">
      <topic>University of Tennessee (Knoxville campus)</topic>
   </subject>
   <subject authority="naf"
            valueURI="http://id.loc.gov/authorities/names/n79109786">
      <name>
         <namePart>Knoxville (Tenn.)</namePart>
      </name>
   </subject>
   <typeOfResource>text</typeOfResource>
   <language>
      <languageTerm type="text" authority="iso639-2b">English</languageTerm>
   </language>
   <relatedItem displayLabel="Project" type="host">
      <titleInfo>
         <title>The Daily Beacon</title>
      </titleInfo>
   </relatedItem>
   <classification authority="lcc">LH1.T2 O7</classification>
   <location>
      <physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation>
   </location>
   <recordInfo>
      <recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource>
   </recordInfo>

<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```