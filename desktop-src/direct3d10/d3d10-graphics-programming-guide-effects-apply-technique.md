---
description: Когда константы, текстуры и состояние шейдера объявлены и инициализированы, осталось только установить состояние воздействия на устройстве.
ms.assetid: b6c88fa1-53d4-40dc-803d-5d1cdfe4777b
title: Применение методики (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb7cc48c9115dfb81c1688a3a499e24d46cc563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496014"
---
# <a name="apply-a-technique-direct3d-10"></a><span data-ttu-id="fe6fb-103">Применение методики (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="fe6fb-103">Apply a Technique (Direct3D 10)</span></span>

<span data-ttu-id="fe6fb-104">Когда константы, текстуры и состояние шейдера объявлены и инициализированы, осталось только установить состояние воздействия на устройстве.</span><span class="sxs-lookup"><span data-stu-id="fe6fb-104">With the constants, textures, and shader state declared and initialized, the only thing left to do is to set the effect state in the device.</span></span>

## <a name="set-non-shader-state-in-the-device"></a><span data-ttu-id="fe6fb-105">Задание состояния, отличного от шейдера, на устройстве</span><span class="sxs-lookup"><span data-stu-id="fe6fb-105">Set Non-Shader State in the Device</span></span>

<span data-ttu-id="fe6fb-106">Некоторые состояния конвейера не задаются каким-либо действием.</span><span class="sxs-lookup"><span data-stu-id="fe6fb-106">Some pipeline state is not set by an effect.</span></span> <span data-ttu-id="fe6fb-107">Например, очистка целевого объекта рендеринга готовит целевой объект отрисовки для данных.</span><span class="sxs-lookup"><span data-stu-id="fe6fb-107">For example clearing a render target prepares the render target for data.</span></span> <span data-ttu-id="fe6fb-108">Ниже приведен пример очистки выходных буферов перед установкой состояния воздействия на устройство.</span><span class="sxs-lookup"><span data-stu-id="fe6fb-108">Before setting the effect state in the device, here is an example of clearing output buffers.</span></span>


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D10RenderTargetView* pRTV = DXUTGetD3D10RenderTargetView();
    pd3dDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D10DepthStencilView* pDSV = DXUTGetD3D10DepthStencilView();
    pd3dDevice->ClearDepthStencilView( pDSV, D3D10_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a><span data-ttu-id="fe6fb-109">Установка состояния воздействия на устройстве</span><span class="sxs-lookup"><span data-stu-id="fe6fb-109">Set Effect State in the Device</span></span>

<span data-ttu-id="fe6fb-110">Установка состояния действия выполняется путем применения состояния действия в цикле подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="fe6fb-110">Setting effect state is done by applying the effect state within the render loop.</span></span> <span data-ttu-id="fe6fb-111">Это делается из внешней среды в.</span><span class="sxs-lookup"><span data-stu-id="fe6fb-111">This is done from the outside in.</span></span> <span data-ttu-id="fe6fb-112">То есть выберите метод, а затем задайте состояние для каждого из проходов (в зависимости от желаемого результата).</span><span class="sxs-lookup"><span data-stu-id="fe6fb-112">That is, select a technique, and then set the state for each of the passes (depending on your desired result).</span></span>


```
    D3D10_TECHNIQUE_DESC techDesc;
    pRenderTechnique->GetDesc( &techDesc );
    for( UINT p = 0; p < techDesc.Passes; ++p )
    {
        }
            ....
            pRenderTechnique->GetPassByIndex( p )->Apply(0);
            pd3dDevice->DrawIndexed( (UINT)pSubset->IndexCount, 0,  
                 (UINT)pSubset->VertexStart );
        }
    }
```



<span data-ttu-id="fe6fb-113">Результат не отображает ничего, он просто устанавливает состояние воздействия на устройство.</span><span class="sxs-lookup"><span data-stu-id="fe6fb-113">An effect doesn't render anything, it simply sets effect state to the device.</span></span> <span data-ttu-id="fe6fb-114">Код отрисовки вызывается после того, как состояние действия изменит состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="fe6fb-114">The rendering code is called after the effect state updates device state.</span></span> <span data-ttu-id="fe6fb-115">В этом примере вызов Дравиндексед выполняет отрисовку.</span><span class="sxs-lookup"><span data-stu-id="fe6fb-115">In this example, the DrawIndexed call performs the rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe6fb-116">См. также</span><span class="sxs-lookup"><span data-stu-id="fe6fb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe6fb-117">Отрисовка влияния (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="fe6fb-117">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



