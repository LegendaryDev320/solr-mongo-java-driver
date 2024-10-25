##Hello Hercules!   Please take a look at this Readme file.

I found some issues here but not working properly. I will update soon.

1. test_core is the sample core for indexing mongodb.
2. copy these 2 jar files on test_core/lib
3. add data-config.xml to your core like on test_core.
4. Here is another sample for data_config.xml
   ```xml
   <?xml version="1.0" encoding="UTF-8" ?>
   <dataConfig>
        <dataSource name="MyMongo" type="MongoDataSource" database="Inventory" />
        <document name="Products">
            <entity processor="MongoEntityProcessor"
                    query="{'Active':1}"
                    collection="ProductData"
                    datasource="MyMongo"
                    deltaQuery="{'UpdateDate':{$gt:{$date:'${dih.last_index_time}'}}}"
                    deltaImportQuery="{'_id':'${dih.delta._id}'}"
                    transformer="MongoMapperTransformer" >
                <field column="title"           name="title"       mongoField="Title"/>
                <field column="description"     name="description" mongoField="Long Description"/>
                <field column="brand"           name="brand"  />
            </entity>
        </document>
    </dataConfig>
6. Added refernece urls here.
   https://github.com/james75/SolrMongoImporter?tab=readme-ov-file
   https://github.com/GuilhermeViterboGalvao/solrMongoDBDataImporter?tab=readme-ov-file
