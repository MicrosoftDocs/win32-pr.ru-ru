---
description: Создание видеопроцессора ДКСВА-HD
ms.assetid: 43a97dc8-19b3-412c-a015-339099bf4f6c
title: Создание видеопроцессора ДКСВА-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89c5a361335f83296eec538a5a6a710b9e19604
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102602"
---
# <a name="creating-a-dxva-hd-video-processor"></a><span data-ttu-id="a6672-103">Создание видеопроцессора ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="a6672-103">Creating a DXVA-HD Video Processor</span></span>

<span data-ttu-id="a6672-104">High Definition (ДКСВА-HD) ускорение видео Microsoft DirectX использует два основных интерфейса:</span><span class="sxs-lookup"><span data-stu-id="a6672-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) uses two primary interfaces:</span></span>

-   <span data-ttu-id="a6672-105">[**Идксвахд \_ Устройство**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span><span class="sxs-lookup"><span data-stu-id="a6672-105">[**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span></span> <span data-ttu-id="a6672-106">Представляет устройство ДКСВА-HD.</span><span class="sxs-lookup"><span data-stu-id="a6672-106">Represents the DXVA-HD device.</span></span> <span data-ttu-id="a6672-107">Используйте этот интерфейс для запроса возможностей устройства и создания обработчика видео.</span><span class="sxs-lookup"><span data-stu-id="a6672-107">Use this interface to query the device capabilities and create the video processor.</span></span>
-   <span data-ttu-id="a6672-108">[**Идксвахд \_ Видеопроцессор**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span><span class="sxs-lookup"><span data-stu-id="a6672-108">[**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span></span> <span data-ttu-id="a6672-109">Представляет набор возможностей обработки видео.</span><span class="sxs-lookup"><span data-stu-id="a6672-109">Represents a set of video processing capabilities.</span></span> <span data-ttu-id="a6672-110">Используйте этот интерфейс для выполнения Блит обработки видео.</span><span class="sxs-lookup"><span data-stu-id="a6672-110">Use this interface to perform the video processing blit.</span></span>

<span data-ttu-id="a6672-111">В приведенном ниже коде предполагается наличие следующих глобальных переменных:</span><span class="sxs-lookup"><span data-stu-id="a6672-111">In the code that follows, the following global variables are assumed:</span></span>


```C++
IDirect3D9Ex            *g_pD3D = NULL;     
IDirect3DDevice9Ex      *g_pD3DDevice = NULL;   // Direct3D device.
IDXVAHD_Device          *g_pDXVAHD = NULL;      // DXVA-HD device.
IDXVAHD_VideoProcessor  *g_pDXVAVP = NULL;      // DXVA-HD video processor.
IDirect3DSurface9       *g_pSurface = NULL;     // Video surface.
        
const D3DFORMAT     RENDER_TARGET_FORMAT = D3DFMT_X8R8G8B8;
const D3DFORMAT     VIDEO_FORMAT         = D3DFMT_X8R8G8B8; 
const UINT          VIDEO_FPS            = 60;
const UINT          VIDEO_WIDTH          = 640;
const UINT          VIDEO_HEIGHT         = 480;
```



<span data-ttu-id="a6672-112">Создание видеопроцессора ДКСВА-HD:</span><span class="sxs-lookup"><span data-stu-id="a6672-112">To create a DXVA-HD video processor:</span></span>

1.  <span data-ttu-id="a6672-113">Заполните структуру [**дксвахд содержимого в виде \_ \_**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) описания содержимого видео.</span><span class="sxs-lookup"><span data-stu-id="a6672-113">Fill in a [**DXVAHD\_CONTENT\_DESC**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) structure with a description of the video content.</span></span> <span data-ttu-id="a6672-114">Драйвер использует эти сведения в качестве подсказки для оптимизации возможностей обработчика видео.</span><span class="sxs-lookup"><span data-stu-id="a6672-114">The driver uses this information as a hint to optimize the capabilities of the video processor.</span></span> <span data-ttu-id="a6672-115">Структура не содержит полного описания формата.</span><span class="sxs-lookup"><span data-stu-id="a6672-115">The structure does not contain a complete format description.</span></span>
    ```C++
        DXVAHD_RATIONAL fps = { VIDEO_FPS, 1 }; 

        DXVAHD_CONTENT_DESC desc;

        desc.InputFrameFormat = DXVAHD_FRAME_FORMAT_PROGRESSIVE;
        desc.InputFrameRate = fps;
        desc.InputWidth = VIDEO_WIDTH;
        desc.InputHeight = VIDEO_HEIGHT;
        desc.OutputFrameRate = fps;
        desc.OutputWidth = VIDEO_WIDTH;
        desc.OutputHeight = VIDEO_HEIGHT;
    ```

    

2.  <span data-ttu-id="a6672-116">Вызовите [**дксвахд \_ креатедевице**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) , чтобы создать устройство дксва-HD.</span><span class="sxs-lookup"><span data-stu-id="a6672-116">Call [**DXVAHD\_CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) to create the DXVA-HD device.</span></span> <span data-ttu-id="a6672-117">Эта функция возвращает указатель на интерфейс [**\_ устройства идксвахд**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) .</span><span class="sxs-lookup"><span data-stu-id="a6672-117">This function returns a pointer to the [**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) interface.</span></span>
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  <span data-ttu-id="a6672-118">Вызовите [**идксвахд \_ Device:: жетвидеопроцессордевицекапс**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span><span class="sxs-lookup"><span data-stu-id="a6672-118">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span></span> <span data-ttu-id="a6672-119">Этот метод заполняет структуру [**\_ впдевкапс дксвахд**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) с помощью возможностей устройства.</span><span class="sxs-lookup"><span data-stu-id="a6672-119">This method fills in a [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure with the device capabilities.</span></span> <span data-ttu-id="a6672-120">Если требуются определенные функции обработки видео, такие как яркостиный ключ или фильтрация изображений, проверьте их доступность с помощью этой структуры.</span><span class="sxs-lookup"><span data-stu-id="a6672-120">If you require specific video processing features, such as luma keying or image filtering, check their availability by using this structure.</span></span>
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  <span data-ttu-id="a6672-121">Убедитесь, что устройство ДКСВА-HD поддерживает необходимые входные форматы видео.</span><span class="sxs-lookup"><span data-stu-id="a6672-121">Check whether the DXVA-HD device supports the input video formats that you require.</span></span> <span data-ttu-id="a6672-122">Раздел [Проверка поддерживаемых форматов дксва-HD](checking-supported-dxva-hd-formats.md) подробно описывает этот шаг.</span><span class="sxs-lookup"><span data-stu-id="a6672-122">The topic [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
5.  <span data-ttu-id="a6672-123">Проверьте, поддерживает ли устройство ДКСВА-HD формат выходных данных, который вам нужен.</span><span class="sxs-lookup"><span data-stu-id="a6672-123">Check whether the DXVA-HD device supports the output format that you require.</span></span> <span data-ttu-id="a6672-124">Раздел [Проверка поддерживаемых форматов дксва-HD](checking-supported-dxva-hd-formats.md) подробно описывает этот шаг.</span><span class="sxs-lookup"><span data-stu-id="a6672-124">The section [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
6.  <span data-ttu-id="a6672-125">Выделение массива структур [**\_ впкапс дксвахд**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) .</span><span class="sxs-lookup"><span data-stu-id="a6672-125">Allocate an array of [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structures.</span></span> <span data-ttu-id="a6672-126">Число элементов массива, которые должны быть выделены, определяется элементом **видеопроцессоркаунт** структуры [**\_ впдевкапс дксвахд**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) , полученным на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="a6672-126">The number of array elements that must be allocated is given by the **VideoProcessorCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure, obtained in step 3.</span></span>
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  <span data-ttu-id="a6672-127">Каждая [**Структура \_ впкапс дксвахд**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) представляет отдельный обработчик видео.</span><span class="sxs-lookup"><span data-stu-id="a6672-127">Each [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure represents a distinct video processor.</span></span> <span data-ttu-id="a6672-128">Вы можете пробрать этот массив, чтобы узнать о возможностях каждого обработчика видео.</span><span class="sxs-lookup"><span data-stu-id="a6672-128">You can loop through this array to discover the capabilities of each video processor.</span></span> <span data-ttu-id="a6672-129">Структура включает сведения о возможностях преобразования чередования, чересстрочности и скорости кадров обработчика видео.</span><span class="sxs-lookup"><span data-stu-id="a6672-129">The structure includes information about the deinterlacing, telecine, and frame-rate conversion capabilities of the video processor.</span></span>
8.  <span data-ttu-id="a6672-130">Выберите обработчик видео для создания.</span><span class="sxs-lookup"><span data-stu-id="a6672-130">Select a video processor to create.</span></span> <span data-ttu-id="a6672-131">Элемент **впгуид** структуры [**\_ впкапс дксвахд**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) содержит идентификатор GUID, который однозначно идентифицирует обработчик видео.</span><span class="sxs-lookup"><span data-stu-id="a6672-131">The **VPGuid** member of the [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure contains a GUID that uniquely identifies the video processor.</span></span> <span data-ttu-id="a6672-132">Передайте этот идентификатор GUID методу [**идксвахд \_ устройства:: креатевидеопроцессор**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) .</span><span class="sxs-lookup"><span data-stu-id="a6672-132">Pass this GUID to the [**IDXVAHD\_Device::CreateVideoProcessor**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) method.</span></span> <span data-ttu-id="a6672-133">Метод возвращает указатель [**\_ видеопроцессор идксвахд**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) .</span><span class="sxs-lookup"><span data-stu-id="a6672-133">The method returns an [**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) pointer.</span></span>
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  <span data-ttu-id="a6672-134">При необходимости вызовите [**идксвахд \_ Device:: креатевидеосурфаце**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) , чтобы создать массив входных поверхностей видео.</span><span class="sxs-lookup"><span data-stu-id="a6672-134">Optionally, call [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) to create an array of input video surfaces.</span></span>

<span data-ttu-id="a6672-135">В следующем примере кода показана полная последовательность шагов.</span><span class="sxs-lookup"><span data-stu-id="a6672-135">The following code example shows the complete sequence of steps:</span></span>


```C++
// Initializes the DXVA-HD video processor.

// NOTE: The following example makes some simplifying assumptions:
//
// 1. There is a single input stream.
// 2. The input frame rate matches the output frame rate.
// 3. No advanced DXVA-HD features are needed, such as luma keying or IVTC.
// 4. The application uses a single input video surface.

HRESULT InitializeDXVAHD()
{
    if (g_pD3DDevice == NULL)
    {
        return E_FAIL;
    }

    HRESULT hr = S_OK;

    IDXVAHD_Device          *pDXVAHD = NULL;
    IDXVAHD_VideoProcessor  *pDXVAVP = NULL;
    IDirect3DSurface9       *pSurf = NULL;

    DXVAHD_RATIONAL fps = { VIDEO_FPS, 1 }; 

    DXVAHD_CONTENT_DESC desc;

    desc.InputFrameFormat = DXVAHD_FRAME_FORMAT_PROGRESSIVE;
    desc.InputFrameRate = fps;
    desc.InputWidth = VIDEO_WIDTH;
    desc.InputHeight = VIDEO_HEIGHT;
    desc.OutputFrameRate = fps;
    desc.OutputWidth = VIDEO_WIDTH;
    desc.OutputHeight = VIDEO_HEIGHT;

#ifdef USE_SOFTWARE_PLUGIN    
    HMODULE hSWPlugin = LoadLibrary(L"C:\\dxvahdsw.dll");

    PDXVAHDSW_Plugin pSWPlugin = (PDXVAHDSW_Plugin)GetProcAddress(hSWPlugin, "DXVAHDSW_Plugin");

    hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc,DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
        pSWPlugin, &pDXVAHD);
#else
    hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
        NULL, &pDXVAHD);
#endif
    if (FAILED(hr))
    {
        goto done;
    }

    DXVAHD_VPDEVCAPS caps;

    hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    if (FAILED(hr))
    {
        goto done;
    }

    // Check whether the device supports the input and output formats.

    hr = CheckInputFormatSupport(pDXVAHD, caps, VIDEO_FORMAT);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CheckOutputFormatSupport(pDXVAHD, caps, RENDER_TARGET_FORMAT);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the VP device.
    hr = CreateVPDevice(pDXVAHD, caps, &pDXVAVP);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the video surface for the primary video stream.
    hr = pDXVAHD->CreateVideoSurface(
        VIDEO_WIDTH,
        VIDEO_HEIGHT,
        VIDEO_FORMAT,
        caps.InputPool,
        0,  // Usage
        DXVAHD_SURFACE_TYPE_VIDEO_INPUT,
        1,      // Number of surfaces to create
        &pSurf, // Array of surface pointers
        NULL
        );

    if (FAILED(hr))
    {
        goto done;
    }


    g_pDXVAHD = pDXVAHD;
    g_pDXVAHD->AddRef();

    g_pDXVAVP = pDXVAVP;
    g_pDXVAVP->AddRef();

    g_pSurface = pSurf;
    g_pSurface->AddRef();

done:
    SafeRelease(&pDXVAHD);
    SafeRelease(&pDXVAVP);
    SafeRelease(&pSurf);
    return hr;
}
```



<span data-ttu-id="a6672-136">Функция Креатевпдевице, показанная в этом примере, создает обработчик видео (шаги 5 – 7):</span><span class="sxs-lookup"><span data-stu-id="a6672-136">The CreateVPDevice function show in this example creates the video processor (steps 5–7):</span></span>


```C++
// Creates a DXVA-HD video processor.

HRESULT CreateVPDevice(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    IDXVAHD_VideoProcessor  **ppDXVAVP
    )
{
    // Create the array of video processor caps. 
    
    DXVAHD_VPCAPS *pVPCaps = 
        new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

    if (pVPCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
        caps.VideoProcessorCount, pVPCaps);

    // At this point, an application could loop through the array and examine
    // the capabilities. For purposes of this example, however, we simply
    // create the first video processor in the list.

    if (SUCCEEDED(hr))
    {
        // The VPGuid member contains the GUID that identifies the video 
        // processor.

        hr = pDXVAHD->CreateVideoProcessor(&pVPCaps[0].VPGuid, ppDXVAVP);
    }

    delete [] pVPCaps;
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="a6672-137">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="a6672-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6672-138">ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="a6672-138">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



