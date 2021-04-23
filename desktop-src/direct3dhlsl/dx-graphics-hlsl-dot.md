---
title: DOT
description: Возвращает скалярное произведение двух векторов.
ms.assetid: ad24c06c-0b40-4dc5-a2b9-1d5438635ed8
keywords:
- точка HLSL
topic_type:
- apiref
api_name:
- dot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6d05abf0d67628d1d77b362b028107e07b83457
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987766"
---
# <a name="dot"></a><span data-ttu-id="536a9-104">DOT</span><span class="sxs-lookup"><span data-stu-id="536a9-104">dot</span></span>

<span data-ttu-id="536a9-105">Возвращает скалярное произведение двух векторов.</span><span class="sxs-lookup"><span data-stu-id="536a9-105">Returns the dot product of two vectors.</span></span>



| <span data-ttu-id="536a9-106">*RET* -точка (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="536a9-106">*ret* dot(*x*, *y*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="536a9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="536a9-107">Parameters</span></span>



| <span data-ttu-id="536a9-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="536a9-108">Item</span></span>                                                   | <span data-ttu-id="536a9-109">Описание</span><span class="sxs-lookup"><span data-stu-id="536a9-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="536a9-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="536a9-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="536a9-111">\[в \] первом векторе.</span><span class="sxs-lookup"><span data-stu-id="536a9-111">\[in\] The first vector.</span></span><br/>  |
| <span data-ttu-id="536a9-112"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="536a9-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="536a9-113">\[во \] втором векторе.</span><span class="sxs-lookup"><span data-stu-id="536a9-113">\[in\] The second vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="536a9-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="536a9-114">Return Value</span></span>

<span data-ttu-id="536a9-115">Скалярное произведение параметра *x* и параметра *y* .</span><span class="sxs-lookup"><span data-stu-id="536a9-115">The dot product of the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="536a9-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="536a9-116">Type Description</span></span>



| <span data-ttu-id="536a9-117">Имя</span><span class="sxs-lookup"><span data-stu-id="536a9-117">Name</span></span>  | [<span data-ttu-id="536a9-118">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="536a9-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="536a9-119">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="536a9-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="536a9-120">Размер</span><span class="sxs-lookup"><span data-stu-id="536a9-120">Size</span></span>                            |
|-------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="536a9-121">*x*</span><span class="sxs-lookup"><span data-stu-id="536a9-121">*x*</span></span>   | [<span data-ttu-id="536a9-122">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="536a9-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="536a9-123">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="536a9-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="536a9-124">any</span><span class="sxs-lookup"><span data-stu-id="536a9-124">any</span></span>                             |
| <span data-ttu-id="536a9-125">*y*</span><span class="sxs-lookup"><span data-stu-id="536a9-125">*y*</span></span>   | [<span data-ttu-id="536a9-126">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="536a9-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="536a9-127">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="536a9-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="536a9-128">те же размеры, что и входные *x*</span><span class="sxs-lookup"><span data-stu-id="536a9-128">same dimensions(s) as input *x*</span></span> |
| <span data-ttu-id="536a9-129">*обратно*</span><span class="sxs-lookup"><span data-stu-id="536a9-129">*ret*</span></span> | [<span data-ttu-id="536a9-130">**скаляр**</span><span class="sxs-lookup"><span data-stu-id="536a9-130">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="536a9-131">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="536a9-131">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="536a9-132">1</span><span class="sxs-lookup"><span data-stu-id="536a9-132">1</span></span>                               |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="536a9-133">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="536a9-133">Minimum Shader Model</span></span>

<span data-ttu-id="536a9-134">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="536a9-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="536a9-135">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="536a9-135">Shader Model</span></span>                                                                       | <span data-ttu-id="536a9-136">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="536a9-136">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="536a9-137">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="536a9-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="536a9-138">да</span><span class="sxs-lookup"><span data-stu-id="536a9-138">yes</span></span>       |
| [<span data-ttu-id="536a9-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="536a9-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="536a9-140">да</span><span class="sxs-lookup"><span data-stu-id="536a9-140">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="536a9-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="536a9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="536a9-142">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="536a9-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

