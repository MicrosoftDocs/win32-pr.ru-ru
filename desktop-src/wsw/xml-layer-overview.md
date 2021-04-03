---
title: Обзор уровня XML
description: API XML в ВВСАПИ основан на модуле чтения XML и объектах модуля записи XML, которые позволяют выполнять чтение или запись XML-документов только в прямом направлении. XML-слой предоставляет приложению полный доступ к содержимому сообщений и управление им.
ms.assetid: 938ca257-fbb8-4569-b791-2148abb1a5a5
keywords:
- Обзор уровня XML веб-служб для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9b5d062754adea7b48bd42a6a501ce17d0e332b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776244"
---
# <a name="xml-layer-overview"></a><span data-ttu-id="132e5-107">Обзор уровня XML</span><span class="sxs-lookup"><span data-stu-id="132e5-107">XML Layer Overview</span></span>

<span data-ttu-id="132e5-108">API XML в ВВСАПИ основан на [модуле чтения XML](xml-reader.md) и объектах [модуля записи XML](xml-writer.md) , которые позволяют выполнять чтение или запись XML-документов только в прямом направлении.</span><span class="sxs-lookup"><span data-stu-id="132e5-108">The XML API in WWSAPI is based on the [XML Reader](xml-reader.md) and [XML Writer](xml-writer.md) objects, which allow reading or writing of XML documents in a forward only fashion.</span></span> <span data-ttu-id="132e5-109">XML-слой предоставляет приложению полный доступ к содержимому сообщений и управление им.</span><span class="sxs-lookup"><span data-stu-id="132e5-109">The XML Layer give the application full access to and control over the content of messages.</span></span>

## <a name="encoding"></a><span data-ttu-id="132e5-110">Кодирование</span><span class="sxs-lookup"><span data-stu-id="132e5-110">Encoding</span></span>

<span data-ttu-id="132e5-111">API XML поддерживает документы, закодированные как:</span><span class="sxs-lookup"><span data-stu-id="132e5-111">The XML API supports documents encoded as:</span></span>

-   <span data-ttu-id="132e5-112">Text (UTF-8, UTF-16LE, UTF-16BE)</span><span class="sxs-lookup"><span data-stu-id="132e5-112">Text (UTF-8, UTF-16LE, UTF-16BE)</span></span>
-   <span data-ttu-id="132e5-113">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="132e5-113">Binary</span></span>
-   <span data-ttu-id="132e5-114">MTOM</span><span class="sxs-lookup"><span data-stu-id="132e5-114">MTOM</span></span>

## <a name="storage"></a><span data-ttu-id="132e5-115">Память</span><span class="sxs-lookup"><span data-stu-id="132e5-115">Storage</span></span>

<span data-ttu-id="132e5-116">API XML поддерживает обработку документов, хранящихся как:</span><span class="sxs-lookup"><span data-stu-id="132e5-116">The XML API supports processing documents stored as:</span></span>

-   <span data-ttu-id="132e5-117">Буфер в памяти закодированных байтов</span><span class="sxs-lookup"><span data-stu-id="132e5-117">An in-memory buffer of encoded bytes</span></span>
-   <span data-ttu-id="132e5-118">Поток</span><span class="sxs-lookup"><span data-stu-id="132e5-118">A stream</span></span>
-   <span data-ttu-id="132e5-119">[XML-буфер](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="132e5-119">An [XML Buffer](xml-buffer.md)</span></span>

<span data-ttu-id="132e5-120">[XML-буфер](xml-buffer.md) — это структурированное представление XML-документа в памяти.</span><span class="sxs-lookup"><span data-stu-id="132e5-120">An [XML Buffer](xml-buffer.md) is a structured in-memory representation of an XML document.</span></span> <span data-ttu-id="132e5-121">Это более эффективное представление, чем документ, закодированный как байты.</span><span class="sxs-lookup"><span data-stu-id="132e5-121">This is a more efficient representation than a document encoded as bytes.</span></span> <span data-ttu-id="132e5-122">Документ XML, хранящийся в XML-буфере, может быть перемещен, прочитан или записан.</span><span class="sxs-lookup"><span data-stu-id="132e5-122">An XML document stored in an An XML Buffer can be navigated, read, or written.</span></span>

## <a name="io"></a><span data-ttu-id="132e5-123">Ввод-вывод</span><span class="sxs-lookup"><span data-stu-id="132e5-123">I/O</span></span>

<span data-ttu-id="132e5-124">API XML никогда не будет выполнять операции ввода-вывода, если только они не запрошены специально.</span><span class="sxs-lookup"><span data-stu-id="132e5-124">The XML API will never perform I/O unless specifically requested.</span></span> <span data-ttu-id="132e5-125">Кроме того, любые операции ввода-вывода могут инициироваться асинхронно.</span><span class="sxs-lookup"><span data-stu-id="132e5-125">Furthermore, any I/O may be initiated in an asynchronous fashion.</span></span> <span data-ttu-id="132e5-126">Дополнительные сведения об асинхронной обработке с помощью XML API см. в разделе [**всфиллреадер**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader) и [**всфлушвритер**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter) .</span><span class="sxs-lookup"><span data-stu-id="132e5-126">See [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader) and [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter) for details on asynchronous processing with the XML API.</span></span>

## <a name="processing"></a><span data-ttu-id="132e5-127">Обработка</span><span class="sxs-lookup"><span data-stu-id="132e5-127">Processing</span></span>

<span data-ttu-id="132e5-128">XML API имеет три разных уровня, на которых документ может быть обработан.</span><span class="sxs-lookup"><span data-stu-id="132e5-128">The XML API has three distinct levels at which the document may be processed.</span></span>

<span data-ttu-id="132e5-129">Документ может обрабатываться [**узлом**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node) за раз.</span><span class="sxs-lookup"><span data-stu-id="132e5-129">A document may be processed a [**node**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node) at a time.</span></span> <span data-ttu-id="132e5-130">Это обеспечивает наиболее детализированную обработку XML-содержимого и обеспечивает полную достоверность данных из документа.</span><span class="sxs-lookup"><span data-stu-id="132e5-130">This offers the most fine-grained handling of the XML content, and provides complete fidelity of data from the document.</span></span> <span data-ttu-id="132e5-131">На этом уровне будут использоваться функции [**всреадноде**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode) и [**всвритеноде**](/windows/desktop/api/WebServices/nf-webservices-wswritenode) и [**вскопиноде**](/windows/desktop/api/WebServices/nf-webservices-wscopynode) .</span><span class="sxs-lookup"><span data-stu-id="132e5-131">At this level, the functions [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode) and [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode) and [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode) would be used.</span></span>

<span data-ttu-id="132e5-132">Следующий уровень управления — это интерфейсы API, такие как [**всреадстартелемент**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement), [**всреадвалуе**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue) и [**всреаденделемент**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement).</span><span class="sxs-lookup"><span data-stu-id="132e5-132">The next level of control are APIs like [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement), [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue) and [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement).</span></span> <span data-ttu-id="132e5-133">Эти API предоставляют множество видов проверки, пропускают пробелы и комментарии, нормализацию текста и CDATA, чтобы предоставить потребителю более простое представление XML.</span><span class="sxs-lookup"><span data-stu-id="132e5-133">These APIs provide numerous kinds of validation, skip whitespace and comments, and normalize text and CDATA to present the consumer with a simpler view of the xml.</span></span>

<span data-ttu-id="132e5-134">Самым высоким уровнем управления является использование API сериализации.</span><span class="sxs-lookup"><span data-stu-id="132e5-134">The highest level of control is to use the Serialization API.</span></span> <span data-ttu-id="132e5-135">Эти API-интерфейсы основываются на сопоставлении между типами данных C и XML, а также могут считывать или записывать сложную структуру в памяти в XML и обратно с помощью одной функции, такой как [**всвритилемент**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement) и [**всреаделемент**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement).</span><span class="sxs-lookup"><span data-stu-id="132e5-135">These APIs are driven off a mapping between C data types and XML, and can read or write a complex in-memory structure to xml and back with a single function like [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement) and [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement).</span></span>

<span data-ttu-id="132e5-136">API-интерфейсы канонизации XML могут использоваться для создания канонической формы XML, которая, в свою очередь, может использоваться для создания криптографических подписей по содержимому XML.</span><span class="sxs-lookup"><span data-stu-id="132e5-136">The XML Canonicalization APIs may be used to generate a canonical form of XML which may in turn be used for generating cryptographic signatures over XML content.</span></span>

## <a name="creating-a-writer"></a><span data-ttu-id="132e5-137">Создание модуля записи</span><span class="sxs-lookup"><span data-stu-id="132e5-137">Creating a writer</span></span>

<span data-ttu-id="132e5-138">Создание и использование модуля записи для записи в буфер в памяти:</span><span class="sxs-lookup"><span data-stu-id="132e5-138">To create and use a writer to write to an in-memory buffer:</span></span>

``` syntax
WsCreateWriter              // Create an instance of a WS_XML_WRITER
// Initialize a WS_XML_WRITER_BUFFER_OUTPUT
WsSetOutput                 // Set the encoding and output of the writer along with any other writer properties
// Write Elements
WsGetWriterProperty(..., WS_XML_WRITER_PROPERTY_BYTES, ...)  // Get the generated bytes as a single byte array
// Use the generated bytes
WsFreeWriter                // Free the writer
```

<span data-ttu-id="132e5-139">Создание и использование модуля записи для записи в поток:</span><span class="sxs-lookup"><span data-stu-id="132e5-139">To create and use a writer to write to a stream:</span></span>

``` syntax
WsCreateWriter              // Create an instance of a WS_XML_WRITER
// Initialize a WS_XML_WRITER_STREAM_OUTPUT
WsSetOutput                 // Set the encoding and output of the writer along with any other writer properties
// Write Elements
WsFlushWriter               // Force any buffered data to be written
WsFreeWriter                // Free the writer
```

<span data-ttu-id="132e5-140">Создание и использование модуля записи для записи в [ \_ \_ буфер WS XML](ws-xml-buffer.md):</span><span class="sxs-lookup"><span data-stu-id="132e5-140">To create and use a writer to write to a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax
WsCreateXmlBuffer           // Create the buffer to write to
WsCreateWriter              // Create an instance of a WS_XML_WRITER
WsSetOutputToBuffer         // Set the output buffer along with any other writer properties
// Write Elements
WsFreeWriter                // Free the writer
// The buffer has the generated document
```

<span data-ttu-id="132e5-141">Во всех случаях для форматирования XML-кода может быть задано значение свойства « [**\_ \_ модуль записи \_ \_ XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id) ».</span><span class="sxs-lookup"><span data-stu-id="132e5-141">In all cases, the property [**WS\_XML\_WRITER\_PROPERTY\_INDENT**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id) may be included to format the xml.</span></span>

## <a name="writing-elements"></a><span data-ttu-id="132e5-142">Запись элементов</span><span class="sxs-lookup"><span data-stu-id="132e5-142">Writing Elements</span></span>

<span data-ttu-id="132e5-143">Запись элемента в модуль записи:</span><span class="sxs-lookup"><span data-stu-id="132e5-143">To write an element to a writer:</span></span>

``` syntax
WsWriteStartElement          // Write a start element
for each attribute
{
// Write an attribute using either
WsWriteStartAttribute    // Write a start attribute
// Write Content
WsWriteEndAttribute      // Write an end attribute
// Or one of the following
WsWriteXmlnsAttribute    // Write an explicit xmlns attribute
}
// Write Elements or Content
WsWriteEndElement
```

<span data-ttu-id="132e5-144">Также можно использовать следующие действия:</span><span class="sxs-lookup"><span data-stu-id="132e5-144">The following may also be used:</span></span>

``` syntax
WsWriteArray                 // Write an array of primitive values as a series of repeated elements
```

## <a name="writing-content"></a><span data-ttu-id="132e5-145">Запись содержимого</span><span class="sxs-lookup"><span data-stu-id="132e5-145">Writing Content</span></span>

<span data-ttu-id="132e5-146">Чтобы записать содержимое в элемент или атрибут, можно использовать следующее:</span><span class="sxs-lookup"><span data-stu-id="132e5-146">To write content to an element or attribute, the following may be used:</span></span>

``` syntax
WsWriteChars                 // Write unicode characters from memory
WsWriteCharsUtf8             // Write UTF-8 encoded characters from memory
WsWriteBytes                 // Write binary data encoded as base64
WsPushBytes                  // Direct the writer to request that bytes be written
WsPullBytes                  // Direct the writer to read the bytes to be written
WsWriteValue                 // Write primitive values such as ints and BOOLs
WsWriteText                  // Write an WS_XML_TEXT
WsWriteQualifiedName         // Write a qualified name
```

<span data-ttu-id="132e5-147">Следующие возможности могут быть использованы для записи в документ, но не могут использоваться в атрибуте.</span><span class="sxs-lookup"><span data-stu-id="132e5-147">The following can be used to write to a document, but may not be used when within an attribute.</span></span>

``` syntax
WsWriteNode                  // Write a single WS_XML_NODE
WsCopyNode                   // Copy a single node, or an entire WS_XML_ELEMENT_NODE and children from an WS_XML_READER
```

<span data-ttu-id="132e5-148">Для записи раздела CDATA в текстовый документ можно использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="132e5-148">The following may be used to write a CDATA section in a text document:</span></span>

``` syntax
WsWriteStartCData            // Start a CDATA section in a text encoding
// Write Content
WsWriteEndCData              // End a CDATA section in text encoding
```

## <a name="miscellaneous"></a><span data-ttu-id="132e5-149">Разное</span><span class="sxs-lookup"><span data-stu-id="132e5-149">Miscellaneous</span></span>

``` syntax
WsGetPrefixFromNamespace     // Find a prefix bound to a namespace
```

## <a name="creating-a-reader"></a><span data-ttu-id="132e5-150">Создание читателя</span><span class="sxs-lookup"><span data-stu-id="132e5-150">Creating a reader</span></span>

<span data-ttu-id="132e5-151">Создание и использование считывателя для чтения из буфера в памяти:</span><span class="sxs-lookup"><span data-stu-id="132e5-151">To create and use a reader to read from an in-memory buffer:</span></span>

``` syntax
WsCreateReader              // Create an instance of a WS_XML_READER
// Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput                  // Set the encoding and input of the reader along with any other reader properties
// Read Elements
WsFreeReader                // Free the reader
```

<span data-ttu-id="132e5-152">Создание и использование читателя для чтения из потока:</span><span class="sxs-lookup"><span data-stu-id="132e5-152">To create and use a reader to reader from a stream:</span></span>

``` syntax
WsCreateReader              // Create an instance of a WS_XML_READER
// Initialize a WS_XML_READER_STREAM_INPUT
WsSetInput                  // Set the encoding and input of the reader along with any other reader properties
WsFillReader                // Populate the reader with data from the underlying stream
// Read Elements
WsFreeReader                // Free the reader
```

<span data-ttu-id="132e5-153">Создание и использование считывателя для чтения из [ \_ XML- \_ буфера WS](ws-xml-buffer.md):</span><span class="sxs-lookup"><span data-stu-id="132e5-153">To create and use a reader to read from a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax
WsCreateXmlBuffer           // Create the buffer to write to
WsCreateReader              // Create an instance of a WS_XML_READER
WsSetInputToBuffer          // Set the input buffer along with any other reader properties
// Read Elements
WsFreeReader                // Free the reader
```

## <a name="reading-elements"></a><span data-ttu-id="132e5-154">Чтение элементов</span><span class="sxs-lookup"><span data-stu-id="132e5-154">Reading Elements</span></span>

<span data-ttu-id="132e5-155">Чтение элемента из средства чтения:</span><span class="sxs-lookup"><span data-stu-id="132e5-155">To read an element from a reader:</span></span>

``` syntax
WsReadToStartElement         // Skip whitespace and comments to position the reader on a specific element
for each attribute of interest
{
WsFindAttribute          // Try Locate the attribute
if (found)
{
WsReadStartAttribute // Set the reader to read the attribute
// Read Content
WsReadEndAttribute   // Return the reader to the element
}
}
WsReadStartElement           // Advance the reader past the current element
// Read Elements or Content
WsWriteEndElement            // Advance the reader past the corresponding end element
```

<span data-ttu-id="132e5-156">Также можно использовать следующие действия:</span><span class="sxs-lookup"><span data-stu-id="132e5-156">The following may also be used:</span></span>

``` syntax
WsReadArray                  // Read an array of primitive values as a series of repeated elements
```

## <a name="reading-content"></a><span data-ttu-id="132e5-157">Чтение содержимого</span><span class="sxs-lookup"><span data-stu-id="132e5-157">Reading Content</span></span>

<span data-ttu-id="132e5-158">Для чтения содержимого из элемента или атрибута можно использовать следующее:</span><span class="sxs-lookup"><span data-stu-id="132e5-158">To read content from an element or attribute, the following may be used:</span></span>

``` syntax
WsReadChars                 // Read characters to memory as unicode
WsReadCharsUtf8             // Read characters to memory encoded as UTF-8
WsReadBytes                 // Read binary data encoded as base64
WsReadValue                 // Read primitive values such as ints and BOOLs
WsReadQualifiedName         // Read a qualified name
```

<span data-ttu-id="132e5-159">Для проверки текущего узла, на котором расположен модуль чтения, можно использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="132e5-159">The following may be used to inspect the current node the reader is positioned on:</span></span>

``` syntax
WsGetReaderNode             // Get the current node
```

## <a name="using-a-buffer"></a><span data-ttu-id="132e5-160">Использование буфера</span><span class="sxs-lookup"><span data-stu-id="132e5-160">Using a buffer</span></span>

<span data-ttu-id="132e5-161">При записи в [ \_ XML- \_ буфер WS](ws-xml-buffer.md) можно использовать следующее:</span><span class="sxs-lookup"><span data-stu-id="132e5-161">When writing to a [WS\_XML\_BUFFER](ws-xml-buffer.md) the following may be used:</span></span>

``` syntax
WsGetWriterPosition          // Get the current position of the writer in the document
WsSetWriterPosition          // Set the current position of the writer in the document
WsMoveWriter                 // Move relative to the current position in the document
WsRemoveNode                 // Delete an element or text from a document
```

<span data-ttu-id="132e5-162">При чтении из [ \_ XML- \_ буфера WS](ws-xml-buffer.md) можно использовать следующее:</span><span class="sxs-lookup"><span data-stu-id="132e5-162">When reading from a [WS\_XML\_BUFFER](ws-xml-buffer.md) the following may be used:</span></span>

``` syntax
WsGetReaderPosition          // Get the current position of the reader in the document
WsSetReaderPosition          // Set the current position of the reader in the document
WsMoveReader                 // Move relative to the current position in the document
```

<span data-ttu-id="132e5-163">Для изменения [ \_ \_ буфера WS XML](ws-xml-buffer.md)можно использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="132e5-163">The following may be used to modify a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax

WsRemoveNode                 // Delete an element or text from a document
```

## <a name="other"></a><span data-ttu-id="132e5-164">Другие</span><span class="sxs-lookup"><span data-stu-id="132e5-164">Other</span></span>

``` syntax
WsGetNamespaceFromPrefix     // Find a namespace bound to a prefix
WsGetXmlAttribute            // Find an "xml:space" or "xml:lang" attribute in scope
```

 

 




