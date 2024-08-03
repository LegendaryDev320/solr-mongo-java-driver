Those three files are needed for connecting mongodb in solr.
This is schema.xml sample.
<?xml version="1.0" encoding="UTF-8" ?>
<schema name="example" version="1.5">
<field name="time_stamp" type="string" indexed="true"  stored="true"  multiValued="false" />
<field name="category" type="string" indexed="true"  stored="true"  multiValued="false" />
<field name="type" type="string" indexed="true"  stored="true"  multiValued="false" />
<field name="servername" type="string" indexed="true"  stored="true"  multiValued="false" />
<field name="code" type="string" indexed="true"  stored="true"  multiValued="false" />
<field name="msg" type="string" indexed="true"  stored="true"  multiValued="false" />
<field name="_ts" type="long" indexed="true" stored="true" />
<field name="ns" type="string" indexed="true" stored="true"/>
   <field name="_version_" type="long" indexed="true" stored="true"/>
   <field name="id" type="string" indexed="true" stored="true" required="true" multiValued="false" />
 <uniqueKey>id</uniqueKey>
    <fieldType name="string" class="solr.StrField" sortMissingLast="true" />
    <fieldType name="boolean" class="solr.BoolField" sortMissingLast="true"/>
</schema>
Best wishes.
