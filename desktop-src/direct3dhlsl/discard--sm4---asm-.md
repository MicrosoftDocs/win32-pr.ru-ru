---
title: отменить (SM4-ASM)
description: Условно отметьте результаты построителя текстуры как отброшенные при достижении конца программы.
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d98365ae6d80710f15cf7204f98d810be30a13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103987075"
---
# <a name="discard-sm4---asm"></a><span data-ttu-id="6d2f5-103">отменить (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6d2f5-103">discard (sm4 - asm)</span></span>

<span data-ttu-id="6d2f5-104">Условно отметьте результаты построителя текстуры как отброшенные при достижении конца программы.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-104">Conditionally flag results of Pixel Shader to be discarded when the end of the program is reached.</span></span>



| <span data-ttu-id="6d2f5-105">отменить { \_ z </span><span class="sxs-lookup"><span data-stu-id="6d2f5-105">discard{\_z</span></span>\|<span data-ttu-id="6d2f5-106">\_NZ} src0. Выбор \_ компонента</span><span class="sxs-lookup"><span data-stu-id="6d2f5-106">\_nz} src0.select\_component</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="6d2f5-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="6d2f5-107">Item</span></span>                                                            | <span data-ttu-id="6d2f5-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6d2f5-108">Description</span></span>                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d2f5-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6d2f5-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6d2f5-110">\[\]значение, определяющее, следует ли отбрасывать текущую обрабатываемую точку.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-110">\[in\] The value that determines whether to discard the current pixel being processed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6d2f5-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="6d2f5-111">Remarks</span></span>

<span data-ttu-id="6d2f5-112">Эта инструкция Помечает текущий пиксель как завершенный, продолжая выполнение, чтобы другие Пиксели, выполняющиеся параллельно, могли получить производные при необходимости.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-112">This instruction flags the current pixel as terminated, while continuing execution, so that other pixels executing in parallel may obtain derivatives if necessary.</span></span> <span data-ttu-id="6d2f5-113">Несмотря на то, что выполнение продолжится, все выходные данные шейдера пиксельных записываются до или после инструкции **Discard** отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-113">Even though execution continues, all Pixel Shader output writes before or after the **discard** instruction are discarded.</span></span>

<span data-ttu-id="6d2f5-114">Для **отмены \_ z**, если все биты в *src0. Select \_* равны нулю, пиксель отбрасывается.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-114">For **discard\_z**, if all bits in *src0.select\_component* are zero, then the pixel is discarded.</span></span>

<span data-ttu-id="6d2f5-115">Если в параметре " **отменить \_ NZ**" какие-либо биты в *src0. Select \_* являются ненулевыми, пиксель отбрасывается.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-115">For **discard\_nz**, if any bits in *src0.select\_component* are nonzero, then the pixel is discarded.</span></span>

<span data-ttu-id="6d2f5-116">Кроме того, инструкция **Discard** может присутствовать внутри любой конструкции управления потоком.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-116">In addition, the **discard** instruction can be present inside any flow control construct.</span></span>

<span data-ttu-id="6d2f5-117">В шейдере могут присутствовать несколько инструкций по **удалению** , и если они выполняются, точка завершается.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-117">Multiple **discard** instructions may be present in a Shader, and if any is executed, the pixel is terminated.</span></span>

<span data-ttu-id="6d2f5-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="6d2f5-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6d2f5-119">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="6d2f5-119">Vertex Shader</span></span> | <span data-ttu-id="6d2f5-120">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="6d2f5-120">Geometry Shader</span></span> | <span data-ttu-id="6d2f5-121">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="6d2f5-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="6d2f5-122">x</span><span class="sxs-lookup"><span data-stu-id="6d2f5-122">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6d2f5-123">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6d2f5-123">Minimum Shader Model</span></span>

<span data-ttu-id="6d2f5-124">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="6d2f5-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6d2f5-125">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6d2f5-125">Shader Model</span></span>                                              | <span data-ttu-id="6d2f5-126">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="6d2f5-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6d2f5-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="6d2f5-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6d2f5-128">да</span><span class="sxs-lookup"><span data-stu-id="6d2f5-128">yes</span></span>       |
| [<span data-ttu-id="6d2f5-129">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="6d2f5-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6d2f5-130">да</span><span class="sxs-lookup"><span data-stu-id="6d2f5-130">yes</span></span>       |
| [<span data-ttu-id="6d2f5-131">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="6d2f5-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6d2f5-132">да</span><span class="sxs-lookup"><span data-stu-id="6d2f5-132">yes</span></span>       |
| [<span data-ttu-id="6d2f5-133">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d2f5-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6d2f5-134">Нет</span><span class="sxs-lookup"><span data-stu-id="6d2f5-134">no</span></span>        |
| [<span data-ttu-id="6d2f5-135">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d2f5-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6d2f5-136">Нет</span><span class="sxs-lookup"><span data-stu-id="6d2f5-136">no</span></span>        |
| [<span data-ttu-id="6d2f5-137">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d2f5-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6d2f5-138">Нет</span><span class="sxs-lookup"><span data-stu-id="6d2f5-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6d2f5-139">См. также</span><span class="sxs-lookup"><span data-stu-id="6d2f5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d2f5-140">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d2f5-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





