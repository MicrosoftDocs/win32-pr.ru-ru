---
title: Создание эталонного устройства
description: В этом разделе показано, как создать эталонное устройство, которое реализует строго точную программную реализацию среды выполнения.
ms.assetid: 00d3f5f2-02c6-4ff4-82a9-0726ad4a8cb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dec5f3834bf1f10027da2a3f3a8e22acdee742b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411237"
---
# <a name="how-to-create-a-reference-device"></a><span data-ttu-id="943ba-103">Как создать эталонное устройство</span><span class="sxs-lookup"><span data-stu-id="943ba-103">How To: Create a Reference Device</span></span>

<span data-ttu-id="943ba-104">В этом разделе показано, как создать эталонное устройство, которое реализует строго точную программную реализацию среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="943ba-104">This topic shows how to create a reference device that implements a highly accurate, software implementation of the runtime.</span></span> <span data-ttu-id="943ba-105">Чтобы создать эталонное устройство, просто укажите, что создаваемое устройство будет использовать справочный драйвер.</span><span class="sxs-lookup"><span data-stu-id="943ba-105">To create a reference device, simply specify that the device you are creating will use a reference driver.</span></span> <span data-ttu-id="943ba-106">В этом примере одновременно создается устройство и цепочка буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="943ba-106">This example creates a device and a swap chain at the same time.</span></span>

<span data-ttu-id="943ba-107">**Создание эталонного устройства**</span><span class="sxs-lookup"><span data-stu-id="943ba-107">**To create a reference device**</span></span>

1.  <span data-ttu-id="943ba-108">Определите начальные параметры для цепочки буферов.</span><span class="sxs-lookup"><span data-stu-id="943ba-108">Define initial parameters for a swap chain.</span></span>
    ```
        DXGI_SWAP_CHAIN_DESC sd;
        ZeroMemory( &sd, sizeof( sd ) );
        sd.BufferCount = 1;
        sd.BufferDesc.Width = 640;
        sd.BufferDesc.Height = 480;
        sd.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
        sd.BufferDesc.RefreshRate.Numerator = 60;
        sd.BufferDesc.RefreshRate.Denominator = 1;
        sd.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        sd.OutputWindow = g_hWnd;
        sd.SampleDesc.Count = 1;
        sd.SampleDesc.Quality = 0;
        sd.Windowed = TRUE;
    ```

    

2.  <span data-ttu-id="943ba-109">Запросите уровень функций, реализующий функции, которые понадобятся вашему приложению.</span><span class="sxs-lookup"><span data-stu-id="943ba-109">Request a feature level that implements the features your application will need.</span></span> <span data-ttu-id="943ba-110">Можно успешно создать эталонное устройство для среды выполнения Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="943ba-110">A reference device can be successfully created for the Direct3D 11 runtime.</span></span>

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_11_0;
    ```

    

    <span data-ttu-id="943ba-111">Дополнительные сведения об уровнях компонентов см. в разделе Перечисление [**\_ \_ уровня функций D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="943ba-111">See more about feature levels in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span>

3.  <span data-ttu-id="943ba-112">Создайте устройство, вызвав [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="943ba-112">Create the device by calling [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>


```
    HRESULT hr = S_OK;
    D3D_FEATURE_LEVEL FeatureLevel;

    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_REFERENCE,
                    NULL, 
                    0,
                    &FeatureLevels, 
                    1, 
                    D3D11_SDK_VERSION, 
                    &sd, 
                    &g_pSwapChain, 
                    &g_pd3dDevice, 
                    &FeatureLevel,
                    &g_pImmediateContext )))
    {
        return hr;
    }
```



<span data-ttu-id="943ba-113">Необходимо указать вызов API со ссылочным типом драйвера из перечисления [**\_ \_ типа драйвера D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) .</span><span class="sxs-lookup"><span data-stu-id="943ba-113">You will need to supply the API call with the reference driver type from the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) enumeration.</span></span> <span data-ttu-id="943ba-114">После выполнения метода будет возвращен интерфейс цепочки буферов, интерфейс устройства, указатель на уровень компонента, предоставленный драйвером, и немедленный интерфейс контекста.</span><span class="sxs-lookup"><span data-stu-id="943ba-114">After the method succeeds, it will return a swap chain interface, a device interface, a pointer to the feature level that was granted by the driver, and an immediate context interface.</span></span>

<span data-ttu-id="943ba-115">Сведения об ограничениях, касающихся создания устройства-образца на определенных уровнях компонентов, см. в разделе [ограничения на создание искривленных и ссылочных устройств](overviews-direct3d-11-devices-limitations.md). [Использование Direct3D 11](how-to-use-direct3d-11.md)</span><span class="sxs-lookup"><span data-stu-id="943ba-115">For information about limitations creating a reference device on certain feature levels, see [Limitations Creating WARP and Reference Devices](overviews-direct3d-11-devices-limitations.md).[How to Use Direct3D 11](how-to-use-direct3d-11.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="943ba-116">См. также</span><span class="sxs-lookup"><span data-stu-id="943ba-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="943ba-117">Устройства</span><span class="sxs-lookup"><span data-stu-id="943ba-117">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="943ba-118">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="943ba-118">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




