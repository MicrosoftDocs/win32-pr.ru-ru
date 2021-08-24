---
title: средство чтения XML
description: Модуль чтения XML — это указатель на входной источник XML. По сути, средство чтения XML считывает один узел XML за раз, но существуют дополнительные вспомогательные API для упрощения чтения последовательности узлов.
ms.assetid: 1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2
keywords:
- Веб-службы чтения XML для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a03ef961cd49c481564b6bad1ad86603c9cb576f0c8aeda1a7cd2d6d18aaeef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770874"
---
# <a name="xml-reader"></a>средство чтения XML

Модуль чтения XML — это указатель на входной источник XML. По сути, средство чтения XML считывает один [узел XML](xml-node.md) за раз, но существуют дополнительные вспомогательные API для упрощения чтения последовательности узлов.


Поддерживаются следующие типы входных данных для читателей:

-   [**Буфер в памяти закодированных байтов**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**Поток**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [XML-буфер](xml-buffer.md)

### <a name="security"></a>Безопасность

Средство чтения проверит, являются ли атрибуты элемента уникальными. Время, необходимое для выполнения этой проверки, — это функция числа атрибутов в элементе, которая может быть максимально допустимой для [**\_ \_ свойств модуля чтения XML \_ \_ \_ -данных WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id). Таким образом, обработка больших документов в случае, если для **\_ \_ \_ свойства \_ Max \_ XML Reader** задано большое значение, может возникать возможность атаки типа "отказ в обслуживании".

Модуль чтения будет сопоставлять префиксы к пространствам имен для каждого элемента и атрибутов. Время, необходимое для выполнения этого сопоставления, — это функция количества атрибутов xmlns в области, которая может иметь размер [**\_ \_ \_ \_ \_ пространства имен WS XML Reader Max**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id). Поэтому обработка больших документов, если это свойство имеет большое значение, может представлять собой возможность атаки типа "отказ в обслуживании".

Хотя читатель гарантирует, что документ будет следовать грамматической спецификации XML и более того, что его аспекты находятся в заданных квотах, содержимое документа все равно должно считаться ненадежным при поступлении из ненадежного источника. Пользователи модуля чтения должны проверять все имена элементов и атрибутов и пространства имен с помощью [**всреадтостартелемент**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**всфиндаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)или вручную проверять [**узлы**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).

Некоторые другие ситуации, которые следует учитывать, включают, но не ограничиваются:

-   Возможно, отсутствуют ожидаемые элементы
-   Могут отображаться непредвиденные элементы
-   Возможно, отсутствуют ожидаемые атрибуты
-   Могут отображаться непредвиденные атрибуты
-   Элементы могут отображаться как пустые элементы
-   Пробелы могут появляться в непредвиденных местах

Пользователи модуля чтения не должны распределять память на основе значений, считанных из документа. Например, рассмотрим следующий XML-документ:

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

Выделение массива на основе предположения, что некоторое количество элементов будет соответствовать потенциальному вектору атаки. Пользователь модуля чтения в этом случае должен последовательно распределять память по мере отображения элементов.

Модуль чтения XML не поддерживает DTD. Пользователю средства чтения не нужно беспокоиться о проверке DTD.

Для средств чтения XML используется следующий обратный вызов:

-   [**\_ \_ обратный вызов WS Read**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

С модулями чтения XML используются следующие перечисления:

-   [**\_ \_ \_ тип кодировки модуля чтения XML WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [**\_ \_ \_ тип входных данных модуля чтения XML WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [**\_ \_ идентификатор свойства модуля чтения XML \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

Для модулей чтения XML используются следующие функции.

-   [**вскреатереадер**](/windows/desktop/api/WebServices/nf-webservices-wscreatereader)
-   [**всфиллреадер**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader)
-   [**всфиндаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)
-   [**всфриреадер**](/windows/desktop/api/WebServices/nf-webservices-wsfreereader)
-   [**всжетнамеспацефромпрефикс**](/windows/desktop/api/WebServices/nf-webservices-wsgetnamespacefromprefix)
-   [**всжетреадерноде**](/windows/desktop/api/WebServices/nf-webservices-wsgetreadernode)
-   [**всжетреадерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition)
-   [**всжетреадерпроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderproperty)
-   [**всжетксмлаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute)
-   [**всмовереадер**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader)
-   [**всреадаррай**](/windows/desktop/api/WebServices/nf-webservices-wsreadarray)
-   [**всреадбитес**](/windows/desktop/api/WebServices/nf-webservices-wsreadbytes)
-   [**всреадчарс**](/windows/desktop/api/WebServices/nf-webservices-wsreadchars)
-   [**WsReadCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wsreadcharsutf8)
-   [**всреадендаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wsreadendattribute)
-   [**всреаденделемент**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)
-   [**всреадноде**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode)
-   [**всреадкуалифиеднаме**](/windows/desktop/api/WebServices/nf-webservices-wsreadqualifiedname)
-   [**всреадстартаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartattribute)
-   [**всреадстартелемент**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)
-   [**всреадтостартелемент**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)
-   [**всреадвалуе**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue)
-   [**вссетинпут**](/windows/desktop/api/WebServices/nf-webservices-wssetinput)
-   [**вссетинпуттобуффер**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer)
-   [**вссетреадерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition)
-   [**всскипноде**](/windows/desktop/api/WebServices/nf-webservices-wsskipnode)

Для модулей чтения XML используется следующий маркер:

-   [\_ \_ модуль чтения XML WS](ws-xml-reader.md)

Для средств чтения XML используются следующие структуры:

-   [**\_ \_ \_ двоичное кодирование модуля чтения XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [**\_ \_ входной буфер модуля чтения XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**\_ \_ кодирование модуля чтения XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [**\_ \_ входные данные модуля чтения XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [**\_ \_ Кодирование MTOM в модуле чтения XML для модуля WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [**\_ \_ Свойства модуля чтения XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [**\_ \_ свойство модуля чтения XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [**\_ \_ \_ входные данные потока модуля чтения XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [**\_ \_ Кодировка текста для модуля чтения XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 




