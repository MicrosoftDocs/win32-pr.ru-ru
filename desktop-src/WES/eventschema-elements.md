---
title: Элементы схемы событий
description: Ниже перечислены элементы, определяемые схемой событий.
ms.assetid: 972c0a78-32d5-45b3-bcc3-6423b60bfa6f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 34149fae8ac273565f98c3f39adb31b61b406ade
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791953"
---
# <a name="event-schema-elements"></a>Элементы схемы событий

Ниже перечислены элементы, определяемые схемой событий. В этом разделе содержатся имена элементов, которые можно найти в журнале событий. Однако, чтобы получить подробные сведения для каждого элемента, см. сложный тип, содержащий элемент.



| Элемент                                                                                                    | Описание                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Бинаревентдата (EventType)**](eventschema-binaryeventdata-eventtype-element.md)                       | Содержит данные события как двоичный BLOB-объект.<br/>                                                                                                                                                   |
| [**Двоичный (Евентдататипе)**](eventschema-binary-eventdatatype-element.md)                                 | Двоичный BLOB-объект данных для событий, записываемых с помощью [ведения журнала событий](/windows/desktop/EventLog/event-logging).<br/>                                                                                                   |
| [**Канал (Рендерингинфотипе)**](eventschema-channel-renderinginfotype-element.md)                       | Строка отображаемого сообщения канала, указанного в событии.<br/>                                                                                                                          |
| [**Канал (Системпропертиестипе)**](eventschema-channel-systempropertiestype-element.md)                 | Канал, в который было записано событие.<br/>                                                                                                                                                  |
| [**Комплексдата (Евентдататипе)**](eventschema-complexdata-eventdatatype-element.md)                       | Структура, определенная в шаблоне для события.<br/>                                                                                                                                  |
| [**Компонент (Дебугдататипе)**](eventschema-component-debugdatatype-element.md)                           | Имя компонента, который записал в журнал сообщение трассировки.<br/>                                                                                                                                    |
| [**Компьютер (Системпропертиестипе)**](eventschema-computer-systempropertiestype-element.md)               | имя компьютера, на котором произошло событие.<br/>                                                                                                                                       |
| [**Корреляция (Системпропертиестипе)**](eventschema-correlation-systempropertiestype-element.md)         | Идентификаторы действий, которые потребители могут использовать для группирования связанных событий.<br/>                                                                                                           |
| [**Датаитемнаме (Процессинжеррордататипе)**](eventschema-dataitemname-processingerrordatatype-element.md) | Содержит имя элемента данных события, вызвавшего ошибку при обработке данных события.<br/>                                                                                            |
| [**Данные (Комплексдататипе)**](eventschema-data-complexdatatype-element.md)                                 | Список элементов данных в структуре. Список элементов находится в том же порядке, что и определено в шаблоне.<br/>                                                                                |
| [**Данные (Евентдататипе)**](eventschema-data-eventdatatype-element.md)                                     | Элемент данных верхнего уровня, определенный в шаблоне для события.<br/>                                                                                                                        |
| [**Дебугдата (EventType)**](eventschema-debugdata-eventtype-element.md)                                   | Содержит данные, которые могут быть зарегистрированы для событий препроцессора трассировки программного обеспечения Windows (WPP).<br/>                                                                                                  |
| [**Код ошибки (Процессинжеррордататипе)**](eventschema-errorcode-processingerrordatatype-element.md)       | Содержит код ошибки, который был вызван, когда произошла ошибка при обработке данных события. <br/>                                                                                                     |
| [**Событие**](eventschema-event-element.md)                                                                 | Это корневой узел данных соформируемого события.<br/>                                                                                                                                           |
| [**EventData (EventType)**](eventschema-eventdata-eventtype-element.md)                                   | Содержит данные о событии.<br/>                                                                                                                                                                    |
| [**EventID (Системпропертиестипе)**](eventschema-eventid-systempropertiestype-element.md)                 | Идентификатор, используемый поставщиком для идентификации события.<br/>                                                                                                                                |
| [**Евентпайлоад (Процессинжеррордататипе)**](eventschema-eventpayload-processingerrordatatype-element.md) | Содержит двоичные данные событий для события, которое привело к ошибке при обработке данных события. <br/>                                                                                           |
| [**Евентрекордид (Системпропертиестипе)**](eventschema-eventrecordid-systempropertiestype-element.md)     | Номер записи, назначенный событию при регистрации.<br/>                                                                                                                                 |
| [**Выполнение (Системпропертиестипе)**](eventschema-execution-systempropertiestype-element.md)             | Содержит сведения о процессе и потоке, которые зарегистрировали событие.<br/>                                                                                                                    |
| [**Филелине (Дебугдататипе)**](eventschema-fileline-debugdatatype-element.md)                             | Имя исходного файла и строка в исходном файле, которая записала в журнал сообщение трассировки.<br/>                                                                                              |
| [**FlagName (Дебугдататипе)**](eventschema-flagname-debugdatatype-element.md)                             | Значение флага, передаваемое поставщику при его включении.<br/>                                                                                                                                  |
| [**Функция (Дебугдататипе)**](eventschema-function-debugdatatype-element.md)                             | Имя функции, которая зарегистрировала сообщение трассировки.<br/>                                                                                                                                     |
| [**Ключевое слово (ключевые слова)**](eventschema-keyword-keywords-element.md)                                         | Содержит отображаемое ключевое слово.<br/>                                                                                                                                                                |
| [**Ключевые слова (Рендерингинфотипе)**](eventschema-keywords-renderingtype-element.md)                         | Список отображаемых ключевых слов.<br/>                                                                                                                                                                |
| [**Ключевые слова (Системпропертиестипе)**](eventschema-keywords-systempropertiestype-element.md)               | Битовая маска ключевых слов, определенных в событии.<br/>                                                                                                                                             |
| [**LevelName (Дебугдататипе)**](eventschema-levelname-debugdatatype-element.md)                           | Значение уровня, передаваемое поставщику при его включении.<br/>                                                                                                                                 |
| [**Level (Рендерингинфотипе)**](eventschema-level-renderingtype-element.md)                               | Строка отображаемого сообщения уровня, указанного в событии.<br/>                                                                                                                            |
| [**Level (Системпропертиестипе)**](eventschema-level-systempropertiestype-element.md)                     | Содержит степень серьезности события.<br/>                                                                                                                                                   |
| [**Сообщение (Дебугдататипе)**](eventschema-message-debugdatatype-element.md)                               | Строка сообщения. XML-код содержит этот элемент, если в событии WPP указано поле Форматтедстринг.<br/>                                                                                     |
| [**Сообщение (Рендерингинфотипе)**](eventschema-message-renderingtype-element.md)                           | Содержит сообщение о событии, которое отображается для события.<br/>                                                                                                                                  |
| [**Код операции (Рендерингинфотипе)**](eventschema-opcode-renderingtype-element.md)                             | Строка отображаемого сообщения кода операции, указанного в событии.<br/>                                                                                                                           |
| [**Код операции (Системпропертиестипе)**](eventschema-opcode-systempropertiestype-element.md)                   | Код операции, определенный в событии.<br/>                                                                                                                                                            |
| [**Процессинжеррордата (EventType)**](eventschema-processingerrordata-eventtype-element.md)               | Содержит подробные сведения об ошибке, возникшей при попытке подготовки к просмотру события.<br/>                                                                                                               |
| [**Поставщик (Системпропертиестипе)**](eventschema-provider-systempropertiestype-element.md)               | Определяет поставщика, который зарегистрировал событие.<br/>                                                                                                                                              |
| [**Поставщик (Рендерингинфотипе)**](eventschema-publisher-renderinginfotype-element.md)                    | Строка отображаемого сообщения для поставщика.<br/>                                                                                                                                               |
| [**Рендерингинфо (EventType)**](eventschema-renderinginfo-eventtype-element.md)                           | Содержит строки отображаемых сообщений для события (включая строку сообщения события и строки сообщения для любого свойства события, например уровень, задача и код операции).<br/>        |
| [**Безопасность (Системпропертиестипе)**](eventschema-security-systempropertiestype-element.md)               | Указывает пользователя, который записал в журнал событие.<br/>                                                                                                                                                  |
| [**SequenceNumber (Дебугдататипе)**](eventschema-sequencenumber-debugdatatype-element.md)                 | Локальный или глобальный порядковый номер сообщения трассировки.<br/>                                                                                                                                   |
| [**Подкомпонент (Дебугдататипе)**](eventschema-subcomponent-debugdatatype-element.md)                     | Указывает поле трассировки отладки Субкомпонентнаме WPP, которое используется в отладочных событиях в каналах отладки.                                                                                                 |
| [**Система (EventType)**](eventschema-system-eventtype-element.md)                                         | Содержит сведения, определяющие поставщик и способ его включения, событие, канал, на который было написано событие, а также системные сведения, такие как идентификатор процесса и потока.<br/> |
| [**Задача (Рендерингинфотипе)**](eventschema-task-renderingtype-element.md)                                 | Строка отображаемого сообщения задачи, указанной в событии.<br/>                                                                                                                             |
| [**Задача (Системпропертиестипе)**](eventschema-task-systempropertiestype-element.md)                       | Задача, определенная в событии.<br/>                                                                                                                                                              |
| [**TimeCreated (Системпропертиестипе)**](eventschema-timecreated-systempropertiestype-element.md)         | Метка времени, определяющая время записи события в журнал.<br/>                                                                                                                                   |
| [**UserData (EventType)**](eventschema-userdata-eventtype-element.md)                                     | Содержит данные о событии.<br/>                                                                                                                                                                    |
| [**Версия (Системпропертиестипе)**](schema-version-systempropertiestype-element.md)                      | Содержит номер версии определения события.<br/>                                                                                                                                      |



 

 

