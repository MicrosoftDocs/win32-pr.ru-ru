---
title: Direct2D и высокое разрешение
description: Описывает, как Direct2D поддерживает дисплеи с высоким разрешением.
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D, высокое разрешение DPI
- высокое разрешение DPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6548849416268f31b8b0c4a4261347c818ffa24c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987829"
---
# <a name="direct2d-and-high-dpi"></a><span data-ttu-id="5e965-105">Direct2D и высокое разрешение</span><span class="sxs-lookup"><span data-stu-id="5e965-105">Direct2D and High-DPI</span></span>

<span data-ttu-id="5e965-106">Написание приложения с поддержкой DPI является ключом к единообразному отображению пользовательского интерфейса в различных параметрах отображения с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="5e965-106">Writing a DPI-aware application is the key to making a user interface (UI) look consistently good across a wide variety of high-DPI display settings.</span></span> <span data-ttu-id="5e965-107">Приложение, которое не учитывает DPI, но работает на параметрах отображения с высоким разрешением, может пострадать от многих визуальных компонентов, включая неправильное масштабирование элементов пользовательского интерфейса, обрезанный текст и размытые изображения.</span><span class="sxs-lookup"><span data-stu-id="5e965-107">An application that is not DPI-aware but is running on a high-DPI display setting can suffer from many visual artifacts, including incorrect scaling of UI elements, clipped text, and blurry images.</span></span> <span data-ttu-id="5e965-108">Благодаря добавлению поддержки в приложении для разрешения DPI представление пользовательского интерфейса приложения становится более предсказуемым, что делает его более наглядным и удобочитаемым для пользователей.</span><span class="sxs-lookup"><span data-stu-id="5e965-108">By adding support in your application for DPI-awareness, you make the presentation of your application's UI more predictable, making it more visually appealing and easier to read for users.</span></span> <span data-ttu-id="5e965-109">К счастью, Direct2D упрощает написание приложений, которые хорошо работают в высоком уровне DPI.</span><span class="sxs-lookup"><span data-stu-id="5e965-109">Fortunately, Direct2D makes it easier than ever to write applications that work well in high-DPI.</span></span> <span data-ttu-id="5e965-110">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="5e965-110">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5e965-111">Поддержка высокого разрешения в Direct2D</span><span class="sxs-lookup"><span data-stu-id="5e965-111">High-DPI Support in Direct2D</span></span>](#high-dpi-support-in-direct2d)
-   [<span data-ttu-id="5e965-112">Windows 8 и высокое разрешение DPI</span><span class="sxs-lookup"><span data-stu-id="5e965-112">Windows 8 and High-DPI</span></span>](#windows-8-and-high-dpi)
-   [<span data-ttu-id="5e965-113">Что такое DIP?</span><span class="sxs-lookup"><span data-stu-id="5e965-113">What is a DIP?</span></span>](#what-is-a-dip)
-   [<span data-ttu-id="5e965-114">См. также</span><span class="sxs-lookup"><span data-stu-id="5e965-114">Related topics</span></span>](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a><span data-ttu-id="5e965-115">Поддержка высокого разрешения в Direct2D</span><span class="sxs-lookup"><span data-stu-id="5e965-115">High-DPI Support in Direct2D</span></span>

<span data-ttu-id="5e965-116">Direct2D предоставляет следующие возможности для работы с сценариями с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="5e965-116">Direct2D provides the following features for working with high-DPI scenarios:</span></span>

-   <span data-ttu-id="5e965-117">Он автоматически учитывает DPI системы при создании оконного целевого объекта отрисовки, если манифест приложения указывает, что приложение правильно обрабатывает DPI.</span><span class="sxs-lookup"><span data-stu-id="5e965-117">It automatically honors the system DPI when creating a windowed render target, so long as the application manifest indicates that the application handles DPI correctly.</span></span> <span data-ttu-id="5e965-118">(Сведения о том, как объявить, что приложение учитывает DPI, см. в разделе [как обеспечить правильное отображение приложения на дисплеях с высоким разрешением](how-to--size-a-window-properly-for-high-dpi-displays.md).)</span><span class="sxs-lookup"><span data-stu-id="5e965-118">(For information on how to declare that your application is DPI-aware, see [How to Ensure That Your Application Displays Properly on High-DPI Displays](how-to--size-a-window-properly-for-high-dpi-displays.md).)</span></span>
-   <span data-ttu-id="5e965-119">Он выражает координаты в DIP (аппаратно-независимые пиксели), что позволяет приложению масштабироваться автоматически при изменении параметра DPI.</span><span class="sxs-lookup"><span data-stu-id="5e965-119">It expresses coordinates in DIPs (Device Independent Pixels), which enables the application to scale automatically when the DPI setting changes.</span></span>
-   <span data-ttu-id="5e965-120">Он позволяет точечным рисункам иметь разрешение DPI и правильно масштабировать их, принимая во внимание DPI.</span><span class="sxs-lookup"><span data-stu-id="5e965-120">It enables bitmaps to have a DPI and correctly scales them by taking the DPI into account.</span></span> <span data-ttu-id="5e965-121">Эта функция также может использоваться для сохранения значков с разными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="5e965-121">This feature can also be used to maintain icons at different resolutions.</span></span>
-   <span data-ttu-id="5e965-122">Он выражает большинство ресурсов в DIP, что делает ресурсы автоматически независимыми от разрешения.</span><span class="sxs-lookup"><span data-stu-id="5e965-122">It expresses most resources in DIPs, which makes the resources automatically independent of resolution.</span></span>
-   <span data-ttu-id="5e965-123">Он использует координатное пространство с плавающей запятой и сглаживание, поэтому любое содержимое может масштабироваться до любых произвольных точек на дюйм.</span><span class="sxs-lookup"><span data-stu-id="5e965-123">It uses a floating-point coordinate space and antialiasing, so any content can be scaled to any arbitrary DPI.</span></span>

<span data-ttu-id="5e965-124">Графический конвейер Direct2D поддерживает масштабирование от 96 DPI до 1200DPI.</span><span class="sxs-lookup"><span data-stu-id="5e965-124">The Direct2D graphics pipeline is designed to scale from 96 DPI to 1200DPI.</span></span>

## <a name="windows-8-and-high-dpi"></a><span data-ttu-id="5e965-125">Windows 8 и высокое разрешение DPI</span><span class="sxs-lookup"><span data-stu-id="5e965-125">Windows 8 and High-DPI</span></span>

<span data-ttu-id="5e965-126">Начиная с Windows 8, существуют дополнительные функции поддержки высокого DPI.</span><span class="sxs-lookup"><span data-stu-id="5e965-126">Starting with Windows 8, there are additional features for high-DPI support.</span></span>

<span data-ttu-id="5e965-127">Если значение DPI контекста устройства достаточно велико, Direct2D изменяет пороговое значение, которое используется для включения вертикального сглаживания текста.</span><span class="sxs-lookup"><span data-stu-id="5e965-127">If the device context DPI is high enough, Direct2D changes the threshold it uses to enable vertical antialiasing of text.</span></span> <span data-ttu-id="5e965-128">Это приводит к ускоренной отрисовке текста на дисплеях с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="5e965-128">This results in faster text rendering on high-DPI displays.</span></span> <span data-ttu-id="5e965-129">Кроме того, можно переключить режим единицы измерения на Пиксели вместо DIP с помощью метода [**ID2D1DeviceContext:: сетунитмоде**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) .</span><span class="sxs-lookup"><span data-stu-id="5e965-129">Additionally, you can switch the unit mode to pixels instead of DIPs using the [**ID2D1DeviceContext::SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) method.</span></span> <span data-ttu-id="5e965-130">Если установить режим единицы измерения в пикселях и в контекстном задании устройства dpi на экране, то оптимизация по-прежнему будет включена.</span><span class="sxs-lookup"><span data-stu-id="5e965-130">If you set the unit mode to pixels and the device context DPI to the screen DPI, the optimization is still enabled.</span></span>

## <a name="what-is-a-dip"></a><span data-ttu-id="5e965-131">Что такое DIP?</span><span class="sxs-lookup"><span data-stu-id="5e965-131">What is a DIP?</span></span>

<span data-ttu-id="5e965-132">Аппаратно-независимый пиксель (DIP) — это логический пиксель, сопоставляемый с пикселами физического устройства с помощью скаляра, DPI.</span><span class="sxs-lookup"><span data-stu-id="5e965-132">A device independent pixel (DIP) is a logical pixel that maps to the pixels of the physical device through a scalar, the DPI.</span></span> <span data-ttu-id="5e965-133">DPI соответствует точкам на дюйм, где точка обозначает физическую точку устройства.</span><span class="sxs-lookup"><span data-stu-id="5e965-133">DPI stands for dots per inch, where a dot represents a physical device pixel.</span></span> <span data-ttu-id="5e965-134">(Номенклатура поступает из печати, где точки — это наименьшая пунктирная точка, которую может создать процесс печати).</span><span class="sxs-lookup"><span data-stu-id="5e965-134">(The nomenclature comes from printing, where dots are the smallest ink dot that a printing process can produce).</span></span> <span data-ttu-id="5e965-135">Так как стандартный монитор используется для 96 точек на дюйм, DPI 96 означало, что аппаратно-независимый пиксель (или DIP) сопоставлено 1:1 с физическим пикселем.</span><span class="sxs-lookup"><span data-stu-id="5e965-135">Because a standard monitor used to have 96 dots per inch, a DPI of 96 meant that a device independent pixel (or DIP) mapped 1:1 with a physical pixel.</span></span> <span data-ttu-id="5e965-136">Например, если значение DPI \* равно 96 2 = 192, то один DIP будет охватывать два физических пикселя.</span><span class="sxs-lookup"><span data-stu-id="5e965-136">For example, if the DPI were 96\*2 = 192, then a single DIP would encompass two physical pixels.</span></span>

<span data-ttu-id="5e965-137">Существует множество причин, по которым приложения не обязательно правильно обрабатывают такое масштабирование. одной из простейших причин является то, что для обнаружения и использования этого скалярного значения при подготовке к просмотру требуется дополнительный объем работы.</span><span class="sxs-lookup"><span data-stu-id="5e965-137">There are many reasons why applications don't necessarily handle this scaling correctly; one of the simplest reasons is that it requires extra work to discover and use this scalar value when rendering.</span></span> <span data-ttu-id="5e965-138">В Direct2D масштабирование применяется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5e965-138">In Direct2D, the scaling is applied by default.</span></span> <span data-ttu-id="5e965-139">Из-за этого сопоставления пикселы физического устройства могут оказаться в дробных координатах DIP, что является одной из причин того, почему Direct2D использует координатное пространство с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="5e965-139">Because of this mapping, physical device pixels might end up at fractional DIP coordinates, which is one of the reasons why Direct2D uses a floating-point coordinate space.</span></span>

<dl> <span data-ttu-id="5e965-140">физический пиксель = (DIP x DPI)/96</span><span class="sxs-lookup"><span data-stu-id="5e965-140">physical pixel = (dip × DPI) / 96</span></span>  
</dl>

<span data-ttu-id="5e965-141">Чтобы преобразовать физическую точку в DIP, используйте следующую формулу:</span><span class="sxs-lookup"><span data-stu-id="5e965-141">To convert a physical pixel to a DIP, use this formula:</span></span>

<dl> <span data-ttu-id="5e965-142">DIP = (физический пиксель × 96)/DPI</span><span class="sxs-lookup"><span data-stu-id="5e965-142">dip = (physical pixel × 96) / DPI</span></span>  
</dl>

> [!Note]
>
> <span data-ttu-id="5e965-143">Начиная с Windows 8, можно переключить режим единицы измерения на Пиксели вместо DIP с помощью метода [**ID2D1DeviceContext:: сетунитмоде**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) .</span><span class="sxs-lookup"><span data-stu-id="5e965-143">Starting with Windows 8, you can switch the unit mode to pixels instead of DIPs using the [**ID2D1DeviceContext::SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) method.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5e965-144">См. также</span><span class="sxs-lookup"><span data-stu-id="5e965-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e965-145">Как обеспечить правильное отображение приложения на дисплеях с высоким разрешением</span><span class="sxs-lookup"><span data-stu-id="5e965-145">How to Ensure That Your Application Displays Properly on High-DPI Displays</span></span>](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 