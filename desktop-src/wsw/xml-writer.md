---
title: Модуль записи XML
description: Модуль записи XML — это API для выпуска XML. По сути, модуль записи XML записывает один узел XML за раз, но существуют дополнительные вспомогательные API для упрощения создания последовательности узлов.
ms.assetid: 69d50793-1d5b-4fc7-bf69-128f8e23a98d
keywords:
- Веб-службы модуля записи XML для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085a02b3aca33ffa3b31e4579d47068a683ee4d8
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "105710401"
---
# <a name="xml-writer"></a><span data-ttu-id="bf80f-107">Модуль записи XML</span><span class="sxs-lookup"><span data-stu-id="bf80f-107">XML Writer</span></span>

<span data-ttu-id="bf80f-108">Модуль записи XML — это API для выпуска XML.</span><span class="sxs-lookup"><span data-stu-id="bf80f-108">XML Writer is an API for emitting XML.</span></span> <span data-ttu-id="bf80f-109">По сути, модуль записи XML записывает один [узел XML](xml-node.md) за раз, но существуют дополнительные вспомогательные API для упрощения создания последовательности узлов.</span><span class="sxs-lookup"><span data-stu-id="bf80f-109">At its core, an XML Writer writes one [XML Node](xml-node.md) at a time, but there are additional helper APIs to make writing a sequence of nodes easier.</span></span>


<span data-ttu-id="bf80f-110">Поддерживаются следующие типы выходных данных модуля записи:</span><span class="sxs-lookup"><span data-stu-id="bf80f-110">The following types of writer output are supported:</span></span>

-   [<span data-ttu-id="bf80f-111">**Буфер в памяти закодированных байтов**</span><span class="sxs-lookup"><span data-stu-id="bf80f-111">**An in-memory buffer of encoded bytes**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [<span data-ttu-id="bf80f-112">**Поток**</span><span class="sxs-lookup"><span data-stu-id="bf80f-112">**A stream**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   <span data-ttu-id="bf80f-113">[XML-буфер](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="bf80f-113">An [XML Buffer](xml-buffer.md)</span></span>

<span data-ttu-id="bf80f-114">С модулем записи XML используются следующие обратные вызовы:</span><span class="sxs-lookup"><span data-stu-id="bf80f-114">The following callbacks are used with the XML writer:</span></span>

-   [<span data-ttu-id="bf80f-115">**\_ \_ обратный вызов динамической строки WS \_**</span><span class="sxs-lookup"><span data-stu-id="bf80f-115">**WS\_DYNAMIC\_STRING\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [<span data-ttu-id="bf80f-116">**\_ \_ обратный вызов по запросу WS \_**</span><span class="sxs-lookup"><span data-stu-id="bf80f-116">**WS\_PULL\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [<span data-ttu-id="bf80f-117">**\_ \_ обратный вызов push-уведомлений WS \_**</span><span class="sxs-lookup"><span data-stu-id="bf80f-117">**WS\_PUSH\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [<span data-ttu-id="bf80f-118">**\_ \_ обратный вызов записи WS**</span><span class="sxs-lookup"><span data-stu-id="bf80f-118">**WS\_WRITE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

<span data-ttu-id="bf80f-119">С модулем записи XML используются следующие перечисления:</span><span class="sxs-lookup"><span data-stu-id="bf80f-119">The following enumerations are used with the XML writer:</span></span>

-   [<span data-ttu-id="bf80f-120">**набор \_ символов WS**</span><span class="sxs-lookup"><span data-stu-id="bf80f-120">**WS\_CHARSET**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [<span data-ttu-id="bf80f-121">**\_ \_ тип кодирования модуля записи XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="bf80f-121">**WS\_XML\_WRITER\_ENCODING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [<span data-ttu-id="bf80f-122">**\_ \_ \_ тип выходных данных модуля записи XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="bf80f-122">**WS\_XML\_WRITER\_OUTPUT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [<span data-ttu-id="bf80f-123">**\_ \_ идентификатор свойства модуля записи XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="bf80f-123">**WS\_XML\_WRITER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

<span data-ttu-id="bf80f-124">С модулем записи XML используются следующие функции:</span><span class="sxs-lookup"><span data-stu-id="bf80f-124">The following functions are used with the XML writer:</span></span>

-   [<span data-ttu-id="bf80f-125">**вскопиноде**</span><span class="sxs-lookup"><span data-stu-id="bf80f-125">**WsCopyNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscopynode)
-   [<span data-ttu-id="bf80f-126">**вскреатевритер**</span><span class="sxs-lookup"><span data-stu-id="bf80f-126">**WsCreateWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatewriter)
-   [<span data-ttu-id="bf80f-127">**всфлушвритер**</span><span class="sxs-lookup"><span data-stu-id="bf80f-127">**WsFlushWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter)
-   [<span data-ttu-id="bf80f-128">**всфривритер**</span><span class="sxs-lookup"><span data-stu-id="bf80f-128">**WsFreeWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreewriter)
-   [<span data-ttu-id="bf80f-129">**всжетпрефиксфромнамеспаце**</span><span class="sxs-lookup"><span data-stu-id="bf80f-129">**WsGetPrefixFromNamespace**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetprefixfromnamespace)
-   [<span data-ttu-id="bf80f-130">**всжетвритерпоситион**</span><span class="sxs-lookup"><span data-stu-id="bf80f-130">**WsGetWriterPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition)
-   [<span data-ttu-id="bf80f-131">**всжетвритерпроперти**</span><span class="sxs-lookup"><span data-stu-id="bf80f-131">**WsGetWriterProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterproperty)
-   [<span data-ttu-id="bf80f-132">**всмовевритер**</span><span class="sxs-lookup"><span data-stu-id="bf80f-132">**WsMoveWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter)
-   [<span data-ttu-id="bf80f-133">**вспуллбитес**</span><span class="sxs-lookup"><span data-stu-id="bf80f-133">**WsPullBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wspullbytes)
-   [<span data-ttu-id="bf80f-134">**вспушбитес**</span><span class="sxs-lookup"><span data-stu-id="bf80f-134">**WsPushBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wspushbytes)
-   [<span data-ttu-id="bf80f-135">**вссетаутпут**</span><span class="sxs-lookup"><span data-stu-id="bf80f-135">**WsSetOutput**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetoutput)
-   [<span data-ttu-id="bf80f-136">**вссетаутпуттобуффер**</span><span class="sxs-lookup"><span data-stu-id="bf80f-136">**WsSetOutputToBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer)
-   [<span data-ttu-id="bf80f-137">**вссетвритерпоситион**</span><span class="sxs-lookup"><span data-stu-id="bf80f-137">**WsSetWriterPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition)
-   [<span data-ttu-id="bf80f-138">**всвритеаррай**</span><span class="sxs-lookup"><span data-stu-id="bf80f-138">**WsWriteArray**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritearray)
-   [<span data-ttu-id="bf80f-139">**всвритебитес**</span><span class="sxs-lookup"><span data-stu-id="bf80f-139">**WsWriteBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritebytes)
-   [<span data-ttu-id="bf80f-140">**всвритечарс**</span><span class="sxs-lookup"><span data-stu-id="bf80f-140">**WsWriteChars**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritechars)
-   [<span data-ttu-id="bf80f-141">**WsWriteCharsUtf8**</span><span class="sxs-lookup"><span data-stu-id="bf80f-141">**WsWriteCharsUtf8**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritecharsutf8)
-   [<span data-ttu-id="bf80f-142">**всвритиндаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="bf80f-142">**WsWriteEndAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendattribute)
-   [<span data-ttu-id="bf80f-143">**всвритиндкдата**</span><span class="sxs-lookup"><span data-stu-id="bf80f-143">**WsWriteEndCData**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendcdata)
-   [<span data-ttu-id="bf80f-144">**всвритинделемент**</span><span class="sxs-lookup"><span data-stu-id="bf80f-144">**WsWriteEndElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendelement)
-   [<span data-ttu-id="bf80f-145">**всвритеноде**</span><span class="sxs-lookup"><span data-stu-id="bf80f-145">**WsWriteNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritenode)
-   [<span data-ttu-id="bf80f-146">**всвритекуалифиеднаме**</span><span class="sxs-lookup"><span data-stu-id="bf80f-146">**WsWriteQualifiedName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritequalifiedname)
-   [<span data-ttu-id="bf80f-147">**всвритестартаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="bf80f-147">**WsWriteStartAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute)
-   [<span data-ttu-id="bf80f-148">**всвритестарткдата**</span><span class="sxs-lookup"><span data-stu-id="bf80f-148">**WsWriteStartCData**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartcdata)
-   [<span data-ttu-id="bf80f-149">**всвритестартелемент**</span><span class="sxs-lookup"><span data-stu-id="bf80f-149">**WsWriteStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartelement)
-   [<span data-ttu-id="bf80f-150">**всвритетекст**</span><span class="sxs-lookup"><span data-stu-id="bf80f-150">**WsWriteText**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritetext)
-   [<span data-ttu-id="bf80f-151">**всвритевалуе**</span><span class="sxs-lookup"><span data-stu-id="bf80f-151">**WsWriteValue**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritevalue)
-   [<span data-ttu-id="bf80f-152">**всвритексмлнсаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="bf80f-152">**WsWriteXmlnsAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritexmlnsattribute)

<span data-ttu-id="bf80f-153">С модулем записи XML используется следующий маркер:</span><span class="sxs-lookup"><span data-stu-id="bf80f-153">The following handle is used with the XML writer:</span></span>

-   [<span data-ttu-id="bf80f-154">\_ \_ модуль записи XML WS</span><span class="sxs-lookup"><span data-stu-id="bf80f-154">WS\_XML\_WRITER</span></span>](ws-xml-writer.md)

<span data-ttu-id="bf80f-155">С модулем записи XML используются следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="bf80f-155">The following structures are used with the XML writer:</span></span>

-   [<span data-ttu-id="bf80f-156">**\_ \_ \_ двоичное кодирование модуля записи XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="bf80f-156">**WS\_XML\_WRITER\_BINARY\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [<span data-ttu-id="bf80f-157">**\_ \_ \_ выходные данные буфера модуля записи XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="bf80f-157">**WS\_XML\_WRITER\_BUFFER\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [<span data-ttu-id="bf80f-158">**\_ \_ кодирование модуля записи XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="bf80f-158">**WS\_XML\_WRITER\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [<span data-ttu-id="bf80f-159">**\_ \_ Кодирование MTOM модуля записи XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="bf80f-159">**WS\_XML\_WRITER\_MTOM\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [<span data-ttu-id="bf80f-160">**\_ \_ выходные данные модуля записи XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="bf80f-160">**WS\_XML\_WRITER\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [<span data-ttu-id="bf80f-161">**\_ \_ Свойства модуля записи XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="bf80f-161">**WS\_XML\_WRITER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [<span data-ttu-id="bf80f-162">**\_ \_ свойство модуля записи XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="bf80f-162">**WS\_XML\_WRITER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [<span data-ttu-id="bf80f-163">**\_ \_ \_ выходные данные потока модуля записи XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="bf80f-163">**WS\_XML\_WRITER\_STREAM\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [<span data-ttu-id="bf80f-164">**\_ \_ Кодировка текста для модуля записи XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="bf80f-164">**WS\_XML\_WRITER\_TEXT\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 




