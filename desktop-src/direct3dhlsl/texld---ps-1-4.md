---
title: текслд — ps_1_4
description: Загружает регистр назначения с использованием данных цвета (RGBA), которые выборке с помощью содержимого регистра исходного кода в качестве координат текстуры. Текстура выборки — это текстура, связанная с номером целевой регистрации.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca305b16db0f390354962a3e959f08b6e956f2ef
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996871"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="514db-104">текслд-PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="514db-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="514db-105">Загружает регистр назначения с использованием данных цвета (RGBA), которые выборке с помощью содержимого регистра исходного кода в качестве координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="514db-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="514db-106">Текстура выборки — это текстура, связанная с номером целевой регистрации.</span><span class="sxs-lookup"><span data-stu-id="514db-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="514db-107">текслд DST, src</span><span class="sxs-lookup"><span data-stu-id="514db-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="514db-108">Регистры</span><span class="sxs-lookup"><span data-stu-id="514db-108">Registers</span></span>



|          |                      | <span data-ttu-id="514db-109">VN</span><span class="sxs-lookup"><span data-stu-id="514db-109">vₙ</span></span>        | <span data-ttu-id="514db-110">CN</span><span class="sxs-lookup"><span data-stu-id="514db-110">cₙ</span></span>  | <span data-ttu-id="514db-111">код</span><span class="sxs-lookup"><span data-stu-id="514db-111">tₙ</span></span>  | <span data-ttu-id="514db-112">RN</span><span class="sxs-lookup"><span data-stu-id="514db-112">rₙ</span></span>  |              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| <span data-ttu-id="514db-113">кон</span><span class="sxs-lookup"><span data-stu-id="514db-113">dst</span></span>      | <span data-ttu-id="514db-114">Регистр назначения</span><span class="sxs-lookup"><span data-stu-id="514db-114">Destination register</span></span> |           |     |     | <span data-ttu-id="514db-115">x</span><span class="sxs-lookup"><span data-stu-id="514db-115">x</span></span>   | <span data-ttu-id="514db-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="514db-116">1\_4</span></span>         |
| <span data-ttu-id="514db-117">src</span><span class="sxs-lookup"><span data-stu-id="514db-117">src</span></span>      | <span data-ttu-id="514db-118">Исходный регистр</span><span class="sxs-lookup"><span data-stu-id="514db-118">Source register</span></span>      |           |     | <span data-ttu-id="514db-119">x</span><span class="sxs-lookup"><span data-stu-id="514db-119">x</span></span>   |     | <span data-ttu-id="514db-120">1 \_ 4 этап 1</span><span class="sxs-lookup"><span data-stu-id="514db-120">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="514db-121">x</span><span class="sxs-lookup"><span data-stu-id="514db-121">x</span></span>   | <span data-ttu-id="514db-122">x</span><span class="sxs-lookup"><span data-stu-id="514db-122">x</span></span>   | <span data-ttu-id="514db-123">1 \_ 4 этапа</span><span class="sxs-lookup"><span data-stu-id="514db-123">1\_4 phase</span></span>   |



 

<span data-ttu-id="514db-124">При использовании r (n) в качестве исходного регистра первые три компонента (XYZ) должны быть инициализированы на предыдущем этапе шейдера.</span><span class="sxs-lookup"><span data-stu-id="514db-124">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="514db-125">Дополнительные сведения о регистрах см. в разделе [PS \_ 1 \_ 1 PS 1 2 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ 3 \_ \_ \_ \_ registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="514db-125">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="514db-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="514db-126">Remarks</span></span>

<span data-ttu-id="514db-127">В этой инструкции показана текстура на этапе текстуры, связанной с номером целевой регистрации.</span><span class="sxs-lookup"><span data-stu-id="514db-127">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="514db-128">Текстура выдается с помощью данных о координатах текстуры из исходного регистра.</span><span class="sxs-lookup"><span data-stu-id="514db-128">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="514db-129">Синтаксис инструкций текслд и текскрд предоставляет поддержку для проектного деления с помощью модификатора регистра текстуры.</span><span class="sxs-lookup"><span data-stu-id="514db-129">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="514db-130">Для построителя текстуры версии 1,4 \_ флаг преобразования D3DTTFF прогнозной текстуры всегда игнорируется.</span><span class="sxs-lookup"><span data-stu-id="514db-130">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="514db-131">Правила использования текслд:</span><span class="sxs-lookup"><span data-stu-id="514db-131">Rules for using texld:</span></span>

1.  <span data-ttu-id="514db-132">Один и тот же модификатор. XYZ или. ксив должен применяться к каждому чтению отдельного регистра t (n) в инструкциях текскрд или текслд.</span><span class="sxs-lookup"><span data-stu-id="514db-132">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="514db-133">Если. ксив используется в t (n) Register READS, это может быть смешано с другими операциями чтения того же регистра t (n) с помощью. ксив \_ DW.</span><span class="sxs-lookup"><span data-stu-id="514db-133">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="514db-134">\_Модификатор источника DZ допустим только для текслд с исходным регистром r (n) (то есть только для фазы 2).</span><span class="sxs-lookup"><span data-stu-id="514db-134">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="514db-135">\_Модификатор источника DZ может использоваться не более двух раз на шейдер.</span><span class="sxs-lookup"><span data-stu-id="514db-135">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="514db-136">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="514db-136">Pixel shader versions</span></span> | <span data-ttu-id="514db-137">1\_1</span><span class="sxs-lookup"><span data-stu-id="514db-137">1\_1</span></span> | <span data-ttu-id="514db-138">1\_2</span><span class="sxs-lookup"><span data-stu-id="514db-138">1\_2</span></span> | <span data-ttu-id="514db-139">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="514db-139">1\_3</span></span> | <span data-ttu-id="514db-140">1\_4</span><span class="sxs-lookup"><span data-stu-id="514db-140">1\_4</span></span> | <span data-ttu-id="514db-141">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="514db-141">2\_0</span></span> | <span data-ttu-id="514db-142">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="514db-142">2\_x</span></span> | <span data-ttu-id="514db-143">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="514db-143">2\_sw</span></span> | <span data-ttu-id="514db-144">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="514db-144">3\_0</span></span> | <span data-ttu-id="514db-145">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="514db-145">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="514db-146">текслд</span><span class="sxs-lookup"><span data-stu-id="514db-146">texld</span></span>                 |      |      |      | <span data-ttu-id="514db-147">x</span><span class="sxs-lookup"><span data-stu-id="514db-147">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="514db-148">Примеры</span><span class="sxs-lookup"><span data-stu-id="514db-148">Examples</span></span>

<span data-ttu-id="514db-149">Инструкция текслд предлагает некоторый контроль над тем, какие компоненты исходных данных координат текстуры используются.</span><span class="sxs-lookup"><span data-stu-id="514db-149">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="514db-150">Полный набор разрешенного синтаксиса для текслд приведен ниже и включает все допустимые модификаторы исходного регистра, селекторы и сочетания масок записи.</span><span class="sxs-lookup"><span data-stu-id="514db-150">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


```
texld  r(m), t(n).xyz
// Uses xyz from t(n) to sample 1D, 2D, or 3D texture
```




```
texld  r(m), t(n)
// Same as previous
```




```
texld  r(m), t(n).xyw
// Uses xyw (skipping z) from t(n) to sample 1D, 2D or 3D texture
```




```
texld  r(m), t(n)_dw.xyw  
// Samples 1D or 2D texture at x/w, y/w from t(n). The result
// is undefined for a cube-map lookup.
```




```
texld  r(m), r(n).xyz
// Samples 1D, 2D, or 3D texture at xyz from r(m) 
// This is possible in the second phase of the shader
```




```
texld  r(m), r(n)
// Same as previous
```




```
texld  r(m), r(n)_dz.xyz
// Samples 1D or 2D texture at x/z, y/z from r(m)
// Possible only in second phase
// The result is undefined for a cube-map lookup
```




```
texld  r(n), r(n)_dz
// Same as previous
```



## <a name="related-topics"></a><span data-ttu-id="514db-151">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="514db-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="514db-152">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="514db-152">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




