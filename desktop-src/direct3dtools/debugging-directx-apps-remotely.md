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
# <a name="debugging-directx-apps-remotely"></a><span data-ttu-id="60a94-103">Удаленная отладка приложений DirectX</span><span class="sxs-lookup"><span data-stu-id="60a94-103">Debugging DirectX apps remotely</span></span>

<span data-ttu-id="60a94-104">Для удаленной отладки приложений DirectX можно использовать Visual Studio и пакет SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="60a94-104">You can use Visual Studio and the Windows 8 SDK to debug DirectX apps remotely.</span></span> <span data-ttu-id="60a94-105">Пакет SDK для Windows 8 предоставляет набор компонентов, поддерживающих разработку DirectX и обеспечивающий проверку ошибок и проверку параметров в дополнение к отладке, предоставляемой Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="60a94-105">The Windows 8 SDK provides a set of components that support DirectX development and provide error checking and parameter validation in addition to the debugging that Visual Studio provides.</span></span> <span data-ttu-id="60a94-106">Эти компоненты D3D11 \_1SDKLayers.dll, D2D1Debug1.dll и Dxgidebug.dll.</span><span class="sxs-lookup"><span data-stu-id="60a94-106">These components are D3D11\_1SDKLayers.dll, D2D1Debug1.dll, and Dxgidebug.dll.</span></span>

<span data-ttu-id="60a94-107">Если требуется удаленная отладка на компьютере без установленного пакета SDK для Windows 8 и требуется такая дополнительная Отладка, необходимо установить пакет удаленной отладки, соответствующий архитектуре, для которого требуется выполнить отладку.</span><span class="sxs-lookup"><span data-stu-id="60a94-107">If you want to debug remotely on a computer without the Windows 8 SDK installed and you want this additional debugging capability, you must install the remote debugging package that is appropriate for the architecture on which you want to debug.</span></span> <span data-ttu-id="60a94-108">Установщик Windows пакеты в `C:\Program Files (x86)\Windows Kits\8.0\Remote\<arch>` установите соответствующую поддержку.</span><span class="sxs-lookup"><span data-stu-id="60a94-108">The Windows Installer Packages in `C:\Program Files (x86)\Windows Kits\8.0\Remote\<arch>` install the appropriate support.</span></span>

<span data-ttu-id="60a94-109">Чтобы включить дополнительные возможности отладки для приложений Direct2D, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="60a94-109">To enable the additional debugging capabilities for Direct2D apps, use this code:</span></span>

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

<span data-ttu-id="60a94-110">Чтобы включить дополнительные возможности отладки для приложений Direct3D, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="60a94-110">To enable the additional debugging capabilities for Direct3D apps, use this code:</span></span>

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

<span data-ttu-id="60a94-111">Дополнительные сведения об отладке приложений Direct2D см. в разделе [уровень отладки Direct2D](/windows/desktop/Direct2D/direct2ddebuglayer-portal).</span><span class="sxs-lookup"><span data-stu-id="60a94-111">For more info about debugging Direct2D apps, see [Direct2D Debug Layer](/windows/desktop/Direct2D/direct2ddebuglayer-portal).</span></span>

<span data-ttu-id="60a94-112">Дополнительные сведения об отладке приложений Direct3D см. в разделе [уровень отладки Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers).</span><span class="sxs-lookup"><span data-stu-id="60a94-112">For more info about debugging Direct3D apps, see [Direct3D Debug Layer](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers).</span></span>