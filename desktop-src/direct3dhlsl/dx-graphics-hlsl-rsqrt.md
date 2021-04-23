---
title: рскрт
description: Возвращает обратную величину квадратного корня указанного значения.
ms.assetid: 4e266e41-cde9-4a59-8937-98bfc63f3b5d
keywords:
- рскрт HLSL
topic_type:
- apiref
api_name:
- rsqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56eb5f1cba8510e57a2c4b5622e10dc91666b6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997082"
---
# <a name="rsqrt"></a><span data-ttu-id="da00d-104">рскрт</span><span class="sxs-lookup"><span data-stu-id="da00d-104">rsqrt</span></span>

<span data-ttu-id="da00d-105">Возвращает обратную величину квадратного корня указанного значения.</span><span class="sxs-lookup"><span data-stu-id="da00d-105">Returns the reciprocal of the square root of the specified value.</span></span>



| <span data-ttu-id="da00d-106">*RET* рскрт (*x*)</span><span class="sxs-lookup"><span data-stu-id="da00d-106">*ret* rsqrt(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="da00d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="da00d-107">Parameters</span></span>



| <span data-ttu-id="da00d-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="da00d-108">Item</span></span>                                                   | <span data-ttu-id="da00d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="da00d-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="da00d-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="da00d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="da00d-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="da00d-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="da00d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da00d-112">Return Value</span></span>

<span data-ttu-id="da00d-113">Обратная часть квадратного корня параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="da00d-113">The reciprocal of the square root of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="da00d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="da00d-114">Remarks</span></span>

<span data-ttu-id="da00d-115">Эта функция использует следующую формулу: 1/ **sqrt**(*x*).</span><span class="sxs-lookup"><span data-stu-id="da00d-115">This function uses the following formula: 1 / **sqrt**(*x*).</span></span>

## <a name="type-description"></a><span data-ttu-id="da00d-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="da00d-116">Type Description</span></span>



| <span data-ttu-id="da00d-117">Имя</span><span class="sxs-lookup"><span data-stu-id="da00d-117">Name</span></span>  | [<span data-ttu-id="da00d-118">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="da00d-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="da00d-119">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="da00d-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="da00d-120">Размер</span><span class="sxs-lookup"><span data-stu-id="da00d-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="da00d-121">*x*</span><span class="sxs-lookup"><span data-stu-id="da00d-121">*x*</span></span>   | <span data-ttu-id="da00d-122">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="da00d-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="da00d-123">**float**</span><span class="sxs-lookup"><span data-stu-id="da00d-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="da00d-124">any</span><span class="sxs-lookup"><span data-stu-id="da00d-124">any</span></span>                            |
| <span data-ttu-id="da00d-125">*обратно*</span><span class="sxs-lookup"><span data-stu-id="da00d-125">*ret*</span></span> | <span data-ttu-id="da00d-126">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="da00d-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="da00d-127">**float**</span><span class="sxs-lookup"><span data-stu-id="da00d-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="da00d-128">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="da00d-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="da00d-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="da00d-129">Minimum Shader Model</span></span>

<span data-ttu-id="da00d-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="da00d-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="da00d-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="da00d-131">Shader Model</span></span>                                                                       | <span data-ttu-id="da00d-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="da00d-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="da00d-133">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="da00d-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="da00d-134">да</span><span class="sxs-lookup"><span data-stu-id="da00d-134">yes</span></span>                 |
| [<span data-ttu-id="da00d-135">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="da00d-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="da00d-136">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="da00d-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="da00d-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da00d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da00d-138">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="da00d-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

