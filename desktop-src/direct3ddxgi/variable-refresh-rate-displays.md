---
description: Для отображения частоты обновления переменных требуется удалить, так как &\# 0034; вертикальной синхронизации-off&\# 0034; support.
ms.assetid: C5F140DD-5BAF-404A-9253-611831C4D424
title: Отображение частоты обновления переменных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349592ce49d1008f6337b53c7f524ac7303907f75cd99205fe79bf55988b934b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118288927"
---
# <a name="variable-refresh-rate-displays"></a>Отображение частоты обновления переменных

Для отображения частоты обновления переменных требуется *разрыв* , так как он также называется «вертикальной синхронизации-Off».

-   [Частота обновления переменной отображается/вертикальной синхронизации отключена](#variable-refresh-rate-displaysvsync-off)
-   [Связанные темы](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a>Частота обновления переменной отображается/вертикальной синхронизации отключена

Поддержка отображения частоты обновления переменных достигается путем установки определенных флагов при создании и представлении цепочки буферов.

чтобы использовать эту функцию, пользователи приложений должны быть в Windows 10 системах с установленным [KB3156421](https://support.microsoft.com/kb/3156421) или годовщиной. Эта функция работает во всех версиях Direct3D 11 и 12, использующих эффекты подкачки с **\_ \_ \_ \_ \* эффектом переключения DXGI** .

Чтобы добавить в приложения поддержку вертикальной синхронизации, можно обратиться к полному выполняющемуся примеру для Direct3D 12, **D3D12Fullscreen** (см. [рабочие образцы](../direct3d12/working-samples.md)). Кроме того, в примере кода есть несколько точек, которые не были явно вызваны, но необходимо обратить внимание на.

-   [**Ресизебуфферс**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (или [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) должен иметь один и тот же флаг создания цепочки подкачки ( \_ \_ флаг цепочки переключения DXGI, \_ \_ разрешающий \_ разрыв), переданный в него (или [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)). [](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present)
-   \_Присутствующая возможность удаления \_ \_ с помощью DXGI может использоваться только с интервалом синхронизации 0. Рекомендуется всегда передавать этот флаг разрыва при использовании интервала синхронизации 0, если [**чеккфеатуресуппорт**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) сообщает, что разрывы поддерживаются *и* приложение находится в оконном режиме, включая полноэкранный режим без рамки. Дополнительные сведения см. в статье константы [**DXGI \_ Present**](dxgi-present.md) .
-   Отключение вертикальной синхронизации не обязательно ункап частоту кадров. разработчикам также [**необходимо убедиться, что вызовы**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) не регулируются другими событиями времени (например, `CompositionTarget::Rendering` событием в приложении на основе XAML).

Приведенный ниже код предменяет несколько ключевых частей, которые необходимо добавить в приложения.

``` syntax
//--------------------------------------------------------------------------------------------------------
// Check Tearing Support
//--------------------------------------------------------------------------------------------------------

// Determines whether tearing support is available for fullscreen borderless windows.

void DXSample::CheckTearingSupport()
{
// Rather than create the 1.5 factory interface directly, we create the 1.4
// interface and query for the 1.5 interface. This will enable the graphics
// debugging tools which might not support the 1.5 factory interface.

    ComPtr<IDXGIFactory4> factory4;
    HRESULT hr = CreateDXGIFactory1(IID_PPV_ARGS(&factory4));
    BOOL allowTearing = FALSE;
    if (SUCCEEDED(hr))
    { 
        ComPtr<IDXGIFactory5> factory5;
        hr = factory4.As(&factory5);
        if (SUCCEEDED(hr))
        {
            hr = factory5->CheckFeatureSupport(DXGI_FEATURE_PRESENT_ALLOW_TEARING, &allowTearing, sizeof(allowTearing));
        }
    }
    m_tearingSupport = SUCCEEDED(hr) && allowTearing;
}

//--------------------------------------------------------------------------------------------------------
// Set up swapchain properly
//--------------------------------------------------------------------------------------------------------

// It is recommended to always use the tearing flag when it is supported.
swapChainDesc.Flags = m_tearingSupport ? DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING : 0;

//--------------------------------------------------------------------------------------------------------
// Present
//--------------------------------------------------------------------------------------------------------

UINT presentFlags = (m_tearingSupport && m_windowedMode) ? DXGI_PRESENT_ALLOW_TEARING : 0;

// Present the frame.
ThrowIfFailed(m_swapChain->Present(0, presentFlags));
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Усовершенствования DXGI 1,5](dxgi-1-5-improvements.md)
</dt> <dt>

[Руководством по программированию для DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
