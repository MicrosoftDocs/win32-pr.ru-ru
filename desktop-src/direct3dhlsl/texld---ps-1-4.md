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
ms.openlocfilehash: d956d9176a6356dc3837ee4f4d13b5bb700dda98
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118829"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="6ba7c-104">текслд-PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="6ba7c-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="6ba7c-105">Загружает регистр назначения с использованием данных цвета (RGBA), которые выборке с помощью содержимого регистра исходного кода в качестве координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="6ba7c-106">Текстура выборки — это текстура, связанная с номером целевой регистрации.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="6ba7c-107">текслд DST, src</span><span class="sxs-lookup"><span data-stu-id="6ba7c-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="6ba7c-108">Регистры</span><span class="sxs-lookup"><span data-stu-id="6ba7c-108">Registers</span></span>



| <span data-ttu-id="6ba7c-109">Значение</span><span class="sxs-lookup"><span data-stu-id="6ba7c-109">Value</span></span>         | <span data-ttu-id="6ba7c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6ba7c-110">Description</span></span>                     | <span data-ttu-id="6ba7c-111">VN</span><span class="sxs-lookup"><span data-stu-id="6ba7c-111">vₙ</span></span>        | <span data-ttu-id="6ba7c-112">CN</span><span class="sxs-lookup"><span data-stu-id="6ba7c-112">cₙ</span></span>  | <span data-ttu-id="6ba7c-113">код</span><span class="sxs-lookup"><span data-stu-id="6ba7c-113">tₙ</span></span>  | <span data-ttu-id="6ba7c-114">RN</span><span class="sxs-lookup"><span data-stu-id="6ba7c-114">rₙ</span></span>  | <span data-ttu-id="6ba7c-115">Версия шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="6ba7c-115">Pixel shader version</span></span>              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| <span data-ttu-id="6ba7c-116">dst</span><span class="sxs-lookup"><span data-stu-id="6ba7c-116">dst</span></span>      | <span data-ttu-id="6ba7c-117">Регистр назначения</span><span class="sxs-lookup"><span data-stu-id="6ba7c-117">Destination register</span></span> |           |     |     | <span data-ttu-id="6ba7c-118">x</span><span class="sxs-lookup"><span data-stu-id="6ba7c-118">x</span></span>   | <span data-ttu-id="6ba7c-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="6ba7c-119">1\_4</span></span>         |
| <span data-ttu-id="6ba7c-120">src</span><span class="sxs-lookup"><span data-stu-id="6ba7c-120">src</span></span>      | <span data-ttu-id="6ba7c-121">Исходный регистр</span><span class="sxs-lookup"><span data-stu-id="6ba7c-121">Source register</span></span>      |           |     | <span data-ttu-id="6ba7c-122">x</span><span class="sxs-lookup"><span data-stu-id="6ba7c-122">x</span></span>   |     | <span data-ttu-id="6ba7c-123">1 \_ 4 этап 1</span><span class="sxs-lookup"><span data-stu-id="6ba7c-123">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="6ba7c-124">x</span><span class="sxs-lookup"><span data-stu-id="6ba7c-124">x</span></span>   | <span data-ttu-id="6ba7c-125">x</span><span class="sxs-lookup"><span data-stu-id="6ba7c-125">x</span></span>   | <span data-ttu-id="6ba7c-126">1 \_ 4 этапа</span><span class="sxs-lookup"><span data-stu-id="6ba7c-126">1\_4 phase</span></span>   |



 

<span data-ttu-id="6ba7c-127">При использовании r (n) в качестве исходного регистра первые три компонента (XYZ) должны быть инициализированы на предыдущем этапе шейдера.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-127">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="6ba7c-128">Дополнительные сведения о регистрах см. в разделе [PS \_ 1 \_ 1 PS 1 2 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ 3 \_ \_ \_ \_ registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="6ba7c-128">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6ba7c-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="6ba7c-129">Remarks</span></span>

<span data-ttu-id="6ba7c-130">В этой инструкции показана текстура на этапе текстуры, связанной с номером целевой регистрации.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-130">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="6ba7c-131">Текстура выдается с помощью данных о координатах текстуры из исходного регистра.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-131">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="6ba7c-132">Синтаксис инструкций текслд и текскрд предоставляет поддержку для проектного деления с помощью модификатора регистра текстуры.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-132">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="6ba7c-133">Для построителя текстуры версии 1,4 \_ флаг преобразования D3DTTFF прогнозной текстуры всегда игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-133">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="6ba7c-134">Правила использования текслд:</span><span class="sxs-lookup"><span data-stu-id="6ba7c-134">Rules for using texld:</span></span>

1.  <span data-ttu-id="6ba7c-135">Один и тот же модификатор. XYZ или. ксив должен применяться к каждому чтению отдельного регистра t (n) в инструкциях текскрд или текслд.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-135">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="6ba7c-136">Если. ксив используется в t (n) Register READS, это может быть смешано с другими операциями чтения того же регистра t (n) с помощью. ксив \_ DW.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-136">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="6ba7c-137">\_Модификатор источника DZ допустим только для текслд с исходным регистром r (n) (то есть только для фазы 2).</span><span class="sxs-lookup"><span data-stu-id="6ba7c-137">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="6ba7c-138">\_Модификатор источника DZ может использоваться не более двух раз на шейдер.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-138">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="6ba7c-139">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="6ba7c-139">Pixel shader versions</span></span> | <span data-ttu-id="6ba7c-140">1\_1</span><span class="sxs-lookup"><span data-stu-id="6ba7c-140">1\_1</span></span> | <span data-ttu-id="6ba7c-141">1\_2</span><span class="sxs-lookup"><span data-stu-id="6ba7c-141">1\_2</span></span> | <span data-ttu-id="6ba7c-142">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6ba7c-142">1\_3</span></span> | <span data-ttu-id="6ba7c-143">1\_4</span><span class="sxs-lookup"><span data-stu-id="6ba7c-143">1\_4</span></span> | <span data-ttu-id="6ba7c-144">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6ba7c-144">2\_0</span></span> | <span data-ttu-id="6ba7c-145">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6ba7c-145">2\_x</span></span> | <span data-ttu-id="6ba7c-146">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6ba7c-146">2\_sw</span></span> | <span data-ttu-id="6ba7c-147">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6ba7c-147">3\_0</span></span> | <span data-ttu-id="6ba7c-148">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6ba7c-148">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6ba7c-149">текслд</span><span class="sxs-lookup"><span data-stu-id="6ba7c-149">texld</span></span>                 |      |      |      | <span data-ttu-id="6ba7c-150">x</span><span class="sxs-lookup"><span data-stu-id="6ba7c-150">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="6ba7c-151">Примеры</span><span class="sxs-lookup"><span data-stu-id="6ba7c-151">Examples</span></span>

<span data-ttu-id="6ba7c-152">Инструкция текслд предлагает некоторый контроль над тем, какие компоненты исходных данных координат текстуры используются.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-152">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="6ba7c-153">Полный набор разрешенного синтаксиса для текслд приведен ниже и включает все допустимые модификаторы исходного регистра, селекторы и сочетания масок записи.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-153">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6ba7c-154">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="6ba7c-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ba7c-155">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="6ba7c-155">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




