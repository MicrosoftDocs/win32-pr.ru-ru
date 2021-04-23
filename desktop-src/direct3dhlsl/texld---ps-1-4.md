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
ms.openlocfilehash: 23827dffc396a40be134be4db3996d2e9f498288
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996939"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="01f4a-104">текслд-PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="01f4a-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="01f4a-105">Загружает регистр назначения с использованием данных цвета (RGBA), которые выборке с помощью содержимого регистра исходного кода в качестве координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="01f4a-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="01f4a-106">Текстура выборки — это текстура, связанная с номером целевой регистрации.</span><span class="sxs-lookup"><span data-stu-id="01f4a-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="01f4a-107">текслд DST, src</span><span class="sxs-lookup"><span data-stu-id="01f4a-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="01f4a-108">Регистры</span><span class="sxs-lookup"><span data-stu-id="01f4a-108">Registers</span></span>



| <span data-ttu-id="01f4a-109">Аргумент</span><span class="sxs-lookup"><span data-stu-id="01f4a-109">Argument</span></span> | <span data-ttu-id="01f4a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="01f4a-110">Description</span></span>          | <span data-ttu-id="01f4a-111">Регистры</span><span class="sxs-lookup"><span data-stu-id="01f4a-111">Registers</span></span> |     |     |     | <span data-ttu-id="01f4a-112">Version</span><span class="sxs-lookup"><span data-stu-id="01f4a-112">Version</span></span>      |
|----------|----------------------|-----------|-----|-----|-----|--------------|
|          |                      | <span data-ttu-id="01f4a-113">VN</span><span class="sxs-lookup"><span data-stu-id="01f4a-113">vₙ</span></span>        | <span data-ttu-id="01f4a-114">CN</span><span class="sxs-lookup"><span data-stu-id="01f4a-114">cₙ</span></span>  | <span data-ttu-id="01f4a-115">код</span><span class="sxs-lookup"><span data-stu-id="01f4a-115">tₙ</span></span>  | <span data-ttu-id="01f4a-116">RN</span><span class="sxs-lookup"><span data-stu-id="01f4a-116">rₙ</span></span>  |              |
| <span data-ttu-id="01f4a-117">кон</span><span class="sxs-lookup"><span data-stu-id="01f4a-117">dst</span></span>      | <span data-ttu-id="01f4a-118">Регистр назначения</span><span class="sxs-lookup"><span data-stu-id="01f4a-118">Destination register</span></span> |           |     |     | <span data-ttu-id="01f4a-119">x</span><span class="sxs-lookup"><span data-stu-id="01f4a-119">x</span></span>   | <span data-ttu-id="01f4a-120">1\_4</span><span class="sxs-lookup"><span data-stu-id="01f4a-120">1\_4</span></span>         |
| <span data-ttu-id="01f4a-121">src</span><span class="sxs-lookup"><span data-stu-id="01f4a-121">src</span></span>      | <span data-ttu-id="01f4a-122">Исходный регистр</span><span class="sxs-lookup"><span data-stu-id="01f4a-122">Source register</span></span>      |           |     | <span data-ttu-id="01f4a-123">x</span><span class="sxs-lookup"><span data-stu-id="01f4a-123">x</span></span>   |     | <span data-ttu-id="01f4a-124">1 \_ 4 этап 1</span><span class="sxs-lookup"><span data-stu-id="01f4a-124">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="01f4a-125">x</span><span class="sxs-lookup"><span data-stu-id="01f4a-125">x</span></span>   | <span data-ttu-id="01f4a-126">x</span><span class="sxs-lookup"><span data-stu-id="01f4a-126">x</span></span>   | <span data-ttu-id="01f4a-127">1 \_ 4 этапа</span><span class="sxs-lookup"><span data-stu-id="01f4a-127">1\_4 phase</span></span>   |



 

<span data-ttu-id="01f4a-128">При использовании r (n) в качестве исходного регистра первые три компонента (XYZ) должны быть инициализированы на предыдущем этапе шейдера.</span><span class="sxs-lookup"><span data-stu-id="01f4a-128">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="01f4a-129">Дополнительные сведения о регистрах см. в разделе [PS \_ 1 \_ 1 PS 1 2 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ 3 \_ \_ \_ \_ registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="01f4a-129">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="01f4a-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="01f4a-130">Remarks</span></span>

<span data-ttu-id="01f4a-131">В этой инструкции показана текстура на этапе текстуры, связанной с номером целевой регистрации.</span><span class="sxs-lookup"><span data-stu-id="01f4a-131">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="01f4a-132">Текстура выдается с помощью данных о координатах текстуры из исходного регистра.</span><span class="sxs-lookup"><span data-stu-id="01f4a-132">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="01f4a-133">Синтаксис инструкций текслд и текскрд предоставляет поддержку для проектного деления с помощью модификатора регистра текстуры.</span><span class="sxs-lookup"><span data-stu-id="01f4a-133">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="01f4a-134">Для построителя текстуры версии 1,4 \_ флаг преобразования D3DTTFF прогнозной текстуры всегда игнорируется.</span><span class="sxs-lookup"><span data-stu-id="01f4a-134">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="01f4a-135">Правила использования текслд:</span><span class="sxs-lookup"><span data-stu-id="01f4a-135">Rules for using texld:</span></span>

1.  <span data-ttu-id="01f4a-136">Один и тот же модификатор. XYZ или. ксив должен применяться к каждому чтению отдельного регистра t (n) в инструкциях текскрд или текслд.</span><span class="sxs-lookup"><span data-stu-id="01f4a-136">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="01f4a-137">Если. ксив используется в t (n) Register READS, это может быть смешано с другими операциями чтения того же регистра t (n) с помощью. ксив \_ DW.</span><span class="sxs-lookup"><span data-stu-id="01f4a-137">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="01f4a-138">\_Модификатор источника DZ допустим только для текслд с исходным регистром r (n) (то есть только для фазы 2).</span><span class="sxs-lookup"><span data-stu-id="01f4a-138">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="01f4a-139">\_Модификатор источника DZ может использоваться не более двух раз на шейдер.</span><span class="sxs-lookup"><span data-stu-id="01f4a-139">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="01f4a-140">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="01f4a-140">Pixel shader versions</span></span> | <span data-ttu-id="01f4a-141">1\_1</span><span class="sxs-lookup"><span data-stu-id="01f4a-141">1\_1</span></span> | <span data-ttu-id="01f4a-142">1\_2</span><span class="sxs-lookup"><span data-stu-id="01f4a-142">1\_2</span></span> | <span data-ttu-id="01f4a-143">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="01f4a-143">1\_3</span></span> | <span data-ttu-id="01f4a-144">1\_4</span><span class="sxs-lookup"><span data-stu-id="01f4a-144">1\_4</span></span> | <span data-ttu-id="01f4a-145">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="01f4a-145">2\_0</span></span> | <span data-ttu-id="01f4a-146">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="01f4a-146">2\_x</span></span> | <span data-ttu-id="01f4a-147">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="01f4a-147">2\_sw</span></span> | <span data-ttu-id="01f4a-148">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="01f4a-148">3\_0</span></span> | <span data-ttu-id="01f4a-149">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="01f4a-149">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="01f4a-150">текслд</span><span class="sxs-lookup"><span data-stu-id="01f4a-150">texld</span></span>                 |      |      |      | <span data-ttu-id="01f4a-151">x</span><span class="sxs-lookup"><span data-stu-id="01f4a-151">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="01f4a-152">Примеры</span><span class="sxs-lookup"><span data-stu-id="01f4a-152">Examples</span></span>

<span data-ttu-id="01f4a-153">Инструкция текслд предлагает некоторый контроль над тем, какие компоненты исходных данных координат текстуры используются.</span><span class="sxs-lookup"><span data-stu-id="01f4a-153">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="01f4a-154">Полный набор разрешенного синтаксиса для текслд приведен ниже и включает все допустимые модификаторы исходного регистра, селекторы и сочетания масок записи.</span><span class="sxs-lookup"><span data-stu-id="01f4a-154">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="01f4a-155">См. также</span><span class="sxs-lookup"><span data-stu-id="01f4a-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01f4a-156">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="01f4a-156">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




