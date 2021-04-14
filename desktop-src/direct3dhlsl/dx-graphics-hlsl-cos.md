---
title: cos
description: Возвращает косинус указанного значения.
ms.assetid: 96c15702-98be-45bc-9abc-60ccc3c217b6
keywords:
- COS HLSL
topic_type:
- apiref
api_name:
- cos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f5c0f4f071d47102c673301a397bfe3ecf178e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413625"
---
# <a name="cos"></a><span data-ttu-id="baecc-104">cos</span><span class="sxs-lookup"><span data-stu-id="baecc-104">cos</span></span>

<span data-ttu-id="baecc-105">Возвращает косинус указанного значения.</span><span class="sxs-lookup"><span data-stu-id="baecc-105">Returns the cosine of the specified value.</span></span>



| <span data-ttu-id="baecc-106">*RET* -cos (*x*)</span><span class="sxs-lookup"><span data-stu-id="baecc-106">*ret* cos(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="baecc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="baecc-107">Parameters</span></span>



| <span data-ttu-id="baecc-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="baecc-108">Item</span></span>                                                   | <span data-ttu-id="baecc-109">Описание</span><span class="sxs-lookup"><span data-stu-id="baecc-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="baecc-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="baecc-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="baecc-111">\[в \] заданном значении в радианах.</span><span class="sxs-lookup"><span data-stu-id="baecc-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="baecc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="baecc-112">Return Value</span></span>

<span data-ttu-id="baecc-113">Косинус параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="baecc-113">The cosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="baecc-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="baecc-114">Type Description</span></span>



| <span data-ttu-id="baecc-115">Имя</span><span class="sxs-lookup"><span data-stu-id="baecc-115">Name</span></span>  | [<span data-ttu-id="baecc-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="baecc-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="baecc-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="baecc-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="baecc-118">Размер</span><span class="sxs-lookup"><span data-stu-id="baecc-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="baecc-119">*x*</span><span class="sxs-lookup"><span data-stu-id="baecc-119">*x*</span></span>   | <span data-ttu-id="baecc-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="baecc-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="baecc-121">**float**</span><span class="sxs-lookup"><span data-stu-id="baecc-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="baecc-122">any</span><span class="sxs-lookup"><span data-stu-id="baecc-122">any</span></span>                            |
| <span data-ttu-id="baecc-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="baecc-123">*ret*</span></span> | <span data-ttu-id="baecc-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="baecc-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="baecc-125">**float**</span><span class="sxs-lookup"><span data-stu-id="baecc-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="baecc-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="baecc-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="baecc-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="baecc-127">Minimum Shader Model</span></span>

<span data-ttu-id="baecc-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="baecc-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="baecc-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="baecc-129">Shader Model</span></span>                                                                       | <span data-ttu-id="baecc-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="baecc-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="baecc-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="baecc-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="baecc-132">да</span><span class="sxs-lookup"><span data-stu-id="baecc-132">yes</span></span>       |
| [<span data-ttu-id="baecc-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="baecc-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="baecc-134">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="baecc-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="baecc-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="baecc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baecc-136">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="baecc-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

