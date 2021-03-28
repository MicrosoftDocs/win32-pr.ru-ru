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
# <a name="how-to-create-a-reference-device"></a>Как создать эталонное устройство

В этом разделе показано, как создать эталонное устройство, которое реализует строго точную программную реализацию среды выполнения. Чтобы создать эталонное устройство, просто укажите, что создаваемое устройство будет использовать справочный драйвер. В этом примере одновременно создается устройство и цепочка буфера обмена.

**Создание эталонного устройства**

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

    

2.  Запросите уровень функций, реализующий функции, которые понадобятся вашему приложению. Можно успешно создать эталонное устройство для среды выполнения Direct3D 11.

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_11_0;
    ```

    

    Дополнительные сведения об уровнях компонентов см. в разделе Перечисление [**\_ \_ уровня функций D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .

3.  Создайте устройство, вызвав [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).


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



Необходимо указать вызов API со ссылочным типом драйвера из перечисления [**\_ \_ типа драйвера D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) . После выполнения метода будет возвращен интерфейс цепочки буферов, интерфейс устройства, указатель на уровень компонента, предоставленный драйвером, и немедленный интерфейс контекста.

Сведения об ограничениях, касающихся создания устройства-образца на определенных уровнях компонентов, см. в разделе [ограничения на создание искривленных и ссылочных устройств](overviews-direct3d-11-devices-limitations.md). [Использование Direct3D 11](how-to-use-direct3d-11.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Устройства](overviews-direct3d-11-devices.md)
</dt> <dt>

[Использование Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




