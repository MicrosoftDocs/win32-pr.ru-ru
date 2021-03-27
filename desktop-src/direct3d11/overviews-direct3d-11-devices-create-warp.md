---
title: Создание устройства деформации
description: В этом разделе показано, как создать устройство деформации, которое реализует средство программной прорисовки с высокой скоростью.
ms.assetid: 6daf661e-bc24-4b90-83a7-031acb57cf87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deda409971d22f46132a1cb9b008d3dd1eb7c407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997110"
---
# <a name="how-to-create-a-warp-device"></a><span data-ttu-id="6797a-103">Как создать устройство деформации</span><span class="sxs-lookup"><span data-stu-id="6797a-103">How To: Create a WARP Device</span></span>

<span data-ttu-id="6797a-104">В этом разделе показано, как создать устройство деформации, которое реализует средство программной прорисовки с высокой скоростью.</span><span class="sxs-lookup"><span data-stu-id="6797a-104">This topic shows how to create a WARP device that implements a high speed software rasterizer.</span></span> <span data-ttu-id="6797a-105">Чтобы создать устройство деформации, просто укажите, что создаваемое устройство будет использовать драйвер деформации.</span><span class="sxs-lookup"><span data-stu-id="6797a-105">To create a WARP device, simply specify that the device you are creating will use a WARP driver.</span></span> <span data-ttu-id="6797a-106">В этом примере одновременно создается устройство и цепочка буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="6797a-106">This example creates a device and a swap chain at the same time.</span></span>

<span data-ttu-id="6797a-107">**Создание устройства деформации**</span><span class="sxs-lookup"><span data-stu-id="6797a-107">**To create a WARP device**</span></span>

1.  <span data-ttu-id="6797a-108">Определите начальные параметры для цепочки буферов.</span><span class="sxs-lookup"><span data-stu-id="6797a-108">Define initial parameters for a swap chain.</span></span>
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

    

2.  <span data-ttu-id="6797a-109">Запросите уровень функций, реализующий функции, которые понадобятся вашему приложению.</span><span class="sxs-lookup"><span data-stu-id="6797a-109">Request a feature level that implements the features your application will need.</span></span> <span data-ttu-id="6797a-110">Устройство деформации можно успешно создать для уровней компонентов **D3D \_ \_ уровня \_ 9 \_ 1** до **D3D \_ \_ уровня \_ 10 \_ 1** и начиная с Windows 8 для всех уровней компонентов.</span><span class="sxs-lookup"><span data-stu-id="6797a-110">A WARP device can be successfully created for feature levels **D3D\_FEATURE\_LEVEL\_9\_1** through **D3D\_FEATURE\_LEVEL\_10\_1** and starting with Windows 8 for all feature levels.</span></span>

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    <span data-ttu-id="6797a-111">Дополнительные сведения об уровнях компонентов см. в разделе Перечисление [**\_ \_ уровня функций D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="6797a-111">See more about feature levels in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span>

3.  <span data-ttu-id="6797a-112">Создайте устройство, вызвав [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="6797a-112">Create the device by calling [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>


```
    HRESULT hr = S_OK;
    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_WARP,
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



<span data-ttu-id="6797a-113">Необходимо указать вызов API с типом драйвера ИСКРИВЛЕНия из перечисления [**\_ \_ типа драйвера D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) .</span><span class="sxs-lookup"><span data-stu-id="6797a-113">You will need to supply the API call with the WARP driver type from the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) enumeration.</span></span> <span data-ttu-id="6797a-114">После выполнения метода будет возвращен интерфейс цепочки буферов, интерфейс устройства, указатель на уровень компонента, предоставленный драйвером, и немедленный интерфейс контекста.</span><span class="sxs-lookup"><span data-stu-id="6797a-114">After the method succeeds, it will return a swap chain interface, a device interface, a pointer to the feature level that was granted by the driver, and an immediate context interface.</span></span>

<span data-ttu-id="6797a-115">Сведения об ограничениях, создающих устройство деформации на определенных уровнях компонентов, см. в разделе [ограничения на создание искривленных и ссылочных устройств](overviews-direct3d-11-devices-limitations.md).</span><span class="sxs-lookup"><span data-stu-id="6797a-115">For information about limitations creating a WARP device on certain feature levels, see [Limitations Creating WARP and Reference Devices](overviews-direct3d-11-devices-limitations.md).</span></span>

## <a name="new-for-windows-8"></a><span data-ttu-id="6797a-116">Новые для Windows 8</span><span class="sxs-lookup"><span data-stu-id="6797a-116">New for Windows 8</span></span>

<span data-ttu-id="6797a-117">Если основным видеоадаптером компьютера является адаптер Microsoft Basic (адаптер деформации), этот компьютер также имеет второй адаптер.</span><span class="sxs-lookup"><span data-stu-id="6797a-117">When a computer's primary display adapter is the "Microsoft Basic Display Adapter" (WARP adapter), that computer also has a second adapter.</span></span> <span data-ttu-id="6797a-118">Вторым адаптером является устройство, предназначенное только для просмотра и не имеющее выходных данных вывода.</span><span class="sxs-lookup"><span data-stu-id="6797a-118">This second adapter is the render-only device that has no display outputs.</span></span> <span data-ttu-id="6797a-119">Дополнительные сведения об устройстве, предназначенном только для просмотра, см. [в разделе новые сведения в Windows 8 о перечислении адаптеров](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).</span><span class="sxs-lookup"><span data-stu-id="6797a-119">For more info about the render-only device, see [new info in Windows 8 about enumerating adapters](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6797a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="6797a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6797a-121">Устройства</span><span class="sxs-lookup"><span data-stu-id="6797a-121">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="6797a-122">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="6797a-122">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 