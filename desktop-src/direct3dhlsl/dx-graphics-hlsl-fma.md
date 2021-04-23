---
title: FMA (Корекрт \_ Math. h)
description: Возвращает плавкий предохранитель с двойной точностью сложения a \ b + c.
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- FMA HLSL
topic_type:
- apiref
api_name:
- fma
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287f07881a00ca53a3f1fe702cf4d95b64bf14c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415484"
---
# <a name="fma"></a><span data-ttu-id="7c5da-104">fma</span><span class="sxs-lookup"><span data-stu-id="7c5da-104">fma</span></span>

<span data-ttu-id="7c5da-105">Возвращает предохранитель с двойной точностью, умноженный на " \* b + c".</span><span class="sxs-lookup"><span data-stu-id="7c5da-105">Returns the double-precision fused multiply-addition of a \* b + c.</span></span>



| <span data-ttu-id="7c5da-106">*RET* FMA (двойное *a*, *b*, *c*);</span><span class="sxs-lookup"><span data-stu-id="7c5da-106">*ret* fma(double *a*, *b*, *c*);</span></span> |
|----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="7c5da-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c5da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c5da-108"><span id="a"></span><span id="A"></span>*конкретного*</span><span class="sxs-lookup"><span data-stu-id="7c5da-108"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="7c5da-109">\[в \] первом значении с плавким предохранителем.</span><span class="sxs-lookup"><span data-stu-id="7c5da-109">\[in\] The first value in the fused multiply-addition.</span></span>

</dd> <dt>

<span data-ttu-id="7c5da-110"><span id="b"></span><span id="B"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="7c5da-110"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="7c5da-111">\[во \] втором значении с плавким предохранителем.</span><span class="sxs-lookup"><span data-stu-id="7c5da-111">\[in\] The second value in the fused multiply-addition.</span></span>

</dd> <dt>

<span data-ttu-id="7c5da-112"><span id="c"></span><span id="C"></span>*ц*</span><span class="sxs-lookup"><span data-stu-id="7c5da-112"><span id="c"></span><span id="C"></span>*c*</span></span>
</dt> <dd>

<span data-ttu-id="7c5da-113">\[в \] третьем значении с плавким предохранителем.</span><span class="sxs-lookup"><span data-stu-id="7c5da-113">\[in\] The third value in the fused multiply-addition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c5da-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c5da-114">Return Value</span></span>

<span data-ttu-id="7c5da-115">Предохранитель с двойной точностью — сложение параметров *a* \* *b*  +  *c*.</span><span class="sxs-lookup"><span data-stu-id="7c5da-115">The double-precision fused multiply-addition of parameters *a* \* *b* + *c*.</span></span> <span data-ttu-id="7c5da-116">Возвращаемое значение должно быть точным до 0,5 единиц с наименьшей точностью (ULP).</span><span class="sxs-lookup"><span data-stu-id="7c5da-116">The returned value must be accurate to 0.5 units of least precision (ULP).</span></span>

## <a name="remarks"></a><span data-ttu-id="7c5da-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="7c5da-117">Remarks</span></span>

<span data-ttu-id="7c5da-118">Встроенная функция **FMA** должна поддерживать значений NaN, INF и денормы.</span><span class="sxs-lookup"><span data-stu-id="7c5da-118">The **fma** intrinsic must support NaNs, INFs, and Denorms.</span></span>

<span data-ttu-id="7c5da-119">Чтобы использовать встроенную функцию **FMA** в коде шейдера, вызовите метод [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) с [**\_ \_ \_ параметром D3D11 Feature D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) , чтобы убедиться, что устройство Direct3D поддерживает параметр [**екстендеддаублесшадеринструктионс**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) .</span><span class="sxs-lookup"><span data-stu-id="7c5da-119">To use the **fma** intrinsic in your shader code, call the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) method with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) to verify that the Direct3D device supports the [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) feature option.</span></span> <span data-ttu-id="7c5da-120">Для встроенной функции **FMA** требуется драйвер дисплея WDDM 1,2, а все драйверы дисплея WDDM 1,2 должны поддерживать **FMA**.</span><span class="sxs-lookup"><span data-stu-id="7c5da-120">The **fma** intrinsic requires a WDDM 1.2 display driver, and all WDDM 1.2 display drivers must support **fma**.</span></span> <span data-ttu-id="7c5da-121">Если приложение создает устройство отрисовки с [уровнем функций](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 или 11,1, а целью компиляции является модель шейдера 5 или более поздней версии, исходный код HLSL может использовать встроенную функцию **FMA** .</span><span class="sxs-lookup"><span data-stu-id="7c5da-121">If your app creates a rendering device with [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 or 11.1 and the compilation target is shader model 5 or later, the HLSL source code can use the **fma** intrinsic.</span></span>

### <a name="type-description"></a><span data-ttu-id="7c5da-122">Описание типа</span><span class="sxs-lookup"><span data-stu-id="7c5da-122">Type Description</span></span>



| <span data-ttu-id="7c5da-123">Имя</span><span class="sxs-lookup"><span data-stu-id="7c5da-123">Name</span></span>  | [<span data-ttu-id="7c5da-124">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="7c5da-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="7c5da-125">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="7c5da-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="7c5da-126">Размер</span><span class="sxs-lookup"><span data-stu-id="7c5da-126">Size</span></span>                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| <span data-ttu-id="7c5da-127">*конкретного*</span><span class="sxs-lookup"><span data-stu-id="7c5da-127">*a*</span></span>   | <span data-ttu-id="7c5da-128">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="7c5da-128">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="7c5da-129">**Дважды**</span><span class="sxs-lookup"><span data-stu-id="7c5da-129">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="7c5da-130">any</span><span class="sxs-lookup"><span data-stu-id="7c5da-130">any</span></span>                          |
| <span data-ttu-id="7c5da-131">*b*</span><span class="sxs-lookup"><span data-stu-id="7c5da-131">*b*</span></span>   | <span data-ttu-id="7c5da-132">то же, что и входные данные *a*</span><span class="sxs-lookup"><span data-stu-id="7c5da-132">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="7c5da-133">**Дважды**</span><span class="sxs-lookup"><span data-stu-id="7c5da-133">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="7c5da-134">те же измерения, что и входные данные *a*</span><span class="sxs-lookup"><span data-stu-id="7c5da-134">same dimensions as input *a*</span></span> |
| <span data-ttu-id="7c5da-135">*c*</span><span class="sxs-lookup"><span data-stu-id="7c5da-135">*c*</span></span>   | <span data-ttu-id="7c5da-136">то же, что и входные данные *a*</span><span class="sxs-lookup"><span data-stu-id="7c5da-136">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="7c5da-137">**Дважды**</span><span class="sxs-lookup"><span data-stu-id="7c5da-137">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="7c5da-138">те же измерения, что и входные данные *a*</span><span class="sxs-lookup"><span data-stu-id="7c5da-138">same dimensions as input *a*</span></span> |
| <span data-ttu-id="7c5da-139">*обратно*</span><span class="sxs-lookup"><span data-stu-id="7c5da-139">*ret*</span></span> | <span data-ttu-id="7c5da-140">то же, что и входные данные *a*</span><span class="sxs-lookup"><span data-stu-id="7c5da-140">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="7c5da-141">**Дважды**</span><span class="sxs-lookup"><span data-stu-id="7c5da-141">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="7c5da-142">те же измерения, что и входные данные *a*</span><span class="sxs-lookup"><span data-stu-id="7c5da-142">same dimensions as input *a*</span></span> |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="7c5da-143">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7c5da-143">Minimum Shader Model</span></span>

<span data-ttu-id="7c5da-144">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="7c5da-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7c5da-145">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7c5da-145">Shader Model</span></span>                                                | <span data-ttu-id="7c5da-146">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="7c5da-146">Supported</span></span> |
|-------------------------------------------------------------|-----------|
| [<span data-ttu-id="7c5da-147">Модель шейдера 5 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7c5da-147">Shader model 5 or later</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="7c5da-148">да</span><span class="sxs-lookup"><span data-stu-id="7c5da-148">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="7c5da-149">Требования</span><span class="sxs-lookup"><span data-stu-id="7c5da-149">Requirements</span></span>



| <span data-ttu-id="7c5da-150">Требование</span><span class="sxs-lookup"><span data-stu-id="7c5da-150">Requirement</span></span> | <span data-ttu-id="7c5da-151">Значение</span><span class="sxs-lookup"><span data-stu-id="7c5da-151">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c5da-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c5da-152">Minimum supported client</span></span><br/> | <span data-ttu-id="7c5da-153">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="7c5da-153">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="7c5da-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c5da-154">Minimum supported server</span></span><br/> | <span data-ttu-id="7c5da-155">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="7c5da-155">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="7c5da-156">Header</span><span class="sxs-lookup"><span data-stu-id="7c5da-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c5da-157"><dt>Корекрт \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c5da-157"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c5da-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c5da-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c5da-159">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="7c5da-159">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

