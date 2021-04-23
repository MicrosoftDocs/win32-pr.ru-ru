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
ms.openlocfilehash: 8d9d9c91b6594ec569536751751a3efca4c32e08
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488547"
---
# <a name="xml-reader"></a><span data-ttu-id="a3cd4-107">средство чтения XML</span><span class="sxs-lookup"><span data-stu-id="a3cd4-107">XML Reader</span></span>

<span data-ttu-id="a3cd4-108">Модуль чтения XML — это указатель на входной источник XML.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-108">XML Reader is a cursor over an input source of XML.</span></span> <span data-ttu-id="a3cd4-109">По сути, средство чтения XML считывает один [узел XML](xml-node.md) за раз, но существуют дополнительные вспомогательные API для упрощения чтения последовательности узлов.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-109">At its core, an XML Reader reads one [XML Node](xml-node.md) at a time, but there are additional helper APIs to make reading a sequence of nodes easier.</span></span>


<span data-ttu-id="a3cd4-110">Поддерживаются следующие типы входных данных для читателей:</span><span class="sxs-lookup"><span data-stu-id="a3cd4-110">The following types of readers input are supported:</span></span>

-   [<span data-ttu-id="a3cd4-111">**Буфер в памяти закодированных байтов**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-111">**An in-memory buffer of encoded bytes**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [<span data-ttu-id="a3cd4-112">**Поток**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-112">**A stream**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   <span data-ttu-id="a3cd4-113">[XML-буфер](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="a3cd4-113">An [XML Buffer](xml-buffer.md)</span></span>

### <a name="security"></a><span data-ttu-id="a3cd4-114">Безопасность</span><span class="sxs-lookup"><span data-stu-id="a3cd4-114">Security</span></span>

<span data-ttu-id="a3cd4-115">Средство чтения проверит, являются ли атрибуты элемента уникальными.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-115">The reader will verify that the attributes present on an element are unique.</span></span> <span data-ttu-id="a3cd4-116">Время, необходимое для выполнения этой проверки, — это функция числа атрибутов в элементе, которая может быть максимально допустимой для [**\_ \_ свойств модуля чтения XML \_ \_ \_ -данных WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span><span class="sxs-lookup"><span data-stu-id="a3cd4-116">The time required to perform this validation is a function of the number of attributes on the element which can be as large as [**WS\_XML\_READER\_PROPERTY\_MAX\_ATTRIBUTES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span></span> <span data-ttu-id="a3cd4-117">Таким образом, обработка больших документов в случае, если для **\_ \_ \_ свойства \_ Max \_ XML Reader** задано большое значение, может возникать возможность атаки типа "отказ в обслуживании".</span><span class="sxs-lookup"><span data-stu-id="a3cd4-117">Therefore, processing large documents when **WS\_XML\_READER\_PROPERTY\_MAX\_ATTRIBUTES** is set to a large value may present an opportunity for a denial of service attack.</span></span>

<span data-ttu-id="a3cd4-118">Модуль чтения будет сопоставлять префиксы к пространствам имен для каждого элемента и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-118">The reader will map prefixes to namespaces for each element and attributes.</span></span> <span data-ttu-id="a3cd4-119">Время, необходимое для выполнения этого сопоставления, — это функция количества атрибутов xmlns в области, которая может иметь размер [**\_ \_ \_ \_ \_ пространства имен WS XML Reader Max**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span><span class="sxs-lookup"><span data-stu-id="a3cd4-119">The time required to perform this mapping is a function of the number of xmlns attributes in scope which may be as large as [**WS\_XML\_READER\_PROPERTY\_MAX\_NAMESPACES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span></span> <span data-ttu-id="a3cd4-120">Поэтому обработка больших документов, если это свойство имеет большое значение, может представлять собой возможность атаки типа "отказ в обслуживании".</span><span class="sxs-lookup"><span data-stu-id="a3cd4-120">Therefore, processing large documents when this property is set to a large value may present an opportunity for a denial of service attack.</span></span>

<span data-ttu-id="a3cd4-121">Хотя читатель гарантирует, что документ будет следовать грамматической спецификации XML и более того, что его аспекты находятся в заданных квотах, содержимое документа все равно должно считаться ненадежным при поступлении из ненадежного источника.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-121">While the reader will ensure that the document follows the grammatical specification of xml and furthermore that its aspects are within the quotas specified, the content of the document must still be considered untrusted when coming from an untrusted source.</span></span> <span data-ttu-id="a3cd4-122">Пользователи модуля чтения должны проверять все имена элементов и атрибутов и пространства имен с помощью [**всреадтостартелемент**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**всфиндаттрибуте**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)или вручную проверять [**узлы**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).</span><span class="sxs-lookup"><span data-stu-id="a3cd4-122">Users of the reader should check all element and attribute names and namespaces using [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute), or by manually inspecting [**nodes**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).</span></span>

<span data-ttu-id="a3cd4-123">Некоторые другие ситуации, которые следует учитывать, включают, но не ограничиваются:</span><span class="sxs-lookup"><span data-stu-id="a3cd4-123">Some other situations to consider include, but are not limited to:</span></span>

-   <span data-ttu-id="a3cd4-124">Возможно, отсутствуют ожидаемые элементы</span><span class="sxs-lookup"><span data-stu-id="a3cd4-124">Expected elements may be missing</span></span>
-   <span data-ttu-id="a3cd4-125">Могут отображаться непредвиденные элементы</span><span class="sxs-lookup"><span data-stu-id="a3cd4-125">Unexpected elements may appear</span></span>
-   <span data-ttu-id="a3cd4-126">Возможно, отсутствуют ожидаемые атрибуты</span><span class="sxs-lookup"><span data-stu-id="a3cd4-126">Expected attributes may be missing</span></span>
-   <span data-ttu-id="a3cd4-127">Могут отображаться непредвиденные атрибуты</span><span class="sxs-lookup"><span data-stu-id="a3cd4-127">Unexpected attributes may appear</span></span>
-   <span data-ttu-id="a3cd4-128">Элементы могут отображаться как пустые элементы</span><span class="sxs-lookup"><span data-stu-id="a3cd4-128">Elements may appear as empty elements</span></span>
-   <span data-ttu-id="a3cd4-129">Пробелы могут появляться в непредвиденных местах</span><span class="sxs-lookup"><span data-stu-id="a3cd4-129">Whitespace may appear in unexpected places</span></span>

<span data-ttu-id="a3cd4-130">Пользователи модуля чтения не должны распределять память на основе значений, считанных из документа.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-130">Users of the reader should not allocate memory based simply on values read from the document.</span></span> <span data-ttu-id="a3cd4-131">Например, рассмотрим следующий XML-документ:</span><span class="sxs-lookup"><span data-stu-id="a3cd4-131">For example, consider the following xml document:</span></span>

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

<span data-ttu-id="a3cd4-132">Выделение массива на основе предположения, что некоторое количество элементов будет соответствовать потенциальному вектору атаки.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-132">Allocating an array based soley on the assumption that some number of elements will follow would be a potential attack vector.</span></span> <span data-ttu-id="a3cd4-133">Пользователь модуля чтения в этом случае должен последовательно распределять память по мере отображения элементов.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-133">The user of the reader in this case should instead incrementally allocate the memory as the elements appear.</span></span>

<span data-ttu-id="a3cd4-134">Модуль чтения XML не поддерживает DTD.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-134">XML reader does not support DTD.</span></span> <span data-ttu-id="a3cd4-135">Пользователю средства чтения не нужно беспокоиться о проверке DTD.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-135">The user of the reader does not need to concern about DTD verification.</span></span>

<span data-ttu-id="a3cd4-136">Для средств чтения XML используется следующий обратный вызов:</span><span class="sxs-lookup"><span data-stu-id="a3cd4-136">The following callback is used with XML readers:</span></span>

-   [<span data-ttu-id="a3cd4-137">**\_ \_ обратный вызов WS Read**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-137">**WS\_READ\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

<span data-ttu-id="a3cd4-138">С модулями чтения XML используются следующие перечисления:</span><span class="sxs-lookup"><span data-stu-id="a3cd4-138">The following enumerations are used with XML readers:</span></span>

-   [<span data-ttu-id="a3cd4-139">**\_ \_ \_ тип кодировки модуля чтения XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-139">**WS\_XML\_READER\_ENCODING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [<span data-ttu-id="a3cd4-140">**\_ \_ \_ тип входных данных модуля чтения XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-140">**WS\_XML\_READER\_INPUT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [<span data-ttu-id="a3cd4-141">**\_ \_ идентификатор свойства модуля чтения XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-141">**WS\_XML\_READER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

<span data-ttu-id="a3cd4-142">Для модулей чтения XML используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-142">The following functions are used with XML readers:</span></span>

-   [<span data-ttu-id="a3cd4-143">**вскреатереадер**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-143">**WsCreateReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatereader)
-   [<span data-ttu-id="a3cd4-144">**всфиллреадер**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-144">**WsFillReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfillreader)
-   [<span data-ttu-id="a3cd4-145">**всфиндаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-145">**WsFindAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)
-   [<span data-ttu-id="a3cd4-146">**всфриреадер**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-146">**WsFreeReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreereader)
-   [<span data-ttu-id="a3cd4-147">**всжетнамеспацефромпрефикс**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-147">**WsGetNamespaceFromPrefix**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetnamespacefromprefix)
-   [<span data-ttu-id="a3cd4-148">**всжетреадерноде**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-148">**WsGetReaderNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreadernode)
-   [<span data-ttu-id="a3cd4-149">**всжетреадерпоситион**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-149">**WsGetReaderPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition)
-   [<span data-ttu-id="a3cd4-150">**всжетреадерпроперти**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-150">**WsGetReaderProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderproperty)
-   [<span data-ttu-id="a3cd4-151">**всжетксмлаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-151">**WsGetXmlAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute)
-   [<span data-ttu-id="a3cd4-152">**всмовереадер**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-152">**WsMoveReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmovereader)
-   [<span data-ttu-id="a3cd4-153">**всреадаррай**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-153">**WsReadArray**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadarray)
-   [<span data-ttu-id="a3cd4-154">**всреадбитес**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-154">**WsReadBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadbytes)
-   [<span data-ttu-id="a3cd4-155">**всреадчарс**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-155">**WsReadChars**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadchars)
-   [<span data-ttu-id="a3cd4-156">**WsReadCharsUtf8**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-156">**WsReadCharsUtf8**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadcharsutf8)
-   [<span data-ttu-id="a3cd4-157">**всреадендаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-157">**WsReadEndAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadendattribute)
-   [<span data-ttu-id="a3cd4-158">**всреаденделемент**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-158">**WsReadEndElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)
-   [<span data-ttu-id="a3cd4-159">**всреадноде**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-159">**WsReadNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadnode)
-   [<span data-ttu-id="a3cd4-160">**всреадкуалифиеднаме**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-160">**WsReadQualifiedName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadqualifiedname)
-   [<span data-ttu-id="a3cd4-161">**всреадстартаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-161">**WsReadStartAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadstartattribute)
-   [<span data-ttu-id="a3cd4-162">**всреадстартелемент**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-162">**WsReadStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)
-   [<span data-ttu-id="a3cd4-163">**всреадтостартелемент**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-163">**WsReadToStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)
-   [<span data-ttu-id="a3cd4-164">**всреадвалуе**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-164">**WsReadValue**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue)
-   [<span data-ttu-id="a3cd4-165">**вссетинпут**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-165">**WsSetInput**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetinput)
-   [<span data-ttu-id="a3cd4-166">**вссетинпуттобуффер**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-166">**WsSetInputToBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer)
-   [<span data-ttu-id="a3cd4-167">**вссетреадерпоситион**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-167">**WsSetReaderPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition)
-   [<span data-ttu-id="a3cd4-168">**всскипноде**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-168">**WsSkipNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsskipnode)

<span data-ttu-id="a3cd4-169">Для модулей чтения XML используется следующий маркер:</span><span class="sxs-lookup"><span data-stu-id="a3cd4-169">The following handle is used with XML readers:</span></span>

-   [<span data-ttu-id="a3cd4-170">\_ \_ модуль чтения XML WS</span><span class="sxs-lookup"><span data-stu-id="a3cd4-170">WS\_XML\_READER</span></span>](ws-xml-reader.md)

<span data-ttu-id="a3cd4-171">Для средств чтения XML используются следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="a3cd4-171">The following structures are used with XML readers:</span></span>

-   [<span data-ttu-id="a3cd4-172">**\_ \_ \_ двоичное кодирование модуля чтения XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-172">**WS\_XML\_READER\_BINARY\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [<span data-ttu-id="a3cd4-173">**\_ \_ входной буфер модуля чтения XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-173">**WS\_XML\_READER\_BUFFER\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [<span data-ttu-id="a3cd4-174">**\_ \_ кодирование модуля чтения XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-174">**WS\_XML\_READER\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [<span data-ttu-id="a3cd4-175">**\_ \_ входные данные модуля чтения XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-175">**WS\_XML\_READER\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [<span data-ttu-id="a3cd4-176">**\_ \_ Кодирование MTOM в модуле чтения XML для модуля WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-176">**WS\_XML\_READER\_MTOM\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [<span data-ttu-id="a3cd4-177">**\_ \_ Свойства модуля чтения XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-177">**WS\_XML\_READER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [<span data-ttu-id="a3cd4-178">**\_ \_ свойство модуля чтения XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-178">**WS\_XML\_READER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [<span data-ttu-id="a3cd4-179">**\_ \_ \_ входные данные потока модуля чтения XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-179">**WS\_XML\_READER\_STREAM\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [<span data-ttu-id="a3cd4-180">**\_ \_ Кодировка текста для модуля чтения XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-180">**WS\_XML\_READER\_TEXT\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 




