---
title: Тип структуры
description: Тип структуры
ms.assetid: 896030b0-07cd-41bd-8c94-e173eabc81dd
keywords:
- HLSL типа структуры
topic_type:
- apiref
api_name:
- Struct Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89435e9c8757d2e732bc6237b02a508d3af4b4db
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119099"
---
# <a name="struct-type"></a><span data-ttu-id="49e61-104">Тип структуры</span><span class="sxs-lookup"><span data-stu-id="49e61-104">Struct Type</span></span>

<span data-ttu-id="49e61-105">Используйте следующий синтаксис, чтобы объявить структуру с помощью HLSL.</span><span class="sxs-lookup"><span data-stu-id="49e61-105">Use the following syntax to declare a structure using HLSL.</span></span>

<span data-ttu-id="49e61-106">*имя* структуры { \[ *интерполатионмодифиер* \] *Type* \[ *R* x *C* \] *MemberName*;     ... };</span><span class="sxs-lookup"><span data-stu-id="49e61-106">struct *Name*{     \[*InterpolationModifier*\] *Type*\[*R* x *C*\] *MemberName*;     ... };</span></span>



 

## <a name="parameters"></a><span data-ttu-id="49e61-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="49e61-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49e61-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Безымян*</span><span class="sxs-lookup"><span data-stu-id="49e61-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="49e61-109">Строка ASCII, однозначно определяющая имя структуры.</span><span class="sxs-lookup"><span data-stu-id="49e61-109">An ASCII string that uniquely identifies the structure name.</span></span>

</dd> <dt>

<span data-ttu-id="49e61-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*интерполатионмодифиер*\]</span><span class="sxs-lookup"><span data-stu-id="49e61-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]</span></span>
</dt> <dd>

<span data-ttu-id="49e61-111">Необязательный модификатор, задающий тип интерполяции.</span><span class="sxs-lookup"><span data-stu-id="49e61-111">Optional modifier that specifies an interpolation type.</span></span> <span data-ttu-id="49e61-112">Подробные сведения см. в разделе [Примечания](#remarks).</span><span class="sxs-lookup"><span data-stu-id="49e61-112">See [Remarks](#remarks) for details.</span></span>

</dd> <dt>

<span data-ttu-id="49e61-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Тип* \[ *R* x *C*\]</span><span class="sxs-lookup"><span data-stu-id="49e61-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Type*\[*R* x *C*\]</span></span>
</dt> <dd>

<span data-ttu-id="49e61-114">Тип элемента с необязательным размером массива столбца Row (*R*) x (*C*).</span><span class="sxs-lookup"><span data-stu-id="49e61-114">The member type with an optional row (*R*) x column (*C*) array size.</span></span> <span data-ttu-id="49e61-115">Структура содержит по крайней мере один элемент. Если он содержит несколько элементов, все они имеют один и тот же тип.</span><span class="sxs-lookup"><span data-stu-id="49e61-115">A structure contains at least one element; if it contains more than one element, the elements are all of the same type.</span></span> <span data-ttu-id="49e61-116">Число строк и столбцов — это целые числа без знака в диапазоне от 1 до 4 включительно.</span><span class="sxs-lookup"><span data-stu-id="49e61-116">The number of rows and columns are unsigned integers between 1 and 4 inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="49e61-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*</span><span class="sxs-lookup"><span data-stu-id="49e61-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*</span></span>
</dt> <dd>

<span data-ttu-id="49e61-118">Строка ASCII, однозначно определяющая имя элемента.</span><span class="sxs-lookup"><span data-stu-id="49e61-118">An ASCII string that uniquely identifies the member name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49e61-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="49e61-119">Remarks</span></span>

<span data-ttu-id="49e61-120">Модификатор интерполяции можно указать для любого члена структуры или аргумента в функции шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="49e61-120">An interpolation modifier can be specified on any structure member or on an argument to a pixel shader function.</span></span> <span data-ttu-id="49e61-121">Если модификатор присутствует в обоих местах, модификатор снаружи (модификатор аргумента пиксельного шейдера) переносит модификаторы внутрь (модификатор структуры).</span><span class="sxs-lookup"><span data-stu-id="49e61-121">If a modifier appears in both places, the outside modifier (the pixel shader argument modifier) overrules the inside modifier (the structure modifier).</span></span>

<span data-ttu-id="49e61-122">При компиляции шейдера или воздействия на пакеты компилятор шейдера члены структуры зависят от [правил упаковки HLSL](dx-graphics-hlsl-packing-rules.md).</span><span class="sxs-lookup"><span data-stu-id="49e61-122">When compiling a shader or an effect, the shader compiler packs structure members according to [HLSL packing rules](dx-graphics-hlsl-packing-rules.md).</span></span>

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a><span data-ttu-id="49e61-123">Модификаторы интерполяции, появившиеся в модели шейдеров 4</span><span class="sxs-lookup"><span data-stu-id="49e61-123">Interpolation Modifiers Introduced in Shader Model 4</span></span>

<span data-ttu-id="49e61-124">Выходные данные шейдера вершин, используемые для входных шейдеров пикселей, линейно интерполируются для получения значений в пикселях во время растрирования.</span><span class="sxs-lookup"><span data-stu-id="49e61-124">Vertex shader outputs that are used for pixel shader inputs are linearly interpolated to get per-pixel values during rasterization.</span></span> <span data-ttu-id="49e61-125">Чтобы задать метод интерполяции, используйте любое из следующих значений, которые поддерживаются в [модели шейдеров 4](dx-graphics-hlsl-sm4.md) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="49e61-125">To set the method of interpolation, use any of the following values, which are supported in [shader model 4](dx-graphics-hlsl-sm4.md) or later.</span></span> <span data-ttu-id="49e61-126">Модификатор игнорируется на выходных данных шейдера вершин, которые не используются в качестве входных шейдеров пикселей.</span><span class="sxs-lookup"><span data-stu-id="49e61-126">The modifier is ignored on any vertex shader output that is not used as a pixel shader input.</span></span>



| <span data-ttu-id="49e61-127">Модификатор интерполяции</span><span class="sxs-lookup"><span data-stu-id="49e61-127">Interpolation Modifier</span></span> | <span data-ttu-id="49e61-128">Описание</span><span class="sxs-lookup"><span data-stu-id="49e61-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49e61-129">**линейной**</span><span class="sxs-lookup"><span data-stu-id="49e61-129">**linear**</span></span>             | <span data-ttu-id="49e61-130">Интерполяция между входными данными шейдера; значение по умолчанию — **линейное** , если модификатор интерполяции не задан.</span><span class="sxs-lookup"><span data-stu-id="49e61-130">Interpolate between shader inputs; **linear** is the default value if no interpolation modifier is specified.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="49e61-131">**центроид**</span><span class="sxs-lookup"><span data-stu-id="49e61-131">**centroid**</span></span>           | <span data-ttu-id="49e61-132">Интерполяция между образцами в охваченной области пикселя (для этого может потребоваться экстраполяция конечных точек из пиксельного центра).</span><span class="sxs-lookup"><span data-stu-id="49e61-132">Interpolate between samples that are somewhere within the covered area of the pixel (this may require extrapolating end points from a pixel center).</span></span> <span data-ttu-id="49e61-133">Выборка центроид может улучшить сглаживание при частичном покрытии пикселя (даже если он не охватывает точек).</span><span class="sxs-lookup"><span data-stu-id="49e61-133">Centroid sampling may improve antialiasing if a pixel is partially covered (even if the pixel center is not covered).</span></span> <span data-ttu-id="49e61-134">Модификатор **центроид** должен сочетаться с модификатором **линейной** или **проекции** .</span><span class="sxs-lookup"><span data-stu-id="49e61-134">The **centroid** modifier must be combined with either the **linear** or **noperspective** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="49e61-135">**Интерполяция**</span><span class="sxs-lookup"><span data-stu-id="49e61-135">**nointerpolation**</span></span>    | <span data-ttu-id="49e61-136">Не выполнять интерполяцию.</span><span class="sxs-lookup"><span data-stu-id="49e61-136">Do not interpolate .</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="49e61-137">**Перспектива**</span><span class="sxs-lookup"><span data-stu-id="49e61-137">**noperspective**</span></span>      | <span data-ttu-id="49e61-138">Не выполнять исправление перспективы во время интерполяции.</span><span class="sxs-lookup"><span data-stu-id="49e61-138">Do not perform perspective-correction during interpolation.</span></span> <span data-ttu-id="49e61-139">Модификатор **"Перспектива"** можно сочетать с модификатором **центроид** .</span><span class="sxs-lookup"><span data-stu-id="49e61-139">The **noperspective** modifier can be combined with the **centroid** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="49e61-140">**Следующий**</span><span class="sxs-lookup"><span data-stu-id="49e61-140">**sample**</span></span>             | <span data-ttu-id="49e61-141">**Доступно в модели шейдеров 4,1 и более поздних версий** Интерполяция в месте выборки, а не в центре пикселей.</span><span class="sxs-lookup"><span data-stu-id="49e61-141">**Available in shader model 4.1 and later** Interpolate at sample location rather than at the pixel center.</span></span> <span data-ttu-id="49e61-142">Это приводит к тому, что шейдер пикселей выполняется для каждого образца, а не для пикселя.</span><span class="sxs-lookup"><span data-stu-id="49e61-142">This causes the pixel shader to execute per-sample rather than per-pixel.</span></span> <span data-ttu-id="49e61-143">Другой способ выполнения отдельных примеров — наличие входных данных с [семантическим SV \_ SampleIndex](dx-graphics-hlsl-semantics.md), который указывает текущий пример.</span><span class="sxs-lookup"><span data-stu-id="49e61-143">Another way to cause per-sample execution is to have an input with [semantic SV\_SampleIndex](dx-graphics-hlsl-semantics.md), which indicates the current sample.</span></span> <span data-ttu-id="49e61-144">Только входные данные с указанным **образцом** (или \_ SampleIndex SV) отличаются между вызовами шейдера в пикселе, тогда как другие входы, которые не задают модификаторы (например, при смешении модификаторов для различных входов), по-прежнему интерполируются в пикселном центре.</span><span class="sxs-lookup"><span data-stu-id="49e61-144">Only the inputs with **sample** specified (or inputting SV\_SampleIndex) differ between shader invocations in the pixel, whereas other inputs that do not specify modifiers (for example, if you mix modifiers on different inputs) still interpolate at the pixel center.</span></span> <span data-ttu-id="49e61-145">При каждом охваченном образце в пикселе выводятся как вызов шейдера пикселей, так и проверка глубины или трафарета.</span><span class="sxs-lookup"><span data-stu-id="49e61-145">Both pixel shader invocation and depth/stencil testing occur for every covered sample in the pixel.</span></span> <span data-ttu-id="49e61-146">Иногда это называется « *ресамплинг*».</span><span class="sxs-lookup"><span data-stu-id="49e61-146">This is sometimes known as *supersampling*.</span></span> <span data-ttu-id="49e61-147">В отличие от того, что в случае отсутствия выборки частоты, известной как *многовыборочная*, построитель текстуры вызывается один раз на пиксель, независимо от количества охваченных выборок, в то время как при тестировании глубины или шаблона возникает частота выборки.</span><span class="sxs-lookup"><span data-stu-id="49e61-147">In contrast, in the absence of sample frequency invocation, known as *multisampling*, the pixel shader is invoked once per pixel regardless of how many samples are covered, while depth/stencil testing occurs at sample frequency.</span></span> <span data-ttu-id="49e61-148">Оба режима обеспечивают эквивалентное сглаживание краев.</span><span class="sxs-lookup"><span data-stu-id="49e61-148">Both modes provide equivalent edge antialiasing.</span></span> <span data-ttu-id="49e61-149">Тем не менее, ресамплинг обеспечивает лучшее качество заливки, чаще вызывая построитель текстуры.</span><span class="sxs-lookup"><span data-stu-id="49e61-149">However, supersampling provides better shading quality by invoking the pixel shader more frequently.</span></span><br/> |



 

<dl> <span data-ttu-id="49e61-150">1. При использовании типа int/uint единственным допустимым параметром является " **интерполяция**".</span><span class="sxs-lookup"><span data-stu-id="49e61-150">1. When using an int/uint type, the only valid option is **nointerpolation**.</span></span>  
</dl>

<span data-ttu-id="49e61-151">Модификаторы интерполяции могут применяться к членам структуры или [аргументам функций](dx-graphics-hlsl-function-parameters.md)или к обоим.</span><span class="sxs-lookup"><span data-stu-id="49e61-151">Interpolation modifiers can be applied to structure members or [function arguments](dx-graphics-hlsl-function-parameters.md), or both.</span></span>

## <a name="examples"></a><span data-ttu-id="49e61-152">Примеры</span><span class="sxs-lookup"><span data-stu-id="49e61-152">Examples</span></span>

<span data-ttu-id="49e61-153">Ниже приведено несколько примеров объявлений структуры.</span><span class="sxs-lookup"><span data-stu-id="49e61-153">Here are some example structure declarations.</span></span>


```
struct struct1
{
  int    a;
}
```



<span data-ttu-id="49e61-154">Это объявление включает массив.</span><span class="sxs-lookup"><span data-stu-id="49e61-154">This declaration includes an array.</span></span>


```
struct struct2
{
  int    a;
  float  b;
  int4x4 iMatrix;
}
```



<span data-ttu-id="49e61-155">Это объявление включает модификатор интерполяции.</span><span class="sxs-lookup"><span data-stu-id="49e61-155">This declaration includes an interpolation modifier.</span></span>


```
struct In
{
  centroid float2 Texcoord;
};
```



## <a name="see-also"></a><span data-ttu-id="49e61-156">См. также</span><span class="sxs-lookup"><span data-stu-id="49e61-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e61-157">Типы данных (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="49e61-157">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





