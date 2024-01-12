## Client rules
|                  Rule                  | Prio |                          Description                         | Info |
|:--------------------------------------:|:----:|:------------------------------------------------------------:|:----:|
| UnusedZedRequestInSearchAndStorageRule |   2  | There should be no Zed Request in Search And Storage Client. |      |

## Common rules
|                      Rule                    | Prio |                                                                                                                                                                                                                                                                                                                                                              Description                                                                                                                                                                                                                                                                                                                                                              | Info |
|:--------------------------------------------:|:----:|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:----:|
| InstanceResolvingRule                        |  2   | Repository, EntityManager, QueryContainer, Facade, DependencyProvider, Client, Service instances can not be initialized directly with "new". Use Dependency Provider and Resolvers                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |      |
| LayerAccessRule                              |  2   | Some layers must not call other layers: <br/>No call from Zed or Glue to Yves, <br/>No call from Glue or Yves or Zed to Client, <br/>No call from Yves to Glue, <br/>No call from Zed Persistence or Presentation to Glue, <br/>No call from Zed Persistence or Presentation to Glue, <br/>No call from Zed or Client or Yves or Glue or Service to Shared, <br/>No call from Zed or Client or Yves or Glue to Service, <br/>No call from Yves or Glue to Zed, <br/>No call from Zed Presentation to Zed Business, <br/>No call from Zed Presentation to Zed Communication, <br/>No call from Zed Business or Communication or Presentation to Zed Persistence, <br/>No call from Client to Zed Persistence, <br/>No call from Zed or Client or Yves or Glue or Service or Shared to Zed Presentation. |      |
| LocatorInDependencyProviderOnlyRule          |  2   | Locator should be used in Dependency Provider only                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |      |
| SingletonInstanceInDependencyProviderOnlyRule |  2   | Singleton getInstance() initialisation should be in Dependency Provider only.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |      |
| WeirdModuleNameRule                          |  2   | Module name should not contain any weird words like test, dummy, example, antelope                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |      |
| ProjectNoBridgeRule                          |  3   | Project should not use and depend on Bridge pattern                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |      |

## Zed rules
|                Rule                | Prio |                                                                      Description                                                                      | Info |
|:----------------------------------:|:----:|:-----------------------------------------------------------------------------------------------------------------------------------------------------:|:----:|
| OrmAccessRule                      |   2  | Defines rules of calls: No call from Orm Query to Zed Business, No call from Orm Entity to Zed Business, No call from Orm Query to Zed Communication. |      |
| OrmNewEntityNotInCommunicationRule |   2  | Orm Entity can not be initialized in Zed Communication. Use Entity Manager.                                                                           |      |
| RepositoryReadOnlyRule             |   2  | Repository should not perform save, update, delete DB operations.                                                                                     |      |