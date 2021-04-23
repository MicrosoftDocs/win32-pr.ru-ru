---
title: Взаимодействие с GDI
description: DirectWrite предоставляет путь перехода от и некоторые возможности взаимодействия с, модели шрифта GDI, а также интерфейсы для отрисовки текста в растровое изображение, которое затем может быть отображено в окне.
ms.assetid: fb73e07b-60fb-4726-bd5b-c14d61ace186
keywords:
- DirectWrite, взаимодействие GDI
- DirectWrite, взаимодействие
- совместимость
- Интерфейс графических устройств (GDI)
- GDI (интерфейс графических устройств)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41c7c99e6bfac0aabddd4a1568b64cd425ccb25b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070046"
---
# <a name="interoperating-with-gdi"></a><span data-ttu-id="79891-108">Взаимодействие с GDI</span><span class="sxs-lookup"><span data-stu-id="79891-108">Interoperating with GDI</span></span>

<span data-ttu-id="79891-109">[DirectWrite](direct-write-portal.md) предоставляет путь перехода от и некоторые возможности взаимодействия с, модели шрифта GDI, а также интерфейсы для отрисовки текста в растровое изображение, которое затем может быть отображено в окне.</span><span class="sxs-lookup"><span data-stu-id="79891-109">[DirectWrite](direct-write-portal.md) provides a migration path from, and some interoperability with, GDI's font model, as well as interfaces for rendering text to a bitmap that can then be drawn on a window.</span></span>

<span data-ttu-id="79891-110">Этот обзор содержит следующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="79891-110">This overview contains the following parts:</span></span>

-   [<span data-ttu-id="79891-111">Введение</span><span class="sxs-lookup"><span data-stu-id="79891-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="79891-112">Часть 1. Идвритегдиинтероп</span><span class="sxs-lookup"><span data-stu-id="79891-112">Part 1: IDWriteGdiInterop</span></span>](#part-1-idwritegdiinterop)
-   [<span data-ttu-id="79891-113">Часть 2. объекты Font</span><span class="sxs-lookup"><span data-stu-id="79891-113">Part 2: Font Objects</span></span>](#part-2-font-objects)
-   [<span data-ttu-id="79891-114">Часть 3. Подготовка к просмотру</span><span class="sxs-lookup"><span data-stu-id="79891-114">Part 3: Rendering</span></span>](#part-3-rendering)

## <a name="introduction"></a><span data-ttu-id="79891-115">Введение</span><span class="sxs-lookup"><span data-stu-id="79891-115">Introduction</span></span>

<span data-ttu-id="79891-116">[DirectWrite](direct-write-portal.md) предоставляет методы для преобразования между LOGFONT структурой GDI и интерфейсами шрифтов DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="79891-116">[DirectWrite](direct-write-portal.md) provides methods for converting between GDI's LOGFONT structure and DirectWrite font interfaces.</span></span> <span data-ttu-id="79891-117">Это позволяет использовать GDI для некоторых или всех перечислений и выделений шрифтов, используя преимущества улучшенной функциональности и производительности DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="79891-117">This allows you to use GDI for some or all of the font enumeration and selection, while taking advantage of the improved functionality and performance of DirectWrite.</span></span> <span data-ttu-id="79891-118">DirectWrite также имеет интерфейсы для отрисовки в точечный рисунок, если требуется отображать текст на поверхности GDI.</span><span class="sxs-lookup"><span data-stu-id="79891-118">DirectWrite also has interfaces for rendering to a bitmap if you want to display text on a GDI surface.</span></span>

## <a name="part-1-idwritegdiinterop"></a><span data-ttu-id="79891-119">Часть 1. Идвритегдиинтероп</span><span class="sxs-lookup"><span data-stu-id="79891-119">Part 1: IDWriteGdiInterop</span></span>

<span data-ttu-id="79891-120">Интерфейс [**идвритегдиинтероп**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) используется для преобразования между структурами шрифтов GDI и интерфейсами шрифтов [DirectWrite](direct-write-portal.md) , а также для создания объекта [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) .</span><span class="sxs-lookup"><span data-stu-id="79891-120">The [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) interface is used to convert between GDI font structures and [DirectWrite](direct-write-portal.md) font interfaces, and also to create an [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object.</span></span> <span data-ttu-id="79891-121">Получите объект **идвритегдиинтероп** с помощью метода [**Идвритефактори:: жетгдиинтероп**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="79891-121">Get an **IDWriteGdiInterop** object by using the [**IDWriteFactory::GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) method, as shown in the following code.</span></span>


```C++
// Create a GDI interop interface.
if (SUCCEEDED(hr))
{
    hr = g_pDWriteFactory->GetGdiInterop(&g_pGdiInterop);
}
```



## <a name="part-2-font-objects"></a><span data-ttu-id="79891-122">Часть 2. объекты Font</span><span class="sxs-lookup"><span data-stu-id="79891-122">Part 2: Font Objects</span></span>

<span data-ttu-id="79891-123">GDI использует структуру LOGFONT для хранения сведений о шрифте и стиле текста.</span><span class="sxs-lookup"><span data-stu-id="79891-123">GDI uses the LOGFONT structure to store information about the font and style of text.</span></span> <span data-ttu-id="79891-124">Метод [**идвритегдиинтероп:: креатефонтфромлогфонт**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) ПРЕОБРАЗУЕТ структуру LOGFONT в объект [**идвритефонт**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="79891-124">The [**IDWriteGdiInterop::CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) method will convert a LOGFONT structure to an [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object, as seen in the following code.</span></span>


```C++
// Convert to a DirectWrite font.
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateFontFromLOGFONT(&lf, &pFont);
}
```



<span data-ttu-id="79891-125">Однако [**идвритефонт**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) не инкапсулирует все те же сведения, что и LOGFONT.</span><span class="sxs-lookup"><span data-stu-id="79891-125">However, [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) does not encapsulate all of the same information that a LOGFONT does.</span></span> <span data-ttu-id="79891-126">Структура LOGFONT содержит размер шрифта, вес, стиль, подчеркивание, зачеркивание, имя начертания шрифта и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="79891-126">A LOGFONT structure contains the font size, weight, style, underline, strikeout, font face name, and some other information.</span></span> <span data-ttu-id="79891-127">Объекты **идвритефонт** содержат сведения о шрифте, его весе и стиле, но не размер шрифта, подчеркивание и т. д.</span><span class="sxs-lookup"><span data-stu-id="79891-127">**IDWriteFont** objects contain information about a font and its weight and style, but not the font size, underline, and so on.</span></span> <span data-ttu-id="79891-128">При использовании [DirectWrite](direct-write-portal.md)элементы сведений, такие как эти, инкапсулируются объектом [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) или для конкретных диапазонов текста — объекта [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="79891-128">With [DirectWrite](direct-write-portal.md), formatting information elements such as these are encapsulated by an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object or, for specific ranges of text, an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="79891-129">У вас есть возможность преобразовать [**идвритефонт**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) в LOGFONT с помощью [**Идвритегдиинтероп:: конвертфонттологфонт**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).</span><span class="sxs-lookup"><span data-stu-id="79891-129">You do have the option to convert a [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) to a LOGFONT by using the [**IDWriteGdiInterop::ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).</span></span>

## <a name="part-3-rendering"></a><span data-ttu-id="79891-130">Часть 3. Подготовка к просмотру</span><span class="sxs-lookup"><span data-stu-id="79891-130">Part 3: Rendering</span></span>

<span data-ttu-id="79891-131">Для отрисовки текста DirectWrite на поверхности GDI используется настраиваемый модуль подготовки текста.</span><span class="sxs-lookup"><span data-stu-id="79891-131">To render DirectWrite text to a GDI surface you use a custom text renderer.</span></span> <span data-ttu-id="79891-132">См. раздел [Подготовка к поверхности GDI](render-to-a-gdi-surface.md) .</span><span class="sxs-lookup"><span data-stu-id="79891-132">See the [Render to a GDI Surface](render-to-a-gdi-surface.md) topic.</span></span>

 

 