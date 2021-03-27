---
title: length
description: Возвращает длину указанного вектора с плавающей точкой.
ms.assetid: eb06c87c-d536-448e-becb-762783cc2a77
keywords:
- Длина HLSL
topic_type:
- apiref
api_name:
- length
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a7a93b0a7d225a25273a2ab4f8bf1d24656b6ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792042"
---
# <a name="length"></a><span data-ttu-id="17525-104">length</span><span class="sxs-lookup"><span data-stu-id="17525-104">length</span></span>

<span data-ttu-id="17525-105">Возвращает длину указанного вектора с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="17525-105">Returns the length of the specified floating-point vector.</span></span>



| <span data-ttu-id="17525-106">Длина *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="17525-106">*ret* length(*x*)</span></span> |
|-------------------|



 

## <a name="parameters"></a><span data-ttu-id="17525-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="17525-107">Parameters</span></span>



| <span data-ttu-id="17525-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="17525-108">Item</span></span>                                                   | <span data-ttu-id="17525-109">Описание</span><span class="sxs-lookup"><span data-stu-id="17525-109">Description</span></span>                                     |
|--------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="17525-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="17525-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="17525-111">Указанный вектор с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="17525-111">The specified floating-point vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="17525-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17525-112">Return Value</span></span>

<span data-ttu-id="17525-113">Скалярная точка с плавающей запятой, представляющая длину параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="17525-113">A floating-point scalar that represents the length of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="17525-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="17525-114">Type Description</span></span>



| <span data-ttu-id="17525-115">Имя</span><span class="sxs-lookup"><span data-stu-id="17525-115">Name</span></span>  | [<span data-ttu-id="17525-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="17525-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="17525-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="17525-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="17525-118">Размер</span><span class="sxs-lookup"><span data-stu-id="17525-118">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="17525-119">*x*</span><span class="sxs-lookup"><span data-stu-id="17525-119">*x*</span></span>   | [<span data-ttu-id="17525-120">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="17525-120">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="17525-121">**float**</span><span class="sxs-lookup"><span data-stu-id="17525-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="17525-122">any</span><span class="sxs-lookup"><span data-stu-id="17525-122">any</span></span>  |
| <span data-ttu-id="17525-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="17525-123">*ret*</span></span> | [<span data-ttu-id="17525-124">**скаляр**</span><span class="sxs-lookup"><span data-stu-id="17525-124">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="17525-125">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="17525-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="17525-126">1</span><span class="sxs-lookup"><span data-stu-id="17525-126">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="17525-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="17525-127">Minimum Shader Model</span></span>

<span data-ttu-id="17525-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="17525-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="17525-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="17525-129">Shader Model</span></span>                                                                       | <span data-ttu-id="17525-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="17525-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="17525-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="17525-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="17525-132">да</span><span class="sxs-lookup"><span data-stu-id="17525-132">yes</span></span>                 |
| [<span data-ttu-id="17525-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17525-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="17525-134">Да ( \_ только VS 1 1 \_ )</span><span class="sxs-lookup"><span data-stu-id="17525-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="17525-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17525-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17525-136">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="17525-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

