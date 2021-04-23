---
title: Direct2D
description: .
ms.assetid: 03b3b91c-9751-4f8d-af24-85067f06930b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2eae62ba2d6ff44920d6b6d4890a8c48bc3c0f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070289"
---
# <a name="direct2d"></a><span data-ttu-id="d5136-103">Direct2D</span><span class="sxs-lookup"><span data-stu-id="d5136-103">Direct2D</span></span>

## <a name="purpose"></a><span data-ttu-id="d5136-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="d5136-104">Purpose</span></span>

<span data-ttu-id="d5136-105">Direct2D — это API для работы с двумерной графикой в непосредственном режиме с аппаратным ускорением, обеспечивающий высокую производительность и высококачественную отрисовку двумерной геометрии, растровых изображений и текста.</span><span class="sxs-lookup"><span data-stu-id="d5136-105">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="d5136-106">API Direct2D разработан для взаимодействия с GDI, GDI+ и Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d5136-106">The Direct2D API is designed to interoperate well with GDI, GDI+, and Direct3D.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="d5136-107">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="d5136-107">Developer audience</span></span>

<span data-ttu-id="d5136-108">Direct2D предназначен главным образом для использования следующими классами разработчиков:</span><span class="sxs-lookup"><span data-stu-id="d5136-108">Direct2D is designed primarily for use by the following classes of developers:</span></span>

-   <span data-ttu-id="d5136-109">Разработчики крупных корпоративных приложений с корпоративным масштабированием.</span><span class="sxs-lookup"><span data-stu-id="d5136-109">Developers of large, enterprise-scale, native applications.</span></span>
-   <span data-ttu-id="d5136-110">Разработчики, создающие наборы средств управления и библиотеки для использования подчиненными разработчиками.</span><span class="sxs-lookup"><span data-stu-id="d5136-110">Developers who create control toolkits and libraries for consumption by downstream developers.</span></span>
-   <span data-ttu-id="d5136-111">Разработчики, которым требуется отрисовка двухмерной графики на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="d5136-111">Developers who require server-side rendering of 2-D graphics.</span></span>
-   <span data-ttu-id="d5136-112">Разработчики, использующие графическое изображение Direct3D и требующие простой, высокопроизводительную визуализацию и отрисовку текста для меню, элементов ПОЛЬЗОВАТЕЛЬСКОГО интерфейса и приголовков (Худс).</span><span class="sxs-lookup"><span data-stu-id="d5136-112">Developers who use Direct3D graphics and need simple, high-performance 2-D and text rendering for menus, user-interface (UI) elements, and Heads-up Displays (HUDs).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d5136-113">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="d5136-113">Run-time requirements</span></span>

-   <span data-ttu-id="d5136-114">Windows 7 или Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для Windows Vista и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="d5136-114">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista and later.</span></span>
-   <span data-ttu-id="d5136-115">Windows Server 2008 R2 или Windows Server 2008 с пакетом обновления 2 (SP2) и обновлением платформы для Windows Server 2008 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="d5136-115">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008 and later.</span></span>

> [!Note]
>
> <span data-ttu-id="d5136-116">Обновление платформы для Windows Vista и обновление платформы для Windows Server 2008 представляют собой набор библиотек времени выполнения, позволяющий разработчикам ориентироваться на приложения Windows 7, Windows Vista, Windows Server 2008 R2 и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d5136-116">The Platform Update for Windows Vista and Platform Update for Windows Server 2008 are a set of run-time libraries that enables developers to target applications to Windows 7, Windows Vista, Windows Server 2008 R2, and Windows Server 2008.</span></span> <span data-ttu-id="d5136-117">Эти обновления будут доступны всем клиентам Windows Vista и Windows Server 2008 с помощью Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="d5136-117">These updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="d5136-118">Сторонние приложения, требующие обновления платформы для Windows Vista или обновления платформы для Windows Server 2008, могут иметь Центр обновления Windows определить, установлена ли требуемая обновленная система. Если это не так, Центр обновления Windows будет скачивать и устанавливать его в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="d5136-118">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span> <span data-ttu-id="d5136-119">Дополнительные сведения об обновлениях см. в [статье обновление платформы для Windows Vista](https://support.microsoft.com/kb/971644).</span><span class="sxs-lookup"><span data-stu-id="d5136-119">For more information about both updates, see [Platform Update for Windows Vista](https://support.microsoft.com/kb/971644).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="d5136-120">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="d5136-120">In this section</span></span>



| <span data-ttu-id="d5136-121">Раздел</span><span class="sxs-lookup"><span data-stu-id="d5136-121">Topic</span></span>                                                                                          | <span data-ttu-id="d5136-122">Описание</span><span class="sxs-lookup"><span data-stu-id="d5136-122">Description</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5136-123">Новые возможности в Direct2D</span><span class="sxs-lookup"><span data-stu-id="d5136-123">What's new in Direct2D</span></span>](what-s-new-in-direct2d-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="d5136-124">Ниже приведены некоторые из новых дополнений к Direct2D.</span><span class="sxs-lookup"><span data-stu-id="d5136-124">Here are some of the new additions to Direct2D.</span></span> <br/>                                                                                                                   |
| [<span data-ttu-id="d5136-125">О Direct2D</span><span class="sxs-lookup"><span data-stu-id="d5136-125">About Direct2D</span></span>](direct2d-overview.md)<br/>                                             | <span data-ttu-id="d5136-126">Представляет Direct2D, API, который предоставляет разработчикам Win32 возможность выполнять двумерные задачи отрисовки графики с высокой производительностью и визуальным качеством.</span><span class="sxs-lookup"><span data-stu-id="d5136-126">Introduces Direct2D, an API that provides Win32 developers with the ability to perform 2-D graphics rendering tasks with superior performance and visual quality.</span></span> <br/> |
| [<span data-ttu-id="d5136-127">Краткое руководство по Direct2D для Windows 8</span><span class="sxs-lookup"><span data-stu-id="d5136-127">Direct2D Quickstart for Windows 8</span></span>](direct2d-quickstart-with-device-context.md)<br/>    | <span data-ttu-id="d5136-128">Содержит сводку действий, необходимых для рисования с помощью Direct2D, а также пример кода.</span><span class="sxs-lookup"><span data-stu-id="d5136-128">Summarizes the steps required to draw with Direct2D and provides example code.</span></span><br/>                                                                                     |
| [<span data-ttu-id="d5136-129">начало работы с Direct2D</span><span class="sxs-lookup"><span data-stu-id="d5136-129">Getting Started with Direct2D</span></span>](getting-started-with-direct2d-nav.md)<br/>              | <span data-ttu-id="d5136-130">Описывает, как приступить к созданию Direct2D приложений, а также примеры кода.</span><span class="sxs-lookup"><span data-stu-id="d5136-130">Describes how to get started creating Direct2D applications and provides example code.</span></span><br/>                                                                             |
| [<span data-ttu-id="d5136-131">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="d5136-131">Programming Guide</span></span>](programming-guide.md)<br/>                                          | <span data-ttu-id="d5136-132">В этом разделе содержатся разделы об концептуальном программировании, в которых описывается использование API Direct2D.</span><span class="sxs-lookup"><span data-stu-id="d5136-132">This section contains conceptual programming topics that describe how to use the Direct2D API.</span></span> <br/>                                                                    |
| [<span data-ttu-id="d5136-133">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="d5136-133">Direct2D reference</span></span>](reference.md)<br/>                                                      | <span data-ttu-id="d5136-134">Подробное описание API Direct2D.</span><span class="sxs-lookup"><span data-stu-id="d5136-134">Describes the Direct2D API in detail.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="d5136-135">Средства и служебные программы</span><span class="sxs-lookup"><span data-stu-id="d5136-135">Tools and Utilities</span></span>](tools-and-utilities.md)<br/>                                      | <span data-ttu-id="d5136-136">Средства и служебные программы, предоставляемые для Direct2D.</span><span class="sxs-lookup"><span data-stu-id="d5136-136">Tools and utilities provided for Direct2D.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="d5136-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="d5136-137">Samples</span></span>](d2d-samples.md)<br/>                                                          | <span data-ttu-id="d5136-138">Примеры приложений, демонстрирующие API Direct2D.</span><span class="sxs-lookup"><span data-stu-id="d5136-138">Sample applications that demonstrate the Direct2D API.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="d5136-139">Глоссарий Direct2D</span><span class="sxs-lookup"><span data-stu-id="d5136-139">Direct2D Glossary</span></span>](direct2d-glossary.md)<br/>                                          | <span data-ttu-id="d5136-140">Описание терминов, часто используемых в документации по Direct2D.</span><span class="sxs-lookup"><span data-stu-id="d5136-140">Describes terms commonly used by the Direct2D documentation.</span></span> <br/>                                                                                                      |



 

## <a name="additional-resources"></a><span data-ttu-id="d5136-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d5136-141">Additional resources</span></span>

-   [<span data-ttu-id="d5136-142">**Графика и игры DirectX**</span><span class="sxs-lookup"><span data-stu-id="d5136-142">**DirectX Graphics and Gaming**</span></span>](/windows/desktop/directx)
-   [<span data-ttu-id="d5136-143">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="d5136-143">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)

 

