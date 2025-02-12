## Client rules
|                  Rule                  | Prio |                                     Description                                    | Info |
|:--------------------------------------:|:----:|:----------------------------------------------------------------------------------:|:----:|
| ClientRule                             |   3  | Must implement an interface with same name and suffix 'Interface'.                 |      |
| ClientInterfaceRule                    |   5  | Every method must also contain the @api tag in docblock and a contract text above. |      |
| ClientDependencyProviderMethodNameRule |   3  | DependencyProvider should only contain additional add*() or get*() methods.        |      |

## Common rules
|                  Rule                 | Prio |                                                                        Description                                                                       | Info |
|:-------------------------------------:|:----:|:--------------------------------------------------------------------------------------------------------------------------------------------------------:|:----:|
| ImplementsApiInheritDocRule           |   5  | Every API public method must also contain the {@inheritDoc} tag in docblock.                                                                             |      |
| GetterReturnTypeRule                  |   5  | Getter must return something. Please add return type.                                                                                                    |      |
| ExistsPostfixRule                     |   4  | Postfix `Exists` must be used instead of `Exist`. Postfix `Exists` must be in the end of method name. Prefix `is` must not be used with postfix `Exist`. |      |
| ExternalMethodExtensionReturnTypeRule |   3  | Method must have return type.                                                                                                                            |      |
| FactoryGetContainNoNewRule            |   3  | A `get*()` method in factories must not contain a `new` keyword.                                                                                         |      |
| FactoryMethodReturnInterfaceRule      |   5  | Every method in a Factory must only return an interface or an array of interfaces.                                                                       |      |
| FactoryCreateContainOneNewRule        |   3  | A `create*()` method in factories must contain exactly 1 `new` statement for instantiation.                                                              |      |
| FactoryNoLoopsRule                    |   3  | Factory methods should not contain loops.                                                                                                                |      |
| FactoryOnlyGetAndCreateRule           |   3  | Factories should only contain get*() and create*() methods.                                                                                              |      |
| FactoryNoLogicRule                    |   4  | Factory should not contain any business logic.                                                                                                           |      |
| FactoryOnlyPublicMethodsRule          |   4  | All the factory methods should be public by default                                                                                                      |      |
| FactoryPropelQueryMethodNameRule      |   4  | Get propel query methods must be named like get*PropelQuery() in factory.                                                                                |      |
| CommunicationControllerRule           |   3  | All public controller methods have the suffix `*Action`                                                                                                  |      |
| PluginSuffixRule                      |   3  | Plugins must be suffixed with 'Plugin'                                                                                                                   |      |
| PluginInterfaceSuffixRule             |   3  | Plugin interfaces must be suffixed with 'PluginInterface'!                                                                                               |      |
| NewPluginExtensionModuleRule          |   4  | A plugin class must implement a ModuleExtension's interface instead of implementing an extension interface of Module                                     |      |

## Shared
|                   Rule                   | Prio |                                                                                  Description                                                                                  | Info |
|:----------------------------------------:|:----:|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:----:|
| ModuleConstantsPathRule                  |   4  | An environment configuration must lie in "Shared" layer.                                                                                                                      |      |
| ModuleConstantsTypeRule                  |   4  | An environment configuration must be an interface.                                                                                                                            |      |
| ModuleConstantsNoMethodAllowedRule       |   4  | The modules *Constants interfaces must only contain constants to be used with env config, no methods etc                                                                      |      |
| ModuleConstantsFormingConstantValuesRule |   5  | The modules ' *Constants interfaces must only contain constants to be used with env config. Their values must be exactly the same as the const key prefixed with module name. |      |

## Service rules
|                   Rule                  | Prio |                                     Description                                    | Info |
|:---------------------------------------:|:----:|:----------------------------------------------------------------------------------:|:----:|
| ServiceInterfaceRule                    |   5  | Every method must also contain the @api tag in docblock and a contract text above. |      |
| ServiceRule                             |   3  | Must implement an interface with same name and suffix 'Interface'.                 |      |
| ServiceDependencyProviderMethodNameRule |   3  | DependencyProvider should only contain additional add*() or get*() methods.        |      |## Shared rules

## Yves rules
|                 Rule                 | Prio |                                 Description                                 | Info |
|:------------------------------------:|:----:|:---------------------------------------------------------------------------:|:----:|
| YvesDependencyProviderMethodNameRule |   3  | DependencyProvider should only contain additional add*() or get*() methods. |      |

## Zed rules
|                       Rule                       | Prio |                                            Description                                           |                           Info                           |
|:------------------------------------------------:|:----:|:------------------------------------------------------------------------------------------------:|:--------------------------------------------------------:|
| AllMethodsPublicInFacadeRule                     |  2   | A facade must only contain public methods.                                                       |                                                          |
| FacadeArgumentsNotAllowedUseEntityTransferRule   |  2   | Facade methods shouldn`t use entity transfers.                                                   |                                                          |
| FacadeArgumentsRule                              |  5   | Every Facade should only retrieve native types or transfer objects.                              | Decremented priority due to core specific implementation |
| FacadeNoLogicRule                                |  2   | A Facade must not contain logic and only delegate.                                               |                                                          |
| FacadeReturnValueRule                            |  5   | Every Facade should only return native types or transfer objects.                                | Decremented priority due to core specific implementation |
| FacadeRule                                       |  2   | A facade must not have properties. It must also not contain any instantiations, only delegation. |                                                          |
| FacadeInterfaceRule                              |  2   | Must implement an interface with same name and suffix 'Interface'.                               |                                                          |
| FacadeSingleFactoryCallRule                      |  2   | Every Facade method should have no more than one factory call.                                   |                                                          |
| ZedDependencyProviderMethodNameRule              |  3   | DependencyProvider should only contain additional add*() or get*() methods.                      |                                                          |
| PluginArgumentsNotAllowedUseEntityTransferRule   |  2   | Plugin methods shouldn`t use entity transfers.                                                   |                                                          |
| ZedDependencyProviderPropelQueryConstantNameRule |  4   | Propel query constants must be named like PROPEL_QUERY_* in dependency provider.                 |                                                          |
| ZedDependencyProviderPropelQueryMethodNameRule   |  4   | Add propel query methods must be named like add*PropelQuery() in dependency provider.            |                                                          |
