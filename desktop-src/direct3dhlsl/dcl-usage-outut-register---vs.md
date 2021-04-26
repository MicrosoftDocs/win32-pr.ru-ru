---
title: вывод dcl_usage (SM1, SM2, SM3-VS ASM)
description: Различные типы выходных регистров были свернуты в двенадцать выходных регистров (два для цвета, восемь для текстуры, одна для позиции, а другая для тумана и размера точки).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 314c9c9a9a9e62915e9224b3cf165bc54d09a516
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999171"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="89fe6-103">\_выходные данные использования дкл (SM1, SM2, SM3-VS ASM)</span><span class="sxs-lookup"><span data-stu-id="89fe6-103">dcl\_usage output (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="89fe6-104">Различные типы выходных регистров были свернуты в двенадцать выходных регистров (два для цвета, восемь для текстуры, одна для позиции, а другая для тумана и размера точки).</span><span class="sxs-lookup"><span data-stu-id="89fe6-104">The various types of output registers have been collapsed into twelve output registers (two for color, eight for texture, one for position, and one for fog and point size).</span></span> <span data-ttu-id="89fe6-105">Они могут использоваться для того, что нужно выполнить для интерполяции для шейдера пикселей: текстурные координаты, цвета, туман и т. д.</span><span class="sxs-lookup"><span data-stu-id="89fe6-105">These can be used for anything the user wants to interpolate for the pixel shader: texture coordinates, colors, fog, and so on.</span></span>

<span data-ttu-id="89fe6-106">Для выходных регистров требуются объявления, которые включают семантику.</span><span class="sxs-lookup"><span data-stu-id="89fe6-106">Output registers require declarations that include semantics.</span></span> <span data-ttu-id="89fe6-107">Например, старые регистры позиции и размера точек заменяются путем объявления выходного регистра с указанием позиции или семантики размера точки.</span><span class="sxs-lookup"><span data-stu-id="89fe6-107">For instance, the old position and point size registers are replaced by declaring an output register with a position or point-size semantic.</span></span>

<span data-ttu-id="89fe6-108">Из двенадцати выходных регистров любое десять (не обязательно O0 на O9) состоит из четырех компонентов (ксизв), а другое должно быть объявлено как положенное (а также включать все четыре компонента), и, по желанию, один из них может быть скалярным размером точки.</span><span class="sxs-lookup"><span data-stu-id="89fe6-108">Of the twelve output registers, any ten (not necessarily o0 to o9) have four components (xyzw), another one must be declared as position (and must also include all four components), and optionally one more can be a scalar point size.</span></span>

## <a name="syntax"></a><span data-ttu-id="89fe6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89fe6-109">Syntax</span></span>

<span data-ttu-id="89fe6-110">Синтаксис для объявления выходных регистров аналогичен объявлениям для входного регистра:</span><span class="sxs-lookup"><span data-stu-id="89fe6-110">The syntax for declaring output registers is similar to the declarations for the input register:</span></span>



|                                  |
|----------------------------------|
| <span data-ttu-id="89fe6-111">\_семантика дкл o \[ . запись \_ маски\]</span><span class="sxs-lookup"><span data-stu-id="89fe6-111">dcl\_semantics o\[.write\_mask\]</span></span> |



 

<span data-ttu-id="89fe6-112">Где:</span><span class="sxs-lookup"><span data-stu-id="89fe6-112">Where:</span></span>

-   <span data-ttu-id="89fe6-113">\_семантика дкл может использовать тот же набор семантики, что и для объявления ввода.</span><span class="sxs-lookup"><span data-stu-id="89fe6-113">dcl\_semantics can use the same set of semantics as for the input declaration.</span></span> <span data-ttu-id="89fe6-114">Семантические имена берутся из [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (и сопряжены с индексом, например position3).</span><span class="sxs-lookup"><span data-stu-id="89fe6-114">Semantic names come from [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (and are paired with an index, such as position3).</span></span> <span data-ttu-id="89fe6-115">Всегда должен быть один выходной регистр с семантикой positiont0, если не используется для обработки вершин.</span><span class="sxs-lookup"><span data-stu-id="89fe6-115">There always has to be one output register with the positiont0 semantic when not used for processing vertices.</span></span> <span data-ttu-id="89fe6-116">Семантика positiont0 и семантика pointsize0 являются единственными, которые имеют смысл за пределами простого разрешения компоновки из вершины в шейдеры пикселей.</span><span class="sxs-lookup"><span data-stu-id="89fe6-116">The positiont0 semantic and the pointsize0 semantic are the only ones that have meaning beyond simply allowing linkage from vertex to pixel shaders.</span></span> <span data-ttu-id="89fe6-117">Для шейдеров с управлением потоком предполагается, что выводится наихудший результат.</span><span class="sxs-lookup"><span data-stu-id="89fe6-117">For shaders with flow control, it is assumed that the worst case output is declared.</span></span> <span data-ttu-id="89fe6-118">Значения по умолчанию отсутствуют, если шейдер фактически не выводит то, что его объявляет (из-за управления потоком).</span><span class="sxs-lookup"><span data-stu-id="89fe6-118">There are no defaults if a shader does not actually output what it declares it should (due to flow control).</span></span>
-   <span data-ttu-id="89fe6-119">o — это выходной регистр.</span><span class="sxs-lookup"><span data-stu-id="89fe6-119">o is an output register.</span></span> <span data-ttu-id="89fe6-120">См. раздел [выходные \_ регистры](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="89fe6-120">See [Output\_Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>
-   <span data-ttu-id="89fe6-121">\_маска записи указывает на один и тот же выходной регистр, который можно объявить несколько раз (так что разные семантики могут применяться к отдельным компонентам), каждый раз с уникальной маской записи.</span><span class="sxs-lookup"><span data-stu-id="89fe6-121">write\_mask indicates the same output register that can be declared multiple times (so different semantics can be applied to individual components), each time with a unique write mask.</span></span> <span data-ttu-id="89fe6-122">Однако одна и та же семантика не может использоваться несколько раз в объявлении.</span><span class="sxs-lookup"><span data-stu-id="89fe6-122">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="89fe6-123">Это означает, что векторы должны состоять из четырех компонентов или меньше и не могут быть передаваться по границам регистров для четырех компонентов (отдельные регистры).</span><span class="sxs-lookup"><span data-stu-id="89fe6-123">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual registers).</span></span> <span data-ttu-id="89fe6-124">При использовании семантики размера точки она должна иметь полную маску записи, так как она считается скалярной.</span><span class="sxs-lookup"><span data-stu-id="89fe6-124">When the point-size semantic is used, it should have full write mask because it is considered a scalar.</span></span> <span data-ttu-id="89fe6-125">При использовании семантики позиций она должна иметь полную маску записи, так как необходимо записать все четыре компонента.</span><span class="sxs-lookup"><span data-stu-id="89fe6-125">When the position semantic is used, it should have a full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="89fe6-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="89fe6-126">Remarks</span></span>



| <span data-ttu-id="89fe6-127">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="89fe6-127">Vertex shader versions</span></span> | <span data-ttu-id="89fe6-128">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="89fe6-128">3\_0</span></span> | <span data-ttu-id="89fe6-129">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="89fe6-129">3\_sw</span></span> |
|------------------------|------|-------|
| <span data-ttu-id="89fe6-130">\_Использование дкл</span><span class="sxs-lookup"><span data-stu-id="89fe6-130">dcl\_usage</span></span>             | <span data-ttu-id="89fe6-131">x</span><span class="sxs-lookup"><span data-stu-id="89fe6-131">x</span></span>    | <span data-ttu-id="89fe6-132">x</span><span class="sxs-lookup"><span data-stu-id="89fe6-132">x</span></span>     |



 

<span data-ttu-id="89fe6-133">Все инструкции по [ \_ использованию дкл](dcl-usage-input-register---vs.md) должны располагаться перед первой исполняемой инструкцией.</span><span class="sxs-lookup"><span data-stu-id="89fe6-133">All [dcl\_usage](dcl-usage-input-register---vs.md) instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="89fe6-134">Примеры объявлений</span><span class="sxs-lookup"><span data-stu-id="89fe6-134">Declaration Examples</span></span>


```
vs_3_0
dcl_color4     o3.x    // color4 is a semantic name.
dcl_texcoord3  o3.yz   // Different semantics can be packed into one register.
dcl_fog        o3.w 
dcl_tangent    o4.xyz
dcl_position   o7.xyzw // position must be declared to some unique register 
                       //   in a vertex shader, with all 4 components.

dcl_psize      o6      // Pointsize cannot have a mask 
                       //   (that is, mask is full .xyzw)
                       // This is an implied scalar register. 
                       // No other semantics can be assigned to any components
                       //   of this register.
                       // If pointsize declaration is not used (typical),
                       //   only 11 "out" registers are available, not 12.
                       // Pixel shaders cannot see this value.

```



## <a name="related-topics"></a><span data-ttu-id="89fe6-135">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="89fe6-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89fe6-136">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="89fe6-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
