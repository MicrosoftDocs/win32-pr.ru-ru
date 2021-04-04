---
title: XML-буфер
description: XML-буфер предоставляет эффективное хранилище в памяти для произвольных XML-данных.
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- Веб-службы буфера XML для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab71121dc451c9ccb186c754d537836f9e899fa9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103988002"
---
# <a name="xml-buffer"></a><span data-ttu-id="b9a19-106">XML-буфер</span><span class="sxs-lookup"><span data-stu-id="b9a19-106">XML Buffer</span></span>

<span data-ttu-id="b9a19-107">XML-буфер предоставляет эффективное хранилище в памяти для произвольных XML-данных.</span><span class="sxs-lookup"><span data-stu-id="b9a19-107">An XML Buffer provides efficient in-memory storage for arbitrary XML data.</span></span>


<span data-ttu-id="b9a19-108">Для чтения данных из буфера XML используйте [средство чтения XML](xml-reader.md) и вызовите [**вссетинпуттобуффер**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) с помощью XML-буфера.</span><span class="sxs-lookup"><span data-stu-id="b9a19-108">To read data from an XML Buffer, use a [XML Reader](xml-reader.md) and call [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) with the XML Buffer.</span></span> <span data-ttu-id="b9a19-109">Модуль чтения будет расположен в начале документа.</span><span class="sxs-lookup"><span data-stu-id="b9a19-109">The reader will be positioned at the start of the document.</span></span>

<span data-ttu-id="b9a19-110">Чтобы вставить данные в буфер, используйте [модуль записи XML](xml-writer.md) и вызовите [**вссетаутпуттобуффер**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) с помощью XML-буфера.</span><span class="sxs-lookup"><span data-stu-id="b9a19-110">To insert data into a buffer, use a [XML Writer](xml-writer.md) and call [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) with the XML Buffer.</span></span> <span data-ttu-id="b9a19-111">Модуль записи будет расположен в конце документа.</span><span class="sxs-lookup"><span data-stu-id="b9a19-111">The writer will be positioned at the end of the document.</span></span>

<span data-ttu-id="b9a19-112">После того как для модуля чтения задается XML-буфер, помимо всех API-интерфейсов средства чтения XML, [**всмовереадер**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) может использоваться для навигации по документу.</span><span class="sxs-lookup"><span data-stu-id="b9a19-112">Once a reader has been set to an XML Buffer, in addition to all of the XML Reader APIs, [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) may be used to navigate the reader through the document.</span></span> <span data-ttu-id="b9a19-113">[**Всжетреадерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) и [**вссетреадерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) также могут использоваться для записи позиций в документ и возврата к нему позже.</span><span class="sxs-lookup"><span data-stu-id="b9a19-113">[**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) and [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) may also be used to record a position in the document and return to it later.</span></span>

<span data-ttu-id="b9a19-114">После установки модуля записи в буфер XML, помимо всех API-интерфейсов модуля записи XML, [**всмовевритер**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) может использоваться для перемещения по модулю записи через документ.</span><span class="sxs-lookup"><span data-stu-id="b9a19-114">Once a writer has been set to an XML Buffer, in addition to all of the XML Writer APIs, [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) may be used to navigate the writer through the document.</span></span> <span data-ttu-id="b9a19-115">[**Всжетвритерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) и [**вссетвритерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) также могут использоваться для записи позиций в документ и возврата к нему позже.</span><span class="sxs-lookup"><span data-stu-id="b9a19-115">[**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) and [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) may also be used to record a position in the document and return to it later.</span></span> <span data-ttu-id="b9a19-116">Модуль записи всегда вставляет данные перед узлом, на котором он расположен.</span><span class="sxs-lookup"><span data-stu-id="b9a19-116">The writer always inserts data before the node to which it is positioned.</span></span>

<span data-ttu-id="b9a19-117">Узлы могут быть удалены из буфера XML путем получения расположения узла с помощью [**всжетреадерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) или [**всжетвритерпоситион**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) и последующего вызова [**всремовеноде**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) с этой позицией.</span><span class="sxs-lookup"><span data-stu-id="b9a19-117">Nodes may be deleted from the XML Buffer by obtaining the position of the node using [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) or [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) and then calling [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) with that position.</span></span> <span data-ttu-id="b9a19-118">Для элементов это приведет к удалению элемента, всех его дочерних элементов, включая соответствующий элемент End.</span><span class="sxs-lookup"><span data-stu-id="b9a19-118">For elements, this will delete the element, all its children including its matching end element.</span></span>

<span data-ttu-id="b9a19-119">Значение координаты представляется [**\_ \_ \_ позицией узла WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position).</span><span class="sxs-lookup"><span data-stu-id="b9a19-119">A position is represented by the value [**WS\_XML\_NODE\_POSITION**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position).</span></span> <span data-ttu-id="b9a19-120">Позиции относятся к конкретному XML-буферу и допустимы только при условии, что XML-буфер является допустимым.</span><span class="sxs-lookup"><span data-stu-id="b9a19-120">Positions are specific to a particular XML Buffer, and are only valid as long as the XML Buffer is valid.</span></span>

<span data-ttu-id="b9a19-121">С XML-буферами используются следующие перечисления:</span><span class="sxs-lookup"><span data-stu-id="b9a19-121">The following enumerations are used with XML buffers:</span></span>

-   [<span data-ttu-id="b9a19-122">**\_Переместить \_ в**</span><span class="sxs-lookup"><span data-stu-id="b9a19-122">**WS\_MOVE\_TO**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [<span data-ttu-id="b9a19-123">**\_ \_ \_ идентификатор свойства XML-буфера WS \_**</span><span class="sxs-lookup"><span data-stu-id="b9a19-123">**WS\_XML\_BUFFER\_PROPERTY\_ID**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

<span data-ttu-id="b9a19-124">Для XML-буферов используются следующие функции:</span><span class="sxs-lookup"><span data-stu-id="b9a19-124">The following functions are used with XML buffers:</span></span>

-   [<span data-ttu-id="b9a19-125">**вскреатексмлбуффер**</span><span class="sxs-lookup"><span data-stu-id="b9a19-125">**WsCreateXmlBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [<span data-ttu-id="b9a19-126">**всремовеноде**</span><span class="sxs-lookup"><span data-stu-id="b9a19-126">**WsRemoveNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

<span data-ttu-id="b9a19-127">Для XML-буферов используется следующий маркер:</span><span class="sxs-lookup"><span data-stu-id="b9a19-127">The following handle is used with XML buffers:</span></span>

-   [<span data-ttu-id="b9a19-128">\_XML- \_ буфер WS</span><span class="sxs-lookup"><span data-stu-id="b9a19-128">WS\_XML\_BUFFER</span></span>](ws-xml-buffer.md)

<span data-ttu-id="b9a19-129">Для XML-буферов используются следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="b9a19-129">The following structures are used with XML buffers:</span></span>

-   [<span data-ttu-id="b9a19-130">**\_свойство "XML- \_ буфер WS" \_**</span><span class="sxs-lookup"><span data-stu-id="b9a19-130">**WS\_XML\_BUFFER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [<span data-ttu-id="b9a19-131">**\_ \_ расположение узла WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="b9a19-131">**WS\_XML\_NODE\_POSITION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




