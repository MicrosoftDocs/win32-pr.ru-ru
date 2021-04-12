---
description: Коды FOURCC
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: Коды FOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb789bc16a1643ee737c1c1a63bdbc5704567931
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139363"
---
# <a name="fourcc-codes"></a><span data-ttu-id="561c1-103">Коды FOURCC</span><span class="sxs-lookup"><span data-stu-id="561c1-103">FOURCC Codes</span></span>

<span data-ttu-id="561c1-104">Многим цифровым форматам мультимедиа назначены коды FOURCC.</span><span class="sxs-lookup"><span data-stu-id="561c1-104">Many digital media formats have FOURCC codes assigned to them.</span></span> <span data-ttu-id="561c1-105">Код FOURCC — это 32-разрядное целое число без знака, которое создается путем сцепления четырех символов ASCII.</span><span class="sxs-lookup"><span data-stu-id="561c1-105">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="561c1-106">Например, код FOURCC для видео YUY2 — "YUY2".</span><span class="sxs-lookup"><span data-stu-id="561c1-106">For example, the FOURCC code for YUY2 video is 'YUY2'.</span></span> <span data-ttu-id="561c1-107">Для сжатых видеоформатов и видеоформатов, отличных от RGB (например, YUV), элементу **бикомпрессион** структуры [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) следует присвоить код FourCC.</span><span class="sxs-lookup"><span data-stu-id="561c1-107">For compressed video formats and non-RGB video formats (such as YUV), the **biCompression** member of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure should be set to the FOURCC code.</span></span>

<span data-ttu-id="561c1-108">Существуют различные макросы C/C++, упрощающие объявление значений FOURCC в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="561c1-108">There are various C/C++ macros that make it easier to declare FOURCC values in source code.</span></span> <span data-ttu-id="561c1-109">Например, макрос **макефауркк** объявляется в ммсистем. h, а макрос **FCC** объявляется в авирифф. h.</span><span class="sxs-lookup"><span data-stu-id="561c1-109">For example, the **MAKEFOURCC** macro is declared in Mmsystem.h, and the **FCC** macro is declared in Aviriff.h.</span></span> <span data-ttu-id="561c1-110">Используйте их следующим образом:</span><span class="sxs-lookup"><span data-stu-id="561c1-110">Use them as follows:</span></span>


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



<span data-ttu-id="561c1-111">Кроме того, можно объявить код FOURCC непосредственно в виде строкового литерала, просто отменив порядок символов.</span><span class="sxs-lookup"><span data-stu-id="561c1-111">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="561c1-112">Пример:</span><span class="sxs-lookup"><span data-stu-id="561c1-112">For example:</span></span>


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



<span data-ttu-id="561c1-113">Обратный порядок необходим, поскольку операционная система Microsoft Windows использует архитектуру с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="561c1-113">Reversing the order is necessary because the Microsoft Windows operating system uses a little-endian architecture.</span></span> <span data-ttu-id="561c1-114">' Y ' = 0x59, ' U ' = 0x55, и ' 2 ' = 0x32, поэтому ' 2YUY ' является 0x32595559.</span><span class="sxs-lookup"><span data-stu-id="561c1-114">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.</span></span>

### <a name="converting-fourcc-codes-to-subtype-guids"></a><span data-ttu-id="561c1-115">Преобразование кодов FOURCC в идентификаторы GUID подтипов</span><span class="sxs-lookup"><span data-stu-id="561c1-115">Converting FOURCC Codes to Subtype GUIDs</span></span>

<span data-ttu-id="561c1-116">Диапазон из 2 \* 32 идентификаторов GUID зарезервирован для представления фаурккс.</span><span class="sxs-lookup"><span data-stu-id="561c1-116">A range of 2\*32 GUIDs is reserved for representing FOURCCs.</span></span> <span data-ttu-id="561c1-117">Эти идентификаторы GUID представляют собой всю форму, `XXXXXXXX-0000-0010-8000-00AA00389B71` где `XXXXXXXX` — это код FourCC.</span><span class="sxs-lookup"><span data-stu-id="561c1-117">These GUIDs are all of the form `XXXXXXXX-0000-0010-8000-00AA00389B71` where `XXXXXXXX` is the FOURCC code.</span></span> <span data-ttu-id="561c1-118">Таким же значением является идентификатор GUID подтипа для YUY2 `32595559-0000-0010-8000-00AA00389B71` .</span><span class="sxs-lookup"><span data-stu-id="561c1-118">Thus, the subtype GUID for YUY2 is `32595559-0000-0010-8000-00AA00389B71`.</span></span>

<span data-ttu-id="561c1-119">Многие из этих идентификаторов GUID уже определены в файле заголовков UUID. h.</span><span class="sxs-lookup"><span data-stu-id="561c1-119">Many of these GUIDs are defined already in the header file Uuids.h.</span></span> <span data-ttu-id="561c1-120">Например, подтип YUY2 определяется как МЕДИАСУБТИПЕ \_ YUY2.</span><span class="sxs-lookup"><span data-stu-id="561c1-120">For example, the YUY2 subtype is defined as MEDIASUBTYPE\_YUY2.</span></span> <span data-ttu-id="561c1-121">Библиотека базовых классов DirectShow также предоставляет вспомогательный класс [**фаурккмап**](fourccmap.md), который можно использовать для преобразования кодов FourCC в значения GUID.</span><span class="sxs-lookup"><span data-stu-id="561c1-121">The DirectShow base class library also provides a helper class, [**FOURCCMap**](fourccmap.md), which can be used to convert FOURCC codes into GUID values.</span></span> <span data-ttu-id="561c1-122">Конструктор **фаурккмап** принимает в качестве входного параметра код FourCC.</span><span class="sxs-lookup"><span data-stu-id="561c1-122">The **FOURCCMap** constructor takes a FOURCC code as an input parameter.</span></span> <span data-ttu-id="561c1-123">Затем можно привести объект **фаурккмап** к соответствующему GUID:</span><span class="sxs-lookup"><span data-stu-id="561c1-123">You can then cast the **FOURCCMap** object to the corresponding GUID:</span></span>


```C++
FOURCCMap fccMap(FCC('YUY2'));
GUID g1 = (GUID)fccMap;

// Equivalent:
GUID g2 = (GUID)FOURCCMap(FCC('YUY2'));
```



## <a name="related-topics"></a><span data-ttu-id="561c1-124">См. также</span><span class="sxs-lookup"><span data-stu-id="561c1-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="561c1-125">**Звуковые подтипы**</span><span class="sxs-lookup"><span data-stu-id="561c1-125">**Audio Subtypes**</span></span>](audio-subtypes.md)
</dt> <dt>

[<span data-ttu-id="561c1-126">Подтипы видео</span><span class="sxs-lookup"><span data-stu-id="561c1-126">Video Subtypes</span></span>](video-subtypes.md)
</dt> <dt>

[<span data-ttu-id="561c1-127">Работа с кодеками</span><span class="sxs-lookup"><span data-stu-id="561c1-127">Working with Codecs</span></span>](working-with-codecs.md)
</dt> </dl>

 

 



