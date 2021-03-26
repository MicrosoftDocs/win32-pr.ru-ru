---
title: firstbithigh - функция
description: Возвращает расположение первого набора битов, начиная с самого высокого бита и заканчивая его обработкой вниз, на каждый компонент.
ms.assetid: 0fa89a9e-1706-44f7-8dd3-c37af5c11ddc
keywords:
- Функция фирстбисигх HLSL
topic_type:
- apiref
api_name:
- firstbithigh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4da4956aa3a12d064566a3767423f42039b01355
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413148"
---
# <a name="firstbithigh-function"></a><span data-ttu-id="ebccc-104">firstbithigh - функция</span><span class="sxs-lookup"><span data-stu-id="ebccc-104">firstbithigh function</span></span>

<span data-ttu-id="ebccc-105">Возвращает расположение первого набора битов, начиная с самого высокого бита и заканчивая его обработкой вниз, на каждый компонент.</span><span class="sxs-lookup"><span data-stu-id="ebccc-105">Gets the location of the first set bit starting from the highest order bit and working downward, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebccc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebccc-106">Syntax</span></span>

``` syntax
int firstbithigh(
  in int value
);
```

## <a name="parameters"></a><span data-ttu-id="ebccc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ebccc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebccc-108">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ebccc-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebccc-109">Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ebccc-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ebccc-110">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="ebccc-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebccc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ebccc-111">Return value</span></span>

<span data-ttu-id="ebccc-112">Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ebccc-112">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ebccc-113">Расположение первого набора бит.</span><span class="sxs-lookup"><span data-stu-id="ebccc-113">The location of the first set bit.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebccc-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ebccc-114">Remarks</span></span>

<span data-ttu-id="ebccc-115">Для целого числа со знаком Первый значащий бит равен нулю для отрицательного числа.</span><span class="sxs-lookup"><span data-stu-id="ebccc-115">For a signed integer, the first significant bit is zero for a negative number.</span></span>

<span data-ttu-id="ebccc-116">Также доступны следующие перегруженные версии:</span><span class="sxs-lookup"><span data-stu-id="ebccc-116">The following overloaded versions are also available:</span></span>

``` syntax
int2 firstbithigh(int2 value);
int3 firstbithigh(int3 value);
int4 firstbithigh(int4 value);
uint firstbithigh(uint value);
uint2 firstbithigh(uint2 value);
uint3 firstbithigh(uint3 value);
uint4 firstbithigh(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="ebccc-117">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ebccc-117">Minimum Shader Model</span></span>

<span data-ttu-id="ebccc-118">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ebccc-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ebccc-119">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ebccc-119">Shader Model</span></span>                                                                | <span data-ttu-id="ebccc-120">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ebccc-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ebccc-121">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="ebccc-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="ebccc-122">да</span><span class="sxs-lookup"><span data-stu-id="ebccc-122">yes</span></span>       |



 

<span data-ttu-id="ebccc-123">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ebccc-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="ebccc-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="ebccc-124">Vertex</span></span> | <span data-ttu-id="ebccc-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ebccc-125">Hull</span></span> | <span data-ttu-id="ebccc-126">Домен</span><span class="sxs-lookup"><span data-stu-id="ebccc-126">Domain</span></span> | <span data-ttu-id="ebccc-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ebccc-127">Geometry</span></span> | <span data-ttu-id="ebccc-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ebccc-128">Pixel</span></span> | <span data-ttu-id="ebccc-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ebccc-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ebccc-130">x</span><span class="sxs-lookup"><span data-stu-id="ebccc-130">x</span></span>      | <span data-ttu-id="ebccc-131">x</span><span class="sxs-lookup"><span data-stu-id="ebccc-131">x</span></span>    | <span data-ttu-id="ebccc-132">x</span><span class="sxs-lookup"><span data-stu-id="ebccc-132">x</span></span>      | <span data-ttu-id="ebccc-133">x</span><span class="sxs-lookup"><span data-stu-id="ebccc-133">x</span></span>        | <span data-ttu-id="ebccc-134">x</span><span class="sxs-lookup"><span data-stu-id="ebccc-134">x</span></span>     | <span data-ttu-id="ebccc-135">x</span><span class="sxs-lookup"><span data-stu-id="ebccc-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ebccc-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebccc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebccc-137">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="ebccc-137">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="ebccc-138">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ebccc-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 