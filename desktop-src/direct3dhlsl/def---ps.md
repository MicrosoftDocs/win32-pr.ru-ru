---
title: DEF-PS
description: Определяет константы с плавающей точкой шейдера пикселей.
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b4f035df97de2645983862dd68aa7ec80fc22d4b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070562"
---
# <a name="def---ps"></a><span data-ttu-id="463aa-103">DEF-PS</span><span class="sxs-lookup"><span data-stu-id="463aa-103">def - ps</span></span>

<span data-ttu-id="463aa-104">Определяет константы с плавающей точкой шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="463aa-104">Defines pixel shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="463aa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="463aa-105">Syntax</span></span>



| <span data-ttu-id="463aa-106">DEF, fVvalue1, fValue2, fValue3, fValue4</span><span class="sxs-lookup"><span data-stu-id="463aa-106">def dst, fVvalue1, fValue2, fValue3, fValue4</span></span> |
|----------------------------------------------|



 

<span data-ttu-id="463aa-107">Где:</span><span class="sxs-lookup"><span data-stu-id="463aa-107">Where:</span></span>

-   <span data-ttu-id="463aa-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="463aa-108">dst is the destination register.</span></span>
-   <span data-ttu-id="463aa-109">fValue1 fValue4 — это значения с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="463aa-109">fValue1 to fValue4 are floating-point values..</span></span>

## <a name="remarks"></a><span data-ttu-id="463aa-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="463aa-110">Remarks</span></span>



| <span data-ttu-id="463aa-111">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="463aa-111">Pixel shader versions</span></span> | <span data-ttu-id="463aa-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="463aa-112">1\_1</span></span> | <span data-ttu-id="463aa-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="463aa-113">1\_2</span></span> | <span data-ttu-id="463aa-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="463aa-114">1\_3</span></span> | <span data-ttu-id="463aa-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="463aa-115">1\_4</span></span> | <span data-ttu-id="463aa-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="463aa-116">2\_0</span></span> | <span data-ttu-id="463aa-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="463aa-117">2\_x</span></span> | <span data-ttu-id="463aa-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="463aa-118">2\_sw</span></span> | <span data-ttu-id="463aa-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="463aa-119">3\_0</span></span> | <span data-ttu-id="463aa-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="463aa-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="463aa-121">def</span><span class="sxs-lookup"><span data-stu-id="463aa-121">def</span></span>                   | <span data-ttu-id="463aa-122">x</span><span class="sxs-lookup"><span data-stu-id="463aa-122">x</span></span>    | <span data-ttu-id="463aa-123">x</span><span class="sxs-lookup"><span data-stu-id="463aa-123">x</span></span>    | <span data-ttu-id="463aa-124">x</span><span class="sxs-lookup"><span data-stu-id="463aa-124">x</span></span>    | <span data-ttu-id="463aa-125">x</span><span class="sxs-lookup"><span data-stu-id="463aa-125">x</span></span>    | <span data-ttu-id="463aa-126">x</span><span class="sxs-lookup"><span data-stu-id="463aa-126">x</span></span>    | <span data-ttu-id="463aa-127">x</span><span class="sxs-lookup"><span data-stu-id="463aa-127">x</span></span>    | <span data-ttu-id="463aa-128">x</span><span class="sxs-lookup"><span data-stu-id="463aa-128">x</span></span>     | <span data-ttu-id="463aa-129">x</span><span class="sxs-lookup"><span data-stu-id="463aa-129">x</span></span>    | <span data-ttu-id="463aa-130">x</span><span class="sxs-lookup"><span data-stu-id="463aa-130">x</span></span>     |



 

<span data-ttu-id="463aa-131">Существует два способа задания константы с плавающей запятой в построителе пикселей.</span><span class="sxs-lookup"><span data-stu-id="463aa-131">There are two ways to set a floating-point constant in a pixel shader.</span></span>

1.  <span data-ttu-id="463aa-132">Используйте DEF для определения константы непосредственно внутри шейдера.</span><span class="sxs-lookup"><span data-stu-id="463aa-132">Use def to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="463aa-133">Используйте API, чтобы задать константу с помощью [**сетпикселшадерконстантф**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span><span class="sxs-lookup"><span data-stu-id="463aa-133">Use the API to set a constant with [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span></span>

<span data-ttu-id="463aa-134">DEF определяет константу шейдера, значение которой загружается каждый раз, когда шейдер задается устройством.</span><span class="sxs-lookup"><span data-stu-id="463aa-134">def defines a shader constant whose value is loaded any time a shader is set to a device.</span></span> <span data-ttu-id="463aa-135">Они называются прямыми константами.</span><span class="sxs-lookup"><span data-stu-id="463aa-135">These are called immediate constants.</span></span> <span data-ttu-id="463aa-136">Немедленные константы имеют приоритет над константами, заданными методом API.</span><span class="sxs-lookup"><span data-stu-id="463aa-136">Immediate constants take precedence over constants set by the API method.</span></span>

-   <span data-ttu-id="463aa-137">Должен располагаться перед первой арифметической или инструкцией адресации в шейдере.</span><span class="sxs-lookup"><span data-stu-id="463aa-137">Must appear before the first arithmetic or addressing instruction in shader.</span></span>
-   <span data-ttu-id="463aa-138">Можно смешивать с инструкциями [дкл-(SM2, SM3-PS ASM)](dcl---ps.md) (другими типами инструкций, которые находятся в начале шейдера).</span><span class="sxs-lookup"><span data-stu-id="463aa-138">Can be intermixed with [dcl - (sm2, sm3 - ps asm)](dcl---ps.md) instructions (which are the other type of instruction that resides at the beginning of a shader).</span></span>
-   <span data-ttu-id="463aa-139">Регистр летнего времени должен быть [регистром констант](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="463aa-139">dst register must be a [constant register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>
-   <span data-ttu-id="463aa-140">Маска записи должна быть заполнена (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="463aa-140">Write mask must be full (default).</span></span>
-   <span data-ttu-id="463aa-141">Если [регистр константы](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) определен несколько раз в шейдере, последний сохраняется.</span><span class="sxs-lookup"><span data-stu-id="463aa-141">If a [constant register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) is defined multiple times in a shader, the last one persists.</span></span>

## <a name="related-topics"></a><span data-ttu-id="463aa-142">См. также</span><span class="sxs-lookup"><span data-stu-id="463aa-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="463aa-143">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="463aa-143">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 