---
title: Модель шейдера 2
description: Модель шейдеров 2 добавила дополнительные возможности в модель шейдера 1.
ms.assetid: 53c367d2-5b6a-4afa-894a-8ab9927169d5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88bd2f6292687c5387fadf65f8f43437904168cc
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104997035"
---
# <a name="shader-model-2"></a><span data-ttu-id="b466d-103">Модель шейдера 2</span><span class="sxs-lookup"><span data-stu-id="b466d-103">Shader Model 2</span></span>

<span data-ttu-id="b466d-104">Модель шейдеров 2 добавила дополнительные возможности в [модель шейдера 1](dx-graphics-hlsl-sm1.md).</span><span class="sxs-lookup"><span data-stu-id="b466d-104">Shader Model 2 added additional capabilities to [shader model 1](dx-graphics-hlsl-sm1.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b466d-105">Компонент</span><span class="sxs-lookup"><span data-stu-id="b466d-105">Feature</span></span></td>
<td><span data-ttu-id="b466d-106">Возможностями.</span><span class="sxs-lookup"><span data-stu-id="b466d-106">Capability</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b466d-107">Набор инструкций</span><span class="sxs-lookup"><span data-stu-id="b466d-107">Instruction Set</span></span></td>
<td><ul>
<li><span data-ttu-id="b466d-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Функции HLSL</strong></a></span><span class="sxs-lookup"><span data-stu-id="b466d-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></li>
<li><span data-ttu-id="b466d-109">Инструкции по сборке (см. <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">инструкции по VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">инструкции vs_2_x</a>, инструкции <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">ps_2_0</a>, инструкции <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x</a>)</span><span class="sxs-lookup"><span data-stu-id="b466d-109">Assembly instructions (see <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">Instructions - vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">Instructions - vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">ps_2_0 Instructions</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x Instructions</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b466d-110">Набор регистров</span><span class="sxs-lookup"><span data-stu-id="b466d-110">Register Set</span></span></td>
<td><ul>
<li><span data-ttu-id="b466d-111">Регистры шейдеров пикселей (см. <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">Ps_2_0 регистры</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">регистры ps_2_x</a>)</span><span class="sxs-lookup"><span data-stu-id="b466d-111">Pixel shader registers (see <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">ps_2_0 Registers</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x Registers</a>)</span></span></li>
<li><span data-ttu-id="b466d-112">Регистры шейдеров вершин (см. раздел <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">registers-VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">registers-vs_2_x</a>)</span><span class="sxs-lookup"><span data-stu-id="b466d-112">Vertex shader registers (see <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">Registers - vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">Registers - vs_2_x</a>)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b466d-113">Максимальный размер шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="b466d-113">Pixel Shader Max</span></span></td>
<td><ul>
<li><span data-ttu-id="b466d-114">ps_2_0-32 текстура + 64, арифметические действия</span><span class="sxs-lookup"><span data-stu-id="b466d-114">ps_2_0 - 32 texture + 64 arithmetic</span></span></li>
<li><span data-ttu-id="b466d-115">ps_2_x-96 минимум и до количества слотов в D3DCAPS9. D3DPSHADERCAPS2_0. Нуминструктионслотс.</span><span class="sxs-lookup"><span data-stu-id="b466d-115">ps_2_x - 96 minimum, and up to the number of slots in D3DCAPS9.D3DPSHADERCAPS2_0.NumInstructionSlots.</span></span> <span data-ttu-id="b466d-116">См. D3DPSHADERCAPS2_0</span><span class="sxs-lookup"><span data-stu-id="b466d-116">See D3DPSHADERCAPS2_0</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b466d-117">Максимум вершинного шейдера</span><span class="sxs-lookup"><span data-stu-id="b466d-117">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="b466d-118">256 инструкции</span><span class="sxs-lookup"><span data-stu-id="b466d-118">256 instructions</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b466d-119">Профили шейдеров</span><span class="sxs-lookup"><span data-stu-id="b466d-119">Shader Profiles</span></span></td>
<td><span data-ttu-id="b466d-120">ps_2_0, ps_2_x, vs_2_0, vs_2_x</span><span class="sxs-lookup"><span data-stu-id="b466d-120">ps_2_0, ps_2_x, vs_2_0, vs_2_x</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b466d-121">Дополнительные сведения о модели шейдеров 2 см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="b466d-121">For more details on shader model 2, see:</span></span>

-   <span data-ttu-id="b466d-122">[Шейдер пикселей 2,0](dx9-graphics-reference-asm-ps-2-0.md), [построитель текстуры 2. x](dx9-graphics-reference-asm-ps-2-x.md)</span><span class="sxs-lookup"><span data-stu-id="b466d-122">[Pixel Shader 2.0](dx9-graphics-reference-asm-ps-2-0.md), [Pixel Shader 2.x](dx9-graphics-reference-asm-ps-2-x.md)</span></span>
-   <span data-ttu-id="b466d-123">[Шейдер вершин 2,0](dx9-graphics-reference-asm-vs-2-0.md), [Вершинный шейдер 2. x](dx9-graphics-reference-asm-vs-2-x.md)</span><span class="sxs-lookup"><span data-stu-id="b466d-123">[Vertex Shader 2.0](dx9-graphics-reference-asm-vs-2-0.md), [Vertex Shader 2.x](dx9-graphics-reference-asm-vs-2-x.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b466d-124">См. также</span><span class="sxs-lookup"><span data-stu-id="b466d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b466d-125">Модели шейдеров и профили шейдеров</span><span class="sxs-lookup"><span data-stu-id="b466d-125">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




