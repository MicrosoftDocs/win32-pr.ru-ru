---
title: Функция асдаубле
description: Повторно интерпретирует значение приведения (2 32-разрядные значения) в Double.
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- Функция асдаубле HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa2c83ee01739a2e2ee9595d0a26e1bdb80fef1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069153"
---
# <a name="asdouble-function"></a><span data-ttu-id="de8cd-104">Функция асдаубле</span><span class="sxs-lookup"><span data-stu-id="de8cd-104">asdouble function</span></span>

<span data-ttu-id="de8cd-105">Повторно интерпретирует значение приведения (2 32-разрядные значения) в Double.</span><span class="sxs-lookup"><span data-stu-id="de8cd-105">Reinterprets a cast value (two 32-bit values) into a double.</span></span>

## <a name="syntax"></a><span data-ttu-id="de8cd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de8cd-106">Syntax</span></span>

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a><span data-ttu-id="de8cd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="de8cd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de8cd-108">*ловбитс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de8cd-108">*lowbits* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de8cd-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="de8cd-109">Type: **uint**</span></span>

<span data-ttu-id="de8cd-110">Младший 32-разрядный шаблон входного значения.</span><span class="sxs-lookup"><span data-stu-id="de8cd-110">The low 32-bit pattern of the input value.</span></span>

</dd> <dt>

<span data-ttu-id="de8cd-111">*хигхбитс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de8cd-111">*highbits* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de8cd-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="de8cd-112">Type: **uint**</span></span>

<span data-ttu-id="de8cd-113">Старший 32-разрядный шаблон входного значения.</span><span class="sxs-lookup"><span data-stu-id="de8cd-113">The high 32-bit pattern of the input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de8cd-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de8cd-114">Return value</span></span>

<span data-ttu-id="de8cd-115">Тип: **Double**</span><span class="sxs-lookup"><span data-stu-id="de8cd-115">Type: **double**</span></span>

<span data-ttu-id="de8cd-116">Входные данные (2 32-разрядные значения) повторно приведены в виде Double.</span><span class="sxs-lookup"><span data-stu-id="de8cd-116">The input (two 32-bit values) recast as a double.</span></span>

## <a name="remarks"></a><span data-ttu-id="de8cd-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="de8cd-117">Remarks</span></span>

<span data-ttu-id="de8cd-118">Также доступна следующая перегруженная версия:</span><span class="sxs-lookup"><span data-stu-id="de8cd-118">The following overloaded version is also available:</span></span>

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

<span data-ttu-id="de8cd-119">Если входное значение является 2 32-разрядным компонентом, то возвращаемый тип будет содержать один Double.</span><span class="sxs-lookup"><span data-stu-id="de8cd-119">If the input value is two 32-bit components, the return type will contain one double.</span></span> <span data-ttu-id="de8cd-120">Если входное значение является 4 32-разрядным компонентом, возвращаемый тип будет содержать два значения типа Double.</span><span class="sxs-lookup"><span data-stu-id="de8cd-120">If the input value is four 32-bit components, the return type will contain two doubles.</span></span> <span data-ttu-id="de8cd-121">Если входное значение является 64-битным типом, то возвращаемое значение будет иметь то же количество компонентов, что и входное значение.</span><span class="sxs-lookup"><span data-stu-id="de8cd-121">If the input value is a 64-bit type, the returned value will have the same number of components as the input value.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="de8cd-122">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="de8cd-122">Minimum Shader Model</span></span>

<span data-ttu-id="de8cd-123">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="de8cd-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="de8cd-124">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="de8cd-124">Shader Model</span></span>                                                                | <span data-ttu-id="de8cd-125">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="de8cd-125">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="de8cd-126">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="de8cd-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="de8cd-127">да</span><span class="sxs-lookup"><span data-stu-id="de8cd-127">yes</span></span>       |



 

<span data-ttu-id="de8cd-128">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="de8cd-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="de8cd-129">Вершина</span><span class="sxs-lookup"><span data-stu-id="de8cd-129">Vertex</span></span> | <span data-ttu-id="de8cd-130">Поверхности</span><span class="sxs-lookup"><span data-stu-id="de8cd-130">Hull</span></span> | <span data-ttu-id="de8cd-131">Домен</span><span class="sxs-lookup"><span data-stu-id="de8cd-131">Domain</span></span> | <span data-ttu-id="de8cd-132">Геометрия</span><span class="sxs-lookup"><span data-stu-id="de8cd-132">Geometry</span></span> | <span data-ttu-id="de8cd-133">Пиксель</span><span class="sxs-lookup"><span data-stu-id="de8cd-133">Pixel</span></span> | <span data-ttu-id="de8cd-134">Вычисления</span><span class="sxs-lookup"><span data-stu-id="de8cd-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="de8cd-135">x</span><span class="sxs-lookup"><span data-stu-id="de8cd-135">x</span></span>      | <span data-ttu-id="de8cd-136">x</span><span class="sxs-lookup"><span data-stu-id="de8cd-136">x</span></span>    | <span data-ttu-id="de8cd-137">x</span><span class="sxs-lookup"><span data-stu-id="de8cd-137">x</span></span>      | <span data-ttu-id="de8cd-138">x</span><span class="sxs-lookup"><span data-stu-id="de8cd-138">x</span></span>        | <span data-ttu-id="de8cd-139">x</span><span class="sxs-lookup"><span data-stu-id="de8cd-139">x</span></span>     | <span data-ttu-id="de8cd-140">x</span><span class="sxs-lookup"><span data-stu-id="de8cd-140">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="de8cd-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de8cd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de8cd-142">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="de8cd-142">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="de8cd-143">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="de8cd-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




