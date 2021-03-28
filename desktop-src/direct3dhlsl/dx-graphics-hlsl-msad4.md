---
title: msad4
description: Сравнивает 4-байтное ссылочное значение и 8-байтовое исходное значение и накапливает вектор с 4 суммами. Каждая сумма соответствует маскированной сумме абсолютных различий между значением ссылки и исходным значением.
ms.assetid: 6497F9AE-4524-44C2-A1C6-2A4ACB30FA9C
keywords:
- msad4 HLSL
topic_type:
- apiref
api_name:
- msad4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 552db3afd07677777b47e939d659c0f6e333e496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104984144"
---
# <a name="msad4"></a><span data-ttu-id="0a30a-105">msad4</span><span class="sxs-lookup"><span data-stu-id="0a30a-105">msad4</span></span>

<span data-ttu-id="0a30a-106">Сравнивает 4-байтное ссылочное значение и 8-байтовое исходное значение и накапливает вектор с 4 суммами.</span><span class="sxs-lookup"><span data-stu-id="0a30a-106">Compares a 4-byte reference value and an 8-byte source value and accumulates a vector of 4 sums.</span></span> <span data-ttu-id="0a30a-107">Каждая сумма соответствует маскированной сумме абсолютных различий между значением ссылки и исходным значением.</span><span class="sxs-lookup"><span data-stu-id="0a30a-107">Each sum corresponds to the masked sum of absolute differences of a different byte alignment between the reference value and the source value.</span></span>



| <span data-ttu-id="0a30a-108">uint4 Result = msad4 (ссылка uint, источник uint2, накопленный uint4);</span><span class="sxs-lookup"><span data-stu-id="0a30a-108">uint4 result = msad4(uint reference, uint2 source, uint4 accum);</span></span> |
|------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="0a30a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a30a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a30a-110"><span id="reference"></span><span id="REFERENCE"></span>*IsReference*</span><span class="sxs-lookup"><span data-stu-id="0a30a-110"><span id="reference"></span><span id="REFERENCE"></span>*reference*</span></span>
</dt> <dd>

<span data-ttu-id="0a30a-111">\[в \] массиве ссылок 4 байта в одном значении **uint** .</span><span class="sxs-lookup"><span data-stu-id="0a30a-111">\[in\] The reference array of 4 bytes in one **uint** value.</span></span>

</dd> <dt>

<span data-ttu-id="0a30a-112"><span id="source"></span><span id="SOURCE"></span>*источника*</span><span class="sxs-lookup"><span data-stu-id="0a30a-112"><span id="source"></span><span id="SOURCE"></span>*source*</span></span>
</dt> <dd>

<span data-ttu-id="0a30a-113">\[в \] исходном массиве из 8 байт в двух значениях **uint2** .</span><span class="sxs-lookup"><span data-stu-id="0a30a-113">\[in\] The source array of 8 bytes in two **uint2** values.</span></span>

</dd> <dt>

<span data-ttu-id="0a30a-114"><span id="accum"></span><span id="ACCUM"></span>*накоплен*</span><span class="sxs-lookup"><span data-stu-id="0a30a-114"><span id="accum"></span><span id="ACCUM"></span>*accum*</span></span>
</dt> <dd>

<span data-ttu-id="0a30a-115">\[в \] векторе из 4 значений.</span><span class="sxs-lookup"><span data-stu-id="0a30a-115">\[in\] A vector of 4 values.</span></span> <span data-ttu-id="0a30a-116">**msad4** добавляет этот вектор к маскированной сумме абсолютных различий между значением ссылки и исходным значением.</span><span class="sxs-lookup"><span data-stu-id="0a30a-116">**msad4** adds this vector to the masked sum of absolute differences of the different byte alignments between the reference value and the source value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a30a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a30a-117">Return Value</span></span>

<span data-ttu-id="0a30a-118">Вектор из 4 сумм.</span><span class="sxs-lookup"><span data-stu-id="0a30a-118">A vector of 4 sums.</span></span> <span data-ttu-id="0a30a-119">Каждая сумма соответствует маскированной сумме абсолютных различий между значением ссылки и исходным значением.</span><span class="sxs-lookup"><span data-stu-id="0a30a-119">Each sum corresponds to the masked sum of absolute differences of different byte alignments between the reference value and the source value.</span></span> <span data-ttu-id="0a30a-120">**msad4** не содержит разницы в сумме, если это различие замаскировано (то есть ссылочный байт равен 0).</span><span class="sxs-lookup"><span data-stu-id="0a30a-120">**msad4** doesn't include a difference in the sum if that difference is masked (that is, the reference byte is 0).</span></span>

## <a name="remarks"></a><span data-ttu-id="0a30a-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="0a30a-121">Remarks</span></span>

<span data-ttu-id="0a30a-122">Чтобы использовать встроенную функцию **msad4** в коде шейдера, вызовите метод [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) с [**\_ \_ \_ параметром D3D11 Feature D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) , чтобы убедиться, что устройство Direct3D поддерживает параметр [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) .</span><span class="sxs-lookup"><span data-stu-id="0a30a-122">To use the **msad4** intrinsic in your shader code, call the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) method with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) to verify that the Direct3D device supports the [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) feature option.</span></span> <span data-ttu-id="0a30a-123">Для встроенной функции **msad4** требуется драйвер дисплея WDDM 1,2, а все драйверы дисплея WDDM 1,2 должны поддерживать **msad4**.</span><span class="sxs-lookup"><span data-stu-id="0a30a-123">The **msad4** intrinsic requires a WDDM 1.2 display driver, and all WDDM 1.2 display drivers must support **msad4**.</span></span> <span data-ttu-id="0a30a-124">Если приложение создает устройство отрисовки с [уровнем функций](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 или 11,1, а целью компиляции является модель шейдера 5 или более поздней версии, исходный код HLSL может использовать встроенную функцию **msad4** .</span><span class="sxs-lookup"><span data-stu-id="0a30a-124">If your app creates a rendering device with [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 or 11.1 and the compilation target is shader model 5 or later, the HLSL source code can use the **msad4** intrinsic.</span></span>

<span data-ttu-id="0a30a-125">Возвращаемые значения точно до 65535.</span><span class="sxs-lookup"><span data-stu-id="0a30a-125">Return values are only accurate up to 65535.</span></span> <span data-ttu-id="0a30a-126">При вызове встроенной функции **msad4** с входными данными, которые могут привести к возвращенным значениям, превышающим 65535, **msad4** выдает неопределенные результаты.</span><span class="sxs-lookup"><span data-stu-id="0a30a-126">If you call the **msad4** intrinsic with inputs that might result in return values greater than 65535, **msad4** produces undefined results.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="0a30a-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0a30a-127">Minimum Shader Model</span></span>

<span data-ttu-id="0a30a-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="0a30a-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0a30a-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0a30a-129">Shader Model</span></span>                                                | <span data-ttu-id="0a30a-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="0a30a-130">Supported</span></span> |
|-------------------------------------------------------------|-----------|
| [<span data-ttu-id="0a30a-131">Модель шейдера 5 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="0a30a-131">Shader model 5 or later</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="0a30a-132">да</span><span class="sxs-lookup"><span data-stu-id="0a30a-132">yes</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="0a30a-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="0a30a-133">Examples</span></span>

<span data-ttu-id="0a30a-134">Ниже приведен пример вычисления результата для **msad4**:</span><span class="sxs-lookup"><span data-stu-id="0a30a-134">Here is an example result calculation for **msad4**:</span></span>


```
reference = 0xA100B2C3;
source.x = 0xD7B0C372
source.y = 0x4F57C2A3
accum = {1,2,3,4}
result.x alignment source: 0xD7B0C372
result.x = accum.x + |0xD7   0xA1| + 0 (masked) + |0xC3   0xB2| + |0x72   0xC3| = 1 + 54 + 0 + 17 + 81 = 153
result.y alignment source: 0xA3D7B0C3
result.y = accum.y + |0xA3   0xA1| + 0 (masked) + |0xB0   0xB2| + |0xC3   0xC3| = 2 + 2 + 0 + 2 + 0 = 6
result.z alignment source: 0xC2A3D7B0
result.z = accum.z + |0xC2   0xA1| + 0 (masked) + |0xD7   0xB2| + |0xB0   0xC3| = 3 + 33 + 0 + 37 + 19 = 92
result.w alignment source: 0x57C2A3D7
result.w = accum.w + |0x57   0xA1| + 0 (masked) + |0xA3   0xB2| + |0xD7   0xC3| = 4 + 74 + 0 + 15 + 20 = 113
result = {153,6,92,113}
```



<span data-ttu-id="0a30a-135">Ниже приведен пример того, как можно использовать **msad4** для поиска эталонного шаблона в буфере:</span><span class="sxs-lookup"><span data-stu-id="0a30a-135">Here is an example of how you can use **msad4** to search for a reference pattern within a buffer:</span></span>


```
uint4 accum = {0,0,0,0};
for(uint i=0;i<REF_SIZE;i++)
    accum = msad4(
        buf_ref[i], 
        uint2(buf_src[DTid.x+i], buf_src[DTid.x+i+1]), 
        accum);
buf_accum[DTid.x] = accum;
```



## <a name="requirements"></a><span data-ttu-id="0a30a-136">Требования</span><span class="sxs-lookup"><span data-stu-id="0a30a-136">Requirements</span></span>



| <span data-ttu-id="0a30a-137">Требование</span><span class="sxs-lookup"><span data-stu-id="0a30a-137">Requirement</span></span> | <span data-ttu-id="0a30a-138">Значение</span><span class="sxs-lookup"><span data-stu-id="0a30a-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="0a30a-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a30a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0a30a-140">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="0a30a-140">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>           |
| <span data-ttu-id="0a30a-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a30a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0a30a-142">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="0a30a-142">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a30a-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a30a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a30a-144">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="0a30a-144">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

