---
title: асфлоат
description: Интерпретирует битовый шаблон x в качестве числа с плавающей запятой.
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- асфлоат HLSL
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a5701d959fb59519318dd7f2e91b6790f4c0b6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997134"
---
# <a name="asfloat"></a><span data-ttu-id="b812e-104">асфлоат</span><span class="sxs-lookup"><span data-stu-id="b812e-104">asfloat</span></span>

<span data-ttu-id="b812e-105">Интерпретирует битовый шаблон *x* в качестве числа с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="b812e-105">Interprets the bit pattern of *x* as a floating-point number.</span></span>



| <span data-ttu-id="b812e-106">RET асфлоат (*x*)</span><span class="sxs-lookup"><span data-stu-id="b812e-106">ret asfloat(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="b812e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b812e-107">Parameters</span></span>



| <span data-ttu-id="b812e-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="b812e-108">Item</span></span>                                                   | <span data-ttu-id="b812e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b812e-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="b812e-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="b812e-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b812e-111">\[во \] входном значении.</span><span class="sxs-lookup"><span data-stu-id="b812e-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b812e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b812e-112">Return Value</span></span>

<span data-ttu-id="b812e-113">Входное значение интерпретируется как число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="b812e-113">The input interpreted as a floating-point number.</span></span>

## <a name="type-description"></a><span data-ttu-id="b812e-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="b812e-114">Type Description</span></span>



| <span data-ttu-id="b812e-115">Имя</span><span class="sxs-lookup"><span data-stu-id="b812e-115">Name</span></span>  | [<span data-ttu-id="b812e-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="b812e-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b812e-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="b812e-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="b812e-118">Размер</span><span class="sxs-lookup"><span data-stu-id="b812e-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b812e-119">*x*</span><span class="sxs-lookup"><span data-stu-id="b812e-119">*x*</span></span>   | <span data-ttu-id="b812e-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="b812e-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="b812e-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b812e-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="b812e-122">any</span><span class="sxs-lookup"><span data-stu-id="b812e-122">any</span></span>                            |
| <span data-ttu-id="b812e-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="b812e-123">*ret*</span></span> | <span data-ttu-id="b812e-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="b812e-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b812e-125">**float**</span><span class="sxs-lookup"><span data-stu-id="b812e-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                | <span data-ttu-id="b812e-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="b812e-126">same dimension(s) as input *x*</span></span> |



 

## <a name="function-overloads"></a><span data-ttu-id="b812e-127">Перегрузки функций</span><span class="sxs-lookup"><span data-stu-id="b812e-127">Function Overloads</span></span>

<dl> <span data-ttu-id="b812e-128">' float <x> асфлоат ( <x> значение float); `  
` float <x> асфлоат ( <x> значение int); `  
` float <x> асфлоат ( <x> значение uint); "</span><span class="sxs-lookup"><span data-stu-id="b812e-128">`float<x> asfloat(float<x> value);`  
`float<x> asfloat(int<x> value);`  
`float<x> asfloat(uint<x> value);`</span></span>
</dl>

## <a name="minimum-shader-model"></a><span data-ttu-id="b812e-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b812e-129">Minimum Shader Model</span></span>

<span data-ttu-id="b812e-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="b812e-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b812e-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b812e-131">Shader Model</span></span>                                                        | <span data-ttu-id="b812e-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="b812e-132">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="b812e-133">[Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров</span><span class="sxs-lookup"><span data-stu-id="b812e-133">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="b812e-134">да</span><span class="sxs-lookup"><span data-stu-id="b812e-134">yes</span></span>       |
| [<span data-ttu-id="b812e-135">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b812e-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="b812e-136">Нет</span><span class="sxs-lookup"><span data-stu-id="b812e-136">no</span></span>        |
| [<span data-ttu-id="b812e-137">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b812e-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="b812e-138">Нет</span><span class="sxs-lookup"><span data-stu-id="b812e-138">no</span></span>        |
| [<span data-ttu-id="b812e-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b812e-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="b812e-140">Нет</span><span class="sxs-lookup"><span data-stu-id="b812e-140">no</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="b812e-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="b812e-141">Remarks</span></span>

<span data-ttu-id="b812e-142">Старые компиляторы неправильно разрешаются `asfloat(bool)` , но обратите внимание, что входные данные типа bool не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b812e-142">Older compilers incorrectly allowed `asfloat(bool)`, but note that bool inputs are not supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="b812e-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b812e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b812e-144">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b812e-144">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

