---
title: Наложение, Ундерлай и основные плоскости
description: В приложениях можно использовать плоскости аппаратного уровня (наложение и ундерлай плоскости).
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- OpenGL в Windows, аппаратный слой плоскости
- аппаратный слой плоскости OpenGL
- наложение плоскостей OpenGL
- ундерлай плоскости OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fe68c4bb57d431151c4d879965fcf7496c8615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661556"
---
# <a name="overlay-underlay-and-main-planes"></a><span data-ttu-id="730a1-107">Наложение, Ундерлай и основные плоскости</span><span class="sxs-lookup"><span data-stu-id="730a1-107">Overlay, Underlay, and Main Planes</span></span>

<span data-ttu-id="730a1-108">В приложениях можно использовать плоскости аппаратного уровня (наложение и ундерлай плоскости).</span><span class="sxs-lookup"><span data-stu-id="730a1-108">You can use hardware layer planes (overlay and underlay planes) in your applications.</span></span> <span data-ttu-id="730a1-109">В Windows форматы пикселей описывают конфигурации пикселей графического устройства.</span><span class="sxs-lookup"><span data-stu-id="730a1-109">With Windows, pixel formats describe the pixel configurations of a graphics device.</span></span> <span data-ttu-id="730a1-110">Каждый формат пикселей описывает глубину и другие характеристики основных буферов цвета и описывает дополнительные буферы (например, глубину, накопление, набор элементов и вспомогательное), используемое основной плоскостью.</span><span class="sxs-lookup"><span data-stu-id="730a1-110">Each pixel format describes the depth and other characteristics of the main color buffers and describes additional buffers (such as depth, accumulation, stencil, and auxiliary) that the main plane uses.</span></span> <span data-ttu-id="730a1-111">Теперь форматы пикселей расширены для включения наложенных и ундерлай буферов.</span><span class="sxs-lookup"><span data-stu-id="730a1-111">Pixel formats are now extended to include overlay and underlay buffers.</span></span>

<span data-ttu-id="730a1-112">Плоскости слоев всегда имеют цветовой буфер, находящуюся спереди, а также могут включать буферы переднего плана и фона.</span><span class="sxs-lookup"><span data-stu-id="730a1-112">Layer planes always have a front-left color buffer and also can include front-right and back color buffers.</span></span> <span data-ttu-id="730a1-113">Каждая плоскость слоя имеет конкретный контекст отрисовки для отображения в буферы слоев.</span><span class="sxs-lookup"><span data-stu-id="730a1-113">Each layer plane has a specific rendering context to render into the layer buffers.</span></span> <span data-ttu-id="730a1-114">Вы не можете использовать функции рисования GDI в слоях плоскости.</span><span class="sxs-lookup"><span data-stu-id="730a1-114">You cannot use GDI drawing functions in layer planes.</span></span>

<span data-ttu-id="730a1-115">Окно управляет цветовыми буферами плоскостей слоев аналогично тому, как она управляет буферами цветовых буферов основной плоскости.</span><span class="sxs-lookup"><span data-stu-id="730a1-115">A window manages the color buffers of layer planes similarly to the way it manages main-plane color buffers.</span></span> <span data-ttu-id="730a1-116">Одновременно можно отобразить несколько окон с наложенными и/или ундерлай плоскостями.</span><span class="sxs-lookup"><span data-stu-id="730a1-116">You can display multiple windows with overlay and/or underlay planes at the same time.</span></span> <span data-ttu-id="730a1-117">Нельзя иметь свободные плавающие окна наложения, которые могут перемещаться по любому окну в главной плоскости рисования.</span><span class="sxs-lookup"><span data-stu-id="730a1-117">You cannot have free-floating overlay windows that can move over any window in the main drawing plane.</span></span> <span data-ttu-id="730a1-118">Кроме того, поскольку он скрывает базовые плоскости в окне в любое время, нельзя использовать всплывающие аппаратные плоскости, не имеющие прозрачного цвета.</span><span class="sxs-lookup"><span data-stu-id="730a1-118">In addition, because it would obscure underlying planes in a window at all times, you cannot use hardware pop-up planes that have no transparent color.</span></span>

<span data-ttu-id="730a1-119">Каждая плоскость слоя в окне имеет связанную палитру.</span><span class="sxs-lookup"><span data-stu-id="730a1-119">Each layer plane in a window has an associated palette.</span></span> <span data-ttu-id="730a1-120">Можно задать палитру слоя уровня индекса, но палитра цветовой плоскости RGBA фиксирована.</span><span class="sxs-lookup"><span data-stu-id="730a1-120">You can set the palette of a color-index layer plane, but the palette of an RGBA color plane is fixed.</span></span> <span data-ttu-id="730a1-121">Если окно находится на переднем плане, необходимо реализовать соответствующую палитру.</span><span class="sxs-lookup"><span data-stu-id="730a1-121">You must realize the appropriate palette when a window is in the foreground.</span></span> <span data-ttu-id="730a1-122">Плоскости слоя имеют прозрачный цвет пикселя или индекс, позволяющий отображать все базовые плоскости слоя.</span><span class="sxs-lookup"><span data-stu-id="730a1-122">Layer planes have a transparent pixel color or index that enables any underlying layer planes to show through.</span></span>

<span data-ttu-id="730a1-123">Состояние контекста отрисовки можно скопировать в другой контекст отрисовки на отдельной плоскости слоя.</span><span class="sxs-lookup"><span data-stu-id="730a1-123">You can copy the state of a rendering context to another rendering context in a separate layer plane.</span></span> <span data-ttu-id="730a1-124">Вы также можете совместно использовать списки отображения между контекстами подготовки к просмотру на разных плоскостях слоя.</span><span class="sxs-lookup"><span data-stu-id="730a1-124">You can also share display lists among rendering contexts in different layer planes.</span></span>

<span data-ttu-id="730a1-125">На плоскостях слоя используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="730a1-125">The following functions are used with layer planes:</span></span>

-   [<span data-ttu-id="730a1-126">**вглкопиконтекст**</span><span class="sxs-lookup"><span data-stu-id="730a1-126">**wglCopyContext**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [<span data-ttu-id="730a1-127">**вглкреателайерконтекст**</span><span class="sxs-lookup"><span data-stu-id="730a1-127">**wglCreateLayerContext**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [<span data-ttu-id="730a1-128">**вглдескрибелайерплане**</span><span class="sxs-lookup"><span data-stu-id="730a1-128">**wglDescribeLayerPlane**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [<span data-ttu-id="730a1-129">**вглжетлайерпалеттинтриес**</span><span class="sxs-lookup"><span data-stu-id="730a1-129">**wglGetLayerPaletteEntries**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [<span data-ttu-id="730a1-130">**вглреализелайерпалетте**</span><span class="sxs-lookup"><span data-stu-id="730a1-130">**wglRealizeLayerPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [<span data-ttu-id="730a1-131">**вглсетлайерпалеттинтриес**</span><span class="sxs-lookup"><span data-stu-id="730a1-131">**wglSetLayerPaletteEntries**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [<span data-ttu-id="730a1-132">**вглсваплайербуфферс**</span><span class="sxs-lookup"><span data-stu-id="730a1-132">**wglSwapLayerBuffers**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




