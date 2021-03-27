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
# <a name="how-to-create-a-warp-device"></a>Как создать устройство деформации

В этом разделе показано, как создать устройство деформации, которое реализует средство программной прорисовки с высокой скоростью. Чтобы создать устройство деформации, просто укажите, что создаваемое устройство будет использовать драйвер деформации. В этом примере одновременно создается устройство и цепочка буфера обмена.

**Создание устройства деформации**

1.  Определите начальные параметры для цепочки буферов.
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

    

2.  Запросите уровень функций, реализующий функции, которые понадобятся вашему приложению. Устройство деформации можно успешно создать для уровней компонентов **D3D \_ \_ уровня \_ 9 \_ 1** до **D3D \_ \_ уровня \_ 10 \_ 1** и начиная с Windows 8 для всех уровней компонентов.

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    Дополнительные сведения об уровнях компонентов см. в разделе Перечисление [**\_ \_ уровня функций D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .

3.  Создайте устройство, вызвав [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).


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



Необходимо указать вызов API с типом драйвера ИСКРИВЛЕНия из перечисления [**\_ \_ типа драйвера D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) . После выполнения метода будет возвращен интерфейс цепочки буферов, интерфейс устройства, указатель на уровень компонента, предоставленный драйвером, и немедленный интерфейс контекста.

Сведения об ограничениях, создающих устройство деформации на определенных уровнях компонентов, см. в разделе [ограничения на создание искривленных и ссылочных устройств](overviews-direct3d-11-devices-limitations.md).

## <a name="new-for-windows-8"></a>Новые для Windows 8

Если основным видеоадаптером компьютера является адаптер Microsoft Basic (адаптер деформации), этот компьютер также имеет второй адаптер. Вторым адаптером является устройство, предназначенное только для просмотра и не имеющее выходных данных вывода. Дополнительные сведения об устройстве, предназначенном только для просмотра, см. [в разделе новые сведения в Windows 8 о перечислении адаптеров](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Устройства](overviews-direct3d-11-devices.md)
</dt> <dt>

[Использование Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 