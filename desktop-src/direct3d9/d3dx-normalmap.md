---
description: Обычные константы создания карт.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37985456e81b20af9b3e4396d10045d5e58c9b7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710599"
---
# <a name="d3dx_normalmap"></a><span data-ttu-id="f315c-103">D3DX \_ нормалмап</span><span class="sxs-lookup"><span data-stu-id="f315c-103">D3DX\_NORMALMAP</span></span>

<span data-ttu-id="f315c-104">Обычные константы создания карт.</span><span class="sxs-lookup"><span data-stu-id="f315c-104">Normal maps generation constants.</span></span>



|                                     |                                                                                                                                                                                                    |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f315c-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="f315c-105">\#define</span></span>                            | <span data-ttu-id="f315c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f315c-106">Description</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="f315c-107">\_ \_ Зеркальная копия D3DX нормалмап \_ U</span><span class="sxs-lookup"><span data-stu-id="f315c-107">D3DX\_NORMALMAP\_MIRROR\_U</span></span>          | <span data-ttu-id="f315c-108">Указывает, что пиксели от края текстуры на оси u должны быть зеркально отображены, а не переноситься в оболочку.</span><span class="sxs-lookup"><span data-stu-id="f315c-108">Indicates that pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="f315c-109">D3DX \_ нормалмап \_ Mirror \_ V</span><span class="sxs-lookup"><span data-stu-id="f315c-109">D3DX\_NORMALMAP\_MIRROR\_V</span></span>          | <span data-ttu-id="f315c-110">Указывает, что пиксели с края текстуры на оси v должны быть зеркальными, а не упакованными.</span><span class="sxs-lookup"><span data-stu-id="f315c-110">Indicates that pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="f315c-111">\_Зеркало D3DX нормалмап \_</span><span class="sxs-lookup"><span data-stu-id="f315c-111">D3DX\_NORMALMAP\_MIRROR</span></span>             | <span data-ttu-id="f315c-112">То же, что и указание D3DX \_ нормалмап \_ Mirror \_ U \| D3DX \_ нормалмап \_ Mirror \_ V.</span><span class="sxs-lookup"><span data-stu-id="f315c-112">Same as specifying D3DX\_NORMALMAP\_MIRROR\_U \| D3DX\_NORMALMAP\_MIRROR\_V.</span></span>                                                                                                                       |
| <span data-ttu-id="f315c-113">D3DX \_ нормалмап \_ инвертсигн</span><span class="sxs-lookup"><span data-stu-id="f315c-113">D3DX\_NORMALMAP\_INVERTSIGN</span></span>         | <span data-ttu-id="f315c-114">Инвертирует направление каждого нормального.</span><span class="sxs-lookup"><span data-stu-id="f315c-114">Inverts the direction of each normal.</span></span>                                                                                                                                                              |
| <span data-ttu-id="f315c-115">D3DX \_ нормалмап \_ COMPUTE \_ перекрытия</span><span class="sxs-lookup"><span data-stu-id="f315c-115">D3DX\_NORMALMAP\_COMPUTE\_OCCLUSION</span></span> | <span data-ttu-id="f315c-116">Выполняет вычисление Терма перекрытия на пиксель и кодирует его в альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="f315c-116">Computes the per-pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="f315c-117">Значение альфа, равное 1, означает, что пиксел не закрывается каким-либо образом, а альфа-канал 0 означает, что пиксель полностью скрыт.</span><span class="sxs-lookup"><span data-stu-id="f315c-117">An alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 means that the pixel is completely obscured.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="f315c-118">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="f315c-118">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="f315c-119">Header</span><span class="sxs-lookup"><span data-stu-id="f315c-119">Header</span></span>                   | <span data-ttu-id="f315c-120">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="f315c-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="f315c-121">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="f315c-121">Minimum operating system</span></span> | <span data-ttu-id="f315c-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f315c-122">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f315c-123">См. также</span><span class="sxs-lookup"><span data-stu-id="f315c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f315c-124">Константы D3DX</span><span class="sxs-lookup"><span data-stu-id="f315c-124">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[<span data-ttu-id="f315c-125">**D3DXComputeNormalMap**</span><span class="sxs-lookup"><span data-stu-id="f315c-125">**D3DXComputeNormalMap**</span></span>](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



