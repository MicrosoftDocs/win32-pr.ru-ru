---
title: Дополнительные функции для использования вне контекста устройства
description: Эти функции предоставляют расширенные возможности управления цветом за пределами контекстов устройств.
ms.assetid: 2f742743-094a-44b8-816b-24246607caeb
keywords:
- Цветовая система Windows (WCS), функции
- WCS (цветовая система Windows), функции
- Управление цветом изображений, функции
- Управление цветом, функции
- цвета, функции
- Справочник по WCS, функции
- Справочник по WCS, функциям
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04b7afe98f468fd3f580adf3eff145bce3aa1ac
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "105719863"
---
# <a name="advanced-functions-for-use-outside-of-a-device-context"></a><span data-ttu-id="dc42e-110">Дополнительные функции для использования вне контекста устройства</span><span class="sxs-lookup"><span data-stu-id="dc42e-110">Advanced Functions for Use Outside of a Device Context</span></span>

<span data-ttu-id="dc42e-111">Эти функции предоставляют расширенные возможности управления цветом за пределами контекстов устройств.</span><span class="sxs-lookup"><span data-stu-id="dc42e-111">These functions provide advanced color management capabilities outside of device contexts.</span></span>



| <span data-ttu-id="dc42e-112">Функция</span><span class="sxs-lookup"><span data-stu-id="dc42e-112">Function</span></span>                                                           | <span data-ttu-id="dc42e-113">Описание</span><span class="sxs-lookup"><span data-stu-id="dc42e-113">Description</span></span>                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc42e-114">**пкмскаллбаккв**</span><span class="sxs-lookup"><span data-stu-id="dc42e-114">**PCMSCALLBACKW**</span></span>](/windows/win32/api/icm/nc-icm-pcmscallbackw) | <span data-ttu-id="dc42e-115">\**Пкмскаллбаккв*\* (или **аппликаллбаккфунктион**) — это функция обратного вызова, которая обновляет данные конфигурации WCS во время выполнения диалогового окна, отображаемого функцией [**сетупколорматчингв**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) .</span><span class="sxs-lookup"><span data-stu-id="dc42e-115">\**PCMSCALLBACKW*\* (or **ApplyCallbackFunction**) is a callback function that you implement that updates the WCS configuration data while the dialog box displayed by the [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) function is executing.</span></span> |
| [<span data-ttu-id="dc42e-116">**чеккбитмапбитс**</span><span class="sxs-lookup"><span data-stu-id="dc42e-116">**CheckBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-checkbitmapbits) | <span data-ttu-id="dc42e-117">Проверяет, попадает ли пиксел указанного растрового изображения в выходной [диапазон](g.md) указанного преобразования.</span><span class="sxs-lookup"><span data-stu-id="dc42e-117">Checks whether the pixels in a specified bitmap lie within the output [gamut](g.md) of a specified transform.</span></span> |
| [<span data-ttu-id="dc42e-118">**чеккколорс**</span><span class="sxs-lookup"><span data-stu-id="dc42e-118">**CheckColors**</span></span>](/windows/win32/api/icm/nf-icm-checkbitmapbits) | <span data-ttu-id="dc42e-119">Определяет, находятся ли цвета в массиве [в выходном](g.md) диапазоне указанного преобразования.</span><span class="sxs-lookup"><span data-stu-id="dc42e-119">Determines whether the colors in an array lie within the output [gamut](g.md) of a specified transform.</span></span> |
| [<span data-ttu-id="dc42e-120">**конвертколорнаметоиндекс**</span><span class="sxs-lookup"><span data-stu-id="dc42e-120">**ConvertColorNameToIndex**</span></span>](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | <span data-ttu-id="dc42e-121">Преобразует имена цветов в именованном пространстве для индексации чисел в профиле по цвету ICC.</span><span class="sxs-lookup"><span data-stu-id="dc42e-121">Converts color names in a named color space to index numbers in an International Color Consortium (ICC) color profile.</span></span> |
| [<span data-ttu-id="dc42e-122">**конвертиндекстоколорнаме**</span><span class="sxs-lookup"><span data-stu-id="dc42e-122">**ConvertIndexToColorName**</span></span>](/windows/win32/api/icm/nf-icm-convertindextocolorname) | <span data-ttu-id="dc42e-123">Преобразует индексы в цветовом пространстве в массив имен в именованном цветовом пространстве.</span><span class="sxs-lookup"><span data-stu-id="dc42e-123">Transforms indices in a color space to an array of names in a named color space.</span></span> |
| [<span data-ttu-id="dc42e-124">**креатеколортрансформв**</span><span class="sxs-lookup"><span data-stu-id="dc42e-124">**CreateColorTransformW**</span></span>](/windows/win32/api/icm/nf-icm-createcolortransformw) | <span data-ttu-id="dc42e-125">Преобразует индексы в цветовом пространстве в массив имен в именованном цветовом пространстве.</span><span class="sxs-lookup"><span data-stu-id="dc42e-125">Transforms indices in a color space to an array of names in a named color space.</span></span> |
| [<span data-ttu-id="dc42e-126">**креатемултипрофилетрансформ**</span><span class="sxs-lookup"><span data-stu-id="dc42e-126">**CreateMultiProfileTransform**</span></span>](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | <span data-ttu-id="dc42e-127">Принимает массив профилей или один [профиль связи устройства](d.md) и создает цветное преобразование, которое приложения могут использовать для выполнения сопоставления цветов.</span><span class="sxs-lookup"><span data-stu-id="dc42e-127">Accepts an array of profiles or a single [device link profile](d.md) and creates a color transform that applications can use to perform color mapping.</span></span> |
| [<span data-ttu-id="dc42e-128">**делетеколортрансформ**</span><span class="sxs-lookup"><span data-stu-id="dc42e-128">**DeleteColorTransform**</span></span>](/windows/win32/api/icm/nf-icm-deletecolortransform) | <span data-ttu-id="dc42e-129">Удаляет заданное преобразование цвета.</span><span class="sxs-lookup"><span data-stu-id="dc42e-129">Deletes a given color transform.</span></span> |
| [<span data-ttu-id="dc42e-130">**жеткмминфо**</span><span class="sxs-lookup"><span data-stu-id="dc42e-130">**GetCMMInfo**</span></span>](/windows/win32/api/icm/nf-icm-getcmminfo) | <span data-ttu-id="dc42e-131">Получает различные сведения о модуле управления цветом (CMM), который создал заданное преобразование цвета.</span><span class="sxs-lookup"><span data-stu-id="dc42e-131">Retrieves various information about the color management module (CMM) that created the specified color transform.</span></span> |
| [<span data-ttu-id="dc42e-132">**жетнамедпрофилеинфо**</span><span class="sxs-lookup"><span data-stu-id="dc42e-132">**GetNamedProfileInfo**</span></span>](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | <span data-ttu-id="dc42e-133">Извлекает сведения о цветном профиле ICC, который указан в первом параметре.</span><span class="sxs-lookup"><span data-stu-id="dc42e-133">Retrieves information about the International Color Consortium (ICC) named color profile that is specified in the first parameter.</span></span> |
| [<span data-ttu-id="dc42e-134">**икмпрогресспроккаллбакк**</span><span class="sxs-lookup"><span data-stu-id="dc42e-134">**ICMProgressProcCallback**</span></span>](icmprogressproccallback.md)         | <span data-ttu-id="dc42e-135">Предоставляемая приложением функция обратного вызова для отчета о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="dc42e-135">Application-supplied callback function to report progress.</span></span> <span data-ttu-id="dc42e-136">Имя этой функции также определяется приложением.</span><span class="sxs-lookup"><span data-stu-id="dc42e-136">The name of this function is also defined by the application.</span></span>                                                 |
| [<span data-ttu-id="dc42e-137">**селекткмм**</span><span class="sxs-lookup"><span data-stu-id="dc42e-137">**SelectCMM**</span></span>](/windows/win32/api/icm/nf-icm-selectcmm) | <span data-ttu-id="dc42e-138">Позволяет выбрать предпочтительный модуль управления цветом (CMM) для использования.</span><span class="sxs-lookup"><span data-stu-id="dc42e-138">Allows you to select the preferred color management module (CMM) to use.</span></span> |
| [<span data-ttu-id="dc42e-139">**сетупколорматчингв**</span><span class="sxs-lookup"><span data-stu-id="dc42e-139">**SetupColorMatchingW**</span></span>](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                   | <span data-ttu-id="dc42e-140">Предоставляет пользовательский контроль над управлением цветом с помощью диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="dc42e-140">Provides user control over color management by way of a dialog box.</span></span>                                                                                                      |
| [<span data-ttu-id="dc42e-141">**транслатебитмапбитс**</span><span class="sxs-lookup"><span data-stu-id="dc42e-141">**TranslateBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-translatebitmapbits)                 | <span data-ttu-id="dc42e-142">Преобразует растровые цвета с помощью преобразования цветов.</span><span class="sxs-lookup"><span data-stu-id="dc42e-142">Converts bitmap colors using a color transform.</span></span>                                                                                                                          |
| [<span data-ttu-id="dc42e-143">**транслатеколорс**</span><span class="sxs-lookup"><span data-stu-id="dc42e-143">**TranslateColors**</span></span>](/windows/win32/api/icm/nf-icm-translatecolors) | <span data-ttu-id="dc42e-144">Преобразует массив цветов из исходного [цветового](c.md) пространства в целевое цветовое пространство, определяемое преобразованием цвета.</span><span class="sxs-lookup"><span data-stu-id="dc42e-144">Translates an array of colors from the source [color space](c.md) to the destination color space as defined by a color transform.</span></span> |
| [<span data-ttu-id="dc42e-145">**вксчеккколорс**</span><span class="sxs-lookup"><span data-stu-id="dc42e-145">**WcsCheckColors**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                           | <span data-ttu-id="dc42e-146">Определяет, находятся ли цвета в массиве в выходном диапазоне указанного преобразования цвета WCS.</span><span class="sxs-lookup"><span data-stu-id="dc42e-146">Determines whether the colors in an array are within the output gamut of a specified WCS color transform.</span></span>                                                                |
| [<span data-ttu-id="dc42e-147">**вкстранслатеколорс**</span><span class="sxs-lookup"><span data-stu-id="dc42e-147">**WcsTranslateColors**</span></span>](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | <span data-ttu-id="dc42e-148">Преобразует массив цветов из исходного цветового пространства в целевое цветовое пространство, определяемое преобразованием цвета.</span><span class="sxs-lookup"><span data-stu-id="dc42e-148">Translates an array of colors from the source color space to the destination color space as defined by a color transform.</span></span>                                                |



 

 

 




