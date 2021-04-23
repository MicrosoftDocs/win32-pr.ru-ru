---
description: Direct3D поддерживает как плоские, так и заливку по методу Гуро. Значение по умолчанию — заливка по методу Гуро. Для управления текущим режимом заливки приложение C++ указывает Член перечисляемого типа D3DSHADEMODE для \_ состояния визуализации D3DRS шадемоде.
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: Состояние заливки (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebac826704fee0e1903c1aa2a2348bff4a089c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710625"
---
# <a name="shading-state-direct3d-9"></a><span data-ttu-id="cce8e-105">Состояние заливки (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cce8e-105">Shading State (Direct3D 9)</span></span>

<span data-ttu-id="cce8e-106">Direct3D поддерживает как плоские, так и заливку по методу Гуро.</span><span class="sxs-lookup"><span data-stu-id="cce8e-106">Direct3D supports both flat and Gouraud shading.</span></span> <span data-ttu-id="cce8e-107">Значение по умолчанию — заливка по методу Гуро.</span><span class="sxs-lookup"><span data-stu-id="cce8e-107">The default is Gouraud shading.</span></span> <span data-ttu-id="cce8e-108">Для управления текущим режимом заливки приложение C++ указывает Член перечисляемого типа [**D3DSHADEMODE**](./d3dshademode.md) для \_ состояния визуализации D3DRS шадемоде.</span><span class="sxs-lookup"><span data-stu-id="cce8e-108">To control the current shading mode, your C++ application specifies a member of the [**D3DSHADEMODE**](./d3dshademode.md) enumerated type for the D3DRS\_SHADEMODE render state.</span></span>

<span data-ttu-id="cce8e-109">В следующем примере кода C++ демонстрируется процесс установки состояния затенения в режим плоской заливки.</span><span class="sxs-lookup"><span data-stu-id="cce8e-109">The following C++ code example demonstrates the process of setting the shading state to flat shading mode.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface.
// Set the shading state.
d3dDevice->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
```



## <a name="related-topics"></a><span data-ttu-id="cce8e-110">См. также</span><span class="sxs-lookup"><span data-stu-id="cce8e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cce8e-111">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="cce8e-111">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
