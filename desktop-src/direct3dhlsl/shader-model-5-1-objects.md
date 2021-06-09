---
title: Объекты модели шейдеров 5,1
description: В модель шейдера 5,1 добавлены следующие объекты.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376ce272e789501e21f5866be37f56daf31bc829
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825721"
---
# <a name="shader-model-51-objects"></a><span data-ttu-id="ba4ab-103">Объекты модели шейдеров 5,1</span><span class="sxs-lookup"><span data-stu-id="ba4ab-103">Shader Model 5.1 Objects</span></span>

<span data-ttu-id="ba4ab-104">В модель шейдера 5,1 добавлены следующие объекты.</span><span class="sxs-lookup"><span data-stu-id="ba4ab-104">The following objects have been added to shader model 5.1.</span></span>

<span data-ttu-id="ba4ab-105">Для [представлений порядка средства прорисовки](/windows/desktop/direct3d11/rasterizer-order-views) (доступно в D3D 11.3 и D3D12) следующие объекты являются новыми и разрешаются только в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="ba4ab-105">For the [Rasterizer Order Views](/windows/desktop/direct3d11/rasterizer-order-views) (available in D3D11.3 and D3D12), the following objects are new, and are only allowed in the pixel shader.</span></span> <span data-ttu-id="ba4ab-106">Обратите внимание, что поддерживаемые методы идентичны соответствующим объектам UAV.</span><span class="sxs-lookup"><span data-stu-id="ba4ab-106">Note that the methods they support are identical to the corresponding UAV objects.</span></span>



| <span data-ttu-id="ba4ab-107">Объект средства программной прорисовки</span><span class="sxs-lookup"><span data-stu-id="ba4ab-107">Rasterizer object</span></span>                                   | <span data-ttu-id="ba4ab-108">Объект UAV</span><span class="sxs-lookup"><span data-stu-id="ba4ab-108">UAV object</span></span>                                                              |
|------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ba4ab-109">растеризерордередбуффер</span><span class="sxs-lookup"><span data-stu-id="ba4ab-109">RasterizerOrderedBuffer</span></span>            | [<span data-ttu-id="ba4ab-110">**рвбуффер**</span><span class="sxs-lookup"><span data-stu-id="ba4ab-110">**RWBuffer**</span></span>](sm5-object-rwbuffer.md)                       |
| <span data-ttu-id="ba4ab-111">растеризерордередбитеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="ba4ab-111">RasterizerOrderedByteAddressBuffer</span></span> | [<span data-ttu-id="ba4ab-112">**рвбитеаддрессбуффер**</span><span class="sxs-lookup"><span data-stu-id="ba4ab-112">**RWByteAddressBuffer**</span></span>](sm5-object-rwbyteaddressbuffer.md) |
| <span data-ttu-id="ba4ab-113">растеризерордередструктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="ba4ab-113">RasterizerOrderedStructuredBuffer</span></span>  | [<span data-ttu-id="ba4ab-114">**рвструктуредбуффер**</span><span class="sxs-lookup"><span data-stu-id="ba4ab-114">**RWStructuredBuffer**</span></span>](sm5-object-rwstructuredbuffer.md)   |
| <span data-ttu-id="ba4ab-115">RasterizerOrderedTexture1D</span><span class="sxs-lookup"><span data-stu-id="ba4ab-115">RasterizerOrderedTexture1D</span></span>         | [<span data-ttu-id="ba4ab-116">**RWTexture1D**</span><span class="sxs-lookup"><span data-stu-id="ba4ab-116">**RWTexture1D**</span></span>](sm5-object-rwtexture1d.md)                 |
| <span data-ttu-id="ba4ab-117">RasterizerOrderedTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="ba4ab-117">RasterizerOrderedTexture1DArray</span></span>    | [<span data-ttu-id="ba4ab-118">**RWTexture1DArray**</span><span class="sxs-lookup"><span data-stu-id="ba4ab-118">**RWTexture1DArray**</span></span>](sm5-object-rwtexture1darray.md)       |
| <span data-ttu-id="ba4ab-119">RasterizerOrderedTexture2D</span><span class="sxs-lookup"><span data-stu-id="ba4ab-119">RasterizerOrderedTexture2D</span></span>         | [<span data-ttu-id="ba4ab-120">**RWTexture2D**</span><span class="sxs-lookup"><span data-stu-id="ba4ab-120">**RWTexture2D**</span></span>](sm5-object-rwtexture2d.md)                 |
| <span data-ttu-id="ba4ab-121">RasterizerOrderedTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="ba4ab-121">RasterizerOrderedTexture2DArray</span></span>    | [<span data-ttu-id="ba4ab-122">**RWTexture2DArray**</span><span class="sxs-lookup"><span data-stu-id="ba4ab-122">**RWTexture2DArray**</span></span>](sm5-object-rwtexture2darray.md)       |
| <span data-ttu-id="ba4ab-123">RasterizerOrderedTexture3D</span><span class="sxs-lookup"><span data-stu-id="ba4ab-123">RasterizerOrderedTexture3D</span></span>         | [<span data-ttu-id="ba4ab-124">**RWTexture3D**</span><span class="sxs-lookup"><span data-stu-id="ba4ab-124">**RWTexture3D**</span></span>](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="ba4ab-125">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ba4ab-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba4ab-126">Модель шейдера 5,1</span><span class="sxs-lookup"><span data-stu-id="ba4ab-126">Shader Model 5.1</span></span>](shader-model-5-1.md)
</dt> <dt>

[<span data-ttu-id="ba4ab-127">Функции HLSL Shader Model 5,1 для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="ba4ab-127">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 
