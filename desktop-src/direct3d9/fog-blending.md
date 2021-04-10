---
description: Смешение тумана означает применение коэффициента тумана к цветам тумана и объекта для создания окончательного цвета, отображаемого в сцене, как описано в формулах тумана (Direct3D 9).
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: Смешение тумана (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa918715a7bbe37b200568a0a9098135c5558b0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139219"
---
# <a name="fog-blending-direct3d-9"></a><span data-ttu-id="7c87c-103">Смешение тумана (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7c87c-103">Fog Blending (Direct3D 9)</span></span>

<span data-ttu-id="7c87c-104">Смешение тумана означает применение коэффициента тумана к цветам тумана и объекта для создания окончательного цвета, отображаемого в сцене, как описано в [формулах тумана (Direct3D 9)](fog-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="7c87c-104">Fog blending refers to the application of the fog factor to the fog and object colors to produce the final color that appears in a scene, as discussed in [Fog Formulas (Direct3D 9)](fog-formulas.md).</span></span> <span data-ttu-id="7c87c-105">\_Состояние отрисовки D3DRS фоженабле управляет наложением тумана.</span><span class="sxs-lookup"><span data-stu-id="7c87c-105">The D3DRS\_FOGENABLE render state controls fog blending.</span></span> <span data-ttu-id="7c87c-106">Задайте для этого состояния отрисовки **значение true** , чтобы включить смешение тумана, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="7c87c-106">Set this render state to **TRUE** to enable fog blending as shown in the following example code.</span></span> <span data-ttu-id="7c87c-107">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="7c87c-107">The default is **FALSE**.</span></span>


```
// For this example, g_pDevice is a valid pointer
// to an IDirect3DDevice9 interface.
HRESULT hr;
hr = g_pDevice->SetRenderState(
                    D3DRS_FOGENABLE,
                    TRUE);
if FAILED(hr)
    return hr;
```



<span data-ttu-id="7c87c-108">Необходимо включить смешение тумана для пиксельного тумана и вершинного тумана.</span><span class="sxs-lookup"><span data-stu-id="7c87c-108">You must enable fog blending for both pixel fog and vertex fog.</span></span> <span data-ttu-id="7c87c-109">Сведения об использовании этих типов тумана см. в разделе [Pixel туман (Direct3D 9)](pixel-fog.md) и [вершинный туман (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="7c87c-109">For information about using these types of fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md) and [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c87c-110">См. также</span><span class="sxs-lookup"><span data-stu-id="7c87c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c87c-111">Типы туманов</span><span class="sxs-lookup"><span data-stu-id="7c87c-111">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 



