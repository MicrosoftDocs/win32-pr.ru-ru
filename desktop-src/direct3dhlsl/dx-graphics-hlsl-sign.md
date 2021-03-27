---
title: sign
description: Возвращает знак x.
ms.assetid: 3e2e04e8-0ffc-4721-a5d8-1ccfa6ca2a1a
keywords:
- подписать HLSL
topic_type:
- apiref
api_name:
- sign
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc177e72e116394ffd6241e0616b84c9066a68a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997150"
---
# <a name="sign"></a><span data-ttu-id="bb72d-104">sign</span><span class="sxs-lookup"><span data-stu-id="bb72d-104">sign</span></span>

<span data-ttu-id="bb72d-105">Возвращает знак *x*.</span><span class="sxs-lookup"><span data-stu-id="bb72d-105">Returns the sign of *x*.</span></span>



| <span data-ttu-id="bb72d-106">знак *возврата* (*x*)</span><span class="sxs-lookup"><span data-stu-id="bb72d-106">*ret* sign(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="bb72d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb72d-107">Parameters</span></span>



| <span data-ttu-id="bb72d-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="bb72d-108">Item</span></span>                                                   | <span data-ttu-id="bb72d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="bb72d-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="bb72d-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="bb72d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="bb72d-111">\[во \] входном значении.</span><span class="sxs-lookup"><span data-stu-id="bb72d-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="bb72d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb72d-112">Return Value</span></span>

<span data-ttu-id="bb72d-113">Возвращает значение-1, если *x* меньше нуля; 0, если *x* равен нулю; и 1, если *x* больше нуля.</span><span class="sxs-lookup"><span data-stu-id="bb72d-113">Returns -1 if *x* is less than zero; 0 if *x* equals zero; and 1 if *x* is greater than zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="bb72d-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="bb72d-114">Type Description</span></span>



| <span data-ttu-id="bb72d-115">Имя</span><span class="sxs-lookup"><span data-stu-id="bb72d-115">Name</span></span>  | [<span data-ttu-id="bb72d-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="bb72d-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="bb72d-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="bb72d-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="bb72d-118">Размер</span><span class="sxs-lookup"><span data-stu-id="bb72d-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="bb72d-119">*x*</span><span class="sxs-lookup"><span data-stu-id="bb72d-119">*x*</span></span>   | <span data-ttu-id="bb72d-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="bb72d-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="bb72d-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="bb72d-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="bb72d-122">any</span><span class="sxs-lookup"><span data-stu-id="bb72d-122">any</span></span>                            |
| <span data-ttu-id="bb72d-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="bb72d-123">*ret*</span></span> | <span data-ttu-id="bb72d-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="bb72d-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="bb72d-125">**int**</span><span class="sxs-lookup"><span data-stu-id="bb72d-125">**int**</span></span>](/windows/desktop/WinProg/windows-data-types)                                          | <span data-ttu-id="bb72d-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="bb72d-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bb72d-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="bb72d-127">Minimum Shader Model</span></span>

<span data-ttu-id="bb72d-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="bb72d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bb72d-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="bb72d-129">Shader Model</span></span>                                                                       | <span data-ttu-id="bb72d-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="bb72d-130">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="bb72d-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="bb72d-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="bb72d-132">да</span><span class="sxs-lookup"><span data-stu-id="bb72d-132">yes</span></span>                         |
| [<span data-ttu-id="bb72d-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bb72d-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="bb72d-134">Да (VS \_ 1 \_ 1 и PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="bb72d-134">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="bb72d-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb72d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb72d-136">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="bb72d-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

