---
title: dcl_input Вжоининстанцеид (SM5-ASM)
description: Объявите идентификатор экземпляра на этапе присоединения шейдера поверхности.
ms.assetid: 2EABB24A-7ED7-460D-A2AD-D2C40DCCB2DC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bae9351fc7183aa37cd660c265aab803f4661e9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103987092"
---
# <a name="dcl_input-vjoininstanceid-sm5---asm"></a><span data-ttu-id="9bba8-103">дкл \_ input вжоининстанцеид (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9bba8-103">dcl\_input vJoinInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="9bba8-104">Объявите идентификатор экземпляра на этапе присоединения шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="9bba8-104">Declare the instance ID in a hull shader join phase.</span></span>



| <span data-ttu-id="9bba8-105">дкл \_ входные вжоининстанцеид</span><span class="sxs-lookup"><span data-stu-id="9bba8-105">dcl\_input vJoinInstanceID</span></span> |
|----------------------------|



 



| <span data-ttu-id="9bba8-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="9bba8-106">Item</span></span>                                                                                                                               | <span data-ttu-id="9bba8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9bba8-107">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="9bba8-108"><span id="vJoinInstanceID"></span><span id="vjoininstanceid"></span><span id="VJOININSTANCEID"></span>*вжоининстанцеид*</span><span class="sxs-lookup"><span data-stu-id="9bba8-108"><span id="vJoinInstanceID"></span><span id="vjoininstanceid"></span><span id="VJOININSTANCEID"></span>*vJoinInstanceID*</span></span><br/> | <span data-ttu-id="9bba8-109">\[в \] идентификаторе экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9bba8-109">\[in\] The instance ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9bba8-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="9bba8-110">Remarks</span></span>

<span data-ttu-id="9bba8-111">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="9bba8-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9bba8-112">Вершина</span><span class="sxs-lookup"><span data-stu-id="9bba8-112">Vertex</span></span> | <span data-ttu-id="9bba8-113">Поверхности</span><span class="sxs-lookup"><span data-stu-id="9bba8-113">Hull</span></span> | <span data-ttu-id="9bba8-114">Домен</span><span class="sxs-lookup"><span data-stu-id="9bba8-114">Domain</span></span> | <span data-ttu-id="9bba8-115">Геометрия</span><span class="sxs-lookup"><span data-stu-id="9bba8-115">Geometry</span></span> | <span data-ttu-id="9bba8-116">Пиксель</span><span class="sxs-lookup"><span data-stu-id="9bba8-116">Pixel</span></span> | <span data-ttu-id="9bba8-117">Вычисления</span><span class="sxs-lookup"><span data-stu-id="9bba8-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="9bba8-118">X</span><span class="sxs-lookup"><span data-stu-id="9bba8-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9bba8-119">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9bba8-119">Minimum Shader Model</span></span>

<span data-ttu-id="9bba8-120">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="9bba8-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9bba8-121">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9bba8-121">Shader Model</span></span>                                              | <span data-ttu-id="9bba8-122">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="9bba8-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9bba8-123">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="9bba8-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9bba8-124">да</span><span class="sxs-lookup"><span data-stu-id="9bba8-124">yes</span></span>       |
| [<span data-ttu-id="9bba8-125">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="9bba8-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9bba8-126">Нет</span><span class="sxs-lookup"><span data-stu-id="9bba8-126">no</span></span>        |
| [<span data-ttu-id="9bba8-127">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="9bba8-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9bba8-128">Нет</span><span class="sxs-lookup"><span data-stu-id="9bba8-128">no</span></span>        |
| [<span data-ttu-id="9bba8-129">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bba8-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9bba8-130">Нет</span><span class="sxs-lookup"><span data-stu-id="9bba8-130">no</span></span>        |
| [<span data-ttu-id="9bba8-131">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bba8-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9bba8-132">Нет</span><span class="sxs-lookup"><span data-stu-id="9bba8-132">no</span></span>        |
| [<span data-ttu-id="9bba8-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bba8-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9bba8-134">Нет</span><span class="sxs-lookup"><span data-stu-id="9bba8-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9bba8-135">См. также</span><span class="sxs-lookup"><span data-stu-id="9bba8-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bba8-136">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bba8-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





