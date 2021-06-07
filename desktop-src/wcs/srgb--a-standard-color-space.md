---
title: sRGB — стандартное цветовое пространство
description: В связи с соображениями пропускной способности интернета Hewlett-Packard и Майкрософт предложили внедрение стандартного предопределенного цветового пространства, известного как sRGB (IEC 61966-2-1), чтобы обеспечить точное сопоставление цветов с минимальными издержками на данные.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Цветовая система Windows (WCS), цветовое пространство sRGB
- WCS (цветовая система Windows), цветовое пространство sRGB
- Управление цветом изображений, цветовое пространство sRGB
- Управление цветом, цветовое пространство sRGB
- цвета, цветовое пространство sRGB
- цветовое пространство sRGB
- цветовые пространства, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5d1b2d87cdca5424f8393ae47e592718f33985
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443645"
---
# <a name="srgb-a-standard-color-space"></a><span data-ttu-id="3a936-110">sRGB: стандартное цветовое пространство</span><span class="sxs-lookup"><span data-stu-id="3a936-110">sRGB: A Standard Color Space</span></span>

<span data-ttu-id="3a936-111">В связи с соображениями пропускной способности интернета Hewlett-Packard и Майкрософт предложили внедрение стандартного предопределенного [цветового пространства](c.md) , известного как *sRGB* (IEC 61966-2-1), чтобы обеспечить точное [Сопоставление цветов](c.md) с минимальными издержками на данные.</span><span class="sxs-lookup"><span data-stu-id="3a936-111">As a result of Internet bandwidth considerations, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined [color space](c.md) known as *sRGB* (IEC 61966-2-1), so as to allow accurate [color mapping](c.md) with very little data overhead.</span></span>

<span data-ttu-id="3a936-112">В справочной папке, посвященной техническим параметрам sRGB, sRGB. hlp, можно найти справочную версию технического документа, в которой обсуждаются технические подробности в \\ справочнике по программированию WCS 1,0.</span><span class="sxs-lookup"><span data-stu-id="3a936-112">A help-file version of a white paper discussing the technical details of sRGB, sRGB.hlp, is available in the \\Help folder of the WCS 1.0 Programmer's Reference.</span></span>

<span data-ttu-id="3a936-113">В различных форматах файлов может использоваться или добавляться флаг, указывающий, что изображение находится в цветовом пространстве sRGB.</span><span class="sxs-lookup"><span data-stu-id="3a936-113">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="3a936-114">В формате, не зависящем от устройства Windows (DIB), установка для элемента **bV5CSType** структуры [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) значение **LCS \_ sRGB** указывает, что цвета DIB находятся в цветовом пространстве sRGB.</span><span class="sxs-lookup"><span data-stu-id="3a936-114">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure to **LCS\_sRGB** specifies that the DIB colors are in the sRGB color space.</span></span>

<span data-ttu-id="3a936-115">WCS 1,0 обеспечивает собственную поддержку sRGB.</span><span class="sxs-lookup"><span data-stu-id="3a936-115">WCS 1.0 provides native support for sRGB.</span></span> <span data-ttu-id="3a936-116">Существует два способа использования WCS 1,0 для отрисовки изображения, определенного в цветовом пространстве sRGB:</span><span class="sxs-lookup"><span data-stu-id="3a936-116">There are two ways to use WCS 1.0 for rendering an image defined in the sRGB color space:</span></span>

<span data-ttu-id="3a936-117">**Отрисовка изображения в контексте устройства**</span><span class="sxs-lookup"><span data-stu-id="3a936-117">**To render an image inside the device context**</span></span>

1.  <span data-ttu-id="3a936-118">Создайте контекст устройства (DC) на устройстве вывода.</span><span class="sxs-lookup"><span data-stu-id="3a936-118">Create a device context (DC) on the display device.</span></span>
2.  <span data-ttu-id="3a936-119">Настройте управление цветом с помощью функции [**сетикммоде**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) .</span><span class="sxs-lookup"><span data-stu-id="3a936-119">Set color management using the [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) function.</span></span>
3.  <span data-ttu-id="3a936-120">Используйте функцию [**сетдибитстодевице**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) для перемещения DIB в контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="3a936-120">Use the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function to transfer the DIB into the DC.</span></span> <span data-ttu-id="3a936-121">При условии, что элемент **bV5CSMType** структуры DIB [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) имеет значение **LCS \_ sRGB**, система выполнит соответствующее управление цветом.</span><span class="sxs-lookup"><span data-stu-id="3a936-121">As long as the **bV5CSMType** member of the DIBs [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure is set to **LCS\_sRGB**, the system will perform the appropriate color management.</span></span>

<span data-ttu-id="3a936-122">**Отрисовка изображения вне контекста устройства**</span><span class="sxs-lookup"><span data-stu-id="3a936-122">**To render an image outside the device context**</span></span>

1.  <span data-ttu-id="3a936-123">Создайте преобразование с помощью [**креатеколортрансформв**](/windows/win32/api/icm/nf-icm-createcolortransformw).</span><span class="sxs-lookup"><span data-stu-id="3a936-123">Create a transform using [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw).</span></span> <span data-ttu-id="3a936-124">Элемент **лкскстипе** структуры [**логколорспаце**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) , на который указывает параметр *Плогколорспаце* , должен иметь значение **LCS \_ sRGB**.</span><span class="sxs-lookup"><span data-stu-id="3a936-124">The **lcsCSType** member of the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure pointed to by the *pLogColorSpace* parameter should be set to **LCS\_sRGB**.</span></span> <span data-ttu-id="3a936-125">Параметр *хдестпрофиле* указывает цветовое пространство устройства вывода.</span><span class="sxs-lookup"><span data-stu-id="3a936-125">The *hDestProfile* parameter indicates the display device's color space.</span></span>
2.  <span data-ttu-id="3a936-126">Используйте созданное преобразование цвета для соответствия цвету изображения перед его отображением на устройстве.</span><span class="sxs-lookup"><span data-stu-id="3a936-126">Use the created color transform to color match the image before displaying it on the device.</span></span>

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a><span data-ttu-id="3a936-127">WCS 1,0 значения по умолчанию для цветового пространства ввода и выходного профиля</span><span class="sxs-lookup"><span data-stu-id="3a936-127">WCS 1.0 Defaults for Input Color Space and Output Profile</span></span>

<span data-ttu-id="3a936-128">Если цветовое пространство ввода не указано, по умолчанию WCS 1,0 использует цветовое пространство sRGB в качестве входного цветового пространства для [сопоставления цветов](c.md).</span><span class="sxs-lookup"><span data-stu-id="3a936-128">When no input color space is specified, by default WCS 1.0 uses the sRGB color space as the input color space for [color mapping](c.md).</span></span>

<span data-ttu-id="3a936-129">Если выходной профиль не указан, но задано устройство по умолчанию, WCS 1,0 выбирает выходной профиль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3a936-129">When no output profile is specified, but a default device is specified, WCS 1.0 selects a default output profile.</span></span> <span data-ttu-id="3a936-130">Если у устройства по умолчанию нет связанного профиля, WCS 1,0 использует цветовое пространство sRGB в качестве выходного профиля.</span><span class="sxs-lookup"><span data-stu-id="3a936-130">If the default device does not have an associated profile, WCS 1.0 uses the sRGB color space as the output profile.</span></span>

<span data-ttu-id="3a936-131">В следующей таблице показаны итоговые преобразования цвета, когда устройство по умолчанию недоступно.</span><span class="sxs-lookup"><span data-stu-id="3a936-131">The following table shows the resulting color transforms when a default device is not available.</span></span>



|  &nbsp;                               | <span data-ttu-id="3a936-132">Указанный выходной профиль</span><span class="sxs-lookup"><span data-stu-id="3a936-132">Output Profile Specified</span></span>                              | <span data-ttu-id="3a936-133">Не указан выходной профиль</span><span class="sxs-lookup"><span data-stu-id="3a936-133">Output Profile Not Specified</span></span>                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="3a936-134">Заданное цветовое пространство ввода</span><span class="sxs-lookup"><span data-stu-id="3a936-134">Input Color Space Specified</span></span>     | <span data-ttu-id="3a936-135">Преобразование использует указанные профили.</span><span class="sxs-lookup"><span data-stu-id="3a936-135">Transform uses the specified profiles.</span></span>                | <span data-ttu-id="3a936-136">Преобразование преобразует из известного цветового пространства ввода в sRGB.</span><span class="sxs-lookup"><span data-stu-id="3a936-136">Transform converts from known input color space to sRGB.</span></span> |
| <span data-ttu-id="3a936-137">Не указано цветовое пространство для входных данных</span><span class="sxs-lookup"><span data-stu-id="3a936-137">Input Color Space Not Specified</span></span> | <span data-ttu-id="3a936-138">Преобразование преобразует из sRGB в известный выходной профиль.</span><span class="sxs-lookup"><span data-stu-id="3a936-138">Transform converts from sRGB to known output profile.</span></span> | <span data-ttu-id="3a936-139">Предполагается преобразование из sRGB в sRGB. ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="3a936-139">Transform from sRGB to sRGB is assumed; nothing is done.</span></span> |



 

## <a name="srgb-and-embedded-profiles"></a><span data-ttu-id="3a936-140">Профили sRGB и Embedded</span><span class="sxs-lookup"><span data-stu-id="3a936-140">sRGB and Embedded Profiles</span></span>

<span data-ttu-id="3a936-141">Начиная с ICM версии 2,0, приложения, использующие WCS, могут внедрять профили в изображения.</span><span class="sxs-lookup"><span data-stu-id="3a936-141">Beginning with ICM version 2.0, applications that utilize WCS can embed profiles in images.</span></span> <span data-ttu-id="3a936-142">Внедренные профили помогают приложениям пользователей поддерживать единообразный внешний вид цвета, даже если изображения передаются через Интернет.</span><span class="sxs-lookup"><span data-stu-id="3a936-142">Embedded profiles assist users' applications in maintaining a consistent color appearance even if images are transmitted across the Internet.</span></span>

<span data-ttu-id="3a936-143">Для изображений, использующих цветовое пространство sRGB, встроенный цветовой профиль не требуется.</span><span class="sxs-lookup"><span data-stu-id="3a936-143">Images that use the sRGB color space do not need an embedded color profile.</span></span> <span data-ttu-id="3a936-144">Так как у них нет встроенного профиля, изображения на основе sRGB меньше и более легко передаются по каналам данных с ограниченной пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="3a936-144">Because they have no embedded profile, sRGB-based images are smaller and more readily transferable across data channels with limited bandwidth.</span></span>

<span data-ttu-id="3a936-145">Приложения должны установить флаг **LCS \_ sRGB** в заголовке точечного рисунка изображения, чтобы указать, что изображение использует цветовое пространство sRGB.</span><span class="sxs-lookup"><span data-stu-id="3a936-145">Applications should set the **LCS\_sRGB** flag in the image's bitmap header to indicate that the image uses the sRGB color space.</span></span> <span data-ttu-id="3a936-146">Дополнительные сведения см. в разделе [структуры заголовков битовых карт Windows](using-structures-in-wcs-1-0.md) и [**логколорспаце**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span><span class="sxs-lookup"><span data-stu-id="3a936-146">For details, see [Windows Bitmap Header Structures](using-structures-in-wcs-1-0.md) and [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span></span>

 

 