**Prefix:**

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```



**Body:**

```
<mods>

<identifier type="pid">{{cells["PID"].value}}</identifier>
<identifier type="local">{{cells["headeridentifier"].value}}</identifier>

<titleInfo><title>{{cells["title"].value}}</title></titleInfo>

{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}

{{if(isBlank(cells['name.0'].value), '', '<name'+ '><namePart>' + cells['name.0'].value + '</namePart>' + if(isBlank(cells['role.0'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['role.0_URI'].value + '">' + cells['role.0'].value + '</roleTerm></role>') + '</name>')}}

{{if(isBlank(cells['name.1'].value), '', '<name'+ '><namePart>' + cells['name.1'].value + '</namePart>' + if(isBlank(cells['role.1'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['role.1_URI'].value + '">' + cells['role.1'].value + '</roleTerm></role>') + '</name>')}}

{{if(isBlank(cells['name.2'].value), '', '<name'+ '><namePart>' + cells['name.2'].value + '</namePart>' + if(isBlank(cells['role.2'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['role.2_URI'].value + '">' + cells['role.2'].value + '</roleTerm></role>') + '</name>')}}

<originInfo>

{{if(isBlank(cells["humanReadableDate"].value),'','<dateCreated>' + cells['humanReadableDate'].value + '</dateCreated>')}}{{if(isBlank(cells["dateCreated_edtf"].value),'','<dateCreated encoding="edtf">' + cells['dateCreated_edtf'].value + '</dateCreated>')}}
{{if(isBlank(cells['dateRange'].value), '', '<dateCreated qualifier="approximate">' + cells['dateRange'].value + '</dateCreated><dateCreated qualifier="approximate" encoding="edtf" point="start">' + cells['dateStart'].value + '</dateCreated><dateCreated qualifier="approximate" encoding="edtf" point="end">' + cells['dateEnd'].value + '</dateCreated>')}}

</originInfo>

<language><languageTerm authority="iso639-2b" type="text">English</languageTerm></language>

<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><internetMediaType>{{cells['internetMediaType'].value}}</internetMediaType></physicalDescription>

{{if(isBlank(cells['DPN_note'].value), '', '<note displayLabel="dpn">' + cells['DPN_note'].value + '</note>')}}

{{if(isBlank(cells['subject.0name'].value), '', '<subject'+ if(isBlank(cells['subject.0name_URI'].value), '', ' valueURI="' + cells['subject.0name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.0name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject.1name'].value), '', '<subject'+ if(isBlank(cells['subject.1name_URI'].value), '', ' valueURI="' + cells['subject.1name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.1name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject.2name'].value), '', '<subject'+ if(isBlank(cells['subject.2name_URI'].value), '', ' valueURI="' + cells['subject.2name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.2name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject.0geographic'].value), '', '<subject' + if(isBlank(cells['subject.0geographic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.0geographic_URI'].value + '">') + '<geographic>' + cells['subject.0geographic'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject.1geographic'].value), '', '<subject' + if(isBlank(cells['subject.1geographic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.1geographic_URI'].value + '">') + '<geographic>' + cells['subject.1geographic'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject.2geographic'].value), '', '<subject' + if(isBlank(cells['subject.2geographic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.2geographic_URI'].value + '">') + '<geographic>' + cells['subject.2geographic'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject.3geographic'].value), '', '<subject' + if(isBlank(cells['subject.3geographic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.3geographic_URI'].value + '">') + '<geographic>' + cells['subject.3geographic'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject.0topic'].value), '', '<subject' + if(isBlank(cells['subject.0topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.0topic_URI'].value + '">') + '<topic>' + cells['subject.0topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject.1topic'].value), '', '<subject' + if(isBlank(cells['subject.1topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.1topic_URI'].value + '">') + '<topic>' + cells['subject.1topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject.2topic'].value), '', '<subject' + if(isBlank(cells['subject.2topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.2topic_URI'].value + '">') + '<topic>' + cells['subject.2topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject.3topic'].value), '', '<subject' + if(isBlank(cells['subject.3topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.3topic_URI'].value + '">') + '<topic>' + cells['subject.3topic'].value + '</topic></subject>')}}

<typeOfResource>{{cells['typeOfResource'].value}}</typeOfResource>

<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['project'].value}}</title></titleInfo></relatedItem>

{{if(isBlank(cells['findingAid'].value), '', '<relatedItem displayLabel="Collection" type="host"><titleInfo><title>' + cells['findingAid'].value + '</title></titleInfo><identifier>' + cells['MS_identifier'].value + '</identifier></relatedItem>')}}

<accessCondition type="use and reproduction" xlink:href="{{cells['Copyright_URI'].value}}">{{cells['Copyright'].value}}</accessCondition> 

<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>

</mods>
```



**Suffix:**

```
</modsCollection>
```