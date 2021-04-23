---
title: Модель шейдера 3
description: Модель шейдеров 3 добавила дополнительные возможности в модель шейдера 2.
ms.assetid: bd09f86e-946f-4281-bc48-1db5cd32b2ae
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c53b8252f617c6ee3b95512a5d930a93f646479
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104413920"
---
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="48824-103">Модель шейдера 3 (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="48824-103">Shader Model 3 (HLSL reference)</span></span>

<span data-ttu-id="48824-104">Модель шейдеров 3 добавила дополнительные возможности в [модель шейдера 2](dx-graphics-hlsl-sm2.md).</span><span class="sxs-lookup"><span data-stu-id="48824-104">Shader Model 3 added additional capabilities to [shader model 2](dx-graphics-hlsl-sm2.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48824-105">Компонент</span><span class="sxs-lookup"><span data-stu-id="48824-105">Feature</span></span></td>
<td><span data-ttu-id="48824-106">Возможностями.</span><span class="sxs-lookup"><span data-stu-id="48824-106">Capability</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48824-107">Набор инструкций</span><span class="sxs-lookup"><span data-stu-id="48824-107">Instruction Set</span></span></td>
<td><ul>
<li><span data-ttu-id="48824-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Функции HLSL</strong></a></span><span class="sxs-lookup"><span data-stu-id="48824-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></li>
<li><span data-ttu-id="48824-109">Инструкции по сборке (см. <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">Ps_3_0 инструкции</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">инструкции — vs_3_0</a>)</span><span class="sxs-lookup"><span data-stu-id="48824-109">Assembly instructions (see <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">ps_3_0 Instructions</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">Instructions - vs_3_0</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48824-110">Набор регистров</span><span class="sxs-lookup"><span data-stu-id="48824-110">Register Set</span></span></td>
<td><ul>
<li><span data-ttu-id="48824-111">Регистры шейдеров пикселей (см. раздел <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">регистры ps_3_0</a>)</span><span class="sxs-lookup"><span data-stu-id="48824-111">Pixel shader registers (see <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">ps_3_0 Registers</a>)</span></span></li>
<li><span data-ttu-id="48824-112">Регистры шейдеров вершин (см. раздел <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">registers-vs_3_0</a>)</span><span class="sxs-lookup"><span data-stu-id="48824-112">Vertex shader registers (see <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">Registers - vs_3_0</a>)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48824-113">Максимальный размер шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="48824-113">Pixel Shader Max</span></span></td>
<td><span data-ttu-id="48824-114">512 минимум и до количества слотов в D3DCAPS9. MaxPixelShader30InstructionSlots (см. <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="48824-114">512 minimum, and up to the number of slots in D3DCAPS9.MaxPixelShader30InstructionSlots (see <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48824-115">Максимум вершинного шейдера</span><span class="sxs-lookup"><span data-stu-id="48824-115">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="48824-116">512 минимум и до количества слотов в D3DCAPS9. MaxVertexShader30InstructionSlots (см. <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="48824-116">512 minimum, and up to the number of slots in D3DCAPS9.MaxVertexShader30InstructionSlots (see <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48824-117">Профили шейдеров</span><span class="sxs-lookup"><span data-stu-id="48824-117">Shader Profiles</span></span></td>
<td><span data-ttu-id="48824-118">ps_3_0, vs_3_0</span><span class="sxs-lookup"><span data-stu-id="48824-118">ps_3_0, vs_3_0</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="48824-119">Дополнительные сведения о шейдерах модели 3 см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="48824-119">For more details on model 3 shaders, see:</span></span>

-   [<span data-ttu-id="48824-120">Построитель текстуры 3,0</span><span class="sxs-lookup"><span data-stu-id="48824-120">Pixel Shader 3.0</span></span>](dx9-graphics-reference-asm-ps-3-0.md)
-   [<span data-ttu-id="48824-121">Шейдер вершин 3,0</span><span class="sxs-lookup"><span data-stu-id="48824-121">Vertex Shader 3.0</span></span>](dx9-graphics-reference-asm-vs-3-0.md)

## <a name="related-topics"></a><span data-ttu-id="48824-122">См. также</span><span class="sxs-lookup"><span data-stu-id="48824-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48824-123">Модели шейдеров и профили шейдеров</span><span class="sxs-lookup"><span data-stu-id="48824-123">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 