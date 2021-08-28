---
title: Создание устройства и непосредственный контекст
description: В этом разделе показано, как инициализировать устройство.
ms.assetid: 02a20ada-b3aa-435e-8d66-117a19222f9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a886e27a557d0c7c59b9d92b5df9d180a930d4fe
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625530"
---
# <a name="how-to-create-a-device-and-immediate-context"></a>Как создать устройство и немедленный контекст

В этом разделе показано, как инициализировать [устройство](overviews-direct3d-11-devices-intro.md). Инициализация [устройства](overviews-direct3d-11-devices-intro.md) — одна из первых задач, которую должно завершить приложение, прежде чем можно будет визуализировать сцену.

**Создание устройства и непосредственный контекст**

Заполните [**структуру \_ \_ последовательностей \_ буфера обмена DXGI**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) сведениями о форматах буферов и измерениях. Дополнительные сведения см. в разделе Создание цепочки буферов обмена.

В следующем примере кода показано, как заполнять структуру [**\_ \_ последовательностей \_ буфера обмена DXGI**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) .


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



Используя структуру [**" \_ \_ цепочка \_ буфера обмена DXGI**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) " из первого шага, вызовите [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) для инициализации устройства и цепочки буферов.


```
D3D_FEATURE_LEVEL  FeatureLevelsRequested = D3D_FEATURE_LEVEL_11_0;
UINT               numLevelsRequested = 1;
D3D_FEATURE_LEVEL  FeatureLevelsSupported;

if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                D3D_DRIVER_TYPE_HARDWARE, 
                NULL, 
                0,
                &FeatureLevelsRequested, 
                numFeatureLevelsRequested, 
                D3D11_SDK_VERSION, 
                &sd, 
                &g_pSwapChain, 
                &g_pd3dDevice, 
                &FeatureLevelsSupported,
                &g_pImmediateContext )))
{
    return hr;
}
```



> [!Note]  
> Если вы запрашиваете устройство [**D3D \_ уровня " \_ \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) " на компьютере с только средой выполнения Direct3D 11,0, [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) немедленно завершает работу с **E \_ INVALIDARG**. Чтобы безопасно запросить все возможные уровни функций на компьютере с DirectX 11,0 или DirectX 11,1, используйте следующий код:
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col  />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>const D3D_FEATURE_LEVEL lvl[] = { D3D_FEATURE_LEVEL_11_1, D3D_FEATURE_LEVEL_11_0,
> D3D_FEATURE_LEVEL_10_1, D3D_FEATURE_LEVEL_10_0,
> D3D_FEATURE_LEVEL_9_3, D3D_FEATURE_LEVEL_9_2, D3D_FEATURE_LEVEL_9_1 };
>
> UINT createDeviceFlags = 0;
> #ifdef _DEBUG
> createDeviceFlags |= D3D11_CREATE_DEVICE_DEBUG;
> #endif
>
> ID3D11Device* device = nullptr;
> HRESULT hr = D3D11CreateDeviceAndSwapChain( nullptr, D3D_DRIVER_TYPE_HARDWARE, nullptr, createDeviceFlags, lvl, _countof(lvl), D3D11_SDK_VERSION, &sd, &g_pSwapChain, &g_pd3ddevice, &FeatureLevelsSupported, &g_pImmediateContext );
> if ( hr == E_INVALIDARG )
> {
>     hr = D3D11CreateDeviceAndSwapChain( nullptr, D3D_DRIVER_TYPE_HARDWARE, nullptr, createDeviceFlags, &lvl[1], _countof(lvl) - 1, D3D11_SDK_VERSION, &sd, &g_pSwapChain, &g_pd3ddevice, &FeatureLevelsSupported, &g_pImmediateContext );
> }
>
> if (FAILED(hr))
>     return hr;</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> Создайте представление целевого объекта отрисовки, вызвав [**ID3D11Device:: креатерендертаржетвиев**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview) и привяжите объект заднего буфера в качестве целевого объекта отрисовки, вызвав [**ссылку ID3D11DeviceContext:: омсетрендертаржетс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets).
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col  />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>ID3D11Texture2D* pBackBuffer;
>
> // Get a pointer to the back buffer
> hr = g_pSwapChain->GetBuffer( 0, __uuidof( ID3D11Texture2D ), 
>                              ( LPVOID* )&pBackBuffer );
>
> // Create a render-target view
> g_pd3dDevice->CreateRenderTargetView( pBackBuffer, NULL,
>                                       &g_pRenderTargetView );
>
> // Bind the view
> g_pImmediateContext->OMSetRenderTargets( 1, &g_pRenderTargetView, NULL );</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> Создайте окно просмотра, чтобы определить, какие части целевого объекта отрисовки будут видимы. Определите окно просмотра с помощью [**структуры \_ окна просмотра D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) и задайте окно просмотра с помощью метода [**ссылку ID3D11DeviceContext:: рссетвиевпортс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) .
>
> <span codelanguage="ManagedCPlusPlus"></span>
>
> <table>
> <colgroup>
> <col  />
> </colgroup>
> <thead>
> <tr class="header">
> <th>C++</th>
> </tr>
> </thead>
> <tbody>
> <tr class="odd">
> <td><pre><code>    // Setup the viewport
>     D3D11_VIEWPORT vp;
>     vp.Width = 640;
>     vp.Height = 480;
>     vp.MinDepth = 0.0f;
>     vp.MaxDepth = 1.0f;
>     vp.TopLeftX = 0;
>     vp.TopLeftY = 0;
>     g_pImmediateContext->RSSetViewports( 1, &vp );</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> ## <a name="related-topics"></a>Связанные темы
>
> <dl> <dt>

[Устройства](overviews-direct3d-11-devices.md)
</dt> <dt>

[Использование Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>
>
>  
>
>  
>
