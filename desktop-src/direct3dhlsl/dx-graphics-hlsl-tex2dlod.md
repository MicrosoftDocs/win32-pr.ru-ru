---
title: tex2Dlod
description: Пример двухмерной текстуры с помощью MIP-карты. Лод mipmap указан в т.в.
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- tex2Dlod HLSL
topic_type:
- apiref
api_name:
- tex2Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f63a922fe86dc10d984369a1a872f84089b4db34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104983984"
---
# <a name="tex2dlod"></a><span data-ttu-id="8a0d3-105">tex2Dlod</span><span class="sxs-lookup"><span data-stu-id="8a0d3-105">tex2Dlod</span></span>

<span data-ttu-id="8a0d3-106">Пример двухмерной текстуры с помощью MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="8a0d3-106">Samples a 2D texture with mipmaps.</span></span> <span data-ttu-id="8a0d3-107">Лод mipmap указан в т.в.</span><span class="sxs-lookup"><span data-stu-id="8a0d3-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="8a0d3-108">RET tex2Dlod (s, t)</span><span class="sxs-lookup"><span data-stu-id="8a0d3-108">ret tex2Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="8a0d3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a0d3-109">Parameters</span></span>



| <span data-ttu-id="8a0d3-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="8a0d3-110">Item</span></span>                                                   | <span data-ttu-id="8a0d3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8a0d3-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="8a0d3-112"><span id="s"></span><span id="S"></span>*#d0*</span><span class="sxs-lookup"><span data-stu-id="8a0d3-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="8a0d3-113">\[в \] состоянии выборки.</span><span class="sxs-lookup"><span data-stu-id="8a0d3-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="8a0d3-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="8a0d3-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="8a0d3-115">\[в \] координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="8a0d3-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8a0d3-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a0d3-116">Return Value</span></span>

<span data-ttu-id="8a0d3-117">Значение данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="8a0d3-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="8a0d3-118">Описание типа</span><span class="sxs-lookup"><span data-stu-id="8a0d3-118">Type Description</span></span>



| <span data-ttu-id="8a0d3-119">Имя</span><span class="sxs-lookup"><span data-stu-id="8a0d3-119">Name</span></span> | <span data-ttu-id="8a0d3-120">В/Из</span><span class="sxs-lookup"><span data-stu-id="8a0d3-120">In/Out</span></span> | [<span data-ttu-id="8a0d3-121">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="8a0d3-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="8a0d3-122">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="8a0d3-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8a0d3-123">Размер</span><span class="sxs-lookup"><span data-stu-id="8a0d3-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="8a0d3-124">s</span><span class="sxs-lookup"><span data-stu-id="8a0d3-124">s</span></span>    | <span data-ttu-id="8a0d3-125">in</span><span class="sxs-lookup"><span data-stu-id="8a0d3-125">in</span></span>     | [<span data-ttu-id="8a0d3-126">**объектами**</span><span class="sxs-lookup"><span data-stu-id="8a0d3-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8a0d3-127">sampler2D</span><span class="sxs-lookup"><span data-stu-id="8a0d3-127">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="8a0d3-128">1</span><span class="sxs-lookup"><span data-stu-id="8a0d3-128">1</span></span>    |
| <span data-ttu-id="8a0d3-129">t</span><span class="sxs-lookup"><span data-stu-id="8a0d3-129">t</span></span>    | <span data-ttu-id="8a0d3-130">in</span><span class="sxs-lookup"><span data-stu-id="8a0d3-130">in</span></span>     | [<span data-ttu-id="8a0d3-131">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="8a0d3-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8a0d3-132">**float**</span><span class="sxs-lookup"><span data-stu-id="8a0d3-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8a0d3-133">4</span><span class="sxs-lookup"><span data-stu-id="8a0d3-133">4</span></span>    |
| <span data-ttu-id="8a0d3-134">обратно</span><span class="sxs-lookup"><span data-stu-id="8a0d3-134">ret</span></span>  | <span data-ttu-id="8a0d3-135">out</span><span class="sxs-lookup"><span data-stu-id="8a0d3-135">out</span></span>    | [<span data-ttu-id="8a0d3-136">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="8a0d3-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="8a0d3-137">**float**</span><span class="sxs-lookup"><span data-stu-id="8a0d3-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8a0d3-138">4</span><span class="sxs-lookup"><span data-stu-id="8a0d3-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8a0d3-139">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8a0d3-139">Minimum Shader Model</span></span>

<span data-ttu-id="8a0d3-140">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="8a0d3-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8a0d3-141">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8a0d3-141">Shader Model</span></span>                                                                       | <span data-ttu-id="8a0d3-142">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8a0d3-142">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8a0d3-143">[Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) и более высокие модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="8a0d3-143">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="8a0d3-144">да</span><span class="sxs-lookup"><span data-stu-id="8a0d3-144">yes</span></span>       |
| [<span data-ttu-id="8a0d3-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a0d3-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="8a0d3-146">Нет</span><span class="sxs-lookup"><span data-stu-id="8a0d3-146">no</span></span>        |
| [<span data-ttu-id="8a0d3-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a0d3-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="8a0d3-148">Нет</span><span class="sxs-lookup"><span data-stu-id="8a0d3-148">no</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="8a0d3-149">Примечания</span><span class="sxs-lookup"><span data-stu-id="8a0d3-149">Remarks</span></span>

<span data-ttu-id="8a0d3-150">Начиная с Direct3D 10 можно использовать новый синтаксис HLSL для доступа к текстурам и другим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="8a0d3-150">Starting with Direct3D 10, you can use new HLSL syntax to access textures and other resources.</span></span> <span data-ttu-id="8a0d3-151">Можно заменить встроенные функции поиска текстур, такие как **tex2Dlod**, более объектно-ориентированным стилем.</span><span class="sxs-lookup"><span data-stu-id="8a0d3-151">You can replace intrinsic-style texture lookup functions, such as **tex2Dlod**, with a more object-oriented style.</span></span> <span data-ttu-id="8a0d3-152">В этом объектно-ориентированном стиле текстуры отделены от образцов и имеют методы для загрузки и выборки.</span><span class="sxs-lookup"><span data-stu-id="8a0d3-152">In this object-oriented style, textures are decoupled from samplers and have methods for loading and sampling.</span></span>

<span data-ttu-id="8a0d3-153">Для примера двухмерной текстуры вместо использования **tex2Dlod** , как в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="8a0d3-153">To sample a 2D texture, instead of using **tex2Dlod** as in this code:</span></span>


```
sampler S;
...
color = tex2Dlod(S, Location);
```



<span data-ttu-id="8a0d3-154">Используйте метод [Самплелевел](dx-graphics-hlsl-to-samplelevel.md) [**объекта текстуры**](dx-graphics-hlsl-to-type.md) , как в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="8a0d3-154">Use the [SampleLevel](dx-graphics-hlsl-to-samplelevel.md) method of a [**Texture Object**](dx-graphics-hlsl-to-type.md) as in this code:</span></span>


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



<span data-ttu-id="8a0d3-155">Чтобы использовать функции поиска текстур в встроенном стиле, такие как **tex2Dlod**, с [моделью шейдер 4](dx-graphics-hlsl-sm4.md) и выше, используйте [**D3DCOMPILE \_ включить \_ обратную \_ Совместимость**](d3dcompile-constants.md) для компиляции.</span><span class="sxs-lookup"><span data-stu-id="8a0d3-155">To use the intrinsic-style texture lookup functions, such as **tex2Dlod**, with [shader model 4](dx-graphics-hlsl-sm4.md) and higher, use [**D3DCOMPILE\_ENABLE\_BACKWARDS\_COMPATIBILITY**](d3dcompile-constants.md) to compile.</span></span> <span data-ttu-id="8a0d3-156">Однако если вы хотите выбрать модель шейдера 4 и более поздних версий (даже [ \* \_ 4 \_ 0 \_ уровня \_ 9 \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) с новым объектно-ориентированным кодом стиля, переходите к более новой HLSL синтаксису.</span><span class="sxs-lookup"><span data-stu-id="8a0d3-156">However, if you want to target shader model 4 and higher (even [\*\_4\_0\_level\_9\_\*](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) with newer object-oriented style code, migrate to the newer HLSL syntax.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a0d3-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a0d3-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a0d3-158">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8a0d3-158">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

