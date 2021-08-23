---
title: XML-узел
description: XML-узел представляет собой один фрагмент XML, например начальный элемент и его атрибуты, конечный элемент, текст или \ 0034; типизированный \ 0034; текстовое содержимое, например целое число или массив байтов. Данные в узле зависят от \_ \_ типа узла WS XML \_ .
ms.assetid: c514c542-029b-46d1-a796-1f132a41b2ad
keywords:
- Веб-службы узла XML для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b851ad0ab0a6a333fedea13036eebf11e8c727a04603c07d8f7e68e66de5ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545654"
---
# <a name="xml-node"></a>XML-узел

XML-узел представляет собой один фрагмент XML, например начальный элемент и его атрибуты, конечный элемент, текст или типизированное текстовое содержимое, например целочисленный или байтовый массив. Данные в узле зависят от [**\_ \_ \_ типа узла WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).


Ниже приведен пример XML-документа для кодирования, представленного с помощью независимых структур кодирования.

``` syntax
<p:PurchaseOrder xmlns:p="http://tempuri.org" p:id="3891">
    <p:Buyer>Joe</p:Buyer>
</p:PurchaseOrder>
```

``` syntax
WS_XML_STRING purchaseOrder = WS_XML_STRING_VALUE("PurchaseOrder");
WS_XML_STRING id            = WS_XML_STRING_VALUE("id");
WS_XML_STRING prefix        = WS_XML_STRING_VALUE("p");
WS_XML_STRING ns            = WS_XML_STRING_VALUE("http://tempuri.org");

WS_XML_ATTRIBUTE xmlnsAttribute =
{
    /* singleQuote */ FALSE,
    /* isXmlNs     */ TRUE,
    /* prefix      */ &prefix,
    /* localName   */ NULL,
    /* ns          */ &ns,
    /* value       */ NULL
};
WS_XML_INT32_TEXT idText =
{
    /* text  */ { WS_XML_TEXT_TYPE_INT32 },
    /* value */ 3891
};
WS_XML_ATTRIBUTE idAttribute =
{
    /* singleQuote */ FALSE,
    /* isXmlNs     */ FALSE,
    /* prefix      */ &prefix,
    /* localName   */ &id,
    /* ns          */ &ns,
    /* value       */ &idText.text,
};
WS_XML_ATTRIBUTE* attributes[2] =
{
    &xmlnsAttribute,
    &idAttribute
};
WS_XML_ELEMENT_NODE elementNode =
{
    /* node           */ { WS_XML_NODE_TYPE_ELEMENT },
    /* prefix         */ &prefix,
    /* localName      */ &purchaseOrder,
    /* ns             */ &ns,
    /* attributeCount */ 2,
    /* attributes     */ attributes,
    /* isEmpty        */ FALSE,
    /* array          */ NULL,
};
WS_XML_UTF8_TEXT joeText =
{
    /* text  */ { WS_XML_TEXT_TYPE_UTF8 },
    /* value */ WS_XML_STRING_VALUE("Joe")
};
WS_XML_TEXT_NODE textNode =
{
    /* node */ { WS_XML_NODE_TYPE_TEXT },
    /* text */ &joeText.text
};
WS_XML_NODE endElementNode =
{
    WS_XML_NODE_TYPE_END_ELEMENT
};
WS_XML_NODE* nodes[3] =
{
    &elementNode.node,
    &textNode.node,
    &endElementNode
};
```

С XML-узлами используются следующие перечисления:

-   [**\_тип значения \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [**\_ \_ тип узла WS \_ XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [**\_тип XML- \_ текста \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

Для XML-узлов используются следующие функции:

-   [**встримксмлвхитеспаце**](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [**всверификсмлнкнаме**](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [**всксмлстринжекуалс**](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

С узлами XML используются следующие макросы:

-   [**\_ \_ \_ значение словаря XML-строк WS \_**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   [**\_строка WS \_ XML \_ null**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))
-   [**\_XML- \_ \_ значение строки WS**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

Для XML-узлов используются следующие структуры:

-   [**\_атрибут WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [**\_Текст XML-файла в \_ кодировке Base64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [**\_текст bool XML-файла WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [**\_ \_ узел комментария WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [**\_текст XML- \_ DateTime \_ для WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [**\_ \_ десятичный текст XML-файла \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [**\_XML- \_ словарь WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [**\_ \_ двойной текст XML-файла WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [**\_узел XML- \_ элемента \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [**\_XML- \_ текст с плавающей запятой WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [**\_текст GUID XML-файла WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [**\_XML- \_ текст WS Int32 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [**\_XML- \_ \_ текст Int64**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [**\_ \_ текст списка WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [**\_узел WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [**WS \_ XML \_ QNAME**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [**\_текст XML-файла \_ QNAME \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [**\_XML- \_ строка WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [**\_текст XML-файла WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [**\_ \_ текстовый узел XML \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [**\_текст XML \_ ИНТЕРВАЛа WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [**\_XML- \_ \_ текст UINT64**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [**\_ \_ текст уникального \_ идентификатора XML-файла WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [**\_Текст XML-документа \_ UTF16 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [**\_Текст XML- \_ UTF8 \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 