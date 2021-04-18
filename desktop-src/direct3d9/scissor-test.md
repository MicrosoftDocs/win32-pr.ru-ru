---
description: Прямоугольный тест исключает Пиксели за пределами прямоугольного прямоугольника, определяемого пользователем прямоугольного подраздела целевого объекта отрисовки.
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: Ножницный тест (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c4298182ab2bb6302c19111e2970d23cef311d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105691998"
---
# <a name="scissor-test-direct3d-9"></a><span data-ttu-id="19b54-103">Ножницный тест (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="19b54-103">Scissor Test (Direct3D 9)</span></span>

<span data-ttu-id="19b54-104">Прямоугольный тест исключает Пиксели за пределами прямоугольного прямоугольника, определяемого пользователем прямоугольного подраздела целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="19b54-104">The scissor test culls pixels that are outside of the scissor rectangle, a user-defined rectangular sub-section of the render target.</span></span>

<span data-ttu-id="19b54-105">Прямоугольный прямоугольник можно использовать для обозначения области целевого объекта отрисовки, в которой рисуется игра игры.</span><span class="sxs-lookup"><span data-stu-id="19b54-105">The scissor rectangle could be used to indicate the area of the render target where the game world is drawn.</span></span> <span data-ttu-id="19b54-106">Область за пределами прямоугольника исключается и может быть назначена графическому интерфейсу игры.</span><span class="sxs-lookup"><span data-stu-id="19b54-106">The area outside the rectangle is culled and could be devoted to a game's GUI.</span></span> <span data-ttu-id="19b54-107">Ножницные тесты не могут исключать непрямоугольные области.</span><span class="sxs-lookup"><span data-stu-id="19b54-107">The scissor test cannot cull non-rectangular areas.</span></span>

<span data-ttu-id="19b54-108">Прямоугольные прямоугольники не могут быть заданы больше, чем целевой объект рендеринга, но могут быть заданы больше, чем окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="19b54-108">Scissor rectangles cannot be set larger than the render target, but they can be set larger than the viewport.</span></span>

<span data-ttu-id="19b54-109">Прямоугольная прямоугольная область управляется состоянием визуализации устройства.</span><span class="sxs-lookup"><span data-stu-id="19b54-109">The scissor rectangle is managed by a device render state.</span></span> <span data-ttu-id="19b54-110">Чтобы включить или отключить ножницы, установите для параметра рендерстате **значение true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="19b54-110">A scissor test is enabled or disabled by setting the renderstate to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="19b54-111">Эта проверка выполняется после вычислки цвета фрагмента, но до альфа-тестирования.</span><span class="sxs-lookup"><span data-stu-id="19b54-111">This test is performed after the fragment color is computed but before alpha testing.</span></span> <span data-ttu-id="19b54-112">[**IDirect3DDevice9:: сетрендертаржет**](/windows/desktop/api) сбрасывает прямоугольный прямоугольник до полного целевого объекта отрисовки, аналогично сбросу окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="19b54-112">[**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) resets the scissor rectangle to the full render target, analogous to the viewport reset.</span></span> <span data-ttu-id="19b54-113">[**IDirect3DDevice9:: сетсЦиссоррект**](/windows/desktop/api) записывается с помощью Статеблоккс и [**IDirect3DDevice9:: креатестатеблокк**](/windows/desktop/api) с параметром все состояния (D3DSBT \_ все значения в [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)).</span><span class="sxs-lookup"><span data-stu-id="19b54-113">[**IDirect3DDevice9::SetScissorRect**](/windows/desktop/api) is recorded by stateblocks, and [**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) with the all state setting (D3DSBT\_ALL value in [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)).</span></span> <span data-ttu-id="19b54-114">Ножницный тест также влияет на операцию [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) устройства.</span><span class="sxs-lookup"><span data-stu-id="19b54-114">The scissor test also affects the device [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) operation.</span></span>


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



<span data-ttu-id="19b54-115">Прямоугольный прямоугольник по умолчанию является полным окном просмотра.</span><span class="sxs-lookup"><span data-stu-id="19b54-115">The default scissor rectangle is the full viewport.</span></span>

<span data-ttu-id="19b54-116">Ножницное тестирование выполняется сразу после завершения обработки пикселя шейдером пикселей или с помощью фиксированного конвейера функций, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="19b54-116">Scissor testing is done just after pixel processing is completed by a pixel shader or the fixed function pipeline, as shown in the following diagram.</span></span>

![Схема, когда прямоугольное тестирование выполняется относительно других шагов](images/scissor-test.png)

## <a name="related-topics"></a><span data-ttu-id="19b54-118">См. также</span><span class="sxs-lookup"><span data-stu-id="19b54-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19b54-119">Конвейер пикселей</span><span class="sxs-lookup"><span data-stu-id="19b54-119">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
