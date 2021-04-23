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
ms.openlocfilehash: ac212205fac02db0ee87d8acbe0b123ffcead921
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "105710402"
---
# <a name="xml-node"></a><span data-ttu-id="a78fd-107">XML-узел</span><span class="sxs-lookup"><span data-stu-id="a78fd-107">XML Node</span></span>

<span data-ttu-id="a78fd-108">XML-узел представляет собой один фрагмент XML, например начальный элемент и его атрибуты, конечный элемент, текст или типизированное текстовое содержимое, например целочисленный или байтовый массив.</span><span class="sxs-lookup"><span data-stu-id="a78fd-108">An XML Node represents a single piece of XML, for example, a start element and its attributes, an end element, text, or "typed" text content such as an integer or byte array.</span></span> <span data-ttu-id="a78fd-109">Данные в узле зависят от [**\_ \_ \_ типа узла WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).</span><span class="sxs-lookup"><span data-stu-id="a78fd-109">The data in a node varies according to the [**WS\_XML\_NODE\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).</span></span>


<span data-ttu-id="a78fd-110">Ниже приведен пример XML-документа для кодирования, представленного с помощью независимых структур кодирования.</span><span class="sxs-lookup"><span data-stu-id="a78fd-110">The following shows an example of an encoding specific xml document represented with encoding independent structures.</span></span>

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

<span data-ttu-id="a78fd-111">С XML-узлами используются следующие перечисления:</span><span class="sxs-lookup"><span data-stu-id="a78fd-111">The following enumerations are used with XML nodes:</span></span>

-   [<span data-ttu-id="a78fd-112">**\_тип значения \_ WS**</span><span class="sxs-lookup"><span data-stu-id="a78fd-112">**WS\_VALUE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [<span data-ttu-id="a78fd-113">**\_ \_ тип узла WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="a78fd-113">**WS\_XML\_NODE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [<span data-ttu-id="a78fd-114">**\_тип XML- \_ текста \_ WS**</span><span class="sxs-lookup"><span data-stu-id="a78fd-114">**WS\_XML\_TEXT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

<span data-ttu-id="a78fd-115">Для XML-узлов используются следующие функции:</span><span class="sxs-lookup"><span data-stu-id="a78fd-115">The following functions are used with XML nodes:</span></span>

-   [<span data-ttu-id="a78fd-116">**встримксмлвхитеспаце**</span><span class="sxs-lookup"><span data-stu-id="a78fd-116">**WsTrimXmlWhitespace**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [<span data-ttu-id="a78fd-117">**всверификсмлнкнаме**</span><span class="sxs-lookup"><span data-stu-id="a78fd-117">**WsVerifyXmlNCName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [<span data-ttu-id="a78fd-118">**всксмлстринжекуалс**</span><span class="sxs-lookup"><span data-stu-id="a78fd-118">**WsXmlStringEquals**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

<span data-ttu-id="a78fd-119">С узлами XML используются следующие макросы:</span><span class="sxs-lookup"><span data-stu-id="a78fd-119">The following macros are used with XML nodes:</span></span>

-   [<span data-ttu-id="a78fd-120">**\_ \_ \_ значение словаря XML-строк WS \_**</span><span class="sxs-lookup"><span data-stu-id="a78fd-120">**WS\_XML\_STRING\_DICTIONARY\_VALUE**</span></span>](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   <span data-ttu-id="a78fd-121">[**\_строка WS \_ XML \_ null**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a78fd-121">[**WS\_XML\_STRING\_NULL**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))</span></span>
-   [<span data-ttu-id="a78fd-122">**\_XML- \_ \_ значение строки WS**</span><span class="sxs-lookup"><span data-stu-id="a78fd-122">**WS\_XML\_STRING\_VALUE**</span></span>](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

<span data-ttu-id="a78fd-123">Для XML-узлов используются следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="a78fd-123">The following structures are used with XML nodes:</span></span>

-   [<span data-ttu-id="a78fd-124">**\_атрибут WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="a78fd-124">**WS\_XML\_ATTRIBUTE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [<span data-ttu-id="a78fd-125">**\_Текст XML-файла в \_ кодировке Base64 \_**</span><span class="sxs-lookup"><span data-stu-id="a78fd-125">**WS\_XML\_BASE64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [<span data-ttu-id="a78fd-126">**\_текст bool XML-файла WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a78fd-126">**WS\_XML\_BOOL\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [<span data-ttu-id="a78fd-127">**\_ \_ узел комментария WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="a78fd-127">**WS\_XML\_COMMENT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [<span data-ttu-id="a78fd-128">**\_текст XML- \_ DateTime \_ для WS**</span><span class="sxs-lookup"><span data-stu-id="a78fd-128">**WS\_XML\_DATETIME\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [<span data-ttu-id="a78fd-129">**\_ \_ десятичный текст XML-файла \_**</span><span class="sxs-lookup"><span data-stu-id="a78fd-129">**WS\_XML\_DECIMAL\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [<span data-ttu-id="a78fd-130">**\_XML- \_ словарь WS**</span><span class="sxs-lookup"><span data-stu-id="a78fd-130">**WS\_XML\_DICTIONARY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [<span data-ttu-id="a78fd-131">**\_ \_ двойной текст XML-файла WS \_**</span><span class="sxs-lookup"><span data-stu-id="a78fd-131">**WS\_XML\_DOUBLE\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [<span data-ttu-id="a78fd-132">**\_узел XML- \_ элемента \_ WS**</span><span class="sxs-lookup"><span data-stu-id="a78fd-132">**WS\_XML\_ELEMENT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [<span data-ttu-id="a78fd-133">**\_XML- \_ текст с плавающей запятой WS \_**</span><span class="sxs-lookup"><span data-stu-id="a78fd-133">**WS\_XML\_FLOAT\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [<span data-ttu-id="a78fd-134">**\_текст GUID XML-файла WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a78fd-134">**WS\_XML\_GUID\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [<span data-ttu-id="a78fd-135">**\_XML- \_ текст WS Int32 \_**</span><span class="sxs-lookup"><span data-stu-id="a78fd-135">**WS\_XML\_INT32\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [<span data-ttu-id="a78fd-136">**\_XML- \_ \_ текст Int64**</span><span class="sxs-lookup"><span data-stu-id="a78fd-136">**WS\_XML\_INT64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [<span data-ttu-id="a78fd-137">**\_ \_ текст списка WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="a78fd-137">**WS\_XML\_LIST\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [<span data-ttu-id="a78fd-138">**\_узел WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="a78fd-138">**WS\_XML\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [<span data-ttu-id="a78fd-139">**WS \_ XML \_ QNAME**</span><span class="sxs-lookup"><span data-stu-id="a78fd-139">**WS\_XML\_QNAME**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [<span data-ttu-id="a78fd-140">**\_текст XML-файла \_ QNAME \_**</span><span class="sxs-lookup"><span data-stu-id="a78fd-140">**WS\_XML\_QNAME\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [<span data-ttu-id="a78fd-141">**\_XML- \_ строка WS**</span><span class="sxs-lookup"><span data-stu-id="a78fd-141">**WS\_XML\_STRING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [<span data-ttu-id="a78fd-142">**\_текст XML-файла WS \_**</span><span class="sxs-lookup"><span data-stu-id="a78fd-142">**WS\_XML\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [<span data-ttu-id="a78fd-143">**\_ \_ текстовый узел XML \_ WS**</span><span class="sxs-lookup"><span data-stu-id="a78fd-143">**WS\_XML\_TEXT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [<span data-ttu-id="a78fd-144">**\_текст XML \_ ИНТЕРВАЛа WS \_**</span><span class="sxs-lookup"><span data-stu-id="a78fd-144">**WS\_XML\_TIMESPAN\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [<span data-ttu-id="a78fd-145">**\_XML- \_ \_ текст UINT64**</span><span class="sxs-lookup"><span data-stu-id="a78fd-145">**WS\_XML\_UINT64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [<span data-ttu-id="a78fd-146">**\_ \_ текст уникального \_ идентификатора XML-файла WS \_**</span><span class="sxs-lookup"><span data-stu-id="a78fd-146">**WS\_XML\_UNIQUE\_ID\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [<span data-ttu-id="a78fd-147">**\_Текст XML-документа \_ UTF16 \_**</span><span class="sxs-lookup"><span data-stu-id="a78fd-147">**WS\_XML\_UTF16\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [<span data-ttu-id="a78fd-148">**\_Текст XML- \_ UTF8 \_ WS**</span><span class="sxs-lookup"><span data-stu-id="a78fd-148">**WS\_XML\_UTF8\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 