---
title: acos
description: Возвращает арккосинус указанного значения.
ms.assetid: c9bc33b8-d586-4c64-9453-5ab97396f2cf
keywords:
- ACOS HLSL
topic_type:
- apiref
api_name:
- acos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2cd909c4a4c1300374bba723f1edabb48d51b2e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134483"
---
# <a name="acos"></a><span data-ttu-id="ee628-104">acos</span><span class="sxs-lookup"><span data-stu-id="ee628-104">acos</span></span>

<span data-ttu-id="ee628-105">Возвращает арккосинус указанного значения.</span><span class="sxs-lookup"><span data-stu-id="ee628-105">Returns the arccosine of the specified value.</span></span>



| <span data-ttu-id="ee628-106">*RET* ACOS (*x*)</span><span class="sxs-lookup"><span data-stu-id="ee628-106">*ret* acos(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="ee628-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee628-107">Parameters</span></span>



| <span data-ttu-id="ee628-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="ee628-108">Item</span></span>                                                   | <span data-ttu-id="ee628-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ee628-109">Description</span></span>                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee628-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="ee628-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ee628-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="ee628-111">\[in\] The specified value.</span></span> <span data-ttu-id="ee628-112">Каждый компонент должен быть значением с плавающей запятой в диапазоне от-1 до 1.</span><span class="sxs-lookup"><span data-stu-id="ee628-112">Each component should be a floating-point value within the range of -1 to 1.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ee628-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee628-113">Return Value</span></span>

<span data-ttu-id="ee628-114">Арккосинус параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="ee628-114">The arccosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="ee628-115">Описание типа</span><span class="sxs-lookup"><span data-stu-id="ee628-115">Type Description</span></span>



| <span data-ttu-id="ee628-116">Имя</span><span class="sxs-lookup"><span data-stu-id="ee628-116">Name</span></span>  | [<span data-ttu-id="ee628-117">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="ee628-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ee628-118">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="ee628-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ee628-119">Размер</span><span class="sxs-lookup"><span data-stu-id="ee628-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ee628-120">*x*</span><span class="sxs-lookup"><span data-stu-id="ee628-120">*x*</span></span>   | <span data-ttu-id="ee628-121">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="ee628-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="ee628-122">**float**</span><span class="sxs-lookup"><span data-stu-id="ee628-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ee628-123">any</span><span class="sxs-lookup"><span data-stu-id="ee628-123">any</span></span>                            |
| <span data-ttu-id="ee628-124">*обратно*</span><span class="sxs-lookup"><span data-stu-id="ee628-124">*ret*</span></span> | <span data-ttu-id="ee628-125">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="ee628-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="ee628-126">**float**</span><span class="sxs-lookup"><span data-stu-id="ee628-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ee628-127">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="ee628-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ee628-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ee628-128">Minimum Shader Model</span></span>

<span data-ttu-id="ee628-129">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ee628-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ee628-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ee628-130">Shader Model</span></span>                                                                       | <span data-ttu-id="ee628-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ee628-131">Supported</span></span>     |
|------------------------------------------------------------------------------------|---------------|
| <span data-ttu-id="ee628-132">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="ee628-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="ee628-133">да</span><span class="sxs-lookup"><span data-stu-id="ee628-133">yes</span></span>           |
| [<span data-ttu-id="ee628-134">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ee628-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ee628-135">\_только VS 1 1 \_</span><span class="sxs-lookup"><span data-stu-id="ee628-135">vs\_1\_1 only</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="ee628-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee628-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee628-137">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ee628-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

