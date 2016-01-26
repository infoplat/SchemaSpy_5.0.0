# SchemaSpy_5.0.0源码学习

##SchemaSpy简介
SchemaSpy是Java开发的的工具（要求java 5或更高版本的支持），主要用来分析数据库中数据模型的元数据，并且能生成基于浏览器可视化的显示。通过点击就可了解数据表的层次结构，父子表关系等，主要通过HTML 链接或者实体关系图来表达。它也被设计成用来帮助解决由于约束而导致的数据库关联失败的迟钝错误。

##生成文件在线示例
这是[一个MySql数据库在线示例](http://sql.suyuening.cn "一个MySql数据库在线示例"){:target="_blank"}。

##调试方法

- 执行：net.sourceforge.schemaspy.Main
- 参数：-charset UTF-8 -t mysql -cp lib\mysql-connector.jar -db mysql  -host localhost -port 3306 -u root -p 123456 -o mysql -s mysql  -nologo -noads -hq

##源码目录说明
    ├─doc
    │      SchemaSpy.mht
    │
    ├─lib
    │      classes12.jar
    │      jtds-1.2.5.jar
    │      jtds-1.3.1.jar
    │      mysql-connector.jar
    │      postgresql-9.1-901.jdbc4.jar
    │      sqljdbc4.jar
    │
    └─src
        │  jquery.js
        │  schemaSpy.css
        │  schemaSpy.js
        │  schemaspy.meta.xsd
        │  schemaSpy.rev
        │
        ├─images
        │      background.gif
        │      tabLeft.gif
        │      tabRight.gif
        │
        └─net
            └─sourceforge
                └─schemaspy
                    │  Config.java
                    │  DbAnalyzer.java
                    │  Main.java
                    │  MultipleSchemaAnalyzer.java
                    │  Revision.java
                    │  SchemaAnalyzer.java
                    │  TableOrderer.java
                    │
                    ├─dbTypes
                    │      db2.properties
                    │      db2net.properties
                    │      db2zos.properties
                    │      derby.properties
                    │      derbynet.properties
                    │      firebird.properties
                    │      hsqldb.properties
                    │      informix.properties
                    │      jtds.properties
                    │      maxdb.properties
                    │      mssql-jtds.properties
                    │      mssql.properties
                    │      mssql05-jtds.properties
                    │      mssql05.properties
                    │      mysql.properties
                    │      ora.properties
                    │      orathin.properties
                    │      pgsql.properties
                    │      sqlite.properties
                    │      sybase.properties
                    │      sybase2.properties
                    │      teradata.properties
                    │      udbt4.properties
                    │
                    ├─model
                    │  │  ConnectionFailure.java
                    │  │  Database.java
                    │  │  EmptySchemaException.java
                    │  │  ExplicitRemoteTable.java
                    │  │  ForeignKeyConstraint.java
                    │  │  ImpliedForeignKeyConstraint.java
                    │  │  InvalidConfigurationException.java
                    │  │  ProcessExecutionException.java
                    │  │  RailsForeignKeyConstraint.java
                    │  │  RemoteTable.java
                    │  │  Table.java
                    │  │  TableColumn.java
                    │  │  TableIndex.java
                    │  │  View.java
                    │  │
                    │  └─xml
                    │          ForeignKeyMeta.java
                    │          SchemaMeta.java
                    │          TableColumnMeta.java
                    │          TableMeta.java
                    │
                    ├─ui
                    │      DbConfigPanel.java
                    │      DbConfigTableModel.java
                    │      DbTypeSelectorModel.java
                    │      DirectoryCellEditor.java
                    │      MainFrame.java
                    │      UiUtils.java
                    │
                    ├─util
                    │      CaseInsensitiveMap.java
                    │      ConnectionURLBuilder.java
                    │      ConsolePasswordReader.java
                    │      DbSpecificConfig.java
                    │      DbSpecificOption.java
                    │      DOMUtil.java
                    │      Dot.java
                    │      HtmlEncoder.java
                    │      Inflection.java
                    │      LineWriter.java
                    │      LogFormatter.java
                    │      PasswordReader.java
                    │      ResourceWriter.java
                    │      Version.java
                    │
                    └─view
                            DefaultSqlFormatter.java
                            DotConnector.java
                            DotConnectorFinder.java
                            DotFormatter.java
                            DotNode.java
                            HtmlAnomaliesPage.java
                            HtmlColumnsPage.java
                            HtmlConstraintsPage.java
                            HtmlDiagramFormatter.java
                            HtmlFormatter.java
                            HtmlMainIndexPage.java
                            HtmlMultipleSchemasIndexPage.java
                            HtmlOrphansPage.java
                            HtmlRelationshipsPage.java
                            HtmlTableDiagrammer.java
                            HtmlTablePage.java
                            ImageWriter.java
                            SqlFormatter.java
                            StyleSheet.java
                            TextFormatter.java
                            WriteStats.java
                            XmlTableFormatter.java
