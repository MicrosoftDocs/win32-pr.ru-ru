---
description: Настройка параметров чередования
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: Настройка параметров чередования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be52ae3023c8e4bc83c3305a104c389f423cffd6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805206"
---
# <a name="setting-deinterlace-preferences"></a><span data-ttu-id="56741-103">Настройка параметров чередования</span><span class="sxs-lookup"><span data-stu-id="56741-103">Setting Deinterlace Preferences</span></span>

<span data-ttu-id="56741-104">Устройство микширования видео (VMR) поддерживает дечередование с аппаратным ускорением, что улучшает качество отображения для чередования видео.</span><span class="sxs-lookup"><span data-stu-id="56741-104">The Video Mixing Renderer (VMR) supports hardware-accelerated deinterlacing, which improves rendering quality for interlaced video.</span></span> <span data-ttu-id="56741-105">Конкретные доступные функции зависят от базового оборудования.</span><span class="sxs-lookup"><span data-stu-id="56741-105">The exact features that are available depend on the underlying hardware.</span></span> <span data-ttu-id="56741-106">Приложение может запрашивать возможности дечередования оборудования и задавать параметры разбора с помощью интерфейса [**ивмрдеинтерлацеконтрол**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) (VMR-7) или [**IVMRDEINTERLACECONTROL9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) Interface (VMR-9).</span><span class="sxs-lookup"><span data-stu-id="56741-106">The application can query for the hardware deinterlacing capabilities and set deinterlacing preferences through the [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) interface (VMR-7) or [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) interface (VMR-9).</span></span> <span data-ttu-id="56741-107">Дечередование выполняется отдельно для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="56741-107">Deinterlacing is performed on a per-stream basis.</span></span>

<span data-ttu-id="56741-108">Существует одно важное различие в поведении чередования между VMR-7 и VMR-9.</span><span class="sxs-lookup"><span data-stu-id="56741-108">There is one important difference in interlacing behavior between the VMR-7 and the VMR-9.</span></span> <span data-ttu-id="56741-109">В системах, где графическое оборудование не поддерживает расширенное чередование, фильтр VMR-7 может вернуться к наложение оборудования и поручить его использовать для дечередования в стиле Боба.</span><span class="sxs-lookup"><span data-stu-id="56741-109">On systems where the graphics hardware doesn't support advanced deinterlacing, the VMR-7 can fall back to the hardware overlay and instruct it to use a BOB style deinterlace.</span></span> <span data-ttu-id="56741-110">В этом случае, несмотря на то, что VMR сообщает о 30fps, на самом деле видео отображается в 60 отражения в секунду.</span><span class="sxs-lookup"><span data-stu-id="56741-110">In this case, although the VMR is reporting 30fps the video is actually being rendered at 60 flips per second.</span></span>

<span data-ttu-id="56741-111">За исключением VMR-7 с использованием наложения оборудования, это происходит с помощью микшера VMR.</span><span class="sxs-lookup"><span data-stu-id="56741-111">Except in the case of the VMR-7 using hardware overlay, deinterlacing is performed by the VMR's mixer.</span></span> <span data-ttu-id="56741-112">Для выполнения дечередования микшер использует ускорение видео DirectX (ДКСВА) с помощью интерфейса драйвера устройства (DDI).</span><span class="sxs-lookup"><span data-stu-id="56741-112">The mixer uses the DirectX Video Acceleration (DXVA) deinterlacing device driver interface (DDI) to perform the deinterlacing.</span></span> <span data-ttu-id="56741-113">Эта DDI не может быть вызвана приложениями, и приложения не могут заменить функцию разчередования VMR.</span><span class="sxs-lookup"><span data-stu-id="56741-113">This DDI is not callable by applications, and applications cannot replace the VMR's deinterlacing functionality.</span></span> <span data-ttu-id="56741-114">Однако приложение может выбрать нужный режим разчередования, как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="56741-114">However, an application can select the desired deinterlacing mode, as described in this section.</span></span>

> [!Note]  
> <span data-ttu-id="56741-115">В этом разделе описываются методы **IVMRDeinterlaceControl9** , но версии VMR-7 практически идентичны.</span><span class="sxs-lookup"><span data-stu-id="56741-115">This section describes the **IVMRDeinterlaceControl9** methods, but the VMR-7 versions are almost identical.</span></span>

 

<span data-ttu-id="56741-116">Чтобы получить возможность разчередования видео для видеопотока, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="56741-116">To get the deinterlacing capabilities for a video stream, do the following:</span></span>

1.  <span data-ttu-id="56741-117">Заполните структуру [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) с описанием видеопотока.</span><span class="sxs-lookup"><span data-stu-id="56741-117">Fill in a [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) structure with a description of the video stream.</span></span> <span data-ttu-id="56741-118">Подробные сведения о том, как заполнять эту структуру, приведены далее.</span><span class="sxs-lookup"><span data-stu-id="56741-118">Details of how to fill in this structure are given later.</span></span>
2.  <span data-ttu-id="56741-119">Передайте структуру в метод [**IVMRDeinterlaceControl9:: жетнумберофдеинтерлацемодес**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) .</span><span class="sxs-lookup"><span data-stu-id="56741-119">Pass the structure to the [**IVMRDeinterlaceControl9::GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) method.</span></span> <span data-ttu-id="56741-120">Вызовите метод дважды.</span><span class="sxs-lookup"><span data-stu-id="56741-120">Call the method twice.</span></span> <span data-ttu-id="56741-121">Первый вызов возвращает число режимов с чередованием, поддерживаемое оборудованием, для указанного формата.</span><span class="sxs-lookup"><span data-stu-id="56741-121">The first call returns the number of deinterlace modes the hardware supports for the specified format.</span></span> <span data-ttu-id="56741-122">Выделите массив GUID этого размера и снова вызовите метод, передав адрес массива.</span><span class="sxs-lookup"><span data-stu-id="56741-122">Allocate an array of GUIDs of this size, and call the method again, passing in the address of the array.</span></span> <span data-ttu-id="56741-123">Второй вызов заполняет массив идентификаторами GUID.</span><span class="sxs-lookup"><span data-stu-id="56741-123">The second call fills the array with GUIDs.</span></span> <span data-ttu-id="56741-124">Каждый идентификатор GUID определяет один режим разчередования.</span><span class="sxs-lookup"><span data-stu-id="56741-124">Each GUID identifies one deinterlacing mode.</span></span>
3.  <span data-ttu-id="56741-125">Чтобы получить возможности в определенном режиме, вызовите метод [**IVMRDeinterlaceControl9:: жетдеинтерлацемодекапс**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) .</span><span class="sxs-lookup"><span data-stu-id="56741-125">To get the capabiltiies of a particular mode, call the [**IVMRDeinterlaceControl9::GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) method.</span></span> <span data-ttu-id="56741-126">Передайте ту же структуру **VMR9VideoDesc** вместе с одним из идентификаторов GUID из массива.</span><span class="sxs-lookup"><span data-stu-id="56741-126">Pass in the same **VMR9VideoDesc** structure, along with one of the GUIDs from the array.</span></span> <span data-ttu-id="56741-127">Метод заполняет структуру [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) с помощью возможностей режима.</span><span class="sxs-lookup"><span data-stu-id="56741-127">The method fills a [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) structure with the mode capabilities.</span></span>

<span data-ttu-id="56741-128">В следующем коде показаны следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="56741-128">The following code shows these steps:</span></span>


```C++
VMR9VideoDesc VideoDesc; 
DWORD dwNumModes = 0;
// Fill in the VideoDesc structure (not shown).
hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
    &dwNumModes, NULL);
if (SUCCEEDED(hr) && (dwNumModes != 0))
{
    // Allocate an array for the GUIDs that identify the modes.
    GUID *pModes = new GUID[dwNumModes];
    if (pModes)
    {
        // Fill the array.
        hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
            &dwNumModes, pModes);
        if (SUCCEEDED(hr))
        {
            // Loop through each item and get the capabilities.
            for (int i = 0; i < dwNumModes; i++)
            {
                VMR9DeinterlaceCaps Caps;
                hr = pDeinterlace->GetDeinterlaceModeCaps(pModes + i, 
                    &VideoDesc, &Caps);
                if (SUCCEEDED(hr))
                {
                    // Examine the Caps structure.
                }
            }
        }
        delete [] pModes;
    }
}
```



<span data-ttu-id="56741-129">Теперь приложение может задать режим разчередования для потока с помощью следующих методов:</span><span class="sxs-lookup"><span data-stu-id="56741-129">Now the application can set the deinterlacing mode for the stream, using the following methods:</span></span>

-   <span data-ttu-id="56741-130">Метод [**сетдеинтерлацемоде**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) задает предпочтительный режим.</span><span class="sxs-lookup"><span data-stu-id="56741-130">The [**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) method sets the preferred mode.</span></span> <span data-ttu-id="56741-131">Используйте GUID \_ null, чтобы отключить дечередование.</span><span class="sxs-lookup"><span data-stu-id="56741-131">Use GUID\_NULL to turn off deinterlacing.</span></span>
-   <span data-ttu-id="56741-132">Метод [**сетдеинтерлацепрефс**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) задает поведение, если запрошенный режим недоступен.</span><span class="sxs-lookup"><span data-stu-id="56741-132">The [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) method specifies the behavior if the requested mode is not available.</span></span>
-   <span data-ttu-id="56741-133">Метод [**жетдеинтерлацемоде**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) Возвращает предпочтительный режим, который был задан.</span><span class="sxs-lookup"><span data-stu-id="56741-133">The [**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) method returns the preferred mode that you set.</span></span>
-   <span data-ttu-id="56741-134">Метод [**жетактуалдеинтерлацемоде**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) возвращает фактически используемый режим, который может быть резервным режимом, если предпочтительный режим недоступен.</span><span class="sxs-lookup"><span data-stu-id="56741-134">The [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) method returns the actual mode in use, which might be a fallback mode, if the preferred mode is not available.</span></span>

<span data-ttu-id="56741-135">Дополнительные сведения см. на страницах справочника по методам.</span><span class="sxs-lookup"><span data-stu-id="56741-135">The method reference pages give more information.</span></span>

<span data-ttu-id="56741-136">**Использование структуры VMR9VideoDesc**</span><span class="sxs-lookup"><span data-stu-id="56741-136">**Using the VMR9VideoDesc Structure**</span></span>

<span data-ttu-id="56741-137">В процедуре, заданной ранее, первым шагом является заполнение структуры **VMR9VideoDesc** с описанием видеопотока.</span><span class="sxs-lookup"><span data-stu-id="56741-137">In the procedure given previously, the first step is to fill in a **VMR9VideoDesc** structure with a description of the video stream.</span></span> <span data-ttu-id="56741-138">Начните с получения типа мультимедиа потока видео.</span><span class="sxs-lookup"><span data-stu-id="56741-138">Start by getting the media type of the video stream.</span></span> <span data-ttu-id="56741-139">Это можно сделать, вызвав [**Ипин:: коннектионмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) в закрепление ввода фильтра VMR.</span><span class="sxs-lookup"><span data-stu-id="56741-139">You can do this by calling [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) on the VMR filter's input pin.</span></span> <span data-ttu-id="56741-140">Затем проверьте, является ли видеопоток чередованием.</span><span class="sxs-lookup"><span data-stu-id="56741-140">Then confirm whether the video stream is interlaced.</span></span> <span data-ttu-id="56741-141">Чередование можно выполнять только в форматах [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="56741-141">Only [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats can be interlaced.</span></span> <span data-ttu-id="56741-142">Если используется формат формата \_ видеоинфо, он должен быть последовательным кадром.</span><span class="sxs-lookup"><span data-stu-id="56741-142">If the format type is FORMAT\_VideoInfo, it must be a progressive frame.</span></span> <span data-ttu-id="56741-143">Если используется формат формата \_ VideoInfo2, проверьте поле **двинтерлацефлагс** для \_ флага аминтерлаце с чередованием.</span><span class="sxs-lookup"><span data-stu-id="56741-143">If the format type is FORMAT\_VideoInfo2, check the **dwInterlaceFlags** field for the AMINTERLACE\_IsInterlaced flag.</span></span> <span data-ttu-id="56741-144">Наличие этого флага означает, что видео чередуются.</span><span class="sxs-lookup"><span data-stu-id="56741-144">The presence of this flag indicates the video is interlaced.</span></span>

<span data-ttu-id="56741-145">Предположим, что переменная **пбми** является указателем на структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) в блоке format.</span><span class="sxs-lookup"><span data-stu-id="56741-145">Assume that the variable **pBMI** is a pointer to the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the format block.</span></span> <span data-ttu-id="56741-146">Задайте следующие значения в структуре **VMR9VideoDesc** :</span><span class="sxs-lookup"><span data-stu-id="56741-146">Set the following values in the **VMR9VideoDesc** structure:</span></span>

-   <span data-ttu-id="56741-147">**двсизе**: задайте для этого поля значение `sizeof(VMR9VideoDesc)` .</span><span class="sxs-lookup"><span data-stu-id="56741-147">**dwSize**: Set this field to `sizeof(VMR9VideoDesc)`.</span></span>
-   <span data-ttu-id="56741-148">**двсамплевидс**: задайте для этого поля значение `pBMI->biWidth` .</span><span class="sxs-lookup"><span data-stu-id="56741-148">**dwSampleWidth**: Set this field to `pBMI->biWidth`.</span></span>
-   <span data-ttu-id="56741-149">**двсамплехеигхт**: задайте для этого поля значение `abs(pBMI->biHeight)` .</span><span class="sxs-lookup"><span data-stu-id="56741-149">**dwSampleHeight**: Set this field to `abs(pBMI->biHeight)`.</span></span>
-   <span data-ttu-id="56741-150">**Самплеформат**. это поле описывает характеристики развертки типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="56741-150">**SampleFormat**: This field describes the interlace characteristics of the media type.</span></span> <span data-ttu-id="56741-151">Проверьте поле **двинтерлацефлагс** в структуре **VIDEOINFOHEADER2** и установите **самплеформат** равным эквивалентному флагу [**VMR9 \_ самплеформат**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) .</span><span class="sxs-lookup"><span data-stu-id="56741-151">Check the **dwInterlaceFlags** field in the **VIDEOINFOHEADER2** structure, and set **SampleFormat** equal to the equivalent [**VMR9\_SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) flag.</span></span> <span data-ttu-id="56741-152">Ниже приведен вспомогательная функция для этого.</span><span class="sxs-lookup"><span data-stu-id="56741-152">A helper function to do this is given below.</span></span>
-   <span data-ttu-id="56741-153">**Инпутсамплефрек**: в этом поле содержится входная частота, которую можно вычислить из поля **Авгтимеперфраме** в структуре **VIDEOINFOHEADER2** .</span><span class="sxs-lookup"><span data-stu-id="56741-153">**InputSampleFreq**: This field gives the input frequency, which can be calculated from the **AvgTimePerFrame** field in the **VIDEOINFOHEADER2** structure.</span></span> <span data-ttu-id="56741-154">В общем случае установите для **двнумератор** значение 10000000 и задайте для **двденоминатор** значение **авгтимеперфраме**.</span><span class="sxs-lookup"><span data-stu-id="56741-154">In the general case, set **dwNumerator** to 10000000, and set **dwDenominator** to **AvgTimePerFrame**.</span></span> <span data-ttu-id="56741-155">Однако можно также проверить наличие некоторых известных ставок кадров:</span><span class="sxs-lookup"><span data-stu-id="56741-155">However, you can also check for some well-known frame rates:</span></span>

    | <span data-ttu-id="56741-156">Среднее время на кадр</span><span class="sxs-lookup"><span data-stu-id="56741-156">Average time per frame</span></span> | <span data-ttu-id="56741-157">Частота кадров (кадров/с)</span><span class="sxs-lookup"><span data-stu-id="56741-157">Frame rate (fps)</span></span> | <span data-ttu-id="56741-158">Числитель</span><span class="sxs-lookup"><span data-stu-id="56741-158">Numerator</span></span> | <span data-ttu-id="56741-159">Подробно</span><span class="sxs-lookup"><span data-stu-id="56741-159">Denominator</span></span> |
    |------------------------|------------------|-----------|-------------|
    | <span data-ttu-id="56741-160">166833</span><span class="sxs-lookup"><span data-stu-id="56741-160">166833</span></span>                 | <span data-ttu-id="56741-161">59,94 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="56741-161">59.94 (NTSC)</span></span>     | <span data-ttu-id="56741-162">60 000</span><span class="sxs-lookup"><span data-stu-id="56741-162">60000</span></span>     | <span data-ttu-id="56741-163">1001</span><span class="sxs-lookup"><span data-stu-id="56741-163">1001</span></span>        |
    | <span data-ttu-id="56741-164">333667</span><span class="sxs-lookup"><span data-stu-id="56741-164">333667</span></span>                 | <span data-ttu-id="56741-165">29,97 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="56741-165">29.97 (NTSC)</span></span>     | <span data-ttu-id="56741-166">30 000</span><span class="sxs-lookup"><span data-stu-id="56741-166">30000</span></span>     | <span data-ttu-id="56741-167">1001</span><span class="sxs-lookup"><span data-stu-id="56741-167">1001</span></span>        |
    | <span data-ttu-id="56741-168">417188</span><span class="sxs-lookup"><span data-stu-id="56741-168">417188</span></span>                 | <span data-ttu-id="56741-169">23,97 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="56741-169">23.97 (NTSC)</span></span>     | <span data-ttu-id="56741-170">24 000</span><span class="sxs-lookup"><span data-stu-id="56741-170">24000</span></span>     | <span data-ttu-id="56741-171">1001</span><span class="sxs-lookup"><span data-stu-id="56741-171">1001</span></span>        |
    | <span data-ttu-id="56741-172">200 000</span><span class="sxs-lookup"><span data-stu-id="56741-172">200000</span></span>                 | <span data-ttu-id="56741-173">50,00 (PAL)</span><span class="sxs-lookup"><span data-stu-id="56741-173">50.00 (PAL)</span></span>      | <span data-ttu-id="56741-174">50</span><span class="sxs-lookup"><span data-stu-id="56741-174">50</span></span>        | <span data-ttu-id="56741-175">1</span><span class="sxs-lookup"><span data-stu-id="56741-175">1</span></span>           |
    | <span data-ttu-id="56741-176">400000</span><span class="sxs-lookup"><span data-stu-id="56741-176">400000</span></span>                 | <span data-ttu-id="56741-177">25,00 (PAL)</span><span class="sxs-lookup"><span data-stu-id="56741-177">25.00 (PAL)</span></span>      | <span data-ttu-id="56741-178">25</span><span class="sxs-lookup"><span data-stu-id="56741-178">25</span></span>        | <span data-ttu-id="56741-179">1</span><span class="sxs-lookup"><span data-stu-id="56741-179">1</span></span>           |
    | <span data-ttu-id="56741-180">416667</span><span class="sxs-lookup"><span data-stu-id="56741-180">416667</span></span>                 | <span data-ttu-id="56741-181">24,00 (пленка)</span><span class="sxs-lookup"><span data-stu-id="56741-181">24.00 (Film)</span></span>     | <span data-ttu-id="56741-182">24</span><span class="sxs-lookup"><span data-stu-id="56741-182">24</span></span>        | <span data-ttu-id="56741-183">1</span><span class="sxs-lookup"><span data-stu-id="56741-183">1</span></span>           |

    

     

-   <span data-ttu-id="56741-184">**Аутпутфрамефрек**: это поле содержит частоту вывода, которую можно вычислить на основе значения **инпутсамплефрек** и характеристик появления входного потока:</span><span class="sxs-lookup"><span data-stu-id="56741-184">**OutputFrameFreq**: This field gives the output frequency, which can be calculated from the **InputSampleFreq** value and the interleaving characteristics of the input stream:</span></span>
    -   <span data-ttu-id="56741-185">Задайте **аутпутфрамефрек. двденоминатор** равным **инпутсамплефрек. двденоминатор**.</span><span class="sxs-lookup"><span data-stu-id="56741-185">Set **OutputFrameFreq.dwDenominator** equal to **InputSampleFreq.dwDenominator**.</span></span>
    -   <span data-ttu-id="56741-186">Если входное видео находится под чередованием, установите **аутпутфрамефрек. двнумератор** в значение 2 x **инпутсамплефрек. двнумератор**.</span><span class="sxs-lookup"><span data-stu-id="56741-186">If the input video is interleaved, set **OutputFrameFreq.dwNumerator** to 2 x **InputSampleFreq.dwNumerator**.</span></span> <span data-ttu-id="56741-187">(После дечередования частота кадров удваивается.) В противном случае установите значение **инпутсамплефрек. двнумератор**.</span><span class="sxs-lookup"><span data-stu-id="56741-187">(After deinterlacing, the frame rate is doubled.) Otherwise, set the value to **InputSampleFreq.dwNumerator**.</span></span>
-   <span data-ttu-id="56741-188">**двфауркк**: задайте для этого поля значение `pBMI->biCompression` .</span><span class="sxs-lookup"><span data-stu-id="56741-188">**dwFourCC**: Set this field to `pBMI->biCompression`.</span></span>

<span data-ttu-id="56741-189">Следующая вспомогательная функция преобразует \_ Флаги аминтерлаце *X* в значения [**VMR9 \_ самплеформат**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) :</span><span class="sxs-lookup"><span data-stu-id="56741-189">The following helper function converts AMINTERLACE\_*X* flags to [**VMR9\_SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) values:</span></span>


```C++
#define IsInterlaced(x) ((x) & AMINTERLACE_IsInterlaced)
#define IsSingleField(x) ((x) & AMINTERLACE_1FieldPerSample)
#define IsField1First(x) ((x) & AMINTERLACE_Field1First)

VMR9_SampleFormat ConvertInterlaceFlags(DWORD dwInterlaceFlags)
{
    if (IsInterlaced(dwInterlaceFlags)) {
        if (IsSingleField(dwInterlaceFlags)) {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldSingleEven;
            }
            else {
                return VMR9_SampleFieldSingleOdd;
            }
        }
        else {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldInterleavedEvenFirst;
             }
            else {
                return VMR9_SampleFieldInterleavedOddFirst;
            }
        }
    }
    else {
        return VMR9_SampleProgressiveFrame;  // Not interlaced.
    }
}
```



 

 



