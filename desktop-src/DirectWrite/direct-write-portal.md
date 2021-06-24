---
title: DirectWrite (DWrite)
description: Современные приложения должны поддерживать высококачественную визуализацию текста, независимые от разрешения шрифты структуры, а полную поддержку текста и макета в Юникоде. DirectWrite, API [DirectX](../directx.md) , предоставляет эти функции и многое другое.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6bdc75845c2387a4fa4335fa462d0b97ec5669
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587944"
---
# <a name="directwrite-dwrite"></a><span data-ttu-id="1a6a6-104">DirectWrite (DWrite)</span><span class="sxs-lookup"><span data-stu-id="1a6a6-104">DirectWrite (DWrite)</span></span>

## <a name="purpose"></a><span data-ttu-id="1a6a6-105">Назначение</span><span class="sxs-lookup"><span data-stu-id="1a6a6-105">Purpose</span></span>

<span data-ttu-id="1a6a6-106">Современные приложения должны поддерживать высококачественную визуализацию текста, независимые от разрешения шрифты структуры, а полную поддержку текста и макета в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-106">Today's applications must support high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support.</span></span> <span data-ttu-id="1a6a6-107">DirectWrite, API [DirectX](../directx.md) , предоставляет эти функции и многое другое.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-107">DirectWrite, a [DirectX](../directx.md) API, provides these features and more.</span></span>

- <span data-ttu-id="1a6a6-108">Независимая от устройства система макета текста, улучшающая удобочитаемость текста в документах и в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-108">A device-independent text layout system that improves text readability in documents and in UI.</span></span>
- <span data-ttu-id="1a6a6-109">Высококачественная, Подпиксельная визуализация текста [Microsoft ClearType](/typography/cleartype/) , которая может использовать [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md)или технологию отрисовки для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-109">High-quality, sub-pixel, [Microsoft ClearType](/typography/cleartype/) text rendering that can use [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md), or application-specific rendering technology.</span></span>
- <span data-ttu-id="1a6a6-110">Текст с аппаратным ускорением при использовании с [Direct2D](rendering-by-using-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="1a6a6-110">Hardware-accelerated text, when used with [Direct2D](rendering-by-using-direct2d.md).</span></span>
- <span data-ttu-id="1a6a6-111">Поддержка многоязычного текста.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-111">Support for multi-format text.</span></span>
- <span data-ttu-id="1a6a6-112">Поддержка расширенных типографских функций шрифтов OpenType.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-112">Support for the advanced typography features of OpenType fonts.</span></span>
- <span data-ttu-id="1a6a6-113">Поддержка макета и отрисовки текста на всех поддерживаемых языках.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-113">Support for the layout and rendering of text in all supported languages.</span></span>
- <span data-ttu-id="1a6a6-114">Макет и отрисовка, совместимые с [GDI](interoperating-with-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="1a6a6-114">[GDI](interoperating-with-gdi.md)-compatible layout and rendering.</span></span>

<span data-ttu-id="1a6a6-115">API поддерживает измерение, рисование и проверку попадания для текста в нескольких форматах.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-115">The API supports measuring, drawing, and hit-testing of multi-format text.</span></span> <span data-ttu-id="1a6a6-116">DirectWrite обрабатывает текст на всех поддерживаемых языках для глобальных и локализованных приложений, основываясь на ключевой инфраструктуре языка, обнаруженной в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-116">DirectWrite handles text in all supported languages for global and localized applications, building on the key language infrastructure found in Windows 7.</span></span> <span data-ttu-id="1a6a6-117">Кроме того, в DirectWrite имеется API низкоуровневой отрисовки глифов, предназначенный для разработчиков, которым необходимо использовать собственные раскладки и выполнять преобразование из Юникода в глифы.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-117">DirectWrite also provides a low-level glyph rendering API for developers who want to perform their own layout and Unicode-to-glyph processing.</span></span>

> [!NOTE]
> <span data-ttu-id="1a6a6-118">[Пакет SDK для приложений Windows](/windows/apps/windows-app-sdk/) представляет новую версию DirectWrite &mdash; под названием двритекоре &mdash; , которая работает в версиях Windows до Windows 8, и открывает дверцу для использования кросс-платформенной платформы.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-118">[Windows App SDK](/windows/apps/windows-app-sdk/) introduces a new version of DirectWrite&mdash;called DWriteCore&mdash;that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="1a6a6-119">Дополнительные сведения см. в разделе [двритекоре Overview](dwritecore-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1a6a6-119">For more details, see [DWriteCore overview](dwritecore-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1a6a6-120">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="1a6a6-120">Run-time requirements</span></span>

- <span data-ttu-id="1a6a6-121">Windows 7 или Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a6a6-121">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>
- <span data-ttu-id="1a6a6-122">Windows Server 2008 R2 или Windows Server 2008 с пакетом обновления 2 (SP2) и обновлением платформы для Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a6a6-122">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1a6a6-123">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="1a6a6-123">In this section</span></span>

| <span data-ttu-id="1a6a6-124">Раздел</span><span class="sxs-lookup"><span data-stu-id="1a6a6-124">Topic</span></span> | <span data-ttu-id="1a6a6-125">Описание</span><span class="sxs-lookup"><span data-stu-id="1a6a6-125">Description</span></span> |
|-|-|
| [<span data-ttu-id="1a6a6-126">Новые возможности в DirectWrite</span><span class="sxs-lookup"><span data-stu-id="1a6a6-126">What's new in DirectWrite</span></span>](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="1a6a6-127">Ниже приведены некоторые из новых дополнений к DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-127">Here are some of the new additions to DirectWrite.</span></span> <br/> |
| [<span data-ttu-id="1a6a6-128">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="1a6a6-128">Programming Guide</span></span>](programming-guide.md)<br/> | <span data-ttu-id="1a6a6-129">В следующих разделах приводятся общие сведения об API DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-129">The following topics provide an overview of the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="1a6a6-130">Справочник по интерфейсам API</span><span class="sxs-lookup"><span data-stu-id="1a6a6-130">API Reference</span></span>](reference.md)<br/> | <span data-ttu-id="1a6a6-131">Описывает API DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-131">Describes the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="1a6a6-132">Образец кода</span><span class="sxs-lookup"><span data-stu-id="1a6a6-132">Sample Code</span></span>](samples.md)<br/> | <span data-ttu-id="1a6a6-133">В этом разделе содержатся сведения о примерах программ для DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="1a6a6-133">This section contains information about sample programs for DirectWrite.</span></span><br/> |
