---
title: Сложные типы схемы Евентманифест
description: Ниже приведены сложные типы, определяемые схемой Евентманифест.
ms.assetid: 25facfdd-3846-4215-9b84-a833d86c39ef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69200d90253b27f9e73035a14ba5817917b24e1367d3bc4a54fff37e15d112ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590063"
---
# <a name="eventmanifest-schema-complex-types"></a>Сложные типы схемы Евентманифест

Ниже приведены сложные типы, определяемые схемой Евентманифест.



| Сложный тип                                                                                       | Описание                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**битмаптипе**](eventmanifestschema-bitmaptype-complextype.md)                                   | Определяет список сопоставлений имен и значений между битовыми значениями и строковыми значениями.<br/>                                                                                                                                                  |
| [**битмапвалуетипе**](eventmanifestschema-bitmapvaluetype-complextype.md)                         | Определяет сопоставление между битовым значением и строковым значением.<br/>                                                                                                                                                                  |
| [**чаннеллисттипе**](eventmanifestschema-channellisttype-complextype.md)                         | Определяет список каналов, к которым поставщики могут регистрировать события.<br/>                                                                                                                                                                |
| [**чаннеллоггингтипе**](eventmanifestschema-channelloggingtype-complextype.md)                   | Определяет свойства файла журнала, который осуществляет резервное копирование канала, например его емкость и последовательный или циклический режим.<br/>                                                                                                |
| [**чаннелпублишингтипе**](eventmanifestschema-channelpublishingtype-complextype.md)             | Определяет свойства ведения журнала для сеанса, используемого каналом.<br/>                                                                                                                                                        |
| [**чаннелтипе**](eventmanifestschema-channeltype-complextype.md)                                 | Определяет канал, к которому поставщики могут регистрировать события.<br/>                                                                                                                                                                         |
| [**датадефинитионтипе**](eventmanifestschema-datadefinitiontype-complextype.md)                   | Определяет элемент данных, который необходимо включить в событие.<br/>                                                                                                                                                                 |
| [**дефинитионтипе**](eventmanifestschema-definitiontype-complextype.md)                           | Определяет список событий, которые поставщик может заносить в журнал.<br/>                                                                                                                                                                         |
| [**евентдефинитионтипе**](eventmanifestschema-eventdefinitiontype-complextype.md)                 | Определяет событие, которое может записывать поставщик.<br/>                                                                                                                                                                               |
| [**евентстипе**](eventmanifestschema-eventstype-complextype.md)                                   | Содержит список поставщиков, определенных в манифесте.<br/>                                                                                                                                                               |
| [**FilterType**](eventmanifestschema-filtertype-complextype.md)                                   | Определяет фильтр данных, используемый сеансом для фильтрации событий на основе данных событий.<br/>                                                                                                                                              |
| [**филтерлисттипе**](eventmanifestschema-filterlisttype-complextype.md)                           | Определяет список фильтров, которые контроллер ETW может передать поставщику для дальнейшего ограничения числа записываемых событий.<br/>                                                                                                       |
| [**импортчаннелтипе**](eventmanifestschema-importchanneltype-complextype.md)                     | Определяет канал, который был определен другим поставщиком или манифестом, содержащим раздел метаданных.<br/>                                                                                                            |
| [**InputType**](eventmanifestschema-inputtype-complextype.md)                                     | Определяет тип входных данных.<br/>                                                                                                                                                                                                  |
| [**инпуттипелисттипе**](eventmanifestschema-inputtypelisttype-complextype.md)                     | Определяет список входных типов.<br/>                                                                                                                                                                                               |
| [**инструментатионманифесттипе**](eventmanifestschema-instrumentationmanifesttype-complextype.md) | Определяет базовый тип для элемента [**инструментатионманифест**](eventmanifestschema-instrumentationmanifest-element.md) .<br/>                                                                                                |
| [**инструментатионтипе**](eventmanifestschema-instrumentationtype-complextype.md)                 | Определяет содержимое раздела инструментирования манифеста.<br/>                                                                                                                                                         |
| [**кэйвордлисттипе**](eventmanifestschema-keywordlisttype-complextype.md)                         | Определяет список ключевых слов, которые классифицируют события.<br/>                                                                                                                                                                           |
| [**кэйвордтипе**](eventmanifestschema-keywordtype-complextype.md)                                 | Определяет ключевое слово, определяющее категорию событий.<br/>                                                                                                                                                                      |
| [**левеллисттипе**](eventmanifestschema-levellisttype-complextype.md)                             | Определяет список уровней серьезности, определяющих уровень детализации события.<br/>                                                                                                                                                    |
| [**LevelType**](eventmanifestschema-leveltype-complextype.md)                                     | Определяет значение серьезности, определяющее уровень детализации регистрируемых событий.<br/>                                                                                                                                           |
| [**локализатионтипе**](eventmanifestschema-localizationtype-complextype.md)                       | Определяет группу локализованных ресурсов, на которые ссылается манифест.<br/>                                                                                                                                                  |
| [**MapType**](eventmanifestschema-maptype-complextype.md)                                         | Определяет список пар "имя-значение".<br/>                                                                                                                                                                                          |
| [**метадататипе**](eventmanifestschema-metadatatype-complextype.md)                               | Определяет типы метаданных, которые можно определить в разделе метаданных манифеста.<br/>                                                                                                                                      |
| [**намедкуеритипе**](eventmanifestschema-namedquerytype-complextype.md)                           | Определяет список именованных запросов, которые запрашивают строку сообщения о событии для значения и выполняют указанное действие, если оно найдено.<br/>                                                                                                     |
| [**опкоделисттипе**](eventmanifestschema-opcodelisttype-complextype.md)                           | Определяет список кодов операций, которые используются для определения операций компонента приложения.<br/>                                                                                                                        |
| [**опкодетипе**](eventmanifestschema-opcodetype-complextype.md)                                   | Определяет операцию в компоненте приложения.<br/>                                                                                                                                                                  |
| [**OutputType**](eventmanifestschema-outputtype-complextype.md)                                   | Определяет тип выходных данных, который определяет, как данные подготавливаются к просмотру.<br/>                                                                                                                                                        |
| [**паттернмаплисттипе**](eventmanifestschema-patternmaplisttype-complextype.md)                   | Определяет список пар регулярных выражений, которые используются для изменения строки сообщения.<br/>                                                                                                                                        |
| [**паттернмаптипе**](eventmanifestschema-patternmaptype-complextype.md)                           | Определяет сопоставление между двумя регулярными выражениями. Одно выражение используется для поиска соответствующей строки в строке сообщения, а другая — для изменения строки перед тем, как служба снова поместит ее в строку сообщения.<br/> |
| [**паттернмапвалуетипе**](eventmanifestschema-patternmapvaluetype-complextype.md)                 | Определяет регулярные выражения, используемые для поиска соответствующей строки в строке сообщения и ее изменения.<br/>                                                                                                                           |
| [**ProviderType**](eventmanifestschema-providertype-complextype.md)                               | Определяет поставщик и метаданные, используемые для определения его событий.<br/>                                                                                                                                                       |
| [**стрингтаблетипе**](eventmanifestschema-stringtabletype-complextype.md)                         | Определяет список локализованных строк, на которые можно ссылаться в манифесте.<br/>                                                                                                                                                 |
| [**структдефинитионтипе**](eventmanifestschema-structdefinitiontype-complextype.md)               | Определяет структуру, содержащую один или несколько элементов данных, которые необходимо включить в событие.<br/>                                                                                                                            |
| [**таскевентдефинитионтипе**](eventmanifestschema-taskeventdefinitiontype-complextype.md)         | Определяет событие, специфическое для задачи, которое поставщик может заносить в журнал.<br/>                                                                                                                                                                    |
| [**тасклисттипе**](eventmanifestschema-tasklisttype-complextype.md)                               | Определяет список задач, которые используются для определения компонентов приложения.<br/>                                                                                                                                          |
| [**TaskType**](eventmanifestschema-tasktype-complextype.md)                                       | Определяет компонент или подкомпонент приложения.<br/>                                                                                                                                                                       |
| [**темплатеитемтипе**](eventmanifestschema-templateitemtype-complextype.md)                       | Шаблон, определяющий данные, включаемые в событие.<br/>                                                                                                                                                                   |
| [**темплателисттипе**](eventmanifestschema-templatelisttype-complextype.md)                       | Определяет список шаблонов, указывающих данные, включаемые в события.<br/>                                                                                                                                                |
| [**типелисттипе**](eventmanifestschema-typelisttype-complextype.md)                               | Определяет типы, используемые в манифесте.<br/>                                                                                                                                                                             |
| [**валуемаптипе**](eventmanifestschema-valuemaptype-complextype.md)                               | Определяет список сопоставлений имен и значений между целочисленными значениями и строковыми значениями.<br/>                                                                                                                                              |
| [**валуемапвалуетипе**](eventmanifestschema-valuemapvaluetype-complextype.md)                     | Определяет сопоставление между целочисленным значением и строковым значением.<br/>                                                                                                                                                             |
| [**XmlType**](eventmanifestschema-xmltype-complextype.md)                                         | Определяет фрагмент XML.<br/>                                                                                                                                                                                                     |
| [**ксмлтипелисттипе**](eventmanifestschema-xmltypelisttype-complextype.md)                         | Определяет выходные типы списка, которые служба использует для определения способа визуализации входного типа данных.<br/>                                                                                                                             |



 

 

 





