---
title: asin
description: Возвращает арксинус указанного значения.
ms.assetid: 49559cb2-3305-4c97-8071-1589bcca3a75
keywords:
- ASIN HLSL
topic_type:
- apiref
api_name:
- asin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2f64865cb3172037f6630dc422a69aa4d135b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070560"
---
# <a name="asin"></a><span data-ttu-id="3a00c-104">asin</span><span class="sxs-lookup"><span data-stu-id="3a00c-104">asin</span></span>

<span data-ttu-id="3a00c-105">Возвращает арксинус указанного значения.</span><span class="sxs-lookup"><span data-stu-id="3a00c-105">Returns the arcsine of the specified value.</span></span>



| <span data-ttu-id="3a00c-106">*RET* -ASIN (*x*)</span><span class="sxs-lookup"><span data-stu-id="3a00c-106">*ret* asin(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="3a00c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a00c-107">Parameters</span></span>



| <span data-ttu-id="3a00c-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="3a00c-108">Item</span></span>                                                   | <span data-ttu-id="3a00c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3a00c-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="3a00c-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="3a00c-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="3a00c-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="3a00c-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3a00c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a00c-112">Return Value</span></span>

<span data-ttu-id="3a00c-113">Арксинус параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="3a00c-113">The arcsine of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a00c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3a00c-114">Remarks</span></span>

<span data-ttu-id="3a00c-115">Каждый компонент параметра *x* должен находиться в диапазоне от-π/2 до π/2.</span><span class="sxs-lookup"><span data-stu-id="3a00c-115">Each component of the *x* parameter should be within the range of -π/2 to π/2.</span></span>

## <a name="type-description"></a><span data-ttu-id="3a00c-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="3a00c-116">Type Description</span></span>



| <span data-ttu-id="3a00c-117">Имя</span><span class="sxs-lookup"><span data-stu-id="3a00c-117">Name</span></span>  | [<span data-ttu-id="3a00c-118">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="3a00c-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="3a00c-119">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="3a00c-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="3a00c-120">Размер</span><span class="sxs-lookup"><span data-stu-id="3a00c-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="3a00c-121">*x*</span><span class="sxs-lookup"><span data-stu-id="3a00c-121">*x*</span></span>   | <span data-ttu-id="3a00c-122">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="3a00c-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="3a00c-123">**float**</span><span class="sxs-lookup"><span data-stu-id="3a00c-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3a00c-124">any</span><span class="sxs-lookup"><span data-stu-id="3a00c-124">any</span></span>                            |
| <span data-ttu-id="3a00c-125">*обратно*</span><span class="sxs-lookup"><span data-stu-id="3a00c-125">*ret*</span></span> | <span data-ttu-id="3a00c-126">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="3a00c-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="3a00c-127">**float**</span><span class="sxs-lookup"><span data-stu-id="3a00c-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3a00c-128">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="3a00c-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3a00c-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="3a00c-129">Minimum Shader Model</span></span>

<span data-ttu-id="3a00c-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="3a00c-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3a00c-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="3a00c-131">Shader Model</span></span>                                                                       | <span data-ttu-id="3a00c-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="3a00c-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3a00c-133">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="3a00c-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="3a00c-134">да</span><span class="sxs-lookup"><span data-stu-id="3a00c-134">yes</span></span>       |
| [<span data-ttu-id="3a00c-135">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a00c-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="3a00c-136">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3a00c-136">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="3a00c-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a00c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a00c-138">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="3a00c-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

