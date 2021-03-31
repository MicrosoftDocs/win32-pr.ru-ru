---
title: насыщенность (ссылка HLSL)
description: Отменяет заданное значение в диапазоне от 0 до 1.
ms.assetid: efe4dedd-732a-4643-8a57-61814434f6ff
keywords:
- насыщенность HLSL
topic_type:
- apiref
api_name:
- saturate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 609443bdc1d0cff6a4c81c8eb26d86a30ea1e721
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337545"
---
# <a name="saturate-hlsl-reference"></a><span data-ttu-id="ce0d6-104">насыщенность (ссылка HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce0d6-104">saturate (HLSL reference)</span></span>

<span data-ttu-id="ce0d6-105">Отменяет заданное значение в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="ce0d6-105">Clamps the specified value within the range of 0 to 1.</span></span>



| <span data-ttu-id="ce0d6-106">*RET* -насыщенность (*x*)</span><span class="sxs-lookup"><span data-stu-id="ce0d6-106">*ret* saturate(*x*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="ce0d6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce0d6-107">Parameters</span></span>



| <span data-ttu-id="ce0d6-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="ce0d6-108">Item</span></span>                                                   | <span data-ttu-id="ce0d6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ce0d6-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="ce0d6-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="ce0d6-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ce0d6-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="ce0d6-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ce0d6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce0d6-112">Return Value</span></span>

<span data-ttu-id="ce0d6-113">Параметр *x* , который был в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="ce0d6-113">The *x* parameter, clamped within the range of 0 to 1.</span></span>

## <a name="type-description"></a><span data-ttu-id="ce0d6-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="ce0d6-114">Type Description</span></span>



| <span data-ttu-id="ce0d6-115">Имя</span><span class="sxs-lookup"><span data-stu-id="ce0d6-115">Name</span></span>  | [<span data-ttu-id="ce0d6-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="ce0d6-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ce0d6-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="ce0d6-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ce0d6-118">Размер</span><span class="sxs-lookup"><span data-stu-id="ce0d6-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ce0d6-119">*x*</span><span class="sxs-lookup"><span data-stu-id="ce0d6-119">*x*</span></span>   | <span data-ttu-id="ce0d6-120">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="ce0d6-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="ce0d6-121">**float**</span><span class="sxs-lookup"><span data-stu-id="ce0d6-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ce0d6-122">any</span><span class="sxs-lookup"><span data-stu-id="ce0d6-122">any</span></span>                            |
| <span data-ttu-id="ce0d6-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="ce0d6-123">*ret*</span></span> | <span data-ttu-id="ce0d6-124">то же, что входные данные *x*</span><span class="sxs-lookup"><span data-stu-id="ce0d6-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="ce0d6-125">**float**</span><span class="sxs-lookup"><span data-stu-id="ce0d6-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ce0d6-126">те же измерения, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="ce0d6-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ce0d6-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ce0d6-127">Minimum Shader Model</span></span>

<span data-ttu-id="ce0d6-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ce0d6-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ce0d6-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ce0d6-129">Shader Model</span></span>                                                                       | <span data-ttu-id="ce0d6-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ce0d6-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ce0d6-131">[Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) и более высокие модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="ce0d6-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="ce0d6-132">да</span><span class="sxs-lookup"><span data-stu-id="ce0d6-132">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ce0d6-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce0d6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce0d6-134">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ce0d6-134">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

