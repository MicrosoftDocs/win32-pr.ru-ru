---
title: Эффекты управления цветом
description: Используйте эффекты управления цветом для преобразования изображения из одного цветового профиля ICC (Международный цветовой консорциум) в другой. Этот результат преобразует изображение в соответствии со спецификацией ICC.
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- эффекты управления цветом
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 5f3783132e0e2af511a99fd8c44d5f899e577a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415373"
---
# <a name="color-management-effect"></a><span data-ttu-id="458fd-105">Эффекты управления цветом</span><span class="sxs-lookup"><span data-stu-id="458fd-105">Color management effect</span></span>

<span data-ttu-id="458fd-106">Используйте эффекты управления цветом для преобразования изображения из одного цветового профиля ICC (Международный цветовой консорциум) в другой.</span><span class="sxs-lookup"><span data-stu-id="458fd-106">Use the color management effect to transform an image from one ICC (International Color Consortium) color profile to another.</span></span> <span data-ttu-id="458fd-107">Этот результат преобразует изображение в соответствии со [спецификацией ICC](https://www.color.org).</span><span class="sxs-lookup"><span data-stu-id="458fd-107">The effect transforms the image according to the [ICC specification](https://www.color.org).</span></span>

<span data-ttu-id="458fd-108">Идентификатором CLSID для этого действия является CLSID \_ D2D1ColorManagement.</span><span class="sxs-lookup"><span data-stu-id="458fd-108">The CLSID for this effect is CLSID\_D2D1ColorManagement.</span></span>

- [<span data-ttu-id="458fd-109">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="458fd-109">Effect properties</span></span>](#effect-properties)
- [<span data-ttu-id="458fd-110">Режимы намерения отрисовки</span><span class="sxs-lookup"><span data-stu-id="458fd-110">Rendering intent modes</span></span>](#rendering-intent-modes)
- [<span data-ttu-id="458fd-111">Режимы альфа-канала входного изображения</span><span class="sxs-lookup"><span data-stu-id="458fd-111">Input image alpha modes</span></span>](#input-image-alpha-modes)
- [<span data-ttu-id="458fd-112">Соответствие спецификации ICC</span><span class="sxs-lookup"><span data-stu-id="458fd-112">Compliance with ICC specification</span></span>](#compliance-with-icc-specification)
- [<span data-ttu-id="458fd-113">Поведение альфа-канала</span><span class="sxs-lookup"><span data-stu-id="458fd-113">Alpha channel behavior</span></span>](#alpha-channel-behavior)
- [<span data-ttu-id="458fd-114">Режимы качества</span><span class="sxs-lookup"><span data-stu-id="458fd-114">Quality modes</span></span>](#quality-modes)
- [<span data-ttu-id="458fd-115">Образец кода</span><span class="sxs-lookup"><span data-stu-id="458fd-115">Sample code</span></span>](#sample-code)
- [<span data-ttu-id="458fd-116">Требования</span><span class="sxs-lookup"><span data-stu-id="458fd-116">Requirements</span></span>](#requirements)
- [<span data-ttu-id="458fd-117">См. также</span><span class="sxs-lookup"><span data-stu-id="458fd-117">Related topics</span></span>](#related-topics)

## <a name="effect-properties"></a><span data-ttu-id="458fd-118">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="458fd-118">Effect properties</span></span>

| <span data-ttu-id="458fd-119">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="458fd-119">Display name and index enumeration</span></span> | <span data-ttu-id="458fd-120">Описание</span><span class="sxs-lookup"><span data-stu-id="458fd-120">Description</span></span> |
|-|-|
| <span data-ttu-id="458fd-121">SourceContext</span><span class="sxs-lookup"><span data-stu-id="458fd-121">SourceContext</span></span><br/> <span data-ttu-id="458fd-122">\_ \_ \_ \_ Контекст цвета источника D2D1 колорманажемент \_</span><span class="sxs-lookup"><span data-stu-id="458fd-122">D2D1\_COLORMANAGEMENT\_PROP\_SOURCE\_COLOR\_CONTEXT</span></span><br/> | <span data-ttu-id="458fd-123">Сведения об исходном цветовом пространстве.</span><span class="sxs-lookup"><span data-stu-id="458fd-123">The source color space information.</span></span> <span data-ttu-id="458fd-124">Тип — [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span><span class="sxs-lookup"><span data-stu-id="458fd-124">The type is [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span></span><br/> <span data-ttu-id="458fd-125">Значение по умолчанию — NULL.</span><span class="sxs-lookup"><span data-stu-id="458fd-125">The default value is NULL.</span></span><br/> |
| <span data-ttu-id="458fd-126">саурцеинтент</span><span class="sxs-lookup"><span data-stu-id="458fd-126">SourceIntent</span></span><br/> <span data-ttu-id="458fd-127">D2D1 \_ колорманажемент \_ , \_ \_ Цель визуализации \_ источника</span><span class="sxs-lookup"><span data-stu-id="458fd-127">D2D1\_COLORMANAGEMENT\_PROP\_SOURCE\_RENDERING\_INTENT</span></span><br/> | <span data-ttu-id="458fd-128">Какую цель визуализации ICC использовать.</span><span class="sxs-lookup"><span data-stu-id="458fd-128">Which ICC rendering intent to use.</span></span> <span data-ttu-id="458fd-129">Тип — D2D1 \_ колорманажемент \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="458fd-129">The type is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT.</span></span><br/> <span data-ttu-id="458fd-130">Значение по умолчанию — D2D1 \_ колорманажемент с \_ намерением подготовки к просмотру \_ \_ искусственного.</span><span class="sxs-lookup"><span data-stu-id="458fd-130">The default value is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL.</span></span><br/> |
| <span data-ttu-id="458fd-131">дестинатионконтекст</span><span class="sxs-lookup"><span data-stu-id="458fd-131">DestinationContext</span></span><br/> <span data-ttu-id="458fd-132">\_ \_ \_ Контекст целевого цвета назначения \_ \_ D2D1 колорманажемент</span><span class="sxs-lookup"><span data-stu-id="458fd-132">D2D1\_COLORMANAGEMENT\_PROP\_DESTINATION\_COLOR\_CONTEXT</span></span><br/> | <span data-ttu-id="458fd-133">Сведения о цветовом пространстве назначения.</span><span class="sxs-lookup"><span data-stu-id="458fd-133">The destination color space information.</span></span> <span data-ttu-id="458fd-134">Тип — [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span><span class="sxs-lookup"><span data-stu-id="458fd-134">The type is [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span></span><br/> <span data-ttu-id="458fd-135">Значение по умолчанию — NULL.</span><span class="sxs-lookup"><span data-stu-id="458fd-135">The default value is NULL.</span></span><br/> |
| <span data-ttu-id="458fd-136">дестинатионинтент</span><span class="sxs-lookup"><span data-stu-id="458fd-136">DestinationIntent</span></span><br/> <span data-ttu-id="458fd-137">\_ \_ \_ \_ Цель визуализации назначения D2D1 колорманажемент \_</span><span class="sxs-lookup"><span data-stu-id="458fd-137">D2D1\_COLORMANAGEMENT\_PROP\_DESTINATION\_RENDERING\_INTENT</span></span><br/> | <span data-ttu-id="458fd-138">Какую цель визуализации ICC использовать.</span><span class="sxs-lookup"><span data-stu-id="458fd-138">Which ICC rendering intent to use.</span></span> <span data-ttu-id="458fd-139">Тип — D2D1 \_ колорманажемент \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="458fd-139">The type is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT.</span></span><br/> <span data-ttu-id="458fd-140">Значение по умолчанию — D2D1 \_ колорманажемент с \_ намерением подготовки к просмотру \_ \_ искусственного.</span><span class="sxs-lookup"><span data-stu-id="458fd-140">The default value is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL.</span></span><br/> |
| <span data-ttu-id="458fd-141">алфамоде</span><span class="sxs-lookup"><span data-stu-id="458fd-141">AlphaMode</span></span><br/> <span data-ttu-id="458fd-142">D2D1 \_ колорманажемент \_ prop \_ , \_ режим альфа</span><span class="sxs-lookup"><span data-stu-id="458fd-142">D2D1\_COLORMANAGEMENT\_PROP\_ALPHA\_MODE</span></span><br/> | <span data-ttu-id="458fd-143">Способ интерпретации альфа-данных, содержащихся во входном изображении.</span><span class="sxs-lookup"><span data-stu-id="458fd-143">How to interpret alpha data that is contained in the input image.</span></span> <span data-ttu-id="458fd-144">Тип — D2D1 \_ колорманажемент \_ Alpha \_ mode.</span><span class="sxs-lookup"><span data-stu-id="458fd-144">The type is D2D1\_COLORMANAGEMENT\_ALPHA\_MODE.</span></span><br/> <span data-ttu-id="458fd-145">Значение по умолчанию — D2D1 колорманажемент Alpha с предварительным \_ \_ \_ \_ умножением.</span><span class="sxs-lookup"><span data-stu-id="458fd-145">The default value is D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_PREMULTIPLIED.</span></span><br/> |
| <span data-ttu-id="458fd-146">Качество</span><span class="sxs-lookup"><span data-stu-id="458fd-146">Quality</span></span><br/> <span data-ttu-id="458fd-147">D2D1 \_ колорманажемент \_ prop \_ Quality</span><span class="sxs-lookup"><span data-stu-id="458fd-147">D2D1\_COLORMANAGEMENT\_PROP\_QUALITY</span></span><br/> | <span data-ttu-id="458fd-148">Уровень качества преобразования.</span><span class="sxs-lookup"><span data-stu-id="458fd-148">The quality level of the transform.</span></span> <span data-ttu-id="458fd-149">Тип — D2D1 \_ колорманажемент \_ Quality.</span><span class="sxs-lookup"><span data-stu-id="458fd-149">The type is D2D1\_COLORMANAGEMENT\_QUALITY.</span></span><br/> <span data-ttu-id="458fd-150">Значение по умолчанию — D2D1 \_ колорманажемент \_ Quality ( \_ нормальное качество).</span><span class="sxs-lookup"><span data-stu-id="458fd-150">The default value is D2D1\_COLORMANAGEMENT\_QUALITY\_NORMAL.</span></span><br/> |

## <a name="rendering-intent-modes"></a><span data-ttu-id="458fd-151">Режимы намерения отрисовки</span><span class="sxs-lookup"><span data-stu-id="458fd-151">Rendering intent modes</span></span>

| <span data-ttu-id="458fd-152">Перечисление</span><span class="sxs-lookup"><span data-stu-id="458fd-152">Enumeration</span></span> | <span data-ttu-id="458fd-153">Описание</span><span class="sxs-lookup"><span data-stu-id="458fd-153">Description</span></span> |
|-|-|
| <span data-ttu-id="458fd-154">D2D1 \_ колорманажемент с \_ намерением подготовки к просмотру \_ \_ искусственного</span><span class="sxs-lookup"><span data-stu-id="458fd-154">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL</span></span> | <span data-ttu-id="458fd-155">Этот действие сжимает или развертывает полный цветовой охват изображения, чтобы заполнить цветовую гамму устройства, чтобы сохранить серый баланс, но точность изображения не может быть сохранена.</span><span class="sxs-lookup"><span data-stu-id="458fd-155">The effect compresses or expands the full color gamut of the image to fill the color gamut of the device, so that gray balance is preserved but colorimetric accuracy may not be preserved.</span></span> |
| <span data-ttu-id="458fd-156">D2D1 \_ колорманажемент, \_ Цель рендеринга — \_ \_ Относительный \_</span><span class="sxs-lookup"><span data-stu-id="458fd-156">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_RELATIVE\_COLORIMETRIC</span></span> | <span data-ttu-id="458fd-157">Этот результат сохраняет чрома цветов в изображении с возможностью оттенок и яркости.</span><span class="sxs-lookup"><span data-stu-id="458fd-157">The effect preserves the chroma of colors in the image at the possible expense of hue and lightness.</span></span> |
| <span data-ttu-id="458fd-158">D2D1 \_ колорманажемент \_ , \_ насыщенность с намерением визуализации \_</span><span class="sxs-lookup"><span data-stu-id="458fd-158">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_SATURATION</span></span> | <span data-ttu-id="458fd-159">Этот результат корректирует цвета, которые выходят за пределы диапазона цветов, отображаемых устройством вывода, до ближайшего доступного цвета.</span><span class="sxs-lookup"><span data-stu-id="458fd-159">The effect adjusts colors that fall outside the range of colors the output device renders to the closest color available.</span></span> <span data-ttu-id="458fd-160">Он не сохраняет белую точку.</span><span class="sxs-lookup"><span data-stu-id="458fd-160">It does not preserve the white point.</span></span> |
| <span data-ttu-id="458fd-161">\_ \_ Цель отрисовки D2D1 колорманажемент — \_ \_ Абсолютная \_</span><span class="sxs-lookup"><span data-stu-id="458fd-161">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_ABSOLUTE\_COLORIMETRIC</span></span> | <span data-ttu-id="458fd-162">Этот результат корректирует все цвета, которые выходят за пределы диапазона, который может быть отображен выходным устройством, до ближайшего к просмотру цвета.</span><span class="sxs-lookup"><span data-stu-id="458fd-162">The effect adjusts any colors that fall outside the range that the output device can render to the closest color that can be rendered.</span></span> <span data-ttu-id="458fd-163">Этот результат не изменяет другие цвета и сохраняет белую точку.</span><span class="sxs-lookup"><span data-stu-id="458fd-163">The effect does not change the other colors and preserves the white point.</span></span> |

## <a name="input-image-alpha-modes"></a><span data-ttu-id="458fd-164">Режимы альфа-канала входного изображения</span><span class="sxs-lookup"><span data-stu-id="458fd-164">Input image alpha modes</span></span>

| <span data-ttu-id="458fd-165">Перечисление</span><span class="sxs-lookup"><span data-stu-id="458fd-165">Enumeration</span></span> | <span data-ttu-id="458fd-166">Описание</span><span class="sxs-lookup"><span data-stu-id="458fd-166">Description</span></span> |
|-|-|
| <span data-ttu-id="458fd-167">Предварительное \_ \_ \_ \_ умножение режима альфа-D2D1 колорманажемент</span><span class="sxs-lookup"><span data-stu-id="458fd-167">D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="458fd-168">Результат предполагает, что предварительно умножается режим альфа.</span><span class="sxs-lookup"><span data-stu-id="458fd-168">The effect assumes the alpha mode is premultiplied.</span></span> |
| <span data-ttu-id="458fd-169">D2D1 \_ колорманажемент \_ Alpha \_ , \_ прямой режим</span><span class="sxs-lookup"><span data-stu-id="458fd-169">D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_STRAIGHT</span></span> | <span data-ttu-id="458fd-170">Результат предполагает, что альфа-канал имеет прямой режим.</span><span class="sxs-lookup"><span data-stu-id="458fd-170">The effect assumes the alpha mode is straight.</span></span> |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a><span data-ttu-id="458fd-171">D2D1_GAMMA1_G2084 изменения поведения</span><span class="sxs-lookup"><span data-stu-id="458fd-171">D2D1_GAMMA1_G2084 behavior changes</span></span>
    
<span data-ttu-id="458fd-172">Если приложение использует [D2D1_GAMMA1_G2084ое](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) пространство или одно из значений перечисления [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) , использующих цветовое пространство SMPTE St. 2084 (искусственного куантизер), приложение будет работать с данными HDR.</span><span class="sxs-lookup"><span data-stu-id="458fd-172">If your application uses the [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) space, or one of the [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) enumeration values that use the SMPTE ST.2084 (Perceptual Quantizer) color space, then the application intends to work with HDR data.</span></span>

<span data-ttu-id="458fd-173">API [**ID2D1DeviceContext5:: креатеколорконтекстфромсимплеколорпрофиле**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) и [**ID2D1DeviceContext5:: креатеколорконтекстфромдксгиколорспаце**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) не учитывается. Вместо этого содержимое HDR масштабируется для размещения в диапазоне 0-1 во время операции деG2084 дегаммы.</span><span class="sxs-lookup"><span data-stu-id="458fd-173">The [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) and [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) APIs don't account for that; rather, the HDR content is scaled to fit in the 0-1 range during the G2084 DeGamma operation.</span></span>

<span data-ttu-id="458fd-174">На практике содержимое, закодированное в этом пространстве гамма, использует ссылку на 10 000 Вхителевел НИТС, который обычно представлен в КККС как 10 000/80 = 125,0.</span><span class="sxs-lookup"><span data-stu-id="458fd-174">In practice, content that is encoded in this gamma space uses a reference WhiteLevel of 10,000 Nits, which would normally be represented in CCCS as 10,000 / 80 = 125.0.</span></span> <span data-ttu-id="458fd-175">Таким образом, чтобы лучше упростить работу с приложением, это простейшее гамма-преобразование также позволяет масштабировать светимость на 125.</span><span class="sxs-lookup"><span data-stu-id="458fd-175">So, to better facilitate your app, it's simplest for this gamma conversion to also scale the luminance by a factor of 125.</span></span> <span data-ttu-id="458fd-176">Начиная с Windows 10, версия 1809 (10,0; Сборка 17763), поведением управления цветом является то, что оно применяет это масштабирование.</span><span class="sxs-lookup"><span data-stu-id="458fd-176">As of Windows 10, version 1809 (10.0; Build 17763), the behavior of the color management effect is such that it applies this scaling.</span></span> <span data-ttu-id="458fd-177">Это означает, что вы, как разработчик, не должны применять второй [цветовой коррекции белого уровня](white-level-adjustment-effect.md) к конвейеру.</span><span class="sxs-lookup"><span data-stu-id="458fd-177">That means that you, as the developer, don't have to apply a second [White level adjustment effect](white-level-adjustment-effect.md) into the pipeline.</span></span>

## <a name="compliance-with-icc-specification"></a><span data-ttu-id="458fd-178">Соответствие спецификации ICC</span><span class="sxs-lookup"><span data-stu-id="458fd-178">Compliance with ICC specification</span></span>

<span data-ttu-id="458fd-179">Результат управления цветом соответствует спецификации ICC версии 4.3 с этими ограничениями:</span><span class="sxs-lookup"><span data-stu-id="458fd-179">The color management effect is compliant with the ICC v4.3 specification, with these limitations:</span></span>

- <span data-ttu-id="458fd-180">Этот результат поддерживает цветовые пространства 1, 3 и 4 канала.</span><span class="sxs-lookup"><span data-stu-id="458fd-180">The effect supports 1, 3, and 4 channel color spaces.</span></span>
- <span data-ttu-id="458fd-181">Этот результат не поддерживает Колорспаце или именованные профили цветов.</span><span class="sxs-lookup"><span data-stu-id="458fd-181">The effect doesn't support ColorSpace or Named Color profiles.</span></span>

## <a name="alpha-channel-behavior"></a><span data-ttu-id="458fd-182">Поведение альфа-канала</span><span class="sxs-lookup"><span data-stu-id="458fd-182">Alpha channel behavior</span></span>

<span data-ttu-id="458fd-183">В целом, если в исходном изображении нет альфа-данных, то в качестве значения альфа-канала устанавливается значение 1 (непрозрачный), а при отсутствии места в целевом изображении данные не удаляются.</span><span class="sxs-lookup"><span data-stu-id="458fd-183">In general, the effect sets alpha to 1 (opaque) if there is no alpha data in the source image and the alpha data is discarded if there is no room in the destination image.</span></span> <span data-ttu-id="458fd-184">В таблице здесь описывается поведение альфа.</span><span class="sxs-lookup"><span data-stu-id="458fd-184">The table here describes the alpha behavior.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="458fd-185">Исходный колорспаце, формат пикселей</span><span class="sxs-lookup"><span data-stu-id="458fd-185">Source colorspace, pixel format</span></span></th>
<th><span data-ttu-id="458fd-186">Целевой колорспаце, формат пикселей</span><span class="sxs-lookup"><span data-stu-id="458fd-186">Destination colorspace, pixel format</span></span></th>
<th><span data-ttu-id="458fd-187">Поведение альфа-канала</span><span class="sxs-lookup"><span data-stu-id="458fd-187">Alpha behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="458fd-188">1 канал, формат пикселей R $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="458fd-188">1 channel, R pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="458fd-189">1 канал, формат пикселей R</span><span class="sxs-lookup"><span data-stu-id="458fd-189">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="458fd-190">(Нет альфа-данных)</span><span class="sxs-lookup"><span data-stu-id="458fd-190">(No alpha data)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="458fd-191">1 канал, формат пикселей RGBA</span><span class="sxs-lookup"><span data-stu-id="458fd-191">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="458fd-192">Для альфа-данных задано значение 1 (непрозрачный)</span><span class="sxs-lookup"><span data-stu-id="458fd-192">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="458fd-193">3 канала, формат пикселей RGBA</span><span class="sxs-lookup"><span data-stu-id="458fd-193">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="458fd-194">Для альфа-данных задано значение 1 (непрозрачный)</span><span class="sxs-lookup"><span data-stu-id="458fd-194">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="458fd-195">4 канала, формат пикселей RGBA</span><span class="sxs-lookup"><span data-stu-id="458fd-195">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="458fd-196">(Нет альфа-данных)</span><span class="sxs-lookup"><span data-stu-id="458fd-196">(No alpha data)</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="458fd-197">1 канал, формат пикселей RGBA $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="458fd-197">1 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="458fd-198">1 канал, формат пикселей R</span><span class="sxs-lookup"><span data-stu-id="458fd-198">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="458fd-199">Данные Alpha отбрасываются</span><span class="sxs-lookup"><span data-stu-id="458fd-199">Alpha data is discarded</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="458fd-200">1 канал, формат пикселей RGBA</span><span class="sxs-lookup"><span data-stu-id="458fd-200">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="458fd-201">Альфа-данные передаются через</span><span class="sxs-lookup"><span data-stu-id="458fd-201">Alpha data is passed through</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="458fd-202">3 канала, формат пикселей RGBA</span><span class="sxs-lookup"><span data-stu-id="458fd-202">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="458fd-203">Альфа-данные передаются через</span><span class="sxs-lookup"><span data-stu-id="458fd-203">Alpha data is passed through</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="458fd-204">4 канала, формат пикселей RGBA</span><span class="sxs-lookup"><span data-stu-id="458fd-204">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="458fd-205">Данные Alpha отбрасываются</span><span class="sxs-lookup"><span data-stu-id="458fd-205">Alpha data is discarded</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="458fd-206">3 канала, формат пикселей RGBA $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="458fd-206">3 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="458fd-207">1 канал, формат пикселей R</span><span class="sxs-lookup"><span data-stu-id="458fd-207">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="458fd-208">Данные Alpha отбрасываются</span><span class="sxs-lookup"><span data-stu-id="458fd-208">Alpha data is discarded</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="458fd-209">1 канал, формат пикселей RGBA</span><span class="sxs-lookup"><span data-stu-id="458fd-209">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="458fd-210">Альфа-данные передаются через</span><span class="sxs-lookup"><span data-stu-id="458fd-210">Alpha data is passed through</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="458fd-211">3 канала, формат пикселей RGBA</span><span class="sxs-lookup"><span data-stu-id="458fd-211">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="458fd-212">Альфа-данные передаются через</span><span class="sxs-lookup"><span data-stu-id="458fd-212">Alpha data is passed through</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="458fd-213">4 канала, формат пикселей RGBA</span><span class="sxs-lookup"><span data-stu-id="458fd-213">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="458fd-214">Данные Alpha отбрасываются</span><span class="sxs-lookup"><span data-stu-id="458fd-214">Alpha data is discarded</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="458fd-215">4 канала, формат пикселей RGBA $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="458fd-215">4 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="458fd-216">1 канал, формат пикселей R</span><span class="sxs-lookup"><span data-stu-id="458fd-216">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="458fd-217">(Нет альфа-данных)</span><span class="sxs-lookup"><span data-stu-id="458fd-217">(No alpha data)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="458fd-218">1 канал, формат пикселей RGBA</span><span class="sxs-lookup"><span data-stu-id="458fd-218">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="458fd-219">Для альфа-данных задано значение 1 (непрозрачный)</span><span class="sxs-lookup"><span data-stu-id="458fd-219">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="458fd-220">3 канала, формат пикселей RGBA</span><span class="sxs-lookup"><span data-stu-id="458fd-220">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="458fd-221">Для альфа-данных задано значение 1 (непрозрачный)</span><span class="sxs-lookup"><span data-stu-id="458fd-221">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="458fd-222">4 канала, формат пикселей RGBA</span><span class="sxs-lookup"><span data-stu-id="458fd-222">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="458fd-223">(Нет альфа-данных)</span><span class="sxs-lookup"><span data-stu-id="458fd-223">(No alpha data)</span></span></td>

</tr>
</tbody>
</table>

## <a name="quality-modes"></a><span data-ttu-id="458fd-224">Режимы качества</span><span class="sxs-lookup"><span data-stu-id="458fd-224">Quality modes</span></span>

| <span data-ttu-id="458fd-225">Режим</span><span class="sxs-lookup"><span data-stu-id="458fd-225">Mode</span></span> | <span data-ttu-id="458fd-226">Описание</span><span class="sxs-lookup"><span data-stu-id="458fd-226">Description</span></span> |
|-|-|
| <span data-ttu-id="458fd-227">D2D1 \_ колорманажемент \_ качество \_</span><span class="sxs-lookup"><span data-stu-id="458fd-227">D2D1\_COLORMANAGEMENT\_QUALITY\_PROOF</span></span> | <span data-ttu-id="458fd-228">Режим наименьшего качества.</span><span class="sxs-lookup"><span data-stu-id="458fd-228">The lowest quality mode.</span></span> <span data-ttu-id="458fd-229">Для этого режима требуется уровень Feature 9 \_ 1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="458fd-229">This mode requires feature level 9\_1 or above.</span></span> |
| <span data-ttu-id="458fd-230">\_ \_ Нормальное качество D2D1 колорманажемент \_</span><span class="sxs-lookup"><span data-stu-id="458fd-230">D2D1\_COLORMANAGEMENT\_QUALITY\_NORMAL</span></span> | <span data-ttu-id="458fd-231">Режим нормального качества.</span><span class="sxs-lookup"><span data-stu-id="458fd-231">Normal quality mode.</span></span> <span data-ttu-id="458fd-232">Для этого режима требуется уровень Feature 9 \_ 1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="458fd-232">This mode requires feature level 9\_1 or above.</span></span> |
| <span data-ttu-id="458fd-233">\_ \_ Лучшее качество D2D1 \_ колорманажемент</span><span class="sxs-lookup"><span data-stu-id="458fd-233">D2D1\_COLORMANAGEMENT\_QUALITY\_BEST</span></span> | <span data-ttu-id="458fd-234">Режим наилучшего качества.</span><span class="sxs-lookup"><span data-stu-id="458fd-234">The best quality mode.</span></span> <span data-ttu-id="458fd-235">Для этого режима требуется уровень компонентов 10 \_ 0 или выше, а также буферы точности с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="458fd-235">This mode requires feature level 10\_0 or above, as well as floating point precision buffers.</span></span> <span data-ttu-id="458fd-236">Этот режим поддерживает точность с плавающей запятой, а также расширенный диапазон, как определено в спецификации ICC v 4.3.</span><span class="sxs-lookup"><span data-stu-id="458fd-236">This mode supports floating point precision as well as extended range as defined in the ICC v4.3 specification.</span></span> |

<span data-ttu-id="458fd-237">Если приложение запрашивает режим качества, не поддерживаемый оборудованием, эффекты управления цветом вызовут ошибку.</span><span class="sxs-lookup"><span data-stu-id="458fd-237">The color management effect fails when drawing if the application requests a quality mode that is not supported by the hardware.</span></span> <span data-ttu-id="458fd-238">Уровень функций можно определить при вызове [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice).</span><span class="sxs-lookup"><span data-stu-id="458fd-238">You can determine the feature level when you call [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice).</span></span> <span data-ttu-id="458fd-239">Чтобы проверить поддержку буфера с плавающей точкой, вызовите [**ID2D1EffectContext:: исбуфферпреЦисионсуппортед**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) со значением [**D2D1 \_ buffer \_ Precision \_ 32BPC \_ float**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).</span><span class="sxs-lookup"><span data-stu-id="458fd-239">You can check for floating point buffer support by calling [**ID2D1EffectContext::IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) with the value [**D2D1\_BUFFER\_PRECISION\_32BPC\_FLOAT**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).</span></span>

## <a name="sample-code"></a><span data-ttu-id="458fd-240">Пример кода</span><span class="sxs-lookup"><span data-stu-id="458fd-240">Sample code</span></span>

<span data-ttu-id="458fd-241">Чтобы получить пример этого эффекта, скачайте [Пример коррекции фотографии Direct2D Effects](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)и ознакомьтесь с занятием 4 примера.</span><span class="sxs-lookup"><span data-stu-id="458fd-241">For an example of this effect, download the [Direct2D effects photo adjustment sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment), and see Lesson 4 of the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="458fd-242">Требования</span><span class="sxs-lookup"><span data-stu-id="458fd-242">Requirements</span></span>

| <span data-ttu-id="458fd-243">Требование</span><span class="sxs-lookup"><span data-stu-id="458fd-243">Requirement</span></span> | <span data-ttu-id="458fd-244">Значение</span><span class="sxs-lookup"><span data-stu-id="458fd-244">Value</span></span> |
|-|-|
| <span data-ttu-id="458fd-245">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="458fd-245">Minimum supported client</span></span> | <span data-ttu-id="458fd-246">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="458fd-246">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="458fd-247">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="458fd-247">Minimum supported server</span></span> | <span data-ttu-id="458fd-248">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="458fd-248">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="458fd-249">Header</span><span class="sxs-lookup"><span data-stu-id="458fd-249">Header</span></span> | <span data-ttu-id="458fd-250">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="458fd-250">d2d1effects.h</span></span> |
| <span data-ttu-id="458fd-251">Библиотека</span><span class="sxs-lookup"><span data-stu-id="458fd-251">Library</span></span> | <span data-ttu-id="458fd-252">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="458fd-252">d2d1.lib, dxguid.lib</span></span> |

## <a name="related-topics"></a><span data-ttu-id="458fd-253">См. также</span><span class="sxs-lookup"><span data-stu-id="458fd-253">Related topics</span></span>

* [<span data-ttu-id="458fd-254">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="458fd-254">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
