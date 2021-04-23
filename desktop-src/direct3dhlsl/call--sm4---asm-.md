---
title: Call (SM4-ASM)
description: Вызывает подпрограмму, помеченную, где в программе отображается метка l \.
ms.assetid: D6B7C52D-2CF7-44DB-81E3-2945477EF94A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dac86fa52140968443f01050cebc57718fea420
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784935"
---
# <a name="call-sm4---asm"></a><span data-ttu-id="6c6be-103">Call (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6c6be-103">call (sm4 - asm)</span></span>

<span data-ttu-id="6c6be-104">Вызывает подпрограмму, помеченную, где в программе отображается метка **l \#** .</span><span class="sxs-lookup"><span data-stu-id="6c6be-104">Calls a subroutine marked by where the label **l\#** appears in the program.</span></span>



| <span data-ttu-id="6c6be-105">вызов l\#</span><span class="sxs-lookup"><span data-stu-id="6c6be-105">call l\#</span></span> |
|----------|



 



| <span data-ttu-id="6c6be-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="6c6be-106">Item</span></span>                                                       | <span data-ttu-id="6c6be-107">Описание</span><span class="sxs-lookup"><span data-stu-id="6c6be-107">Description</span></span>                                    |
|------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="6c6be-108"><span id="l_"></span><span id="L_"></span>*н\#*</span><span class="sxs-lookup"><span data-stu-id="6c6be-108"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/> | <span data-ttu-id="6c6be-109">\[в \] метке подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="6c6be-109">\[in\] The label of the subroutine.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6c6be-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="6c6be-110">Remarks</span></span>

<span data-ttu-id="6c6be-111">При обнаружении [RET](ret--sm4---asm-.md) верните выполнение инструкции после этого вызова.</span><span class="sxs-lookup"><span data-stu-id="6c6be-111">When a [ret](ret--sm4---asm-.md) is encountered, return execution to the instruction after this call.</span></span>

<span data-ttu-id="6c6be-112">Формат маркера содержит смещение соответствующей метки в шейдере для удобства.</span><span class="sxs-lookup"><span data-stu-id="6c6be-112">The token format contains the offset of the corresponding label in the Shader as a convenience.</span></span>

<span data-ttu-id="6c6be-113">В следующем примере показана инструкция Call.</span><span class="sxs-lookup"><span data-stu-id="6c6be-113">The following example shows the call instruction.</span></span>


```
                ...
                call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret
```



### <a name="restrictions"></a><span data-ttu-id="6c6be-114">Ограничения</span><span class="sxs-lookup"><span data-stu-id="6c6be-114">Restrictions</span></span>

-   <span data-ttu-id="6c6be-115">Подпрограммы могут вкладывать 32 в глубину вложенности.</span><span class="sxs-lookup"><span data-stu-id="6c6be-115">Subroutines can nest 32 deep.</span></span>
-   <span data-ttu-id="6c6be-116">Стек адресов возврата управляется прозрачно в реализации.</span><span class="sxs-lookup"><span data-stu-id="6c6be-116">The return address stack is managed transparently by the implementation.</span></span>
-   <span data-ttu-id="6c6be-117">Если в стеке адресов возврата уже 32 записей и выдается **вызов** , то вызов пропускается.</span><span class="sxs-lookup"><span data-stu-id="6c6be-117">If there are already 32 entries on the return address stack and a **call** is issued, the call is skipped over.</span></span>
-   <span data-ttu-id="6c6be-118">Автоматический стек параметров отсутствует.</span><span class="sxs-lookup"><span data-stu-id="6c6be-118">There is no automatic parameter stack.</span></span> <span data-ttu-id="6c6be-119">Приложение может использовать индексируемый временный массив регистров (x \# \[ \] ) для реализации стека вручную.</span><span class="sxs-lookup"><span data-stu-id="6c6be-119">The application can use an indexable temporary register array (x\#\[\]) to manually implement a stack.</span></span> <span data-ttu-id="6c6be-120">Однако возвращаемые из вызова подпрограммы адреса не отображаются и являются ортогональными для любого ручного управления стеком, выполняемого приложением.</span><span class="sxs-lookup"><span data-stu-id="6c6be-120">However, the subroutine call return addresses are not visible and are orthogonal to any manual stack management done by the application.</span></span>
-   <span data-ttu-id="6c6be-121">Индексирование параметра *l \#* не разрешено.</span><span class="sxs-lookup"><span data-stu-id="6c6be-121">Indexing of the *l\#* parameter is not permitted.</span></span>
-   <span data-ttu-id="6c6be-122">Рекурсия не разрешена.</span><span class="sxs-lookup"><span data-stu-id="6c6be-122">Recursion is not permitted.</span></span>

<span data-ttu-id="6c6be-123">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="6c6be-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6c6be-124">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="6c6be-124">Vertex Shader</span></span> | <span data-ttu-id="6c6be-125">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="6c6be-125">Geometry Shader</span></span> | <span data-ttu-id="6c6be-126">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="6c6be-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6c6be-127">x</span><span class="sxs-lookup"><span data-stu-id="6c6be-127">x</span></span>             | <span data-ttu-id="6c6be-128">x</span><span class="sxs-lookup"><span data-stu-id="6c6be-128">x</span></span>               | <span data-ttu-id="6c6be-129">x</span><span class="sxs-lookup"><span data-stu-id="6c6be-129">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6c6be-130">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6c6be-130">Minimum Shader Model</span></span>

<span data-ttu-id="6c6be-131">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="6c6be-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6c6be-132">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6c6be-132">Shader Model</span></span>                                              | <span data-ttu-id="6c6be-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="6c6be-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6c6be-134">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="6c6be-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6c6be-135">да</span><span class="sxs-lookup"><span data-stu-id="6c6be-135">yes</span></span>       |
| [<span data-ttu-id="6c6be-136">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="6c6be-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6c6be-137">да</span><span class="sxs-lookup"><span data-stu-id="6c6be-137">yes</span></span>       |
| [<span data-ttu-id="6c6be-138">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="6c6be-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6c6be-139">да</span><span class="sxs-lookup"><span data-stu-id="6c6be-139">yes</span></span>       |
| [<span data-ttu-id="6c6be-140">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c6be-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6c6be-141">Нет</span><span class="sxs-lookup"><span data-stu-id="6c6be-141">no</span></span>        |
| [<span data-ttu-id="6c6be-142">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c6be-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6c6be-143">Нет</span><span class="sxs-lookup"><span data-stu-id="6c6be-143">no</span></span>        |
| [<span data-ttu-id="6c6be-144">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c6be-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6c6be-145">Нет</span><span class="sxs-lookup"><span data-stu-id="6c6be-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6c6be-146">См. также</span><span class="sxs-lookup"><span data-stu-id="6c6be-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c6be-147">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6c6be-147">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





