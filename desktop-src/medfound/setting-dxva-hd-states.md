---
description: .
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Настройка состояний ДКСВА-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e539796aa5d3997b35739e75c80b438a7b5da50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711396"
---
# <a name="setting-dxva-hd-states"></a><span data-ttu-id="f0efd-103">Настройка состояний ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="f0efd-103">Setting DXVA-HD States</span></span>

<span data-ttu-id="f0efd-104">Во время обработки видео устройство Microsoft DirectX Video ускорение High Definition (ДКСВА-HD) поддерживает постоянное состояние от одного кадра до следующего.</span><span class="sxs-lookup"><span data-stu-id="f0efd-104">During video processing, the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device maintains a persistent state from one frame to the next.</span></span> <span data-ttu-id="f0efd-105">Каждое состояние имеет задокументированное значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f0efd-105">Each state has a documented default.</span></span> <span data-ttu-id="f0efd-106">После настройки устройства задайте все состояния, которые вы хотите изменить, по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f0efd-106">After you configure the device, set any states that you wish to change from their defaults.</span></span> <span data-ttu-id="f0efd-107">Перед обработкой каждого кадра обновите все состояния, которые должны быть изменены.</span><span class="sxs-lookup"><span data-stu-id="f0efd-107">Before you process each frame, update any states that should change.</span></span>

> [!Note]  
> <span data-ttu-id="f0efd-108">Этот проект отличается от ДКСВА-президента.</span><span class="sxs-lookup"><span data-stu-id="f0efd-108">This design differs from DXVA-VP.</span></span> <span data-ttu-id="f0efd-109">В ДКСВА-президент приложение должно указать все параметры каждого из этих кадров.</span><span class="sxs-lookup"><span data-stu-id="f0efd-109">In DXVA-VP, the application must specify all of the VP parameters with each frame.</span></span>

 

<span data-ttu-id="f0efd-110">Состояния устройств делятся на две категории:</span><span class="sxs-lookup"><span data-stu-id="f0efd-110">Device states fall into two categories:</span></span>

-   <span data-ttu-id="f0efd-111">Состояния *потоков* применяют каждый входной поток отдельно.</span><span class="sxs-lookup"><span data-stu-id="f0efd-111">*Stream* states apply each input stream separately.</span></span> <span data-ttu-id="f0efd-112">К каждому потоку можно применить разные параметры.</span><span class="sxs-lookup"><span data-stu-id="f0efd-112">You can apply different settings to each stream.</span></span>
-   <span data-ttu-id="f0efd-113">Состояния *Блит* применяются глобально ко всей Блит обработки видео.</span><span class="sxs-lookup"><span data-stu-id="f0efd-113">*Blit* states apply globally to the entire video processing blit.</span></span>

<span data-ttu-id="f0efd-114">Определены следующие состояния потока.</span><span class="sxs-lookup"><span data-stu-id="f0efd-114">The following stream states are defined.</span></span>



| <span data-ttu-id="f0efd-115">Состояние потока</span><span class="sxs-lookup"><span data-stu-id="f0efd-115">Stream State</span></span>                                   | <span data-ttu-id="f0efd-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f0efd-116">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0efd-117">**ДКСВАХД \_ \_ состояния потока \_ D3DFORMAT**</span><span class="sxs-lookup"><span data-stu-id="f0efd-117">**DXVAHD\_STREAM\_STATE\_D3DFORMAT**</span></span>           | <span data-ttu-id="f0efd-118">Входной формат видео.</span><span class="sxs-lookup"><span data-stu-id="f0efd-118">Input video format.</span></span>                                                                                             |
| <span data-ttu-id="f0efd-119">**\_ \_ \_ Формат кадра состояния потока \_ дксвахд**</span><span class="sxs-lookup"><span data-stu-id="f0efd-119">**DXVAHD\_STREAM\_STATE\_FRAME\_FORMAT**</span></span>       | <span data-ttu-id="f0efd-120">Чередование.</span><span class="sxs-lookup"><span data-stu-id="f0efd-120">Interlacing.</span></span>                                                                                                    |
| <span data-ttu-id="f0efd-121">**\_ \_ \_ \_ цветовое пространство ввода состояния потока дксвахд \_**</span><span class="sxs-lookup"><span data-stu-id="f0efd-121">**DXVAHD\_STREAM\_STATE\_INPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="f0efd-122">Цветное пространство ввода.</span><span class="sxs-lookup"><span data-stu-id="f0efd-122">Input color space.</span></span> <span data-ttu-id="f0efd-123">Это состояние задает диапазон цветов RGB и матрицу передачи Икбкр для входного потока.</span><span class="sxs-lookup"><span data-stu-id="f0efd-123">This state specifies the RGB color range and the YCbCr transfer matrix for the input stream.</span></span> |
| <span data-ttu-id="f0efd-124">**\_ \_ \_ частота вывода состояния потока \_ дксвахд**</span><span class="sxs-lookup"><span data-stu-id="f0efd-124">**DXVAHD\_STREAM\_STATE\_OUTPUT\_RATE**</span></span>        | <span data-ttu-id="f0efd-125">Частота выходных кадров.</span><span class="sxs-lookup"><span data-stu-id="f0efd-125">Output frame rate.</span></span> <span data-ttu-id="f0efd-126">Это состояние управляет преобразованием частоты кадров.</span><span class="sxs-lookup"><span data-stu-id="f0efd-126">This state controls frame-rate conversion.</span></span>                                                   |
| <span data-ttu-id="f0efd-127">**\_ \_ \_ исходный \_ прямоугольник состояния потока дксвахд**</span><span class="sxs-lookup"><span data-stu-id="f0efd-127">**DXVAHD\_STREAM\_STATE\_SOURCE\_RECT**</span></span>        | <span data-ttu-id="f0efd-128">Исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="f0efd-128">Source rectangle.</span></span>                                                                                               |
| <span data-ttu-id="f0efd-129">**\_ \_ \_ целевой \_ прямоугольник состояния потока дксвахд**</span><span class="sxs-lookup"><span data-stu-id="f0efd-129">**DXVAHD\_STREAM\_STATE\_DESTINATION\_RECT**</span></span>   | <span data-ttu-id="f0efd-130">Прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="f0efd-130">Destination rectangle.</span></span>                                                                                          |
| <span data-ttu-id="f0efd-131">**ДКСВАХД \_ потоковое \_ состояние \_ Alpha**</span><span class="sxs-lookup"><span data-stu-id="f0efd-131">**DXVAHD\_STREAM\_STATE\_ALPHA**</span></span>               | <span data-ttu-id="f0efd-132">Плоская альфа-версия.</span><span class="sxs-lookup"><span data-stu-id="f0efd-132">Planar alpha.</span></span>                                                                                                   |
| <span data-ttu-id="f0efd-133">**\_ \_ Палитра состояния потока дксвахд \_**</span><span class="sxs-lookup"><span data-stu-id="f0efd-133">**DXVAHD\_STREAM\_STATE\_PALETTE**</span></span>             | <span data-ttu-id="f0efd-134">Цветовая палитра.</span><span class="sxs-lookup"><span data-stu-id="f0efd-134">Color palette.</span></span> <span data-ttu-id="f0efd-135">Это состояние применяется только к входным форматам палеттизед.</span><span class="sxs-lookup"><span data-stu-id="f0efd-135">This state applies only to palettized input formats.</span></span>                                             |
| <span data-ttu-id="f0efd-136">**\_ \_ \_ ключ яркости состояния потока \_ дксвахд**</span><span class="sxs-lookup"><span data-stu-id="f0efd-136">**DXVAHD\_STREAM\_STATE\_LUMA\_KEY**</span></span>           | <span data-ttu-id="f0efd-137">Ключ яркости.</span><span class="sxs-lookup"><span data-stu-id="f0efd-137">Luma key.</span></span>                                                                                                       |
| <span data-ttu-id="f0efd-138">**пропорции \_ состояния потока дксвахд \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0efd-138">**DXVAHD\_STREAM\_STATE\_ASPECT\_RATIO**</span></span>       | <span data-ttu-id="f0efd-139">Пропорция в пикселях.</span><span class="sxs-lookup"><span data-stu-id="f0efd-139">Pixel aspect ratio.</span></span>                                                                                             |
| <span data-ttu-id="f0efd-140">**\_ \_ Фильтр состояния потока \_ дксвахд \_ XXXX**</span><span class="sxs-lookup"><span data-stu-id="f0efd-140">**DXVAHD\_STREAM\_STATE\_FILTER\_Xxxx**</span></span>        | <span data-ttu-id="f0efd-141">Параметры фильтра изображений.</span><span class="sxs-lookup"><span data-stu-id="f0efd-141">Image filter settings.</span></span> <span data-ttu-id="f0efd-142">Драйвер может поддерживать яркость, контрастность и другие фильтры изображений.</span><span class="sxs-lookup"><span data-stu-id="f0efd-142">The driver can support brightness, contrast, and other image filters.</span></span>                    |



 

<span data-ttu-id="f0efd-143">Определены следующие состояния Блит:</span><span class="sxs-lookup"><span data-stu-id="f0efd-143">The following blit states are defined:</span></span>



| <span data-ttu-id="f0efd-144">Состояние Блит</span><span class="sxs-lookup"><span data-stu-id="f0efd-144">Blit State</span></span>                                   | <span data-ttu-id="f0efd-145">Описание</span><span class="sxs-lookup"><span data-stu-id="f0efd-145">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f0efd-146">**\_ \_ \_ целевой \_ прямоугольник состояния БЛТ дксвахд**</span><span class="sxs-lookup"><span data-stu-id="f0efd-146">**DXVAHD\_BLT\_STATE\_TARGET\_RECT**</span></span>         | <span data-ttu-id="f0efd-147">Целевой прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="f0efd-147">Target rectangle.</span></span>                                                            |
| <span data-ttu-id="f0efd-148">**\_ \_ \_ цвет фона состояния дксвахд \_ БЛТ**</span><span class="sxs-lookup"><span data-stu-id="f0efd-148">**DXVAHD\_BLT\_STATE\_BACKGROUND\_COLOR**</span></span>    | <span data-ttu-id="f0efd-149">Цвет фона.</span><span class="sxs-lookup"><span data-stu-id="f0efd-149">Background color.</span></span>                                                            |
| <span data-ttu-id="f0efd-150">**\_ \_ \_ \_ цветовая область вывода состояния БЛТ дксвахд \_**</span><span class="sxs-lookup"><span data-stu-id="f0efd-150">**DXVAHD\_BLT\_STATE\_OUTPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="f0efd-151">Цветовое пространство вывода.</span><span class="sxs-lookup"><span data-stu-id="f0efd-151">Output color space.</span></span>                                                          |
| <span data-ttu-id="f0efd-152">**\_ \_ \_ Заливка альфа-дксвахд состояния БЛТ \_**</span><span class="sxs-lookup"><span data-stu-id="f0efd-152">**DXVAHD\_BLT\_STATE\_ALPHA\_FILL**</span></span>          | <span data-ttu-id="f0efd-153">Режим заливки альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="f0efd-153">Alpha fill mode.</span></span>                                                             |
| <span data-ttu-id="f0efd-154">**ДКСВАХД \_ БЛТ \_ состояния \_**</span><span class="sxs-lookup"><span data-stu-id="f0efd-154">**DXVAHD\_BLT\_STATE\_CONSTRICTION**</span></span>         | <span data-ttu-id="f0efd-155">Ограничением.</span><span class="sxs-lookup"><span data-stu-id="f0efd-155">Constriction.</span></span> <span data-ttu-id="f0efd-156">Это состояние определяет, довнсамплес ли устройство к выходным данным.</span><span class="sxs-lookup"><span data-stu-id="f0efd-156">This state controls whether the device downsamples the output.</span></span> |



 

<span data-ttu-id="f0efd-157">Чтобы задать состояние потока, вызовите метод [**идксвахд \_ видеопроцессор:: сетвидеопроцессстреамстате**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) .</span><span class="sxs-lookup"><span data-stu-id="f0efd-157">To set a stream state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) method.</span></span> <span data-ttu-id="f0efd-158">Чтобы задать состояние Блит, вызовите метод [**идксвахд \_ видеопроцессор:: сетвидеопроцессблтстате**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) .</span><span class="sxs-lookup"><span data-stu-id="f0efd-158">To set a blit state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) method.</span></span> <span data-ttu-id="f0efd-159">В обоих методах значение перечисления указывает заданное состояние.</span><span class="sxs-lookup"><span data-stu-id="f0efd-159">In both of these methods, an enumeration value specifies the state to set.</span></span> <span data-ttu-id="f0efd-160">Данные о состоянии задаются с помощью структуры данных, зависящей от состояния, которую приложение приводит к **типу \* void** .</span><span class="sxs-lookup"><span data-stu-id="f0efd-160">The state data is given using a state-specific data structure, which the application casts to a **void\*** type.</span></span>

<span data-ttu-id="f0efd-161">В следующем примере кода задается входной формат и прямоугольник назначения для потока 0 и устанавливается черный цвет фона.</span><span class="sxs-lookup"><span data-stu-id="f0efd-161">The following code example sets the input format and destination rectangle for stream 0, and sets the background color to black.</span></span>


```C++
HRESULT SetDXVAHDStates(HWND hwnd, D3DFORMAT inputFormat)
{
    // Set the initial stream states.

    // Set the format of the input stream

    DXVAHD_STREAM_STATE_D3DFORMAT_DATA d3dformat = { inputFormat };

    HRESULT hr = g_pDXVAVP->SetVideoProcessStreamState(
        0,  // Stream index
        DXVAHD_STREAM_STATE_D3DFORMAT,
        sizeof(d3dformat),
        &d3dformat
        );

    if (SUCCEEDED(hr))
    { 
        // For this example, the input stream contains progressive frames.

        DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { DXVAHD_FRAME_FORMAT_PROGRESSIVE };
        
        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index
            DXVAHD_STREAM_STATE_FRAME_FORMAT,
            sizeof(frame_format),
            &frame_format
            );
    }

    if (SUCCEEDED(hr))
    { 
        // Compute the letterbox area.

        RECT rcDest;
        GetClientRect(hwnd, &rcDest);

        RECT rcSrc;
        SetRect(&rcSrc, 0, 0, VIDEO_WIDTH, VIDEO_HEIGHT);

        rcDest = LetterBoxRect(rcSrc, rcDest);

        // Set the destination rectangle, so the frame is displayed within the 
        // letterbox area. Otherwise, the frame is stretched to cover the 
        // entire surface.

        DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA DstRect = { TRUE, rcDest };

        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index 
            DXVAHD_STREAM_STATE_DESTINATION_RECT,
            sizeof(DstRect),
            &DstRect
            );
    }

    if (SUCCEEDED(hr))
    { 
        DXVAHD_COLOR_RGBA rgbBackground = { 0.0f, 0.0f, 0.0f, 1.0f };  // RGBA

        DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA background = { FALSE, rgbBackground };

        hr = g_pDXVAVP->SetVideoProcessBltState(
            DXVAHD_BLT_STATE_BACKGROUND_COLOR,
            sizeof (background),
            &background
            );
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="f0efd-162">См. также</span><span class="sxs-lookup"><span data-stu-id="f0efd-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0efd-163">ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="f0efd-163">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



