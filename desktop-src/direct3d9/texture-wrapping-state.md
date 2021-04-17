---
description: D3DRS \_ WRAP0 через D3DRS \_ WRAP7 Rendering States включает и отключает перенос u и v для различных текстур в многотекстурном каскадном соединении.
ms.assetid: c584eee6-1187-4741-b3af-4bd79d93be77
title: Состояние переноса текстур (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19cb025df6716371397d62cc730c5584e2dab862
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495567"
---
# <a name="texture-wrapping-state-direct3d-9"></a><span data-ttu-id="82e56-103">Состояние переноса текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="82e56-103">Texture Wrapping State (Direct3D 9)</span></span>

<span data-ttu-id="82e56-104">D3DRS \_ WRAP0 через D3DRS \_ WRAP7 Rendering States включает и отключает перенос u и v для различных текстур в многотекстурном каскадном соединении.</span><span class="sxs-lookup"><span data-stu-id="82e56-104">The D3DRS\_WRAP0 through D3DRS\_WRAP7 render states enable and disable u- and v-wrapping for various textures in the device's multitexture cascade.</span></span> <span data-ttu-id="82e56-105">Для этих состояний отрисовки можно задать сочетание \_ флагов D3DWRAPCOORD 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD \_ 2 и D3DWRAPCOORD 3, \_ чтобы включить перенос в первую, второй, третьем и четвертом направлениях текстуры.</span><span class="sxs-lookup"><span data-stu-id="82e56-105">You can set these render states to a combination of the D3DWRAPCOORD\_0, D3DWRAPCOORD\_1, D3DWRAPCOORD\_2, and D3DWRAPCOORD\_3 flags to enable wrapping in first, second, third, and fourth directions of the texture.</span></span> <span data-ttu-id="82e56-106">Чтобы полностью отключить заключение, используйте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="82e56-106">Use a value of zero to disable wrapping altogether.</span></span> <span data-ttu-id="82e56-107">По умолчанию перенос текстур отключен во всех направлениях для всех стадий текстуры.</span><span class="sxs-lookup"><span data-stu-id="82e56-107">Texture wrapping is disabled in all directions for all texture stages by default.</span></span>

<span data-ttu-id="82e56-108">Общие сведения см. в разделе [Перенос текстур (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="82e56-108">For a conceptual overview, see [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="82e56-109">См. также</span><span class="sxs-lookup"><span data-stu-id="82e56-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82e56-110">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="82e56-110">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



