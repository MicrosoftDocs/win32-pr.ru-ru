---
title: Функция асуинт
description: Повторно интерпретирует битовый шаблон 64-разрядного значения как два целых числа без знака (32).
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- Функция асуинт HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c54ed89e112482df4a54f35e24a04694e88fa490
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069152"
---
# <a name="asuint-function"></a><span data-ttu-id="ee44b-104">Функция асуинт</span><span class="sxs-lookup"><span data-stu-id="ee44b-104">asuint function</span></span>

<span data-ttu-id="ee44b-105">Повторно интерпретирует битовый шаблон 64-разрядного значения как два целых числа без знака (32).</span><span class="sxs-lookup"><span data-stu-id="ee44b-105">Reinterprets the bit pattern of a 64-bit value as two unsigned 32-bit integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee44b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee44b-106">Syntax</span></span>

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a><span data-ttu-id="ee44b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee44b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee44b-108">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee44b-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee44b-109">Тип: **Double**</span><span class="sxs-lookup"><span data-stu-id="ee44b-109">Type: **double**</span></span>

<span data-ttu-id="ee44b-110">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="ee44b-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="ee44b-111">*ловбитс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ee44b-111">*lowbits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee44b-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="ee44b-112">Type: **uint**</span></span>

<span data-ttu-id="ee44b-113">Младший 32-разрядный шаблон *значения*.</span><span class="sxs-lookup"><span data-stu-id="ee44b-113">The low 32-bit pattern of *value*.</span></span>

</dd> <dt>

<span data-ttu-id="ee44b-114">*хигхбитс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ee44b-114">*highbits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee44b-115">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="ee44b-115">Type: **uint**</span></span>

<span data-ttu-id="ee44b-116">Старший 32-разрядный шаблон *значения*.</span><span class="sxs-lookup"><span data-stu-id="ee44b-116">The high 32-bit pattern of *value*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee44b-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee44b-117">Return value</span></span>

<span data-ttu-id="ee44b-118">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ee44b-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee44b-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="ee44b-119">Remarks</span></span>

<span data-ttu-id="ee44b-120">Эта функция является альтернативной версией встроенной функции [**асуинт**](dx-graphics-hlsl-asuint.md) , которая была доступна в более ранних моделях шейдеров и была представлена для шейдера Model 5.</span><span class="sxs-lookup"><span data-stu-id="ee44b-120">This function is an alternate version of the [**asuint**](dx-graphics-hlsl-asuint.md) intrinsic that has been available in earlier shader models, and was introduced for Shader Model 5.</span></span> <span data-ttu-id="ee44b-121">Исходная функция (распознанная в компиляторе HLSL по другой сигнатуре) остается доступной для модели шейдера 5.</span><span class="sxs-lookup"><span data-stu-id="ee44b-121">The original function (recognized in the HLSL compiler by its different signature) remains available to Shader Model 5.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="ee44b-122">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ee44b-122">Minimum Shader Model</span></span>

<span data-ttu-id="ee44b-123">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ee44b-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ee44b-124">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ee44b-124">Shader Model</span></span>                                                                | <span data-ttu-id="ee44b-125">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ee44b-125">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ee44b-126">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="ee44b-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="ee44b-127">да</span><span class="sxs-lookup"><span data-stu-id="ee44b-127">yes</span></span>       |



 

<span data-ttu-id="ee44b-128">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ee44b-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="ee44b-129">Вершина</span><span class="sxs-lookup"><span data-stu-id="ee44b-129">Vertex</span></span> | <span data-ttu-id="ee44b-130">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ee44b-130">Hull</span></span> | <span data-ttu-id="ee44b-131">Домен</span><span class="sxs-lookup"><span data-stu-id="ee44b-131">Domain</span></span> | <span data-ttu-id="ee44b-132">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ee44b-132">Geometry</span></span> | <span data-ttu-id="ee44b-133">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ee44b-133">Pixel</span></span> | <span data-ttu-id="ee44b-134">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ee44b-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ee44b-135">x</span><span class="sxs-lookup"><span data-stu-id="ee44b-135">x</span></span>      | <span data-ttu-id="ee44b-136">x</span><span class="sxs-lookup"><span data-stu-id="ee44b-136">x</span></span>    | <span data-ttu-id="ee44b-137">x</span><span class="sxs-lookup"><span data-stu-id="ee44b-137">x</span></span>      | <span data-ttu-id="ee44b-138">x</span><span class="sxs-lookup"><span data-stu-id="ee44b-138">x</span></span>        | <span data-ttu-id="ee44b-139">x</span><span class="sxs-lookup"><span data-stu-id="ee44b-139">x</span></span>     | <span data-ttu-id="ee44b-140">x</span><span class="sxs-lookup"><span data-stu-id="ee44b-140">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ee44b-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee44b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee44b-142">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="ee44b-142">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="ee44b-143">**асуинт (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ee44b-143">**asuint (DirectX HLSL)**</span></span>](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[<span data-ttu-id="ee44b-144">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ee44b-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




