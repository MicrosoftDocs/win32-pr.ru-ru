---
title: Воздействие на компенсацию DPI
description: Используйте результат компенсации коэффициента DPI для автоматической корректировки входного точечного рисунка в соответствии с DPI контекста. Это полезно в ситуациях, когда точечный рисунок создается или загружается на разные DPI, чем на экране.
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a0477d2a57f39738fa9b1ce16c97995c60cf96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892774"
---
# <a name="dpi-compensation-effect"></a><span data-ttu-id="04c00-104">Воздействие на компенсацию DPI</span><span class="sxs-lookup"><span data-stu-id="04c00-104">DPI compensation effect</span></span>

<span data-ttu-id="04c00-105">Используйте результат компенсации коэффициента DPI для автоматической корректировки входного точечного рисунка в соответствии с DPI контекста.</span><span class="sxs-lookup"><span data-stu-id="04c00-105">Use the DPI compensation effect to automatically adjust an input bitmap to match the DPI of the context.</span></span> <span data-ttu-id="04c00-106">Это полезно в ситуациях, когда точечный рисунок создается или загружается на разные DPI, чем на экране.</span><span class="sxs-lookup"><span data-stu-id="04c00-106">This is useful for situations where a bitmap is created or loaded at a different DPI than the screen.</span></span>

<span data-ttu-id="04c00-107">Идентификатором CLSID для этого действия является CLSID \_ D2D1DpiCompensation.</span><span class="sxs-lookup"><span data-stu-id="04c00-107">The CLSID for this effect is CLSID\_D2D1DpiCompensation.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="04c00-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="04c00-108">Effect properties</span></span>



| <span data-ttu-id="04c00-109">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="04c00-109">Display name and index enumeration</span></span>                                                       | <span data-ttu-id="04c00-110">Описание</span><span class="sxs-lookup"><span data-stu-id="04c00-110">Description</span></span>                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04c00-111">интерполатионмоде</span><span class="sxs-lookup"><span data-stu-id="04c00-111">InterpolationMode</span></span><br/> <span data-ttu-id="04c00-112">\_ \_ \_ Режим интерполяции D2D1 дпикомпенсатион Prop \_</span><span class="sxs-lookup"><span data-stu-id="04c00-112">D2D1\_DPICOMPENSATION\_PROP\_INTERPOLATION\_MODE</span></span><br/> | <span data-ttu-id="04c00-113">Режим интерполяции, который применяется для масштабирования изображения.</span><span class="sxs-lookup"><span data-stu-id="04c00-113">The interpolation mode the effect uses to scale the image.</span></span><br/> <span data-ttu-id="04c00-114">Тип — D2D1 \_ дпикомпенсатион \_ Режим интерполяции \_ .</span><span class="sxs-lookup"><span data-stu-id="04c00-114">The type is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE.</span></span><br/> <span data-ttu-id="04c00-115">Значение по умолчанию — D2D1 \_ дпикомпенсатион \_ Режим интерполяции \_ \_ линейный.</span><span class="sxs-lookup"><span data-stu-id="04c00-115">The default value is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR .</span></span><br/>                  |
| <span data-ttu-id="04c00-116">бордермоде</span><span class="sxs-lookup"><span data-stu-id="04c00-116">BorderMode</span></span><br/> <span data-ttu-id="04c00-117">\_Режим границы D2D1 дпикомпенсатион " \_ prop" \_ \_</span><span class="sxs-lookup"><span data-stu-id="04c00-117">D2D1\_DPICOMPENSATION\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="04c00-118">Режим, используемый для вычисления границы изображения: Soft или Hard.</span><span class="sxs-lookup"><span data-stu-id="04c00-118">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="04c00-119">Дополнительные сведения см. в разделе [режимы границ](https://www.bing.com/search?q=Border+modes) .</span><span class="sxs-lookup"><span data-stu-id="04c00-119">See [Border modes](https://www.bing.com/search?q=Border+modes) for more info.</span></span> <br/> <span data-ttu-id="04c00-120">Тип — D2D1 \_ границы \_ .</span><span class="sxs-lookup"><span data-stu-id="04c00-120">The type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="04c00-121">Значение по умолчанию — D2D1 \_ границы \_ режима \_ Soft.</span><span class="sxs-lookup"><span data-stu-id="04c00-121">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/> |
| <span data-ttu-id="04c00-122">инпутдпи</span><span class="sxs-lookup"><span data-stu-id="04c00-122">InputDpi</span></span><br/> <span data-ttu-id="04c00-123">D2D1 \_ дпикомпенсатион \_ prop \_ Ввод \_ dpi</span><span class="sxs-lookup"><span data-stu-id="04c00-123">D2D1\_DPICOMPENSATION\_PROP\_INPUT\_DPI</span></span><br/>                   | <span data-ttu-id="04c00-124">Значение DPI для входного изображения.</span><span class="sxs-lookup"><span data-stu-id="04c00-124">The DPI of the input image.</span></span><br/> <span data-ttu-id="04c00-125">Тип — FLOAT.</span><span class="sxs-lookup"><span data-stu-id="04c00-125">The type is FLOAT.</span></span><br/> <span data-ttu-id="04c00-126">Значение по умолчанию — 96.0 f.</span><span class="sxs-lookup"><span data-stu-id="04c00-126">The default value is 96.0f.</span></span><br/>                                                                                                                                    |



 

## <a name="interpolation-modes"></a><span data-ttu-id="04c00-127">Режимы интерполяции</span><span class="sxs-lookup"><span data-stu-id="04c00-127">Interpolation modes</span></span>



| <span data-ttu-id="04c00-128">Перечисление</span><span class="sxs-lookup"><span data-stu-id="04c00-128">Enumeration</span></span>                                                       | <span data-ttu-id="04c00-129">Описание</span><span class="sxs-lookup"><span data-stu-id="04c00-129">Description</span></span>                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04c00-130">\_ \_ \_ \_ Ближайший сосед в режиме интерполяции D2D1 дпикомпенсатион \_</span><span class="sxs-lookup"><span data-stu-id="04c00-130">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="04c00-131">Выбирает ближайшую одиночную точку и использует ее.</span><span class="sxs-lookup"><span data-stu-id="04c00-131">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="04c00-132">В этом режиме используется меньше времени на обработку, но выводится изображение самого низкого качества.</span><span class="sxs-lookup"><span data-stu-id="04c00-132">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="04c00-133">\_ \_ Линейный режим интерполяции D2D1 дпикомпенсатион \_ \_</span><span class="sxs-lookup"><span data-stu-id="04c00-133">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="04c00-134">Использует выборку с четырьмя точками и линейную интерполяцию.</span><span class="sxs-lookup"><span data-stu-id="04c00-134">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="04c00-135">Этот режим использует больше времени на обработку, чем ближайший соседний режим, но выводит изображение более высокого качества.</span><span class="sxs-lookup"><span data-stu-id="04c00-135">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="04c00-136">D2D1 \_ дпикомпенсатион \_ Режим интерполяции ( \_ \_ кубический)</span><span class="sxs-lookup"><span data-stu-id="04c00-136">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="04c00-137">Использует 16-примерный ядро кубических для интерполяции.</span><span class="sxs-lookup"><span data-stu-id="04c00-137">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="04c00-138">Этот режим использует наибольшее время обработки, но выводит изображение с более высоким качеством.</span><span class="sxs-lookup"><span data-stu-id="04c00-138">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="04c00-139">D2D1 \_ дпикомпенсатион \_ Режим интерполяции — \_ \_ \_ многопримерная \_ линейная</span><span class="sxs-lookup"><span data-stu-id="04c00-139">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="04c00-140">Использует 4 линейных образца в пределах одного пикселя для удобного сглаживания.</span><span class="sxs-lookup"><span data-stu-id="04c00-140">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="04c00-141">Этот режим хорошо подходит для уменьшения масштаба по небольшим объемам на изображениях с небольшими пикселями.</span><span class="sxs-lookup"><span data-stu-id="04c00-141">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="04c00-142">D2D1 \_ дпикомпенсатион \_ Режим интерполяции — \_ \_ анизотропная</span><span class="sxs-lookup"><span data-stu-id="04c00-142">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="04c00-143">Использует анизотропную фильтрацию для выборки шаблона в соответствии с преобразованной формой точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="04c00-143">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="04c00-144">D2D1 \_ дпикомпенсатион \_ \_ Режим интерполяции \_ высокого \_ качества, \_ кубический</span><span class="sxs-lookup"><span data-stu-id="04c00-144">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="04c00-145">Использует высококачественное ядро кубического размера для выполнения предварительно довнскале образа, если довнскалинг участвует в матрице преобразования.</span><span class="sxs-lookup"><span data-stu-id="04c00-145">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="04c00-146">Затем использует режим интерполяции кубических для окончательного вывода.</span><span class="sxs-lookup"><span data-stu-id="04c00-146">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="04c00-147">Если не выбрать режим, то по умолчанию будет применяться \_ \_ линейный режим интерполяции D2D1 дпикомпенстион \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="04c00-147">If you don't select a mode, the effect defaults to D2D1\_DPICOMPENSTION\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

## <a name="border-modes"></a><span data-ttu-id="04c00-148">Режимы границ</span><span class="sxs-lookup"><span data-stu-id="04c00-148">Border modes</span></span>



| <span data-ttu-id="04c00-149">Имя</span><span class="sxs-lookup"><span data-stu-id="04c00-149">Name</span></span>                     | <span data-ttu-id="04c00-150">Описание</span><span class="sxs-lookup"><span data-stu-id="04c00-150">Description</span></span>                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04c00-151">\_ \_ Мягкий режим границы \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="04c00-151">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="04c00-152">Пиксели за пределами входных границ создаются [зеркальной границей](border.md).</span><span class="sxs-lookup"><span data-stu-id="04c00-152">Pixels outside of the input boundaries are generated by the [mirror border effect](border.md).</span></span> <br/> |
| <span data-ttu-id="04c00-153">Жесткое D2D1 в \_ \_ режиме границы \_</span><span class="sxs-lookup"><span data-stu-id="04c00-153">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="04c00-154">Пиксели за пределами входных границ имеют прозрачный черный цвет.</span><span class="sxs-lookup"><span data-stu-id="04c00-154">Pixels outside of the input boundaries are transparent black.</span></span><br/>                                    |



 

## <a name="requirements"></a><span data-ttu-id="04c00-155">Требования</span><span class="sxs-lookup"><span data-stu-id="04c00-155">Requirements</span></span>



| <span data-ttu-id="04c00-156">Требование</span><span class="sxs-lookup"><span data-stu-id="04c00-156">Requirement</span></span> | <span data-ttu-id="04c00-157">Значение</span><span class="sxs-lookup"><span data-stu-id="04c00-157">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04c00-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04c00-158">Minimum supported client</span></span> | <span data-ttu-id="04c00-159">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="04c00-159">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="04c00-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04c00-160">Minimum supported server</span></span> | <span data-ttu-id="04c00-161">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="04c00-161">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="04c00-162">Header</span><span class="sxs-lookup"><span data-stu-id="04c00-162">Header</span></span>                   | <span data-ttu-id="04c00-163">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="04c00-163">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="04c00-164">Библиотека</span><span class="sxs-lookup"><span data-stu-id="04c00-164">Library</span></span>                  | <span data-ttu-id="04c00-165">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="04c00-165">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="04c00-166">См. также</span><span class="sxs-lookup"><span data-stu-id="04c00-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04c00-167">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="04c00-167">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

