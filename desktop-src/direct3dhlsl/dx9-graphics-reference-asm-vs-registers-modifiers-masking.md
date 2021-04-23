---
title: Маскирование регистров назначения
description: Маскирование указывает, какие компоненты регистра назначения будут обновлены в результате выполнения инструкции. Регистры текстур имеют один набор правил и нетекстурные регистры имеют еще один набор правил.
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ce15f75f424cb7796ef7db7a8b89bd5bcbfa9cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411161"
---
# <a name="destination-register-masking"></a><span data-ttu-id="9b9d4-104">Маскирование регистров назначения</span><span class="sxs-lookup"><span data-stu-id="9b9d4-104">Destination Register Masking</span></span>

<span data-ttu-id="9b9d4-105">Маскирование указывает, какие компоненты регистра назначения будут обновлены в результате выполнения инструкции.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-105">Masking specifies which components of the destination register will be updated with the result of an instruction.</span></span> <span data-ttu-id="9b9d4-106">Регистры текстур имеют один набор правил и нетекстурные регистры имеют еще один набор правил.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-106">Texture registers have one set of rules and nontexture registers have another set of rules.</span></span>

-   <span data-ttu-id="9b9d4-107">DX9 \_ графика \_ Справочник \_ по \_ \_ шаблонам ASM VS registers \_ \_ . Этот раздел содержит правила применения масок к целевым регистрам.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-107">dx9\_graphics\_reference\_asm\_vs\_registers\_modifiers\_masking - This section contains rules for applying masks to destination registers.</span></span>
-   <span data-ttu-id="9b9d4-108">\_Маски регистров текстур \_ — регистры текстур имеют уникальные правила.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-108">Texture\_Register\_Masks - Texture registers have some unique rules.</span></span>

## <a name="destination-register-masking"></a><span data-ttu-id="9b9d4-109">Маскирование регистров назначения</span><span class="sxs-lookup"><span data-stu-id="9b9d4-109">Destination Register Masking</span></span>

<span data-ttu-id="9b9d4-110">Как показано в следующей таблице, Маскирование (где — это один из допустимых [регистров шейдера](dx9-graphics-reference-asm-vs-registers.md)вершин шейдера вершин) может применяться к отдельным компонентам векторных данных.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-110">As shown in the following table, masking (where r is one of the valid vertex shader [Vertex Shader Registers](dx9-graphics-reference-asm-vs-registers.md)) can be applied to the individual components of the vector data.</span></span>



| <span data-ttu-id="9b9d4-111">Модификатор компонента</span><span class="sxs-lookup"><span data-stu-id="9b9d4-111">Component modifier</span></span> | <span data-ttu-id="9b9d4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9b9d4-112">Description</span></span>      |
|--------------------|------------------|
| <span data-ttu-id="9b9d4-113">r. {x} {y} {z} {w}</span><span class="sxs-lookup"><span data-stu-id="9b9d4-113">r.{x}{y}{z}{w}</span></span>     | <span data-ttu-id="9b9d4-114">Маска назначения</span><span class="sxs-lookup"><span data-stu-id="9b9d4-114">Destination mask</span></span> |



 

-   <span data-ttu-id="9b9d4-115">В целом, указание масок записи для регистра назначения является хорошим стилем написания кода.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-115">In general, specifying destination register write masks is good coding style.</span></span> <span data-ttu-id="9b9d4-116">Это упрощает чтение и обслуживание кода.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-116">It makes code easier to read and maintain.</span></span>
-   <span data-ttu-id="9b9d4-117">Можно указать любое сочетание компонентов (в том числе None), если x предшествует y, y – z, и z предшествует w.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-117">Any combination of components may be specified (including none) as long as x precedes y, y precedes z, and z precedes w.</span></span>
-   <span data-ttu-id="9b9d4-118">Регистры выходных и Офог должны использовать только одну маску.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-118">The oPts and oFog output registers must use only one mask.</span></span>
-   <span data-ttu-id="9b9d4-119">Для некоторых инструкций требуется, чтобы регистр назначения использовал одну маску записи: EXP, експп, log, логп, pow, rcp и РСК.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-119">Certain instructions require the destination register to use a single write mask: exp, expp, log, logp, pow, rcp, and rsq.</span></span>
-   <span data-ttu-id="9b9d4-120">В версии 1,0 инструкции ФРК требовалось одно из следующих сочетаний маски:. x или. y или. XY.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-120">In version 1.0, the frc instruction required one of the following mask combinations: .x or .y or .xy.</span></span> <span data-ttu-id="9b9d4-121">Версия 2,0 не имеет ограничений маски.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-121">Version 2.0 has no mask restriction.</span></span>
-   <span data-ttu-id="9b9d4-122">для синкос требуется одно из следующих сочетаний маски:. x или. y или. xyz.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-122">sincos requires one of the following mask combinations: .x or .y or .xyz.</span></span>
-   <span data-ttu-id="9b9d4-123">для m3x2 требуется маска записи. XY.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-123">m3x2 requires the .xy write mask.</span></span>
-   <span data-ttu-id="9b9d4-124">для m3x3 и m4x3 требуется маска записи. xyz.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-124">m3x3 and m4x3 require the .xyz write mask.</span></span>
-   <span data-ttu-id="9b9d4-125">m3x4 и m4x4 должны иметь маску записи. XYZ или маску записи по умолчанию (ксизв).</span><span class="sxs-lookup"><span data-stu-id="9b9d4-125">m3x4 and m4x4 require either the .xyz write mask or the default write mask (xyzw).</span></span>

## <a name="texture-register-masks"></a><span data-ttu-id="9b9d4-126">Маски регистров текстур</span><span class="sxs-lookup"><span data-stu-id="9b9d4-126">Texture Register Masks</span></span>

<span data-ttu-id="9b9d4-127">Правила проверки использования модификаторов в регистрах координат текстуры более тесны, чем правила проверки для других регистров.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-127">The validation rules for using modifiers on texture coordinate registers are tighter than the validation rules for other registers.</span></span>

-   <span data-ttu-id="9b9d4-128">При написании отн все предыдущие регистры (отн-1 ~ oT0) также должны быть записаны.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-128">If oTn is written, all previous registers (oTn-1 ~ oT0) have to be written as well.</span></span>
-   <span data-ttu-id="9b9d4-129">"Объединенная" маска записи для любого \# регистра объекта должна быть в точности одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="9b9d4-129">The "combined" write mask for any oT\# register must be exactly one of the following:</span></span>
    -   <span data-ttu-id="9b9d4-130">. x</span><span class="sxs-lookup"><span data-stu-id="9b9d4-130">.x</span></span>
    -   <span data-ttu-id="9b9d4-131">. XY</span><span class="sxs-lookup"><span data-stu-id="9b9d4-131">.xy</span></span>
    -   <span data-ttu-id="9b9d4-132">. XYZ</span><span class="sxs-lookup"><span data-stu-id="9b9d4-132">.xyz</span></span>
    -   <span data-ttu-id="9b9d4-133">. ксизв (эквивалентно не использованию модификаторов компонентов)</span><span class="sxs-lookup"><span data-stu-id="9b9d4-133">.xyzw (which is equivalent to not using any component modifiers)</span></span>

<span data-ttu-id="9b9d4-134">Например, шейдер вершин может выводить данные в регистры текстур в отдельных инструкциях.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-134">For example, a vertex shader can output to texture registers in separate instructions.</span></span>


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



<span data-ttu-id="9b9d4-135">Инструкции можно также объединить.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-135">Or, the instructions can be combined.</span></span>


```
    oT0.xyz  
    oT1.xy  
    oT2.xyzw    
```



<span data-ttu-id="9b9d4-136">Эти ограничения применяются только к регистрам координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="9b9d4-136">These restrictions apply only to the texture coordinate registers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b9d4-137">См. также</span><span class="sxs-lookup"><span data-stu-id="9b9d4-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b9d4-138">Модификаторы регистра для шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="9b9d4-138">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




