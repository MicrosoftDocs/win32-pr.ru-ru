---
description: В этом разделе описаны внутренние сведения о том, как сопоставитель источников создает источник мультимедиа.
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: Обработчики схем и обработчики Byte-Stream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54976f45c7f07e12b6f095297231d306d0644704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711404"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a><span data-ttu-id="edfc6-103">Обработчики схем и обработчики Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="edfc6-103">Scheme Handlers and Byte-Stream Handlers</span></span>

<span data-ttu-id="edfc6-104">В этом разделе описаны внутренние сведения о том, как сопоставитель источников создает источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="edfc6-104">This topic describes the internal details of how the source resolver creates a media source.</span></span> <span data-ttu-id="edfc6-105">Прочтите этот раздел, если вы реализуете пользовательский источник мультимедиа для Media Foundation и хотите, чтобы источник мультимедиа был доступен приложениям через сопоставитель источников.</span><span class="sxs-lookup"><span data-stu-id="edfc6-105">Read this topic if you are implementing a custom media source for Media Foundation, and you want the media source to be available to applications via the source resolver.</span></span>

<span data-ttu-id="edfc6-106">Сопоставитель источников может создать источник мультимедиа на основе URL-адреса или потока байтов (то есть [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) указателя).</span><span class="sxs-lookup"><span data-stu-id="edfc6-106">The source resolver can create a media source from a URL or from a byte stream (that is, an [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) pointer).</span></span> <span data-ttu-id="edfc6-107">Для этого он использует вспомогательные объекты, называемые *обработчиками*.</span><span class="sxs-lookup"><span data-stu-id="edfc6-107">To do so, it uses helper objects called *handlers*.</span></span> <span data-ttu-id="edfc6-108">Для URL-адресов сопоставитель источников использует *обработчики схем*.</span><span class="sxs-lookup"><span data-stu-id="edfc6-108">For URLs, the source resolver uses *scheme handlers*.</span></span> <span data-ttu-id="edfc6-109">Для байтовых потоков используется *обработчики потока байтов*.</span><span class="sxs-lookup"><span data-stu-id="edfc6-109">For byte streams, it uses *byte-stream handlers*.</span></span>

<span data-ttu-id="edfc6-110">Обработчик схемы принимает в качестве входных данных URL-адрес и создает источник мультимедиа или поток байтов.</span><span class="sxs-lookup"><span data-stu-id="edfc6-110">A scheme handler takes a URL as input and creates either a media source or a byte stream.</span></span> <span data-ttu-id="edfc6-111">Если он создает поток байтов, сопоставитель источника передает его в обработчик потока байтов, который создает источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="edfc6-111">If it creates a byte stream, the source resolver will pass that to a byte-stream handler, which creates the media source.</span></span> <span data-ttu-id="edfc6-112">Этот процесс показан на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="edfc6-112">The following image illustrates this process.</span></span>

![Схема, показывающая процесс разрешения источника](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a><span data-ttu-id="edfc6-114">Обработчики схем</span><span class="sxs-lookup"><span data-stu-id="edfc6-114">Scheme Handlers</span></span>

<span data-ttu-id="edfc6-115">Обработчики схем используются, когда приложение вызывает [**имфсаурцересолвер:: креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) или его асинхронный эквивалент, [**бегинкреатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span><span class="sxs-lookup"><span data-stu-id="edfc6-115">Scheme handlers are used when the application calls [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) or its asynchronous equivalent, [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span>

<span data-ttu-id="edfc6-116">Сопоставитель источников ищет обработчики схем в реестре.</span><span class="sxs-lookup"><span data-stu-id="edfc6-116">The source resolver looks up scheme handlers in the registry.</span></span> <span data-ttu-id="edfc6-117">Обработчики схем перечисляются по схеме URL-адресов в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="edfc6-117">Scheme handlers are listed by URL scheme, under the following keys:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

<span data-ttu-id="edfc6-118">где *<scheme>* — это схема URL-адресов, которую обработчик предназначен для синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="edfc6-118">where *<scheme>* is the URL scheme that the handler is designed to parse.</span></span> <span data-ttu-id="edfc6-119">Схема включает символ ":" в конце; Например, "http:".</span><span class="sxs-lookup"><span data-stu-id="edfc6-119">The scheme includes the trailing ':' character; for example, "http:".</span></span>

<span data-ttu-id="edfc6-120">Чтобы зарегистрировать новый обработчик схемы, добавьте запись, имя которой является идентификатором CLSID обработчика схемы, в канонической строковой форме: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` .</span><span class="sxs-lookup"><span data-stu-id="edfc6-120">To register a new scheme handler, add an entry whose name is the CLSID of the scheme handler, in canonical string form: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}`.</span></span> <span data-ttu-id="edfc6-121">Значением записи является строка (REG \_ SZ), содержащая краткое описание обработчика, например "мой обработчик схемы".</span><span class="sxs-lookup"><span data-stu-id="edfc6-121">The value of the entry is a string (REG\_SZ) containing a brief description of the handler, such as "My Scheme Handler."</span></span> <span data-ttu-id="edfc6-122">Важной частью записи является CLSID.</span><span class="sxs-lookup"><span data-stu-id="edfc6-122">The important part of the entry is the CLSID.</span></span> <span data-ttu-id="edfc6-123">Сопоставитель источника создает обработчик, вызывая **CoCreateInstance** с этим идентификатором CLSID.</span><span class="sxs-lookup"><span data-stu-id="edfc6-123">The source resolver creates the handler by calling **CoCreateInstance** with this CLSID.</span></span>

<span data-ttu-id="edfc6-124">Обработчики схем предоставляют интерфейс [**имфсчемехандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) .</span><span class="sxs-lookup"><span data-stu-id="edfc6-124">Scheme handlers expose the [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) interface.</span></span> <span data-ttu-id="edfc6-125">Если сопоставитель источника обнаруживает обработчик схемы, соответствующий схеме URL-адреса, сопоставитель источника вызывает [**имфсчемехандлер:: бегинкреатеобжект**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), передавая исходный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="edfc6-125">If the source resolver finds a scheme handler that matches the URL scheme, the source resolver calls [**IMFSchemeHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), passing in the original URL.</span></span> <span data-ttu-id="edfc6-126">Обработчик схемы откроет URL-адрес и попытается проанализировать содержимое.</span><span class="sxs-lookup"><span data-stu-id="edfc6-126">The scheme handler will open the URL and attempt to parse the contents.</span></span> <span data-ttu-id="edfc6-127">На этом этапе обработчик схемы имеет два варианта:</span><span class="sxs-lookup"><span data-stu-id="edfc6-127">At that point, the scheme handler has two options:</span></span>

-   <span data-ttu-id="edfc6-128">Создайте источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="edfc6-128">Create a media source.</span></span>
-   <span data-ttu-id="edfc6-129">Создание потока байтов.</span><span class="sxs-lookup"><span data-stu-id="edfc6-129">Create a byte stream.</span></span>

<span data-ttu-id="edfc6-130">При создании источника мультимедиа сопоставитель источника Возвращает источник мультимедиа для приложения.</span><span class="sxs-lookup"><span data-stu-id="edfc6-130">If it creates a media source, the source resolver returns the media source to the application.</span></span> <span data-ttu-id="edfc6-131">Если он создает поток байтов, сопоставитель источника пытается найти соответствующий обработчик потока байтов, как описано в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="edfc6-131">If it creates a byte stream, the source resolver attempts to find an appropriate byte-stream handler, as described in the next section.</span></span>

## <a name="byte-stream-handlers"></a><span data-ttu-id="edfc6-132">Обработчики Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="edfc6-132">Byte-Stream Handlers</span></span>

<span data-ttu-id="edfc6-133">Обработчики потока байтов используются, когда приложение вызывает [**имфсаурцересолвер:: креатеобжектфромбитестреам**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) или его асинхронный эквивалент, [**бегинкреатеобжектфромбитестреам**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream).</span><span class="sxs-lookup"><span data-stu-id="edfc6-133">Byte-stream handlers are used when the application calls [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) or its asynchronous equivalent, [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream).</span></span> <span data-ttu-id="edfc6-134">Они также используются, когда обработчик схемы возвращает поток байтов, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="edfc6-134">They are also used when a scheme handler returns a byte stream, as described previously.</span></span>

<span data-ttu-id="edfc6-135">Как и в случае с обработчиками схем, в реестре перечислены обработчики потока байтов.</span><span class="sxs-lookup"><span data-stu-id="edfc6-135">As with scheme handlers, byte-stream handlers are listed in the registry.</span></span> <span data-ttu-id="edfc6-136">Они перечислены либо по расширению имени файла, либо по типу MIME (или к обоим), в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="edfc6-136">They are listed either by file name extension or MIME type (or both), under the following keys:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

<span data-ttu-id="edfc6-137">где *<ExtensionOrMimeType>* — это расширение имени файла или тип MIME.</span><span class="sxs-lookup"><span data-stu-id="edfc6-137">where *<ExtensionOrMimeType>* is the file name extension or MIME type.</span></span> <span data-ttu-id="edfc6-138">Расширения файлов включают в себя начальный символ "."; Например, ". wmv".</span><span class="sxs-lookup"><span data-stu-id="edfc6-138">File extensions include the initial '.' character; for example, ".wmv".</span></span>

<span data-ttu-id="edfc6-139">Расширение имени файла является частью URL-адреса, предоставленного приложением.</span><span class="sxs-lookup"><span data-stu-id="edfc6-139">The file name extension is part of the URL, provided by the application.</span></span> <span data-ttu-id="edfc6-140">Тип MIME может быть доступен через атрибут [**\_ \_ \_ типа содержимого MF BYTESTREAM**](mf-bytestream-content-type-attribute.md) в байтовом потоке.</span><span class="sxs-lookup"><span data-stu-id="edfc6-140">The MIME type might be available through the [**MF\_BYTESTREAM\_CONTENT\_TYPE**](mf-bytestream-content-type-attribute.md) attribute on the byte stream.</span></span>

<span data-ttu-id="edfc6-141">Чтобы зарегистрировать новый обработчик потока байтов, добавьте запись, имя которой является идентификатором CLSID обработчика, в канонической форме строки.</span><span class="sxs-lookup"><span data-stu-id="edfc6-141">To register a new byte-stream handler, add an entry whose name is the CLSID of the handler, in canonical string form.</span></span> <span data-ttu-id="edfc6-142">Значение записи — это строка (REG \_ SZ), содержащая краткое описание обработчика, например «мой обработчик Byte-Stream».</span><span class="sxs-lookup"><span data-stu-id="edfc6-142">The value of the entry is a string (REG\_SZ) containing a brief description of the handler, such as "My Byte-Stream Handler."</span></span> <span data-ttu-id="edfc6-143">Сопоставитель источников вызывает **CoCreateInstance** для создания обработчика из идентификатора CLSID.</span><span class="sxs-lookup"><span data-stu-id="edfc6-143">The source resolver calls **CoCreateInstance** to create the handler from the CLSID.</span></span> <span data-ttu-id="edfc6-144">Один и тот же обработчик можно зарегистрировать в нескольких расширениях или типах MIME.</span><span class="sxs-lookup"><span data-stu-id="edfc6-144">You can register the same handler under more than one extension or MIME type.</span></span>

<span data-ttu-id="edfc6-145">Обработчики потока байтов предоставляют интерфейс [**имфбитестреамхандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .</span><span class="sxs-lookup"><span data-stu-id="edfc6-145">Byte-stream handlers expose the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span> <span data-ttu-id="edfc6-146">Если сопоставитель источника находит соответствующий обработчик потока байтов, он вызывает [**имфбитестреамхандлер:: бегинкреатеобжект**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span><span class="sxs-lookup"><span data-stu-id="edfc6-146">If the source resolver finds a matching byte-stream handler, it calls [**IMFByteStreamHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span></span> <span data-ttu-id="edfc6-147">Входные данные для этого метода являются указателем на байтовый поток, а также исходным URL-адресом, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="edfc6-147">The input to this method is a pointer to the byte stream, plus the original URL, if available.</span></span> <span data-ttu-id="edfc6-148">Обработчик потока байтов считывает данные из потока байтов до тех пор, пока не проанализирует достаточно данных для создания источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="edfc6-148">The byte-stream handler reads from the byte stream until it parses enough data to create the media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="edfc6-149">См. также</span><span class="sxs-lookup"><span data-stu-id="edfc6-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edfc6-150">Сопоставитель источников</span><span class="sxs-lookup"><span data-stu-id="edfc6-150">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



