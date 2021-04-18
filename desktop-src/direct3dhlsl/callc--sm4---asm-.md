---
title: каллк (SM4-ASM)
description: Условно вызывает подпрограмму, помеченную, где в программе отображается метка l \.
ms.assetid: 7F6E81CE-0C38-499B-B83E-FA76FA154451
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6bc8c9d1e4a99ce25f99253518482181cdb74d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996903"
---
# <a name="callc-sm4---asm"></a><span data-ttu-id="06252-103">каллк (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="06252-103">callc (sm4 - asm)</span></span>

<span data-ttu-id="06252-104">Условно вызывает подпрограмму, помеченную, где в программе отображается метка **l \#** .</span><span class="sxs-lookup"><span data-stu-id="06252-104">Conditionally calls a subroutine marked by where the label **l\#** appears in the program.</span></span>



| <span data-ttu-id="06252-105">каллк { \_ z </span><span class="sxs-lookup"><span data-stu-id="06252-105">callc{\_z</span></span>\|<span data-ttu-id="06252-106">\_NZ} src0. Select \_ , компонент l\#</span><span class="sxs-lookup"><span data-stu-id="06252-106">\_nz} src0.select\_component, l\#</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="06252-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="06252-107">Item</span></span>                                                            | <span data-ttu-id="06252-108">Описание</span><span class="sxs-lookup"><span data-stu-id="06252-108">Description</span></span>                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="06252-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="06252-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="06252-110">\[в \] компоненте, для которого необходимо проверить условие.</span><span class="sxs-lookup"><span data-stu-id="06252-110">\[in\] The component on which to test the condition.</span></span><br/> |
| <span data-ttu-id="06252-111"><span id="l_"></span><span id="L_"></span>*н\#*</span><span class="sxs-lookup"><span data-stu-id="06252-111"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/>      | <span data-ttu-id="06252-112">\[в \] метке подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="06252-112">\[in\] The label of the subroutine.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="06252-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="06252-113">Remarks</span></span>

<span data-ttu-id="06252-114">При обнаружении [RET](ret--sm4---asm-.md) верните выполнение инструкции после этого вызова.</span><span class="sxs-lookup"><span data-stu-id="06252-114">When a [ret](ret--sm4---asm-.md) is encountered, return execution to the instruction after this call.</span></span>

<span data-ttu-id="06252-115">Формат маркера содержит смещение соответствующей метки в шейдере для удобства.</span><span class="sxs-lookup"><span data-stu-id="06252-115">The token format contains the offset of the corresponding label in the Shader as a convenience.</span></span>

<span data-ttu-id="06252-116">В следующем примере показана инструкция Call.</span><span class="sxs-lookup"><span data-stu-id="06252-116">The following example shows the call instruction.</span></span>


```
                ...
                callc_z  r1.y, l3 // if all bits in r0.x are 0, call l3
                callc_nz r2.z, l3 // if any bit in r0.x is nonzero, call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret

```



### <a name="restrictions"></a><span data-ttu-id="06252-117">Ограничения</span><span class="sxs-lookup"><span data-stu-id="06252-117">Restrictions</span></span>

-   <span data-ttu-id="06252-118">Подпрограммы могут вкладывать 32 в глубину вложенности.</span><span class="sxs-lookup"><span data-stu-id="06252-118">Subroutines can nest 32 deep.</span></span>
-   <span data-ttu-id="06252-119">Стек адресов возврата управляется прозрачно в реализации.</span><span class="sxs-lookup"><span data-stu-id="06252-119">The return address stack is managed transparently by the implementation.</span></span>
-   <span data-ttu-id="06252-120">Если в стеке адресов возврата уже 32 записей и выдается **вызов** , то вызов пропускается.</span><span class="sxs-lookup"><span data-stu-id="06252-120">If there are already 32 entries on the return address stack and a **call** is issued, the call is skipped over.</span></span>
-   <span data-ttu-id="06252-121">Автоматический стек параметров отсутствует.</span><span class="sxs-lookup"><span data-stu-id="06252-121">There is no automatic parameter stack.</span></span> <span data-ttu-id="06252-122">Приложение может использовать индексируемый временный массив регистров (x \# \[ \] ) для реализации стека вручную.</span><span class="sxs-lookup"><span data-stu-id="06252-122">The application can use an indexable temporary register array (x\#\[\]) to manually implement a stack.</span></span> <span data-ttu-id="06252-123">Однако возвращаемые из вызова подпрограммы адреса не отображаются и являются ортогональными для любого ручного управления стеком, выполняемого приложением.</span><span class="sxs-lookup"><span data-stu-id="06252-123">However, the subroutine call return addresses are not visible and are orthogonal to any manual stack management done by the application.</span></span>
-   <span data-ttu-id="06252-124">Индексирование параметра *l \#* не разрешено.</span><span class="sxs-lookup"><span data-stu-id="06252-124">Indexing of the *l\#* parameter is not permitted.</span></span>
-   <span data-ttu-id="06252-125">32-разрядный регистр, предоставляемый *src0* , тестируется на битовом уровне.</span><span class="sxs-lookup"><span data-stu-id="06252-125">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="06252-126">Если любой бит не равен нулю, **каллк \_ NZ** выполняет вызов.</span><span class="sxs-lookup"><span data-stu-id="06252-126">If any bit is nonzero, **callc\_nz** will perform the call.</span></span> <span data-ttu-id="06252-127">Если все биты равны нулю, **каллк \_ z** выполнит вызов.</span><span class="sxs-lookup"><span data-stu-id="06252-127">If all bits are zero, **callc\_z** will perform the call.</span></span>
-   <span data-ttu-id="06252-128">Рекурсия не разрешена.</span><span class="sxs-lookup"><span data-stu-id="06252-128">Recursion is not permitted.</span></span>

<span data-ttu-id="06252-129">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="06252-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="06252-130">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="06252-130">Vertex Shader</span></span> | <span data-ttu-id="06252-131">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="06252-131">Geometry Shader</span></span> | <span data-ttu-id="06252-132">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="06252-132">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="06252-133">x</span><span class="sxs-lookup"><span data-stu-id="06252-133">x</span></span>             | <span data-ttu-id="06252-134">x</span><span class="sxs-lookup"><span data-stu-id="06252-134">x</span></span>               | <span data-ttu-id="06252-135">x</span><span class="sxs-lookup"><span data-stu-id="06252-135">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="06252-136">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="06252-136">Minimum Shader Model</span></span>

<span data-ttu-id="06252-137">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="06252-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="06252-138">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="06252-138">Shader Model</span></span>                                              | <span data-ttu-id="06252-139">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="06252-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="06252-140">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="06252-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="06252-141">да</span><span class="sxs-lookup"><span data-stu-id="06252-141">yes</span></span>       |
| [<span data-ttu-id="06252-142">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="06252-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="06252-143">да</span><span class="sxs-lookup"><span data-stu-id="06252-143">yes</span></span>       |
| [<span data-ttu-id="06252-144">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="06252-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="06252-145">да</span><span class="sxs-lookup"><span data-stu-id="06252-145">yes</span></span>       |
| [<span data-ttu-id="06252-146">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06252-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="06252-147">Нет</span><span class="sxs-lookup"><span data-stu-id="06252-147">no</span></span>        |
| [<span data-ttu-id="06252-148">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06252-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="06252-149">Нет</span><span class="sxs-lookup"><span data-stu-id="06252-149">no</span></span>        |
| [<span data-ttu-id="06252-150">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06252-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="06252-151">Нет</span><span class="sxs-lookup"><span data-stu-id="06252-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="06252-152">См. также</span><span class="sxs-lookup"><span data-stu-id="06252-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06252-153">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06252-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





