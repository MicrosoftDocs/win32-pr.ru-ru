---
title: firstbitlow - функция
description: Возвращает расположение первого набора битов, начиная с наименьшего бита и работая над каждым компонентом.
ms.assetid: 204250f3-1a9b-445d-bd16-4cc9a5d9d60a
keywords:
- Функция фирстбитлов HLSL
topic_type:
- apiref
api_name:
- firstbitlow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a647314383bc022b7c3b3e1b5a255a42a099c620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070197"
---
# <a name="firstbitlow-function"></a><span data-ttu-id="234b0-104">firstbitlow - функция</span><span class="sxs-lookup"><span data-stu-id="234b0-104">firstbitlow function</span></span>

<span data-ttu-id="234b0-105">Возвращает расположение первого набора битов, начиная с наименьшего бита и работая над каждым компонентом.</span><span class="sxs-lookup"><span data-stu-id="234b0-105">Returns the location of the first set bit starting from the lowest order bit and working upward, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="234b0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="234b0-106">Syntax</span></span>

``` syntax
int firstbitlow(
  in int value
);
```

## <a name="parameters"></a><span data-ttu-id="234b0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="234b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="234b0-108">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="234b0-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="234b0-109">Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="234b0-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="234b0-110">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="234b0-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="234b0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="234b0-111">Return value</span></span>

<span data-ttu-id="234b0-112">Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="234b0-112">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="234b0-113">Расположение первого набора бит.</span><span class="sxs-lookup"><span data-stu-id="234b0-113">The location of the first set bit.</span></span>

## <a name="remarks"></a><span data-ttu-id="234b0-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="234b0-114">Remarks</span></span>

<span data-ttu-id="234b0-115">Также доступны следующие перегруженные версии:</span><span class="sxs-lookup"><span data-stu-id="234b0-115">The following overloaded versions are also available:</span></span>

``` syntax
uint2 firstbitlow(uint2 value);
uint3 firstbitlow(uint3 value);
uint4 firstbitlow(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="234b0-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="234b0-116">Minimum Shader Model</span></span>

<span data-ttu-id="234b0-117">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="234b0-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="234b0-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="234b0-118">Shader Model</span></span>                                                                | <span data-ttu-id="234b0-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="234b0-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="234b0-120">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="234b0-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="234b0-121">да</span><span class="sxs-lookup"><span data-stu-id="234b0-121">yes</span></span>       |



 

<span data-ttu-id="234b0-122">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="234b0-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="234b0-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="234b0-123">Vertex</span></span> | <span data-ttu-id="234b0-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="234b0-124">Hull</span></span> | <span data-ttu-id="234b0-125">Домен</span><span class="sxs-lookup"><span data-stu-id="234b0-125">Domain</span></span> | <span data-ttu-id="234b0-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="234b0-126">Geometry</span></span> | <span data-ttu-id="234b0-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="234b0-127">Pixel</span></span> | <span data-ttu-id="234b0-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="234b0-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="234b0-129">x</span><span class="sxs-lookup"><span data-stu-id="234b0-129">x</span></span>      | <span data-ttu-id="234b0-130">x</span><span class="sxs-lookup"><span data-stu-id="234b0-130">x</span></span>    | <span data-ttu-id="234b0-131">x</span><span class="sxs-lookup"><span data-stu-id="234b0-131">x</span></span>      | <span data-ttu-id="234b0-132">x</span><span class="sxs-lookup"><span data-stu-id="234b0-132">x</span></span>        | <span data-ttu-id="234b0-133">x</span><span class="sxs-lookup"><span data-stu-id="234b0-133">x</span></span>     | <span data-ttu-id="234b0-134">x</span><span class="sxs-lookup"><span data-stu-id="234b0-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="234b0-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="234b0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="234b0-136">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="234b0-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="234b0-137">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="234b0-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 