---
description: Направляет генератору кода создать файл и указать имя выходного файла.
ms.assetid: d2ee6886-995f-453d-8121-f849b2d910ec
title: 'элемент '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41970da9cc6e389f4e45c5e55901ce8eb2e7797f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995871"
---
# <a name="file-element"></a>элемент 

Направляет генератору кода создать файл и указать имя выходного файла.

## <a name="usage"></a>Использование

``` syntax
<file
  name = "pathname string">
  child elements
</file>
```

## <a name="attributes"></a>Атрибуты



| attribute           | Тип                       | Обязательно       | Описание                                                                                                                         |
|---------------------|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **name**<br/> | Строка пути<br/> | Да<br/> | Имя выходного файла для созданного содержимого. Строка filename должна содержать сведения о полном пути.<br/> <br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                 | Описание                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Корпорация**<br/>                                                                                    | Разделы Text и CDATA копируются в файл без изменения. Исходный код, который не является функцией входных данных контракта, может быть добавлен в выходные файлы с помощью текста и разделов CDATA.<br/> <br/> |
| [**енумератионвалуедекларатионс**](enumerationvaluedeclarations.md)<br/>                         | Создает объявления C для значений всех перечисляемых типов.<br/> <br/>                                                                                                                                   |
| [**евентсаурцебуилдердекларатионс**](eventsourcebuilderdeclarations.md)<br/>                     | Создает объявления для функций, которые создают классы источника событий.<br/> <br/>                                                                                                                         |
| [**евентсаурцебуилдеримплементатионс**](eventsourcebuilderimplementations.md)<br/>               | Создает функции, создающие классы источника событий.<br/> <br/>                                                                                                                                          |
| [**функтиондекларатионс**](functiondeclarations.md)<br/>                                         | Создает объявления реализации для функций-посредников для операций с типом порта.<br/> <br/>                                                                                                            |
| [**хостбуилдердекларатион**](hostbuilderdeclaration.md)<br/>                                     | Создает объявление для функции, которая создает типизированный узел.<br/> <br/>                                                                                                                              |
| [**хостбуилдеримплементатион**](hostbuilderimplementation.md)<br/>                               | Создает функцию, которая создает типизированный узел.<br/> <br/>                                                                                                                                                |
| [**идлфунктиондекларатионс**](idlfunctiondeclarations.md)<br/>                                   | Создает объявления IDL для функций-посредников для операций с типом порта.<br/> <br/>                                                                                                                       |
| [**относится**](include.md)<br/>                                                                   | Включает в создаваемые выходные данные содержимое макроса или файла.<br/> <br/>                                                                                                                              |
| [**иункновндекларатионс**](iunknowndeclarations.md)<br/>                                         | Создает объявления для QueryInterface, AddRef и Release.<br/> <br/>                                                                                                                                 |
| [**иункновндефинитионс**](iunknowndefinitions.md)<br/>                                           | Создает реализации для QueryInterface, AddRef и Release.<br/> <br/>                                                                                                                              |
| [**литералинклуде**](literalinclude.md)<br/>                                                     | Помещает в созданный код инструкцию C или IDL include. <br/> <br/>                                                                                                                                    |
| [**мессажеструктуредефинитионс**](messagestructuredefinitions.md)<br/>                           | Создает определения структуры C для типов сообщений.<br/> <br/>                                                                                                                                           |
| [**мессажетипедекларатионс**](messagetypedeclarations.md)<br/>                                   | Создает объявления констант C для таблиц схемы XML для типов сообщений.<br/> <br/>                                                                                                                     |
| [**мессажетипедефинитионс**](messagetypedefinitions.md)<br/>                                     | Создает константы C для таблиц схемы XML для типов сообщений.<br/> <br/>                                                                                                                                 |
| [**намеспацедекларатионс**](namespacedeclarations.md)<br/>                                       | Создает объявления C для таблиц пространств имен.<br/> <br/>                                                                                                                                                 |
| [**намеспацедефинитионс**](namespacedefinitions.md)<br/>                                         | Создает определения языка C для таблиц пространств имен.<br/> <br/>                                                                                                                                                  |
| [**порттипедекларатионс**](porttypedeclarations.md)<br/>                                         | Создает объявления констант C для типов портов.<br/> <br/>                                                                                                                                              |
| [**порттипедефинитионс**](porttypedefinitions.md)<br/>                                           | Создает константы C для типов портов.<br/> <br/>                                                                                                                                                          |
| [**проксибуилдердекларатионс**](proxybuilderdeclarations.md)<br/>                                 | Создает объявления для функций для создания типизированных прокси-серверов.<br/> <br/>                                                                                                                                  |
| [**проксибуилдеримплементатионс**](proxybuilderimplementations.md)<br/>                           | Создает функции для создания типизированных прокси-серверов.<br/> <br/>                                                                                                                                                   |
| [**проксифунктионимплементатионс**](proxyfunctionimplementations.md)<br/>                         | Создает реализации для функций-посредников для операций с типом порта.<br/> <br/>                                                                                                                        |
| [**релатионшипметадатадекларатион**](relationshipmetadatadeclaration.md)<br/>                   | Создает прямую декларацию для метаданных размещения, указанных в элементе [**хостметадата**](hostmetadata.md) . <br/> <br/>                                                                       |
| [**релатионшипметадатадефинитион**](relationshipmetadatadefinition.md)<br/>                     | Создает определение константы C для метаданных размещения, указанных в элементе [**хостметадата**](hostmetadata.md) . <br/> <br/>                                                                     |
| [**структдекларатионс**](structdeclarations.md)<br/>                                             | Создает объявления структуры C для известных типов.<br/> <br/>                                                                                                                                            |
| [**структдефинитионс**](structdefinitions.md)<br/>                                               | Создает определения структуры C для известных типов.<br/> <br/>                                                                                                                                             |
| [**стубдекларатионс**](stubdeclarations.md)<br/>                                                 | Создает объявления для функций-заглушек для операций с типом порта.<br/> <br/>                                                                                                                            |
| [**стубдефинитионс**](stubdefinitions.md)<br/>                                                   | Создает реализации для функций-заглушек для операций с типом порта.<br/> <br/>                                                                                                                         |
| [**субскриптионфунктиондекларатионс**](subscriptionfunctiondeclarations.md)<br/>                 | Создает объявления реализации для функций-посредников подписки и отмены подписки для операций уведомления типа порта.<br/> <br/>                                                                         |
| [**субскриптионидлфунктиондекларатионс**](subscriptionidlfunctiondeclarations.md)<br/>           | Создает объявления IDL для функций-посредников подписки и отмены подписки для операций уведомления типа порта.<br/> <br/>                                                                                    |
| [**субскриптионпроксифунктионимплементатионс**](subscriptionproxyfunctionimplementations.md)<br/> | Создает реализации для функций-посредников подписки и отмены подписки для операций уведомления типа порта.<br/> <br/>                                                                                     |
| **text**<br/>                                                                                     | Разделы Text и CDATA копируются в файл без изменения. Исходный код, который не является функцией входных данных контракта, может быть добавлен в выходные файлы с помощью текста и разделов CDATA.<br/> <br/> |
| [**сисмоделметадатадекларатион**](thismodelmetadatadeclaration.md)<br/>                         | Создает прямую декларацию для константы C для метаданных производителя, указанных в элементе [**сисмоделметадата**](thismodelmetadata.md) .<br/> <br/>                                      |
| [**сисмоделметадатадефинитион**](thismodelmetadatadefinition.md)<br/>                           | Создает константу C для метаданных производителя, указанных в элементе [**сисмоделметадата**](thismodelmetadata.md) .<br/> <br/>                                                                  |
| [**типетабледекларатионс**](typetabledeclarations.md)<br/>                                       | Создает объявления констант C для таблиц схемы XML для известных типов.<br/> <br/>                                                                                                                       |
| [**типетабледефинитионс**](typetabledefinitions.md)<br/>                                         | Создает константы C для таблиц схемы XML для известных типов.<br/> <br/>                                                                                                                                   |



### <a name="child-element-sequence"></a>Последовательность дочерних элементов

``` syntax
(
  text, 
  CDATA, 
  namespaceDeclarations*, 
  namespaceDefinitions*, 
  structDeclarations*, 
  structDefinitions*, 
  typeTableDeclarations*, 
  typeTableDefinitions*, 
  thisModelMetadataDeclaration*, 
  thisModelMetadataDefinition*, 
  portTypeDeclarations*, 
  portTypeDefinitions*, 
  messageStructureDefinitions*, 
  messageTypeDeclarations*, 
  messageTypeDefinitions*, 
  idlFunctionDeclarations*, 
  subscriptionIdlFunctionDeclarations*, 
  functionDeclarations*, 
  subscriptionFunctionDeclarations*, 
  proxyFunctionImplementations*, 
  subscriptionProxyFunctionImplementations*, 
  stubDeclarations*, 
  stubDefinitions*, 
  enumerationValueDeclarations*, 
  include*, 
  IUnknownDeclarations*, 
  IUnknownDefinitions*, 
  relationshipMetadataDeclaration*, 
  relationshipMetadataDefinition*, 
  proxyBuilderDeclarations*, 
  proxyBuilderImplementations*, 
  hostBuilderDeclaration*, 
  hostBuilderImplementation*, 
  eventSourceBuilderDeclarations*, 
  eventSourceBuilderImplementations*, 
  literalInclude*
)
```

## <a name="parent-elements"></a>Родительские элементы



| Элемент                                     | Описание                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**всдкодежен**](wsdcodegen.md)<br/> | Корневой элемент XML-файла скрипта генератора кода WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Примечания

Имя файла определяется значением атрибута Name или дочернего элемента. Содержимое файла определяется другими дочерними элементами, Text и CDATA в элементе **File** . Текст и CDATA копируются в файл без изменений. Дочерние элементы заменяются созданным кодом. Текст, CDATA и дочерние элементы могут выполняться в любом порядке и могут повторяться неограниченно долго.

## <a name="element-information"></a>Сведения об элементе



| Метка | Значение |
|-------------------------------------|---------------|
| Минимальная поддерживаемая система<br/> | Windows Vista |
| Может быть пустым                        | нет            |



 

 




