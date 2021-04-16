---
description: Для отображения частоты обновления переменных требуется удалить, так как &\# 0034; вертикальной синхронизации-off&\# 0034; support.
ms.assetid: C5F140DD-5BAF-404A-9253-611831C4D424
title: Отображение частоты обновления переменных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da6e658d84c51a6b51bc32855226194b9c22507e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262357"
---
# <a name="variable-refresh-rate-displays"></a><span data-ttu-id="91833-103">Отображение частоты обновления переменных</span><span class="sxs-lookup"><span data-stu-id="91833-103">Variable refresh rate displays</span></span>

<span data-ttu-id="91833-104">Для отображения частоты обновления переменных требуется *разрыв* , так как он также называется «вертикальной синхронизации-Off».</span><span class="sxs-lookup"><span data-stu-id="91833-104">Variable refresh rate displays require *tearing* to be enabled, this is also known as "vsync-off" support.</span></span>

-   [<span data-ttu-id="91833-105">Частота обновления переменной отображается/вертикальной синхронизации отключена</span><span class="sxs-lookup"><span data-stu-id="91833-105">Variable refresh rate displays/Vsync off</span></span>](#variable-refresh-rate-displaysvsync-off)
-   [<span data-ttu-id="91833-106">См. также</span><span class="sxs-lookup"><span data-stu-id="91833-106">Related topics</span></span>](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a><span data-ttu-id="91833-107">Частота обновления переменной отображается/вертикальной синхронизации отключена</span><span class="sxs-lookup"><span data-stu-id="91833-107">Variable refresh rate displays/Vsync off</span></span>

<span data-ttu-id="91833-108">Поддержка отображения частоты обновления переменных достигается путем установки определенных флагов при создании и представлении цепочки буферов.</span><span class="sxs-lookup"><span data-stu-id="91833-108">Support for variable refresh rate displays is achieved by setting certain flags when creating and presenting the swap chain.</span></span>

<span data-ttu-id="91833-109">Чтобы использовать эту функцию, пользователи приложений должны быть в системах Windows 10 с либо [KB3156421](https://support.microsoft.com/kb/3156421) , либо годовщиной установки.</span><span class="sxs-lookup"><span data-stu-id="91833-109">To use this feature, app users need to be on Windows 10 systems with either [KB3156421](https://support.microsoft.com/kb/3156421) or the Anniversary Update installed.</span></span> <span data-ttu-id="91833-110">Эта функция работает во всех версиях Direct3D 11 и 12 с использованием \**\_ \_ эффекта \_ перелистывания \_ \* для эффектов переключения DXGI*.</span><span class="sxs-lookup"><span data-stu-id="91833-110">The feature works on all versions of Direct3D 11 and 12 using \**DXGI\_SWAP\_EFFECT\_FLIP\_\** _ swap effects.</span></span>

<span data-ttu-id="91833-111">Чтобы добавить в приложения поддержку вертикальной синхронизации, можно обратиться к полному выполняющемуся примеру для Direct3D 12, _ *D3D12Fullscreen*\* (см. [рабочие образцы](../direct3d12/working-samples.md)).</span><span class="sxs-lookup"><span data-stu-id="91833-111">To add vsync-off support to your apps, you can refer to a complete running sample for Direct3D 12, _ *D3D12Fullscreen*\* (refer to [Working Samples](../direct3d12/working-samples.md)).</span></span> <span data-ttu-id="91833-112">Кроме того, в примере кода есть несколько точек, которые не были явно вызваны, но необходимо обратить внимание на.</span><span class="sxs-lookup"><span data-stu-id="91833-112">There are also a few points not explicitly called out in the sample code but you need to pay attention to.</span></span>

-   <span data-ttu-id="91833-113">[**Ресизебуфферс**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (или [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) должен иметь один и тот же флаг создания цепочки подкачки ( \_ \_ флаг цепочки переключения DXGI, \_ \_ разрешающий \_ разрыв), переданный в него (или [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)). [](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present)</span><span class="sxs-lookup"><span data-stu-id="91833-113">[**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (or [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) must have the same swap chain creation flag (DXGI\_SWAP\_CHAIN\_FLAG\_ALLOW\_TEARING) passed to it as [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (or [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).</span></span>
-   <span data-ttu-id="91833-114">\_Присутствующая возможность удаления \_ \_ с помощью DXGI может использоваться только с интервалом синхронизации 0.</span><span class="sxs-lookup"><span data-stu-id="91833-114">DXGI\_PRESENT\_ALLOW\_TEARING can only be used with sync interval 0.</span></span> <span data-ttu-id="91833-115">Рекомендуется всегда передавать этот флаг разрыва при использовании интервала синхронизации 0, если [**чеккфеатуресуппорт**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) сообщает, что разрывы поддерживаются *и* приложение находится в оконном режиме, включая полноэкранный режим без рамки.</span><span class="sxs-lookup"><span data-stu-id="91833-115">It is recommended to always pass this tearing flag when using sync interval 0 if [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) reports that tearing is supported *and* the app is in a windowed mode - including border-less fullscreen mode.</span></span> <span data-ttu-id="91833-116">Дополнительные сведения см. в статье константы [**DXGI \_ Present**](dxgi-present.md) .</span><span class="sxs-lookup"><span data-stu-id="91833-116">Refer to the [**DXGI\_PRESENT**](dxgi-present.md) constants for more details.</span></span>
-   <span data-ttu-id="91833-117">Отключение вертикальной синхронизации не обязательно ункап частоту кадров. разработчикам также [**необходимо убедиться, что вызовы**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) не регулируются другими событиями времени (например, `CompositionTarget::Rendering` событием в приложении на основе XAML).</span><span class="sxs-lookup"><span data-stu-id="91833-117">Disabling vsync does not necessarily uncap your frame rate: developers also need to make sure [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) calls are not throttled by other timing events (such as the `CompositionTarget::Rendering` event in an XAML-based app).</span></span>

<span data-ttu-id="91833-118">Приведенный ниже код предменяет несколько ключевых частей, которые необходимо добавить в приложения.</span><span class="sxs-lookup"><span data-stu-id="91833-118">The code below recaps a few key pieces you need to add to your apps.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="91833-119">См. также</span><span class="sxs-lookup"><span data-stu-id="91833-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91833-120">Усовершенствования DXGI 1,5</span><span class="sxs-lookup"><span data-stu-id="91833-120">DXGI 1.5 Improvements</span></span>](dxgi-1-5-improvements.md)
</dt> <dt>

[<span data-ttu-id="91833-121">Руководством по программированию для DXGI</span><span class="sxs-lookup"><span data-stu-id="91833-121">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
