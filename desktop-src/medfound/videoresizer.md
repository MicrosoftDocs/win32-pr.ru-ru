---
description: Изменяет размер видеопотока.
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: DSP-размер видеоролика (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7826f21cadc6d30bc2b8b04bbcc741c2bf31bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692578"
---
# <a name="video-resizer-dsp"></a><span data-ttu-id="001e6-103">DSP изменения видеоконтроллеров</span><span class="sxs-lookup"><span data-stu-id="001e6-103">Video Resizer DSP</span></span>

<span data-ttu-id="001e6-104">Изменяет размер видеопотока.</span><span class="sxs-lookup"><span data-stu-id="001e6-104">Resizes a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="001e6-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="001e6-105">CLSID</span></span>

<span data-ttu-id="001e6-106">\_КРЕСИЗЕРДМО CLSID</span><span class="sxs-lookup"><span data-stu-id="001e6-106">CLSID\_CResizerDMO</span></span>

## <a name="interfaces"></a><span data-ttu-id="001e6-107">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="001e6-107">Interfaces</span></span>

-   [<span data-ttu-id="001e6-108">**имедиаобжект**</span><span class="sxs-lookup"><span data-stu-id="001e6-108">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="001e6-109">**имфреалтимеклиент**</span><span class="sxs-lookup"><span data-stu-id="001e6-109">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="001e6-110">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="001e6-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="001e6-111">**ипропертисторе**</span><span class="sxs-lookup"><span data-stu-id="001e6-111">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [<span data-ttu-id="001e6-112">**ивмресизерпропс**</span><span class="sxs-lookup"><span data-stu-id="001e6-112">**IWMResizerProps**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops)

## <a name="formats"></a><span data-ttu-id="001e6-113">Форматы</span><span class="sxs-lookup"><span data-stu-id="001e6-113">Formats</span></span>

<span data-ttu-id="001e6-114">DSP для изменения размера видео поддерживает следующие подтипы входных и выходных данных, когда он выступает в качестве объекта мультимедиа DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="001e6-114">The Video Resizer DSP supports the following input/output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="001e6-115">МЕДИАСУБТИПЕ \_ ийув</span><span class="sxs-lookup"><span data-stu-id="001e6-115">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="001e6-116">МЕДИАСУБТИПЕ \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="001e6-116">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="001e6-117">МЕДИАСУБТИПЕ \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="001e6-117">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="001e6-118">МЕДИАСУБТИПЕ \_ I420</span><span class="sxs-lookup"><span data-stu-id="001e6-118">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="001e6-119">МЕДИАСУБТИПЕ \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="001e6-119">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="001e6-120">МЕДИАСУБТИПЕ \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="001e6-120">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="001e6-121">МЕДИАСУБТИПЕ \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="001e6-121">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="001e6-122">МЕДИАСУБТИПЕ \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="001e6-122">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="001e6-123">МЕДИАСУБТИПЕ \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="001e6-123">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="001e6-124">МЕДИАСУБТИПЕ \_ айув</span><span class="sxs-lookup"><span data-stu-id="001e6-124">MEDIASUBTYPE\_AYUV</span></span>
-   <span data-ttu-id="001e6-125">МЕДИАСУБТИПЕ \_ V216</span><span class="sxs-lookup"><span data-stu-id="001e6-125">MEDIASUBTYPE\_V216</span></span>
-   <span data-ttu-id="001e6-126">МЕДИАСУБТИПЕ \_ YV12</span><span class="sxs-lookup"><span data-stu-id="001e6-126">MEDIASUBTYPE\_YV12</span></span>

<span data-ttu-id="001e6-127">DSP для изменения размера видео поддерживает следующие подтипы входных и выходных данных, когда он выступает в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="001e6-127">The Video Resizer DSP supports the following input/output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="001e6-128">Мфвидеоформат \_ ийув</span><span class="sxs-lookup"><span data-stu-id="001e6-128">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="001e6-129">Мфвидеоформат \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="001e6-129">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="001e6-130">Мфвидеоформат \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="001e6-130">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="001e6-131">Мфвидеоформат \_ I420</span><span class="sxs-lookup"><span data-stu-id="001e6-131">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="001e6-132">Мфвидеоформат \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="001e6-132">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="001e6-133">Мфвидеоформат \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="001e6-133">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="001e6-134">Мфвидеоформат \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="001e6-134">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="001e6-135">Мфвидеоформат \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="001e6-135">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="001e6-136">Мфвидеоформат \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="001e6-136">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="001e6-137">Мфвидеоформат \_ айув</span><span class="sxs-lookup"><span data-stu-id="001e6-137">MFVideoFormat\_AYUV</span></span>
-   <span data-ttu-id="001e6-138">Мфвидеоформат \_ V216</span><span class="sxs-lookup"><span data-stu-id="001e6-138">MFVideoFormat\_V216</span></span>
-   <span data-ttu-id="001e6-139">Мфвидеоформат \_ YV12</span><span class="sxs-lookup"><span data-stu-id="001e6-139">MFVideoFormat\_YV12</span></span>

## <a name="properties"></a><span data-ttu-id="001e6-140">Свойства</span><span class="sxs-lookup"><span data-stu-id="001e6-140">Properties</span></span>

-   [<span data-ttu-id="001e6-141">МФПКЭЙ. \_ \_ левый размер \_ src</span><span class="sxs-lookup"><span data-stu-id="001e6-141">MFPKEY\_RESIZE\_SRC\_LEFT</span></span>](mfpkey-resize-src-left.md)
-   [<span data-ttu-id="001e6-142">МФПКЭЙ \_ изменить размер \_ src \_ сверху</span><span class="sxs-lookup"><span data-stu-id="001e6-142">MFPKEY\_RESIZE\_SRC\_TOP</span></span>](mfpkey-resize-src-top.md)
-   [<span data-ttu-id="001e6-143">МФПКЭЙ \_ изменить \_ ширину src \_</span><span class="sxs-lookup"><span data-stu-id="001e6-143">MFPKEY\_RESIZE\_SRC\_WIDTH</span></span>](mfpkey-resize-src-width.md)
-   [<span data-ttu-id="001e6-144">МФПКЭЙ \_ изменить \_ высоту src \_</span><span class="sxs-lookup"><span data-stu-id="001e6-144">MFPKEY\_RESIZE\_SRC\_HEIGHT</span></span>](mfpkey-resize-src-height.md)
-   [<span data-ttu-id="001e6-145">МФПКЭЙ \_ изменить размер \_ летнего времени \_ влево</span><span class="sxs-lookup"><span data-stu-id="001e6-145">MFPKEY\_RESIZE\_DST\_LEFT</span></span>](mfpkey-resize-dst-left.md)
-   [<span data-ttu-id="001e6-146">МФПКЭЙ \_ изменить размер \_ летнего времени \_ сверху</span><span class="sxs-lookup"><span data-stu-id="001e6-146">MFPKEY\_RESIZE\_DST\_TOP</span></span>](mfpkey-resize-dst-top.md)
-   [<span data-ttu-id="001e6-147">МФПКЭЙ \_ изменить \_ ширину летнего времени \_</span><span class="sxs-lookup"><span data-stu-id="001e6-147">MFPKEY\_RESIZE\_DST\_WIDTH</span></span>](mfpkey-resize-dst-width.md)
-   [<span data-ttu-id="001e6-148">МФПКЭЙ \_ изменить \_ высоту летнего времени \_</span><span class="sxs-lookup"><span data-stu-id="001e6-148">MFPKEY\_RESIZE\_DST\_HEIGHT</span></span>](mfpkey-resize-dst-height.md)
-   [<span data-ttu-id="001e6-149">МФПКЭЙ \_ изменить \_ качество</span><span class="sxs-lookup"><span data-stu-id="001e6-149">MFPKEY\_RESIZE\_QUALITY</span></span>](mfpkey-resize-quality.md)
-   [<span data-ttu-id="001e6-150">МФПКЭЙ \_ изменить размер \_ чередования</span><span class="sxs-lookup"><span data-stu-id="001e6-150">MFPKEY\_RESIZE\_INTERLACE</span></span>](mfpkey-resize-interlace.md)
-   [<span data-ttu-id="001e6-151">МФПКЭЙ \_ изменить размер \_ жеомапкс</span><span class="sxs-lookup"><span data-stu-id="001e6-151">MFPKEY\_RESIZE\_GEOMAPX</span></span>](mfpkey-resize-geomapx.md)
-   [<span data-ttu-id="001e6-152">МФПКЭЙ \_ изменить размер \_ жеомапи</span><span class="sxs-lookup"><span data-stu-id="001e6-152">MFPKEY\_RESIZE\_GEOMAPY</span></span>](mfpkey-resize-geomapy.md)
-   [<span data-ttu-id="001e6-153">МФПКЭЙ \_ изменить размер \_ жеомапвидс</span><span class="sxs-lookup"><span data-stu-id="001e6-153">MFPKEY\_RESIZE\_GEOMAPWIDTH</span></span>](mfpkey-resize-geomapwidth.md)
-   [<span data-ttu-id="001e6-154">МФПКЭЙ \_ изменить размер \_ жеомафеигхт</span><span class="sxs-lookup"><span data-stu-id="001e6-154">MFPKEY\_RESIZE\_GEOMAPHEIGHT</span></span>](mfpkey-resize-geomapheight.md)
-   [<span data-ttu-id="001e6-155">МФПКЭЙ \_ изменить размер \_ минапкс</span><span class="sxs-lookup"><span data-stu-id="001e6-155">MFPKEY\_RESIZE\_MINAPX</span></span>](mfpkey-resize-minapx.md)
-   [<span data-ttu-id="001e6-156">МФПКЭЙ \_ изменить размер \_ минапи</span><span class="sxs-lookup"><span data-stu-id="001e6-156">MFPKEY\_RESIZE\_MINAPY</span></span>](mfpkey-resize-minapy.md)
-   [<span data-ttu-id="001e6-157">МФПКЭЙ \_ изменить размер \_ минапвидс</span><span class="sxs-lookup"><span data-stu-id="001e6-157">MFPKEY\_RESIZE\_MINAPWIDTH</span></span>](mfpkey-resize-minapwidth.md)
-   [<span data-ttu-id="001e6-158">МФПКЭЙ \_ изменить размер \_ минафеигхт</span><span class="sxs-lookup"><span data-stu-id="001e6-158">MFPKEY\_RESIZE\_MINAPHEIGHT</span></span>](mfpkey-resize-minapheight.md)
-   [<span data-ttu-id="001e6-159">МФПКЭЙ \_ изменить размер \_ пансканапкс</span><span class="sxs-lookup"><span data-stu-id="001e6-159">MFPKEY\_RESIZE\_PANSCANAPX</span></span>](mfpkey-resize-panscanapx.md)
-   [<span data-ttu-id="001e6-160">МФПКЭЙ \_ изменить размер \_ пансканапи</span><span class="sxs-lookup"><span data-stu-id="001e6-160">MFPKEY\_RESIZE\_PANSCANAPY</span></span>](mfpkey-resize-panscanapy.md)
-   [<span data-ttu-id="001e6-161">МФПКЭЙ \_ изменить размер \_ пансканапвидс</span><span class="sxs-lookup"><span data-stu-id="001e6-161">MFPKEY\_RESIZE\_PANSCANAPWIDTH</span></span>](mfpkey-resize-panscanapwidth.md)
-   [<span data-ttu-id="001e6-162">МФПКЭЙ \_ изменить размер \_ пансканафеигхт</span><span class="sxs-lookup"><span data-stu-id="001e6-162">MFPKEY\_RESIZE\_PANSCANAPHEIGHT</span></span>](mfpkey-resize-panscanapheight.md)
-   [<span data-ttu-id="001e6-163">МФПКЭЙ \_ пикселаспектратио</span><span class="sxs-lookup"><span data-stu-id="001e6-163">MFPKEY\_PIXELASPECTRATIO</span></span>](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a><span data-ttu-id="001e6-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="001e6-164">Remarks</span></span>

<span data-ttu-id="001e6-165">Поставщик схемы DSP для изменения видео реализуется как COM-объект, который может использоваться в качестве DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="001e6-165">The Video Resizer DSP is implemented as a COM object that can act as a DMO or an MFT.</span></span> <span data-ttu-id="001e6-166">Объект имеет один идентификатор класса (CLSID), независимо от того, действует ли он как DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="001e6-166">The object has a single class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span> <span data-ttu-id="001e6-167">Сведения о том, когда DSP выступает в качестве DMO или MFT, см. в разделе [обработчики цифровых сигналов](windowsmediadigitalsignalprocessors.md).</span><span class="sxs-lookup"><span data-stu-id="001e6-167">For information about when a DSP acts as a DMO or an MFT, see [Digital Signal Processors](windowsmediadigitalsignalprocessors.md).</span></span>

<span data-ttu-id="001e6-168">Глобальные уникальные идентификаторы (GUID) для подтипов мультимедиа RGB различаются в зависимости от того, выступает ли DSP в роли DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="001e6-168">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="001e6-169">Идентификаторы GUID для подтипов мультимедиа, отличных от RGB, одинаковы, независимо от того, выступает ли DSP в роли DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="001e6-169">The GUIDs for non-RGB media subtypes are the same, regardless of whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="001e6-170">Сведения об идентификаторах GUID, представляющих подтипы мультимедиа, см. в разделе [GUID для подтипов видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="001e6-170">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="001e6-171">Этот DSP может выполнять обрезку и масштабирование изображения видео.</span><span class="sxs-lookup"><span data-stu-id="001e6-171">This DSP can perform both cropping and scaling on the video image.</span></span> <span data-ttu-id="001e6-172">Формат выходного типа должен соответствовать формату входного типа.</span><span class="sxs-lookup"><span data-stu-id="001e6-172">The format of the output type must match the format of the input type.</span></span> <span data-ttu-id="001e6-173">DSP не выполняет преобразование цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="001e6-173">The DSP does not perform color-space conversions.</span></span>

<span data-ttu-id="001e6-174">Перед настройкой типа выходных данных можно определить любой из следующих регионов, используя свойства, перечисленные в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="001e6-174">Before setting the output type, you can define any of the following regions by using the properties listed in this table.</span></span>



| <span data-ttu-id="001e6-175">Регион</span><span class="sxs-lookup"><span data-stu-id="001e6-175">Region</span></span>                   | <span data-ttu-id="001e6-176">Свойства</span><span class="sxs-lookup"><span data-stu-id="001e6-176">Properties</span></span>                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="001e6-177">Исходный прямоугольник</span><span class="sxs-lookup"><span data-stu-id="001e6-177">Source rectangle</span></span>         | <span data-ttu-id="001e6-178">МФПКЭЙ. \_ \_ левый размер \_ src</span><span class="sxs-lookup"><span data-stu-id="001e6-178">MFPKEY\_RESIZE\_SRC\_LEFT</span></span><br/> <span data-ttu-id="001e6-179">МФПКЭЙ \_ изменить размер \_ src \_ сверху</span><span class="sxs-lookup"><span data-stu-id="001e6-179">MFPKEY\_RESIZE\_SRC\_TOP</span></span><br/> <span data-ttu-id="001e6-180">МФПКЭЙ \_ изменить \_ ширину src \_</span><span class="sxs-lookup"><span data-stu-id="001e6-180">MFPKEY\_RESIZE\_SRC\_WIDTH</span></span><br/> <span data-ttu-id="001e6-181">МФПКЭЙ \_ изменить \_ высоту src \_</span><span class="sxs-lookup"><span data-stu-id="001e6-181">MFPKEY\_RESIZE\_SRC\_HEIGHT</span></span><br/>            |
| <span data-ttu-id="001e6-182">Прямоугольник назначения</span><span class="sxs-lookup"><span data-stu-id="001e6-182">Destination rectangle</span></span>    | <span data-ttu-id="001e6-183">МФПКЭЙ \_ изменить размер \_ летнего времени \_ влево</span><span class="sxs-lookup"><span data-stu-id="001e6-183">MFPKEY\_RESIZE\_DST\_LEFT</span></span><br/> <span data-ttu-id="001e6-184">МФПКЭЙ \_ изменить размер \_ летнего времени \_ сверху</span><span class="sxs-lookup"><span data-stu-id="001e6-184">MFPKEY\_RESIZE\_DST\_TOP</span></span><br/> <span data-ttu-id="001e6-185">МФПКЭЙ \_ изменить \_ ширину летнего времени \_</span><span class="sxs-lookup"><span data-stu-id="001e6-185">MFPKEY\_RESIZE\_DST\_WIDTH</span></span><br/> <span data-ttu-id="001e6-186">МФПКЭЙ \_ изменить \_ высоту летнего времени \_</span><span class="sxs-lookup"><span data-stu-id="001e6-186">MFPKEY\_RESIZE\_DST\_HEIGHT</span></span><br/>            |
| <span data-ttu-id="001e6-187">Геометрическое апертуро</span><span class="sxs-lookup"><span data-stu-id="001e6-187">Geometric aperture</span></span>       | <span data-ttu-id="001e6-188">МФПКЭЙ \_ изменить размер \_ жеомапкс</span><span class="sxs-lookup"><span data-stu-id="001e6-188">MFPKEY\_RESIZE\_GEOMAPX</span></span><br/> <span data-ttu-id="001e6-189">МФПКЭЙ \_ изменить размер \_ жеомапи</span><span class="sxs-lookup"><span data-stu-id="001e6-189">MFPKEY\_RESIZE\_GEOMAPY</span></span><br/> <span data-ttu-id="001e6-190">МФПКЭЙ \_ изменить размер \_ жеомапвидс</span><span class="sxs-lookup"><span data-stu-id="001e6-190">MFPKEY\_RESIZE\_GEOMAPWIDTH</span></span><br/> <span data-ttu-id="001e6-191">МФПКЭЙ \_ изменить размер \_ жеомафеигхт</span><span class="sxs-lookup"><span data-stu-id="001e6-191">MFPKEY\_RESIZE\_GEOMAPHEIGHT</span></span><br/>             |
| <span data-ttu-id="001e6-192">Минимальный отображаемый апертур</span><span class="sxs-lookup"><span data-stu-id="001e6-192">Minimum display aperture</span></span> | <span data-ttu-id="001e6-193">МФПКЭЙ \_ изменить размер \_ минапкс</span><span class="sxs-lookup"><span data-stu-id="001e6-193">MFPKEY\_RESIZE\_MINAPX</span></span><br/> <span data-ttu-id="001e6-194">МФПКЭЙ \_ изменить размер \_ минапи</span><span class="sxs-lookup"><span data-stu-id="001e6-194">MFPKEY\_RESIZE\_MINAPY</span></span><br/> <span data-ttu-id="001e6-195">МФПКЭЙ \_ изменить размер \_ минапвидс</span><span class="sxs-lookup"><span data-stu-id="001e6-195">MFPKEY\_RESIZE\_MINAPWIDTH</span></span><br/> <span data-ttu-id="001e6-196">МФПКЭЙ \_ изменить размер \_ минафеигхт</span><span class="sxs-lookup"><span data-stu-id="001e6-196">MFPKEY\_RESIZE\_MINAPHEIGHT</span></span><br/>                 |
| <span data-ttu-id="001e6-197">Регион для сдвига и сканирования</span><span class="sxs-lookup"><span data-stu-id="001e6-197">Pan/scan region</span></span>          | <span data-ttu-id="001e6-198">МФПКЭЙ \_ изменить размер \_ пансканапкс</span><span class="sxs-lookup"><span data-stu-id="001e6-198">MFPKEY\_RESIZE\_PANSCANAPX</span></span><br/> <span data-ttu-id="001e6-199">МФПКЭЙ \_ изменить размер \_ пансканапи</span><span class="sxs-lookup"><span data-stu-id="001e6-199">MFPKEY\_RESIZE\_PANSCANAPY</span></span><br/> <span data-ttu-id="001e6-200">МФПКЭЙ \_ изменить размер \_ пансканапвидс</span><span class="sxs-lookup"><span data-stu-id="001e6-200">MFPKEY\_RESIZE\_PANSCANAPWIDTH</span></span><br/> <span data-ttu-id="001e6-201">МФПКЭЙ \_ изменить размер \_ пансканафеигхт</span><span class="sxs-lookup"><span data-stu-id="001e6-201">MFPKEY\_RESIZE\_PANSCANAPHEIGHT</span></span><br/> |



 

<span data-ttu-id="001e6-202">В каждом случае необходимо установить все связанные свойства, чтобы параметр вступил в силу.</span><span class="sxs-lookup"><span data-stu-id="001e6-202">In each case, you must set all of the associated properties for the setting to take effect.</span></span>

<span data-ttu-id="001e6-203">DSP копирует часть исходного изображения, определенное исходным прямоугольником, и растягивает или сжимает его в прямоугольнике назначения в выходном буфере.</span><span class="sxs-lookup"><span data-stu-id="001e6-203">The DSP copies the portion of the source image defined by source rectangle, and stretches or compresses it onto the destination rectangle on the output buffer.</span></span> <span data-ttu-id="001e6-204">Исходный и конечный прямоугольники не должны иметь одинаковый размер.</span><span class="sxs-lookup"><span data-stu-id="001e6-204">The source and destination rectangles do not need to be the same size.</span></span> <span data-ttu-id="001e6-205">Размер кадра в выходном типе носителя должен быть достаточно большим для размещения прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="001e6-205">The frame size in the output media type must be large enough to hold the destination rectangle.</span></span>

<span data-ttu-id="001e6-206">Геометрическое Апертура, минимальный апертур экрана и регион сдвига и сканирования не влияют на то, как DSP изменяет размер видео.</span><span class="sxs-lookup"><span data-stu-id="001e6-206">The geometric aperture, minimum display aperture, and pan/scan region do not affect how the DSP resizes the video.</span></span> <span data-ttu-id="001e6-207">Однако они могут повлиять на то, как нисходящий компонент интерпретирует кадр видео.</span><span class="sxs-lookup"><span data-stu-id="001e6-207">However, they might affect how the downstream component interprets the video frame.</span></span> <span data-ttu-id="001e6-208">В частности, расширенный обработчик видео (Евр) использует эти значения при вычислении пропорций изображения и области отображения.</span><span class="sxs-lookup"><span data-stu-id="001e6-208">In particular, the enhanced video renderer (EVR) uses these values when it calculates the picture aspect ratio and the display area.</span></span>

<span data-ttu-id="001e6-209">При использовании Media Foundation типов носителей можно задать геометрическое апертуру, минимальный отображаемый апертур, а также регионы сдвига и сканирования непосредственно в выходном типе носителя.</span><span class="sxs-lookup"><span data-stu-id="001e6-209">If you are using Media Foundation media types, you can set the geometric aperture, minimum display aperture, and pan/scan regions directly in the output media type.</span></span> <span data-ttu-id="001e6-210">В противном случае, если используются типы мультимедиа DMO, задайте их с помощью свойств.</span><span class="sxs-lookup"><span data-stu-id="001e6-210">Otherwise, if you are using DMO media types, set them using the properties.</span></span>

<span data-ttu-id="001e6-211">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="001e6-211">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="001e6-212">**\_ \_ геометрическое \_ Апертура MF**</span><span class="sxs-lookup"><span data-stu-id="001e6-212">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
-   [<span data-ttu-id="001e6-213">**\_ \_ Минимальный \_ \_ Апертура экрана MF MT**</span><span class="sxs-lookup"><span data-stu-id="001e6-213">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
-   [<span data-ttu-id="001e6-214">**\_ \_ \_ Апертура для поиска MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="001e6-214">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a><span data-ttu-id="001e6-215">Требования</span><span class="sxs-lookup"><span data-stu-id="001e6-215">Requirements</span></span>



| <span data-ttu-id="001e6-216">Требование</span><span class="sxs-lookup"><span data-stu-id="001e6-216">Requirement</span></span> | <span data-ttu-id="001e6-217">Значение</span><span class="sxs-lookup"><span data-stu-id="001e6-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="001e6-218">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="001e6-218">Minimum supported client</span></span><br/> | <span data-ttu-id="001e6-219">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="001e6-219">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="001e6-220">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="001e6-220">Minimum supported server</span></span><br/> | <span data-ttu-id="001e6-221">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="001e6-221">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="001e6-222">Header</span><span class="sxs-lookup"><span data-stu-id="001e6-222">Header</span></span><br/>                   | <dl> <span data-ttu-id="001e6-223"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="001e6-223"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="001e6-224">DLL</span><span class="sxs-lookup"><span data-stu-id="001e6-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="001e6-225"><dt>Vidreszr.dll</dt></span><span class="sxs-lookup"><span data-stu-id="001e6-225"><dt>Vidreszr.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="001e6-226">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="001e6-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="001e6-227">Обработчики цифровых сигналов</span><span class="sxs-lookup"><span data-stu-id="001e6-227">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
