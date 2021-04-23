---
title: Применение методики (Direct3D 11)
description: Когда константы, текстуры и состояние шейдера объявлены и инициализированы, осталось только установить состояние воздействия на устройстве.
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e67668b27c1f0271974f20edc62619a7b1ae8ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068063"
---
# <a name="apply-a-technique-direct3d-11"></a><span data-ttu-id="fea32-103">Применение методики (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="fea32-103">Apply a Technique (Direct3D 11)</span></span>

<span data-ttu-id="fea32-104">Когда константы, текстуры и состояние шейдера объявлены и инициализированы, осталось только установить состояние воздействия на устройстве.</span><span class="sxs-lookup"><span data-stu-id="fea32-104">With the constants, textures, and shader state declared and initialized, the only thing left to do is to set the effect state in the device.</span></span>

## <a name="set-non-shader-state-in-the-device"></a><span data-ttu-id="fea32-105">Задание состояния, отличного от шейдера, на устройстве</span><span class="sxs-lookup"><span data-stu-id="fea32-105">Set Non-Shader State in the Device</span></span>

<span data-ttu-id="fea32-106">Некоторые состояния конвейера не задаются каким-либо действием.</span><span class="sxs-lookup"><span data-stu-id="fea32-106">Some pipeline state is not set by an effect.</span></span> <span data-ttu-id="fea32-107">Например, очистка целевого объекта рендеринга готовит целевой объект отрисовки для данных.</span><span class="sxs-lookup"><span data-stu-id="fea32-107">For example clearing a render target prepares the render target for data.</span></span> <span data-ttu-id="fea32-108">Ниже приведен пример очистки выходных буферов перед установкой состояния воздействия на устройство.</span><span class="sxs-lookup"><span data-stu-id="fea32-108">Before setting the effect state in the device, here is an example of clearing output buffers.</span></span>


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D11RenderTargetView* pRTV = DXUTGetD3D11RenderTargetView();
    pD3DDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D11DepthStencilView* pDSV = DXUTGetD3D11DepthStencilView();
    pD3DDevice->ClearDepthStencilView( pDSV, D3D11_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a><span data-ttu-id="fea32-109">Установка состояния воздействия на устройстве</span><span class="sxs-lookup"><span data-stu-id="fea32-109">Set Effect State in the Device</span></span>

<span data-ttu-id="fea32-110">Установка состояния действия выполняется путем применения состояния действия в цикле подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="fea32-110">Setting effect state is done by applying the effect state within the render loop.</span></span> <span data-ttu-id="fea32-111">Это делается из внешней среды в.</span><span class="sxs-lookup"><span data-stu-id="fea32-111">This is done from the outside in.</span></span> <span data-ttu-id="fea32-112">То есть выберите метод, а затем задайте состояние для каждого из проходов (в зависимости от желаемого результата).</span><span class="sxs-lookup"><span data-stu-id="fea32-112">That is, select a technique, and then set the state for each of the passes (depending on your desired result).</span></span>


```
    D3D11_TECHNIQUE_DESC techDesc;
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



<span data-ttu-id="fea32-113">Результат не отображает ничего, он просто устанавливает состояние воздействия на устройство.</span><span class="sxs-lookup"><span data-stu-id="fea32-113">An effect doesn't render anything, it simply sets effect state to the device.</span></span> <span data-ttu-id="fea32-114">Код отрисовки вызывается после того, как состояние действия изменит состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="fea32-114">The rendering code is called after the effect state updates device state.</span></span> <span data-ttu-id="fea32-115">В этом примере вызов Дравиндексед выполняет отрисовку.</span><span class="sxs-lookup"><span data-stu-id="fea32-115">In this example, the DrawIndexed call performs the rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fea32-116">См. также</span><span class="sxs-lookup"><span data-stu-id="fea32-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fea32-117">Отрисовка результата (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="fea32-117">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




