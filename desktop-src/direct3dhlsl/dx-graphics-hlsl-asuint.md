---
title: асуинт
description: Интерпретирует битовый шаблон x как целое число без знака.
ms.assetid: 8401001d-f9ee-43da-9756-f311e9f2bb20
keywords:
- асуинт HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a2d351eb36c6910790e2dceb94e3a97951ad850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984060"
---
# <a name="asuint"></a><span data-ttu-id="cbb73-104">асуинт</span><span class="sxs-lookup"><span data-stu-id="cbb73-104">asuint</span></span>

<span data-ttu-id="cbb73-105">Интерпретирует битовый шаблон *x* как целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="cbb73-105">Interprets the bit pattern of *x* as an unsigned integer.</span></span>



| <span data-ttu-id="cbb73-106">RET асуинт (*x*)</span><span class="sxs-lookup"><span data-stu-id="cbb73-106">ret asuint(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="cbb73-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbb73-107">Parameters</span></span>



| <span data-ttu-id="cbb73-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="cbb73-108">Item</span></span>                                                   | <span data-ttu-id="cbb73-109">Описание</span><span class="sxs-lookup"><span data-stu-id="cbb73-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="cbb73-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="cbb73-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="cbb73-111">\[во \] входном значении.</span><span class="sxs-lookup"><span data-stu-id="cbb73-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="cbb73-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbb73-112">Return Value</span></span>

<span data-ttu-id="cbb73-113">Входное значение интерпретируется как целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="cbb73-113">The input interpreted as an unsigned integer.</span></span>

## <a name="type-description"></a><span data-ttu-id="cbb73-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="cbb73-114">Type Description</span></span>



| <span data-ttu-id="cbb73-115">Имя</span><span class="sxs-lookup"><span data-stu-id="cbb73-115">Name</span></span>  | [<span data-ttu-id="cbb73-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="cbb73-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="cbb73-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="cbb73-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="cbb73-118">Размер</span><span class="sxs-lookup"><span data-stu-id="cbb73-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="cbb73-119">*x*</span><span class="sxs-lookup"><span data-stu-id="cbb73-119">*x*</span></span>   | <span data-ttu-id="cbb73-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="cbb73-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="cbb73-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="cbb73-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="cbb73-122">any</span><span class="sxs-lookup"><span data-stu-id="cbb73-122">any</span></span>                            |
| <span data-ttu-id="cbb73-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="cbb73-123">*ret*</span></span> | <span data-ttu-id="cbb73-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="cbb73-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="cbb73-125">**uint**</span><span class="sxs-lookup"><span data-stu-id="cbb73-125">**uint**</span></span>](/windows/desktop/WinProg/windows-data-types)                                         | <span data-ttu-id="cbb73-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="cbb73-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cbb73-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="cbb73-127">Minimum Shader Model</span></span>

<span data-ttu-id="cbb73-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="cbb73-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cbb73-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="cbb73-129">Shader Model</span></span>                                                        | <span data-ttu-id="cbb73-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="cbb73-130">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="cbb73-131">[Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров</span><span class="sxs-lookup"><span data-stu-id="cbb73-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="cbb73-132">да</span><span class="sxs-lookup"><span data-stu-id="cbb73-132">yes</span></span>       |
| [<span data-ttu-id="cbb73-133">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cbb73-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="cbb73-134">Нет</span><span class="sxs-lookup"><span data-stu-id="cbb73-134">no</span></span>        |
| [<span data-ttu-id="cbb73-135">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cbb73-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="cbb73-136">Нет</span><span class="sxs-lookup"><span data-stu-id="cbb73-136">no</span></span>        |
| [<span data-ttu-id="cbb73-137">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cbb73-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="cbb73-138">Нет</span><span class="sxs-lookup"><span data-stu-id="cbb73-138">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="cbb73-139">См. также</span><span class="sxs-lookup"><span data-stu-id="cbb73-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbb73-140">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="cbb73-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

