---
description: Создание видеопроцессора ДКСВА-HD
ms.assetid: 43a97dc8-19b3-412c-a015-339099bf4f6c
title: Создание видеопроцессора ДКСВА-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4945153dfd3e14f1d2caae9b0a84f201745ea24722781bf998930477054138c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974823"
---
# <a name="creating-a-dxva-hd-video-processor"></a>Создание видеопроцессора ДКСВА-HD

High Definition (ДКСВА-HD) ускорение видео Microsoft DirectX использует два основных интерфейса:

-   [**Идксвахд \_ Устройство**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device). Представляет устройство ДКСВА-HD. Используйте этот интерфейс для запроса возможностей устройства и создания обработчика видео.
-   [**Идксвахд \_ Видеопроцессор**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor). Представляет набор возможностей обработки видео. Используйте этот интерфейс для выполнения Блит обработки видео.

В приведенном ниже коде предполагается наличие следующих глобальных переменных:


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



Создание видеопроцессора ДКСВА-HD:

1.  Заполните структуру [**дксвахд содержимого в виде \_ \_**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) описания содержимого видео. Драйвер использует эти сведения в качестве подсказки для оптимизации возможностей обработчика видео. Структура не содержит полного описания формата.
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

    

2.  Вызовите [**дксвахд \_ креатедевице**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) , чтобы создать устройство дксва-HD. Эта функция возвращает указатель на интерфейс [**\_ устройства идксвахд**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) .
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  Вызовите [**идксвахд \_ Device:: жетвидеопроцессордевицекапс**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps). Этот метод заполняет структуру [**\_ впдевкапс дксвахд**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) с помощью возможностей устройства. Если требуются определенные функции обработки видео, такие как яркостиный ключ или фильтрация изображений, проверьте их доступность с помощью этой структуры.
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  Убедитесь, что устройство ДКСВА-HD поддерживает необходимые входные форматы видео. Раздел [Проверка поддерживаемых форматов дксва-HD](checking-supported-dxva-hd-formats.md) подробно описывает этот шаг.
5.  Проверьте, поддерживает ли устройство ДКСВА-HD формат выходных данных, который вам нужен. Раздел [Проверка поддерживаемых форматов дксва-HD](checking-supported-dxva-hd-formats.md) подробно описывает этот шаг.
6.  Выделение массива структур [**\_ впкапс дксвахд**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) . Число элементов массива, которые должны быть выделены, определяется элементом **видеопроцессоркаунт** структуры [**\_ впдевкапс дксвахд**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) , полученным на шаге 3.
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  Каждая [**Структура \_ впкапс дксвахд**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) представляет отдельный обработчик видео. Вы можете пробрать этот массив, чтобы узнать о возможностях каждого обработчика видео. Структура включает сведения о возможностях преобразования чередования, чересстрочности и скорости кадров обработчика видео.
8.  Выберите обработчик видео для создания. Элемент **впгуид** структуры [**\_ впкапс дксвахд**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) содержит идентификатор GUID, который однозначно идентифицирует обработчик видео. Передайте этот идентификатор GUID методу [**идксвахд \_ устройства:: креатевидеопроцессор**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) . Метод возвращает указатель [**\_ видеопроцессор идксвахд**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) .
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  При необходимости вызовите [**идксвахд \_ Device:: креатевидеосурфаце**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) , чтобы создать массив входных поверхностей видео.

В следующем примере кода показана полная последовательность шагов.


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



Функция Креатевпдевице, показанная в этом примере, создает обработчик видео (шаги 5 – 7):


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[ДКСВА-HD](dxva-hd.md)
</dt> </dl>

 

 



