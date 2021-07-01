---
title: dcl_semantics (SM3-PS ASM)
description: Объявите ассоциацию между выходным шейдером вершин и входными данными шейдера пикселей.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c506d2ad23003f93bbaea409cacc60b18c86534
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129711"
---
# <a name="dcl_semantics-sm3---ps-asm"></a><span data-ttu-id="7001d-103">\_семантика дкл (SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="7001d-103">dcl\_semantics (sm3 - ps asm)</span></span>

<span data-ttu-id="7001d-104">Объявите ассоциацию между выходным шейдером вершин и входными данными шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="7001d-104">Declare the association between vertex shader output and pixel shader input.</span></span>

## <a name="syntax"></a><span data-ttu-id="7001d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7001d-105">Syntax</span></span>

<span data-ttu-id="7001d-106">\_семантика дкл \[ \_ центроид \] DST \[ . Write \_ Mask\]</span><span class="sxs-lookup"><span data-stu-id="7001d-106">dcl\_semantics \[\_centroid\] dst\[.write\_mask\]</span></span>



 

<span data-ttu-id="7001d-107">Где:</span><span class="sxs-lookup"><span data-stu-id="7001d-107">Where:</span></span>

-   <span data-ttu-id="7001d-108">\_семантика: определяет предполагаемое использование данных и может быть любым из значений в [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (без \_ префикса D3DDECLUSAGE).</span><span class="sxs-lookup"><span data-stu-id="7001d-108">\_semantics: Identifies the intended data usage, and may be any of the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (without the D3DDECLUSAGE\_ prefix).</span></span> <span data-ttu-id="7001d-109">Кроме того, целочисленный индекс может быть добавлен к семантике для различения параметров, использующих подобную семантику.</span><span class="sxs-lookup"><span data-stu-id="7001d-109">Additionally, an integer index can be appended to the semantic to distinguish parameters that use similar semantics.</span></span>
-   <span data-ttu-id="7001d-110">\[\_[Центроид](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] является необязательным модификатором инструкции.</span><span class="sxs-lookup"><span data-stu-id="7001d-110">\[\_[Centroid](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)\] is an optional instruction modifier.</span></span> <span data-ttu-id="7001d-111">Он поддерживается в \_ инструкциях по использованию дкл, которые объявляют входные регистры и инструкции по поиску текстур.</span><span class="sxs-lookup"><span data-stu-id="7001d-111">It is is supported on dcl\_usage instructions that declare the input registers and on texture lookup instructions.</span></span> <span data-ttu-id="7001d-112">К центроид добавляется без пробела.</span><span class="sxs-lookup"><span data-stu-id="7001d-112">The centroid is appended with no space.</span></span>
-   <span data-ttu-id="7001d-113">DST: регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="7001d-113">dst: destination register.</span></span> <span data-ttu-id="7001d-114">См. раздел [ \_ \_ регистры PS 3 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="7001d-114">See [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span></span>
-   <span data-ttu-id="7001d-115">\_маска записи. один и тот же выходной регистр может быть объявлен несколько раз, каждый раз с уникальной маской записи (так что разные семантики могут применяться к отдельным компонентам).</span><span class="sxs-lookup"><span data-stu-id="7001d-115">write\_mask: The same output register may be declared multiple times, each time with a unique write mask (so different semantics can be applied to individual components).</span></span> <span data-ttu-id="7001d-116">Однако одна и та же семантика не может использоваться несколько раз в объявлении.</span><span class="sxs-lookup"><span data-stu-id="7001d-116">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="7001d-117">Это означает, что векторы должны состоять из четырех компонентов или меньше и не могут переключаться между четырьмя границами регистров (отдельные выходные регистры).</span><span class="sxs-lookup"><span data-stu-id="7001d-117">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual output registers).</span></span> <span data-ttu-id="7001d-118">При \_ использовании семантики псизе она должна иметь полную маску записи, так как она считается скалярной.</span><span class="sxs-lookup"><span data-stu-id="7001d-118">When the \_psize semantic is used, it should have a full write mask because it is considered a scalar.</span></span> <span data-ttu-id="7001d-119">При \_ использовании семантики расположения она должна иметь полную маску записи, так как необходимо записать все четыре компонента.</span><span class="sxs-lookup"><span data-stu-id="7001d-119">When the \_position semantic is used, it should have full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="7001d-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="7001d-120">Remarks</span></span>



| <span data-ttu-id="7001d-121">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="7001d-121">Pixel shader versions</span></span> | <span data-ttu-id="7001d-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="7001d-122">1\_1</span></span> | <span data-ttu-id="7001d-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="7001d-123">1\_2</span></span> | <span data-ttu-id="7001d-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7001d-124">1\_3</span></span> | <span data-ttu-id="7001d-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="7001d-125">1\_4</span></span> | <span data-ttu-id="7001d-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7001d-126">2\_0</span></span> | <span data-ttu-id="7001d-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7001d-127">2\_x</span></span> | <span data-ttu-id="7001d-128">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7001d-128">2\_sw</span></span> | <span data-ttu-id="7001d-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7001d-129">3\_0</span></span> | <span data-ttu-id="7001d-130">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7001d-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7001d-131">\_Использование дкл</span><span class="sxs-lookup"><span data-stu-id="7001d-131">dcl\_usage</span></span>            |      |      |      |      |      |      |       | <span data-ttu-id="7001d-132">x</span><span class="sxs-lookup"><span data-stu-id="7001d-132">x</span></span>    | <span data-ttu-id="7001d-133">x</span><span class="sxs-lookup"><span data-stu-id="7001d-133">x</span></span>     |



 

<span data-ttu-id="7001d-134">Все \_ инструкции по использованию дкл должны располагаться перед первой исполняемой инструкцией.</span><span class="sxs-lookup"><span data-stu-id="7001d-134">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="7001d-135">Примеры объявлений</span><span class="sxs-lookup"><span data-stu-id="7001d-135">Declaration Examples</span></span>


```
ps_3_0

; Declaring inputs
dcl_normal      v0.xyz
dcl_blendweight v0.w ; Must be same reg# as normal, matching vshader packing
dcl_texcoord1   v1.y ; Mask can be any subset of mask from vshader semantic
dcl_texcoord0   v1.zw; Has to be same reg# as texcoord1, to match vshader

; Declaring samplers
dcl_2d s0
dcl_2d s1

def c0, 0, 0, 0, 0

mov r0.x, v1.y ; texcoord1
mov r0.y, c0
texld r0, r0, s0

texld r1, v1.zw, s1
...
(output regs in ps_3_0 are same as ps_2_0: oC0-oC3, oDepth)
```



## <a name="related-topics"></a><span data-ttu-id="7001d-136">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="7001d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7001d-137">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="7001d-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

<span data-ttu-id="7001d-138">[Пример сглаживания](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="7001d-138">[Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
