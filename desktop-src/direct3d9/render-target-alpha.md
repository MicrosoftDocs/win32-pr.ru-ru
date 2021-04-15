---
description: Теперь при смешении буферов кадров можно смешивать альфа-каналы независимо от смешения цветов на целевых объектах отрисовки. Этот элемент управления включается с новым состоянием отрисовки, D3DRS \_ сепаратеалфабленденабле.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Целевой альфа-канал прорисовки (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70f395406559782172448b5555daff056ffd54c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536509"
---
# <a name="render-target-alpha-direct3d-9"></a><span data-ttu-id="c0092-104">Целевой альфа-канал прорисовки (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c0092-104">Render Target Alpha (Direct3D 9)</span></span>

<span data-ttu-id="c0092-105">Теперь при смешении буферов кадров можно смешивать альфа-каналы независимо от смешения цветов на целевых объектах отрисовки.</span><span class="sxs-lookup"><span data-stu-id="c0092-105">The frame buffer blender can now blend alpha channels independent from color-channel blending on render targets.</span></span> <span data-ttu-id="c0092-106">Этот элемент управления включается с новым состоянием отрисовки, D3DRS \_ сепаратеалфабленденабле.</span><span class="sxs-lookup"><span data-stu-id="c0092-106">This control is enabled with a new render state, D3DRS\_SEPARATEALPHABLENDENABLE.</span></span>

<span data-ttu-id="c0092-107">Если параметру D3DRS \_ сепаратеалфабленденабле присвоено значение **false** (это условие по умолчанию), то коэффициенты смешения и операции, применяемые к альфа-каналу, совпадают с параметрами, определенными для смешения цветовых каналов.</span><span class="sxs-lookup"><span data-stu-id="c0092-107">When D3DRS\_SEPARATEALPHABLENDENABLE is set to **FALSE** (which is the default condition), the render-target blending factors and operations applied to alpha are the same as those defined for blending color channels.</span></span> <span data-ttu-id="c0092-108">Драйверу необходимо установить D3DPMISCCAPS \_ сепаратеалфабленд Cap, чтобы указать, что она может поддерживать альфа-смешение для визуализации.</span><span class="sxs-lookup"><span data-stu-id="c0092-108">A driver needs to set the D3DPMISCCAPS\_SEPARATEALPHABLEND cap to indicate that it can support render-target alpha blending.</span></span> <span data-ttu-id="c0092-109">Обязательно включите D3DRS алфабленд, \_ чтобы сообщить конвейеру, что требуется альфа-смешение.</span><span class="sxs-lookup"><span data-stu-id="c0092-109">Be sure to enable D3DRS\_ALPHABLEND to tell the pipeline that alpha blending is needed.</span></span>

<span data-ttu-id="c0092-110">Чтобы управлять факторами в альфа-канале для накладываемых объектов визуализации, два новых состояния рендеринга определяются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c0092-110">To control the factors in the alpha channel of the render-target blenders, two new render states are defined as follows:</span></span>


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



<span data-ttu-id="c0092-111">Как и в \_ случае с D3DRS сркбленд и D3DRS \_ дестбленд, для них можно задать одно из значений в перечислении [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="c0092-111">Like the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND, these can be set to one of the values in the [**D3DBLEND**](./d3dblend.md) enumeration.</span></span> <span data-ttu-id="c0092-112">Параметры перехода исходного и конечного параметров можно объединить несколькими способами в зависимости от параметров в Сркблендкапс и Дестблендкапс элементов [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="c0092-112">The source and destination blend settings can be combined in several ways, depending on the settings in the SrcBlendCaps and DestBlendCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

<span data-ttu-id="c0092-113">Альфа-смешение выполняется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="c0092-113">The alpha blending is done as follows:</span></span>

<span data-ttu-id="c0092-114">Рендертаржеталфа = (альфа<sub>в</sub> \* сркблендоп) блендоп (Alpha<sub>RT</sub> \* дестблендоп)</span><span class="sxs-lookup"><span data-stu-id="c0092-114">renderTargetAlpha = (alpha<sub>in</sub> \* srcBlendOp) BlendOp (alpha<sub>rt</sub> \* destBlendOp)</span></span>

<span data-ttu-id="c0092-115">Где:</span><span class="sxs-lookup"><span data-stu-id="c0092-115">Where:</span></span>

-   <span data-ttu-id="c0092-116">Альфа<sub>в</sub> — это входное альфа-значение.</span><span class="sxs-lookup"><span data-stu-id="c0092-116">alpha<sub>in</sub> is the input alpha value.</span></span>
-   <span data-ttu-id="c0092-117">Сркблендоп является одним из факторов смешения в [**D3DBLEND**](./d3dblend.md).</span><span class="sxs-lookup"><span data-stu-id="c0092-117">srcBlendOp is one of the blend factors in [**D3DBLEND**](./d3dblend.md).</span></span>
-   <span data-ttu-id="c0092-118">Блендоп является одним из факторов смешения в [**D3DBLENDOP**](./d3dblendop.md).</span><span class="sxs-lookup"><span data-stu-id="c0092-118">BlendOp is one of the blend factors in [**D3DBLENDOP**](./d3dblendop.md).</span></span>
-   <span data-ttu-id="c0092-119">Alpha<sub>RT</sub> — это значение альфа-целевого объекта Render.</span><span class="sxs-lookup"><span data-stu-id="c0092-119">alpha<sub>rt</sub> is the render-target alpha value.</span></span>
-   <span data-ttu-id="c0092-120">Дестблендоп является одним из факторов смешения в [**D3DBLEND**](./d3dblend.md).</span><span class="sxs-lookup"><span data-stu-id="c0092-120">destBlendOp is one of the blend factors in [**D3DBLEND**](./d3dblend.md).</span></span>
-   <span data-ttu-id="c0092-121">Рендертаржеталфа — это Последнее смешение альфа-значения.</span><span class="sxs-lookup"><span data-stu-id="c0092-121">renderTargetAlpha is the final blended alpha value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0092-122">См. также</span><span class="sxs-lookup"><span data-stu-id="c0092-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0092-123">Альфа-смешение</span><span class="sxs-lookup"><span data-stu-id="c0092-123">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 
