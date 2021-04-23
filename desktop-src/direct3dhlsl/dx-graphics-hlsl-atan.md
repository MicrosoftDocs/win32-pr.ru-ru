---
title: atan
description: Возвращает арктангенс указанного значения.
ms.assetid: e3ce3ac3-1012-414f-a193-102208083e39
keywords:
- Atan HLSL
topic_type:
- apiref
api_name:
- atan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 290ced1e5100e3bbc780fab6ab984deaca38528f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792049"
---
# <a name="atan"></a><span data-ttu-id="9ea1a-104">atan</span><span class="sxs-lookup"><span data-stu-id="9ea1a-104">atan</span></span>

<span data-ttu-id="9ea1a-105">Возвращает арктангенс указанного значения.</span><span class="sxs-lookup"><span data-stu-id="9ea1a-105">Returns the arctangent of the specified value.</span></span>



| <span data-ttu-id="9ea1a-106">*RET* ATAN (*x*)</span><span class="sxs-lookup"><span data-stu-id="9ea1a-106">*ret* atan(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="9ea1a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ea1a-107">Parameters</span></span>



| <span data-ttu-id="9ea1a-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="9ea1a-108">Item</span></span>                                                   | <span data-ttu-id="9ea1a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9ea1a-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="9ea1a-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="9ea1a-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="9ea1a-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="9ea1a-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="9ea1a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ea1a-112">Return Value</span></span>

<span data-ttu-id="9ea1a-113">Арктангенс параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="9ea1a-113">The arctangent of the *x* parameter.</span></span> <span data-ttu-id="9ea1a-114">Это значение находится в диапазоне от-π/2 до π/2.</span><span class="sxs-lookup"><span data-stu-id="9ea1a-114">This value is within the range of -π/2 to π/2.</span></span>

## <a name="type-description"></a><span data-ttu-id="9ea1a-115">Описание типа</span><span class="sxs-lookup"><span data-stu-id="9ea1a-115">Type Description</span></span>



| <span data-ttu-id="9ea1a-116">Имя</span><span class="sxs-lookup"><span data-stu-id="9ea1a-116">Name</span></span>  | [<span data-ttu-id="9ea1a-117">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="9ea1a-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="9ea1a-118">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="9ea1a-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="9ea1a-119">Размер</span><span class="sxs-lookup"><span data-stu-id="9ea1a-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="9ea1a-120">*x*</span><span class="sxs-lookup"><span data-stu-id="9ea1a-120">*x*</span></span>   | <span data-ttu-id="9ea1a-121">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="9ea1a-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="9ea1a-122">**float**</span><span class="sxs-lookup"><span data-stu-id="9ea1a-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9ea1a-123">any</span><span class="sxs-lookup"><span data-stu-id="9ea1a-123">any</span></span>                            |
| <span data-ttu-id="9ea1a-124">*обратно*</span><span class="sxs-lookup"><span data-stu-id="9ea1a-124">*ret*</span></span> | <span data-ttu-id="9ea1a-125">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="9ea1a-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="9ea1a-126">**float**</span><span class="sxs-lookup"><span data-stu-id="9ea1a-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9ea1a-127">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="9ea1a-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9ea1a-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9ea1a-128">Minimum Shader Model</span></span>

<span data-ttu-id="9ea1a-129">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="9ea1a-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9ea1a-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9ea1a-130">Shader Model</span></span>                                                                       | <span data-ttu-id="9ea1a-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="9ea1a-131">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9ea1a-132">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="9ea1a-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="9ea1a-133">да</span><span class="sxs-lookup"><span data-stu-id="9ea1a-133">yes</span></span>       |
| [<span data-ttu-id="9ea1a-134">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9ea1a-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="9ea1a-135">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9ea1a-135">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="9ea1a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ea1a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ea1a-137">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="9ea1a-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

