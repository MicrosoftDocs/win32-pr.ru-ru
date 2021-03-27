---
title: нормализовать
description: Нормализует заданный вектор с плавающей запятой в соответствии с x/Length (x).
ms.assetid: 7fd6f8ff-f3ff-4d14-b3fc-b44fdddf6c75
keywords:
- нормализация HLSL
topic_type:
- apiref
api_name:
- normalize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f48c78f80f5f92f950795018f05a46c7883d9736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987852"
---
# <a name="normalize"></a><span data-ttu-id="53264-104">нормализовать</span><span class="sxs-lookup"><span data-stu-id="53264-104">normalize</span></span>

<span data-ttu-id="53264-105">Нормализует заданный вектор с плавающей запятой в соответствии с x/Length (x).</span><span class="sxs-lookup"><span data-stu-id="53264-105">Normalizes the specified floating-point vector according to x / length(x).</span></span>



| <span data-ttu-id="53264-106">*RET* -нормализовать (*x*)</span><span class="sxs-lookup"><span data-stu-id="53264-106">*ret* normalize(*x*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="53264-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="53264-107">Parameters</span></span>



| <span data-ttu-id="53264-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="53264-108">Item</span></span>                                                   | <span data-ttu-id="53264-109">Описание</span><span class="sxs-lookup"><span data-stu-id="53264-109">Description</span></span>                                            |
|--------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="53264-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="53264-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="53264-111">\[в \] указанном векторе с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="53264-111">\[in\] The specified floating-point vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="53264-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53264-112">Return Value</span></span>

<span data-ttu-id="53264-113">Нормализованный параметр *x* .</span><span class="sxs-lookup"><span data-stu-id="53264-113">The normalized *x* parameter.</span></span> <span data-ttu-id="53264-114">Если длина параметра *x* равна 0, результат имеет неопределенное значение.</span><span class="sxs-lookup"><span data-stu-id="53264-114">If the length of the *x* parameter is 0, the result is indefinite.</span></span>

## <a name="remarks"></a><span data-ttu-id="53264-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="53264-115">Remarks</span></span>

<span data-ttu-id="53264-116">Встроенная функция **нормализации** HLSL использует следующую формулу: *x*  /  [**length**](dx-graphics-hlsl-length.md)(*x*).</span><span class="sxs-lookup"><span data-stu-id="53264-116">The **normalize** HLSL intrinsic function uses the following formula: *x* / [**length**](dx-graphics-hlsl-length.md)(*x*).</span></span>

## <a name="type-description"></a><span data-ttu-id="53264-117">Описание типа</span><span class="sxs-lookup"><span data-stu-id="53264-117">Type Description</span></span>



| <span data-ttu-id="53264-118">Имя</span><span class="sxs-lookup"><span data-stu-id="53264-118">Name</span></span>  | [<span data-ttu-id="53264-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="53264-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="53264-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="53264-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="53264-121">Размер</span><span class="sxs-lookup"><span data-stu-id="53264-121">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="53264-122">*x*</span><span class="sxs-lookup"><span data-stu-id="53264-122">*x*</span></span>   | [<span data-ttu-id="53264-123">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="53264-123">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="53264-124">**float**</span><span class="sxs-lookup"><span data-stu-id="53264-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="53264-125">any</span><span class="sxs-lookup"><span data-stu-id="53264-125">any</span></span>                            |
| <span data-ttu-id="53264-126">*обратно*</span><span class="sxs-lookup"><span data-stu-id="53264-126">*ret*</span></span> | <span data-ttu-id="53264-127">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="53264-127">same as input *x*</span></span>                                                                   | [<span data-ttu-id="53264-128">**float**</span><span class="sxs-lookup"><span data-stu-id="53264-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="53264-129">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="53264-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="53264-130">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="53264-130">Minimum Shader Model</span></span>

<span data-ttu-id="53264-131">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="53264-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="53264-132">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="53264-132">Shader Model</span></span>                                                                       | <span data-ttu-id="53264-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="53264-133">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="53264-134">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="53264-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="53264-135">да</span><span class="sxs-lookup"><span data-stu-id="53264-135">yes</span></span>                 |
| [<span data-ttu-id="53264-136">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53264-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="53264-137">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="53264-137">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="53264-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53264-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53264-139">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="53264-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

