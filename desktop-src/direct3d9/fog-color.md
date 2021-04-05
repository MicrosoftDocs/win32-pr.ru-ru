---
description: Цвет тумана для пиксельных и вершинных туманов задается с помощью \_ состояния рендеринга D3DRS фогколор. Значения состояния рендеринга могут быть любым цветом RGB, указанным в качестве цвета RGBA. Компонент Alpha игнорируется.
ms.assetid: 76366496-553d-4dbf-868d-d58b5377d36a
title: Цвет тумана (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c9ae217a26ab38be5e3f232fb9dfcd4c2977f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072129"
---
# <a name="fog-color-direct3d-9"></a><span data-ttu-id="cd386-105">Цвет тумана (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cd386-105">Fog Color (Direct3D 9)</span></span>

<span data-ttu-id="cd386-106">Цвет тумана для пиксельных и вершинных туманов задается с помощью \_ состояния рендеринга D3DRS фогколор.</span><span class="sxs-lookup"><span data-stu-id="cd386-106">Fog color for both pixel and vertex fog is set through the D3DRS\_FOGCOLOR render state.</span></span> <span data-ttu-id="cd386-107">Значения состояния рендеринга могут быть любым цветом RGB, указанным в качестве цвета RGBA.</span><span class="sxs-lookup"><span data-stu-id="cd386-107">The render state values can be any RGB color, specified as an RGBA color.</span></span> <span data-ttu-id="cd386-108">Компонент Alpha игнорируется.</span><span class="sxs-lookup"><span data-stu-id="cd386-108">The alpha component is ignored.</span></span>

<span data-ttu-id="cd386-109">В следующем примере C++ для цвета тумана устанавливается белый цвет.</span><span class="sxs-lookup"><span data-stu-id="cd386-109">The following C++ example sets the fog color to white.</span></span>


```
/* For this example, the d3dDevice variable is
* a valid pointer to an IDirect3DDevice9 interface.
*/
HRESULT hr;
hr = d3dDevice->SetRenderState(
                    D3DRS_FOGCOLOR,
                    0x00FFFFFF); // Highest 8 bits are not used.
if(FAILED(hr))
    return hr;
```



<span data-ttu-id="cd386-110">Туман применяется по-разному с помощью фиксированного конвейера функций и программируемого конвейера.</span><span class="sxs-lookup"><span data-stu-id="cd386-110">Fog is applied differently by the fixed function pipeline and the programmable pipeline.</span></span>

1.  <span data-ttu-id="cd386-111">Если драйвер поддерживает D3DPMISCCAPS \_ фогандспекуларалфа:</span><span class="sxs-lookup"><span data-stu-id="cd386-111">If the driver supports D3DPMISCCAPS\_FOGANDSPECULARALPHA:</span></span>
    -   <span data-ttu-id="cd386-112">Если используется фиксированный конвейер функции и задан параметр D3DRS \_ фогколор, то значение v1. w (в шейдере пикселей) равно значению, заданному в тумане рендерстате.</span><span class="sxs-lookup"><span data-stu-id="cd386-112">If the fixed function pipeline is used and D3DRS\_FOGCOLOR is set, v1.w (in the pixel shader) equals the value set in fog renderstate.</span></span>
    -   <span data-ttu-id="cd386-113">Если используется программируемый конвейер, то значение v1. w (в шейдере пикселей) равно 0, даже если oD1. w явно записывается в шейдер вершин.</span><span class="sxs-lookup"><span data-stu-id="cd386-113">If the programmable pipeline is used, then v1.w (in the pixel shader) equals 0, even if oD1.w is explicitly written in a vertex shader.</span></span>
2.  <span data-ttu-id="cd386-114">Если драйвер не поддерживает D3DPMISCCAPS \_ фогандспекуларалфа:</span><span class="sxs-lookup"><span data-stu-id="cd386-114">If the driver does NOT support D3DPMISCCAPS\_FOGANDSPECULARALPHA:</span></span>
    -   <span data-ttu-id="cd386-115">Если используется фиксированный конвейер функции и задан параметр D3DRS \_ фогколор, то значение v1. w (в построителе пиксельных шейдеров) равно значению, заданному в тумане рендерстате.</span><span class="sxs-lookup"><span data-stu-id="cd386-115">If the fixed function pipeline is used and D3DRS\_FOGCOLOR is set, then v1.w (in the pixel shader) equals value set in fog renderstate.</span></span>
    -   <span data-ttu-id="cd386-116">Если Офог явно записывается в шейдер вершин, значение v1. w (в шейдере пикселей) равно Офог, а затем — от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="cd386-116">If oFog is explicitly written in a vertex shader, v1.w (in the pixel shader) equals oFog, clamped between 0 and 1.</span></span>
    -   <span data-ttu-id="cd386-117">Если ни один из двух описанных выше вариантов не применяется, значение v1. w (в шейдере пикселей) равно 0, даже если oD1. w явно записывается в шейдер вершин.</span><span class="sxs-lookup"><span data-stu-id="cd386-117">If neither of the above two cases applies, v1.w (in the pixel shader) equals 0, even if oD1.w is explicitly written in a vertex shader.</span></span>

<span data-ttu-id="cd386-118">Дополнительные сведения см. в разделе [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="cd386-118">For more information, see [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd386-119">См. также</span><span class="sxs-lookup"><span data-stu-id="cd386-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd386-120">Типы туманов</span><span class="sxs-lookup"><span data-stu-id="cd386-120">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 



