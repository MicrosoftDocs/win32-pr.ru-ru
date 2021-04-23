---
description: Файл MFT обработчика видео — это Microsoft Media Foundation преобразование (MFT), которое выполняет колорспаце преобразование, изменение размера видео, дечередование, преобразование частоты кадров, вращение, кадрирование, пространственное левое и правое представление, распаковать и зеркальное отображение.
ms.assetid: 1476995A-9692-4B08-8EF7-7DB6321BEC24
title: Файл MFT видеопроцессора (Камерауиконтрол. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53783b42073414e4dc440546698bf295b404dcc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718125"
---
# <a name="video-processor-mft"></a><span data-ttu-id="a1e34-103">Файл MFT видеопроцессора</span><span class="sxs-lookup"><span data-stu-id="a1e34-103">Video Processor MFT</span></span>

<span data-ttu-id="a1e34-104">Файл MFT обработчика видео — это Microsoft Media Foundation преобразование (MFT), которое выполняет колорспаце преобразование, изменение размера видео, дечередование, преобразование частоты кадров, вращение, кадрирование, пространственное левое и правое представление, распаковать и зеркальное отображение.</span><span class="sxs-lookup"><span data-stu-id="a1e34-104">The video processor MFT is a Microsoft Media Foundation transform (MFT) that performs colorspace conversion, video resizing, deinterlacing, frame rate conversion, rotation, cropping, spatial left and right view unpacking, and mirroring.</span></span>

## <a name="clsid"></a><span data-ttu-id="a1e34-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="a1e34-105">CLSID</span></span>

<span data-ttu-id="a1e34-106">\_ВИДЕОПРОЦЕССОРМФТ CLSID</span><span class="sxs-lookup"><span data-stu-id="a1e34-106">CLSID\_VideoProcessorMFT</span></span>

## <a name="interfaces"></a><span data-ttu-id="a1e34-107">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="a1e34-107">Interfaces</span></span>

-   [<span data-ttu-id="a1e34-108">**имфреалтимеклиентекс**</span><span class="sxs-lookup"><span data-stu-id="a1e34-108">**IMFRealTimeClientEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
-   [<span data-ttu-id="a1e34-109">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="a1e34-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="a1e34-110">**имфвидеопроцессорконтрол**</span><span class="sxs-lookup"><span data-stu-id="a1e34-110">**IMFVideoProcessorControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol)

## <a name="input-formats"></a><span data-ttu-id="a1e34-111">Форматы входных данных</span><span class="sxs-lookup"><span data-stu-id="a1e34-111">Input Formats</span></span>

-   <span data-ttu-id="a1e34-112">**Мфвидеоформат \_ ARGB32**</span><span class="sxs-lookup"><span data-stu-id="a1e34-112">**MFVideoFormat\_ARGB32**</span></span>
-   <span data-ttu-id="a1e34-113">**Мфвидеоформат \_ айув**</span><span class="sxs-lookup"><span data-stu-id="a1e34-113">**MFVideoFormat\_AYUV**</span></span>
-   <span data-ttu-id="a1e34-114">**Мфвидеоформат \_ I420**</span><span class="sxs-lookup"><span data-stu-id="a1e34-114">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="a1e34-115">**Мфвидеоформат \_ ийув**</span><span class="sxs-lookup"><span data-stu-id="a1e34-115">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="a1e34-116">**Мфвидеоформат \_ NV11**</span><span class="sxs-lookup"><span data-stu-id="a1e34-116">**MFVideoFormat\_NV11**</span></span>
-   <span data-ttu-id="a1e34-117">**Мфвидеоформат \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="a1e34-117">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="a1e34-118">**Мфвидеоформат \_ Rgb24**</span><span class="sxs-lookup"><span data-stu-id="a1e34-118">**MFVideoFormat\_RGB24**</span></span>
-   <span data-ttu-id="a1e34-119">**Мфвидеоформат \_ RGB32**</span><span class="sxs-lookup"><span data-stu-id="a1e34-119">**MFVideoFormat\_RGB32**</span></span>
-   <span data-ttu-id="a1e34-120">**Мфвидеоформат \_ RGB555**</span><span class="sxs-lookup"><span data-stu-id="a1e34-120">**MFVideoFormat\_RGB555**</span></span>
-   <span data-ttu-id="a1e34-121">**Мфвидеоформат \_ RGB565**</span><span class="sxs-lookup"><span data-stu-id="a1e34-121">**MFVideoFormat\_RGB565**</span></span>
-   <span data-ttu-id="a1e34-122">**Мфвидеоформат \_ RGB8**</span><span class="sxs-lookup"><span data-stu-id="a1e34-122">**MFVideoFormat\_RGB8**</span></span>
-   <span data-ttu-id="a1e34-123">**Мфвидеоформат \_ UYVY**</span><span class="sxs-lookup"><span data-stu-id="a1e34-123">**MFVideoFormat\_UYVY**</span></span>
-   <span data-ttu-id="a1e34-124">**Мфвидеоформат \_ V410**</span><span class="sxs-lookup"><span data-stu-id="a1e34-124">**MFVideoFormat\_v410**</span></span>
-   <span data-ttu-id="a1e34-125">**Мфвидеоформат \_ Y216**</span><span class="sxs-lookup"><span data-stu-id="a1e34-125">**MFVideoFormat\_Y216**</span></span>
-   <span data-ttu-id="a1e34-126">**Мфвидеоформат \_ Y41P**</span><span class="sxs-lookup"><span data-stu-id="a1e34-126">**MFVideoFormat\_Y41P**</span></span>
-   <span data-ttu-id="a1e34-127">**Мфвидеоформат \_ Y41T**</span><span class="sxs-lookup"><span data-stu-id="a1e34-127">**MFVideoFormat\_Y41T**</span></span>
-   <span data-ttu-id="a1e34-128">**Мфвидеоформат \_ Y42T**</span><span class="sxs-lookup"><span data-stu-id="a1e34-128">**MFVideoFormat\_Y42T**</span></span>
-   <span data-ttu-id="a1e34-129">**Мфвидеоформат \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="a1e34-129">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="a1e34-130">**Мфвидеоформат \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="a1e34-130">**MFVideoFormat\_YV12**</span></span>
-   <span data-ttu-id="a1e34-131">**Мфвидеоформат \_ ивю**</span><span class="sxs-lookup"><span data-stu-id="a1e34-131">**MFVideoFormat\_YVYU**</span></span>

## <a name="output-formats"></a><span data-ttu-id="a1e34-132">Форматы выходных данных</span><span class="sxs-lookup"><span data-stu-id="a1e34-132">Output Formats</span></span>

-   <span data-ttu-id="a1e34-133">**Мфвидеоформат \_ ARGB32**</span><span class="sxs-lookup"><span data-stu-id="a1e34-133">**MFVideoFormat\_ARGB32**</span></span>
-   <span data-ttu-id="a1e34-134">**Мфвидеоформат \_ айув**</span><span class="sxs-lookup"><span data-stu-id="a1e34-134">**MFVideoFormat\_AYUV**</span></span>
-   <span data-ttu-id="a1e34-135">**Мфвидеоформат \_ I420**</span><span class="sxs-lookup"><span data-stu-id="a1e34-135">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="a1e34-136">**Мфвидеоформат \_ ийув**</span><span class="sxs-lookup"><span data-stu-id="a1e34-136">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="a1e34-137">**Мфвидеоформат \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="a1e34-137">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="a1e34-138">**Мфвидеоформат \_ Rgb24**</span><span class="sxs-lookup"><span data-stu-id="a1e34-138">**MFVideoFormat\_RGB24**</span></span>
-   <span data-ttu-id="a1e34-139">**Мфвидеоформат \_ RGB32**</span><span class="sxs-lookup"><span data-stu-id="a1e34-139">**MFVideoFormat\_RGB32**</span></span>
-   <span data-ttu-id="a1e34-140">**Мфвидеоформат \_ RGB555**</span><span class="sxs-lookup"><span data-stu-id="a1e34-140">**MFVideoFormat\_RGB555**</span></span>
-   <span data-ttu-id="a1e34-141">**Мфвидеоформат \_ RGB565**</span><span class="sxs-lookup"><span data-stu-id="a1e34-141">**MFVideoFormat\_RGB565**</span></span>
-   <span data-ttu-id="a1e34-142">**Мфвидеоформат \_ UYVY**</span><span class="sxs-lookup"><span data-stu-id="a1e34-142">**MFVideoFormat\_UYVY**</span></span>
-   <span data-ttu-id="a1e34-143">**Мфвидеоформат \_ Y216**</span><span class="sxs-lookup"><span data-stu-id="a1e34-143">**MFVideoFormat\_Y216**</span></span>
-   <span data-ttu-id="a1e34-144">**Мфвидеоформат \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="a1e34-144">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="a1e34-145">**Мфвидеоформат \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="a1e34-145">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="a1e34-146">Поддерживается не все сочетания форматов входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a1e34-146">Not every combination of input and output formats is supported.</span></span> <span data-ttu-id="a1e34-147">Чтобы проверить, поддерживается ли преобразование, задайте тип входных данных, а затем вызовите [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="a1e34-147">To test whether a conversion is supported, set the input type and then call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span>

<span data-ttu-id="a1e34-148">Дополнительные сведения об этих форматах см. в разделе [GUID для подтипов видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="a1e34-148">For more information about these formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1e34-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1e34-149">Remarks</span></span>

<span data-ttu-id="a1e34-150">Экземпляр обработчика видео можно создать одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="a1e34-150">An instance of the video processor can be created in one of the following ways:</span></span>

-   <span data-ttu-id="a1e34-151">Путем вызова [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="a1e34-151">By calling [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="a1e34-152">Обработчик видео регистрируется в категории **MFT \_ Категория \_ \_ обработчика видео** .</span><span class="sxs-lookup"><span data-stu-id="a1e34-152">The video processor is registered under the **MFT\_CATEGORY\_VIDEO\_PROCESSOR** category.</span></span>
-   <span data-ttu-id="a1e34-153">Вызывая **функцию com** , мы передаем ей CLSID CLSID **\_ видеопроцессормфт**.</span><span class="sxs-lookup"><span data-stu-id="a1e34-153">By calling the COM function **CoCreateInstance** passing it the CLSID **CLSID\_VideoProcessorMFT**.</span></span>

<span data-ttu-id="a1e34-154">Следующие замечания относятся к работе с исходными прямоугольниками и конечными прямоугольниками в **MFT обработчика видео**.</span><span class="sxs-lookup"><span data-stu-id="a1e34-154">The following remarks pertain to working with source rectangles and destination rectangles in the **Video Processor MFT**.</span></span> <span data-ttu-id="a1e34-155">Исходный и конечный прямоугольники задаются с помощью [**имфвидеопроцессорконтрол:: сетдестинатионректангле**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) и [**сетсаурцеректангле**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) , а также в некоторых случаях с [**имфмедиаенгиникс:: UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).</span><span class="sxs-lookup"><span data-stu-id="a1e34-155">Source and destination rectangles are set with [**IMFVideoProcessorControl::SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) and [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) and some times with [**IMFMediaEngineEx::UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).</span></span>

-   <span data-ttu-id="a1e34-156">Исходный прямоугольник должен быть согласован и округляться в соответствии с требованиями цветового формата кадра, выводимого обработчику видео.</span><span class="sxs-lookup"><span data-stu-id="a1e34-156">The source rectangle should be aligned and rounded to match the requirements of the color format of the frame inputted to the video processor.</span></span> <span data-ttu-id="a1e34-157">Это важно, поскольку такие форматы, как 420 и 422, имеют требования к измерениям и смещениям, которые могут быть созданы и доступны.</span><span class="sxs-lookup"><span data-stu-id="a1e34-157">This is important because formats like 420 and 422 have requirements about the dimensions and offsets that can be created and accessed.</span></span> <span data-ttu-id="a1e34-158">Например, исходный прямоугольник {1, 0, 319, 240} (левый, верхний, правый, нижний) будет округляться до {2, 0, 320, 240}, если входной формат имеет значение 420.</span><span class="sxs-lookup"><span data-stu-id="a1e34-158">For example, a source rectangle of {1, 0, 319, 240} (left, top, right, bottom) will be rounded to {2, 0, 320, 240} when the input format is 420.</span></span>
-   <span data-ttu-id="a1e34-159">Как конечный, так и исходный прямоугольник всегда будут относиться к соответствующим кадрам — исходному прямоугольнику исходного фрейма и конечному прямоугольнику назначения.</span><span class="sxs-lookup"><span data-stu-id="a1e34-159">Both the destination and source rectangle will always be clamped to fit inside their respective frames—the source rectangle to the source frame and the destination rectangle to the destination frame.</span></span> <span data-ttu-id="a1e34-160">Это означает, что отрицательные значения не имеют смысла — они будут всегда относиться к 0.</span><span class="sxs-lookup"><span data-stu-id="a1e34-160">This means that negative values are not meaningful—they will be always clamped to 0.</span></span>
-   <span data-ttu-id="a1e34-161">Исходный прямоугольник находится в системе координат конечного фрейма, за вычетом любого прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="a1e34-161">The source rectangle is in the destination frame's coordinate system, minus any destination rectangle.</span></span> <span data-ttu-id="a1e34-162">Это означает, что преобразования, такие как вращение, отменяются в исходном прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="a1e34-162">This means that transformations like rotation are "undone" on the source rectangle.</span></span> <span data-ttu-id="a1e34-163">Поэтому не нужно знать, была ли видео повернуто или трехмерное.</span><span class="sxs-lookup"><span data-stu-id="a1e34-163">Therefore, you do not need to know if the video was rotated or 3D unpacked.</span></span> <span data-ttu-id="a1e34-164">Например, можно нарисовать прямоугольник поверх тега Video, взять относительные координаты (относительно тега Video), нормализовать их (диапазон от 0 до 1) и передавать их вниз в качестве исходного прямоугольника, и они должны работать, как ожидалось, даже при вращении видео.</span><span class="sxs-lookup"><span data-stu-id="a1e34-164">For example, you could draw a rectangle on top of the video tag, take the relative coordinates (relative to the video tag), normalize them (range 0 to 1) and pass them down as the source rectangle and they should work as expected, even if the video is being rotated.</span></span>

<span data-ttu-id="a1e34-165">Процессор видео поддерживает обработку видео с ускорением GPU с помощью Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="a1e34-165">The video processor supports GPU-accelerated video processing, using Microsoft Direct3D 11.</span></span> <span data-ttu-id="a1e34-166">Дополнительные сведения см. в [разделе \_ \_ \_ о сопоставлении MF SA D3D11](mf-sa-d3d11-aware.md).</span><span class="sxs-lookup"><span data-stu-id="a1e34-166">For more information, see [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md).</span></span>

### <a name="stereoscopic-video"></a><span data-ttu-id="a1e34-167">Видео стереоскопик</span><span class="sxs-lookup"><span data-stu-id="a1e34-167">Stereoscopic Video</span></span>

<span data-ttu-id="a1e34-168">Процессор видео поддерживает операцию "Просмотр распаковки" для трехмерных видеокадров:</span><span class="sxs-lookup"><span data-stu-id="a1e34-168">The video processor supports the view unpacking operation on 3D video frames:</span></span>

<span data-ttu-id="a1e34-169">Если входной кадр содержит два представления, Упакованные в один кадр, обработчик видео может разделить представления на отдельные буферы или извлечь базовое представление и отменить второе представление.</span><span class="sxs-lookup"><span data-stu-id="a1e34-169">If the input frame contains two views packed in the same frame, the video processor can split the views into separate buffers, or extract the base view and discard the second view.</span></span> <span data-ttu-id="a1e34-170">Чтобы включить распаковать представление, установите для атрибута [ \_ \_ 3DVIDEO \_ выходной атрибут MF](mf-enable-3dvideo-output.md) значение **MF3DVideoOutputType \_ стерео** или **MF3DVideoOutputType \_ басевиев**.</span><span class="sxs-lookup"><span data-stu-id="a1e34-170">To enable view unpacking, set the [MF\_ENABLE\_3DVIDEO\_OUTPUT](mf-enable-3dvideo-output.md) attribute to **MF3DVideoOutputType\_Stereo** or **MF3DVideoOutputType\_BaseView**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1e34-171">Требования</span><span class="sxs-lookup"><span data-stu-id="a1e34-171">Requirements</span></span>



| <span data-ttu-id="a1e34-172">Требование</span><span class="sxs-lookup"><span data-stu-id="a1e34-172">Requirement</span></span> | <span data-ttu-id="a1e34-173">Значение</span><span class="sxs-lookup"><span data-stu-id="a1e34-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e34-174">Header</span><span class="sxs-lookup"><span data-stu-id="a1e34-174">Header</span></span><br/> | <dl> <span data-ttu-id="a1e34-175"><dt>Камерауиконтрол. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1e34-175"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1e34-176">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1e34-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1e34-177">Обработчики цифровых сигналов</span><span class="sxs-lookup"><span data-stu-id="a1e34-177">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




