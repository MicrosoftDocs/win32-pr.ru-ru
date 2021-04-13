---
title: Удаленная отладка приложений DirectX
description: Для удаленной отладки приложений DirectX можно использовать Visual Studio и пакет SDK для Windows 8.
ms.assetid: CA471465-47C2-4706-B391-C9E6C2CD69D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55548cd282bf643e16f22177e46643c6e283a909
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413684"
---
# <a name="debugging-directx-apps-remotely"></a>Удаленная отладка приложений DirectX

Для удаленной отладки приложений DirectX можно использовать Visual Studio и пакет SDK для Windows 8. Пакет SDK для Windows 8 предоставляет набор компонентов, поддерживающих разработку DirectX и обеспечивающий проверку ошибок и проверку параметров в дополнение к отладке, предоставляемой Visual Studio. Эти компоненты D3D11 \_1SDKLayers.dll, D2D1Debug1.dll и Dxgidebug.dll.

Если требуется удаленная отладка на компьютере без установленного пакета SDK для Windows 8 и требуется такая дополнительная Отладка, необходимо установить пакет удаленной отладки, соответствующий архитектуре, для которого требуется выполнить отладку. Установщик Windows пакеты в `C:\Program Files (x86)\Windows Kits\8.0\Remote\<arch>` установите соответствующую поддержку.

Чтобы включить дополнительные возможности отладки для приложений Direct2D, используйте следующий код:

```cpp
    D2D1_FACTORY_OPTIONS options;
    ZeroMemory(&options, sizeof(D2D1_FACTORY_OPTIONS));

#if defined(_DEBUG)
     // If the project is in a debug build, enable Direct2D debugging via SDK Layers.
    options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;
#endif

    DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );         
```

Чтобы включить дополнительные возможности отладки для приложений Direct3D, используйте следующий код:

```cpp
    // This flag supports surfaces with a different color channel ordering than the API default.
    // It is recommended usage, and is required for compatibility with Direct2D.
    UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    ComPtr<IDXGIDevice> dxgiDevice;

#if defined(_DEBUG)
    // If the project is in a debug build, enable debugging via SDK Layers with this flag.
    creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
    DX::ThrowIfFailed(
        D3D11CreateDevice(
            nullptr,                    // specify null to use the default adapter
            D3D_DRIVER_TYPE_HARDWARE,
            0,                          // leave as 0 unless software device
            creationFlags,              // optionally set debug and Direct2D compatibility flags
            featureLevels,              // list of feature levels this app can support
            ARRAYSIZE(featureLevels),   // number of entries in above list
            D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION for modern
            &device,                    // returns the Direct3D device created
            &m_featureLevel,            // returns feature level of device created
            &context                    // returns the device immediate context
            )
        );
```

Дополнительные сведения об отладке приложений Direct2D см. в разделе [уровень отладки Direct2D](/windows/desktop/Direct2D/direct2ddebuglayer-portal).

Дополнительные сведения об отладке приложений Direct3D см. в разделе [уровень отладки Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers).