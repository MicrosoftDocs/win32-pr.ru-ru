---
title: D3DCOLORtoUBYTE4
description: Преобразует вектор 4D с плавающей запятой, заданный D3DCOLOR, в UBYTE4.
ms.assetid: 20a7be00-1e36-41c3-bc98-933b3faa8f35
keywords:
- D3DCOLORtoUBYTE4 HLSL
topic_type:
- apiref
api_name:
- D3DCOLORtoUBYTE4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c60f0934d6700ec7fbd9e6d9e6443cb6409ab15f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533458"
---
# <a name="d3dcolortoubyte4"></a><span data-ttu-id="65d0a-104">D3DCOLORtoUBYTE4</span><span class="sxs-lookup"><span data-stu-id="65d0a-104">D3DCOLORtoUBYTE4</span></span>

<span data-ttu-id="65d0a-105">Преобразует вектор 4D с плавающей запятой, заданный D3DCOLOR, в UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="65d0a-105">Converts a floating-point, 4D vector set by a D3DCOLOR to a UBYTE4.</span></span>



| <span data-ttu-id="65d0a-106">*RET* D3DCOLORtoUBYTE4 (*x*)</span><span class="sxs-lookup"><span data-stu-id="65d0a-106">*ret* D3DCOLORtoUBYTE4(*x*)</span></span> |
|-----------------------------|



 

<span data-ttu-id="65d0a-107">Эта функция свиззлес и масштабирует компоненты параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="65d0a-107">This function swizzles and scales components of the *x* parameter.</span></span> <span data-ttu-id="65d0a-108">Используйте эту функцию, чтобы компенсировать отсутствие поддержки UBYTE4 в определенном оборудовании.</span><span class="sxs-lookup"><span data-stu-id="65d0a-108">Use this function to compensate for the lack of UBYTE4 support in some hardware.</span></span>

## <a name="parameters"></a><span data-ttu-id="65d0a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="65d0a-109">Parameters</span></span>



| <span data-ttu-id="65d0a-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="65d0a-110">Item</span></span>                                                   | <span data-ttu-id="65d0a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="65d0a-111">Description</span></span>                                              |
|--------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="65d0a-112"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="65d0a-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="65d0a-113">\[в \] Vector4 с плавающей запятой для преобразования.</span><span class="sxs-lookup"><span data-stu-id="65d0a-113">\[in\] The floating-point vector4 to convert.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="65d0a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65d0a-114">Return Value</span></span>

<span data-ttu-id="65d0a-115">UBYTE4 представление параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="65d0a-115">The UBYTE4 representation of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="65d0a-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="65d0a-116">Type Description</span></span>



| <span data-ttu-id="65d0a-117">Имя</span><span class="sxs-lookup"><span data-stu-id="65d0a-117">Name</span></span>  | [<span data-ttu-id="65d0a-118">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="65d0a-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="65d0a-119">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="65d0a-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="65d0a-120">Размер</span><span class="sxs-lookup"><span data-stu-id="65d0a-120">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="65d0a-121">*x*</span><span class="sxs-lookup"><span data-stu-id="65d0a-121">*x*</span></span>   | [<span data-ttu-id="65d0a-122">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="65d0a-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="65d0a-123">**float**</span><span class="sxs-lookup"><span data-stu-id="65d0a-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="65d0a-124">4</span><span class="sxs-lookup"><span data-stu-id="65d0a-124">4</span></span>    |
| <span data-ttu-id="65d0a-125">*обратно*</span><span class="sxs-lookup"><span data-stu-id="65d0a-125">*ret*</span></span> | [<span data-ttu-id="65d0a-126">**уязвимо**</span><span class="sxs-lookup"><span data-stu-id="65d0a-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="65d0a-127">**цело**</span><span class="sxs-lookup"><span data-stu-id="65d0a-127">**integer**</span></span>](/windows/desktop/WinProg/windows-data-types)                      | <span data-ttu-id="65d0a-128">4</span><span class="sxs-lookup"><span data-stu-id="65d0a-128">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="65d0a-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="65d0a-129">Minimum Shader Model</span></span>

<span data-ttu-id="65d0a-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="65d0a-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="65d0a-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="65d0a-131">Shader Model</span></span>                                                                       | <span data-ttu-id="65d0a-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="65d0a-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="65d0a-133">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="65d0a-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="65d0a-134">да</span><span class="sxs-lookup"><span data-stu-id="65d0a-134">yes</span></span>       |
| [<span data-ttu-id="65d0a-135">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65d0a-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="65d0a-136">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="65d0a-136">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="65d0a-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65d0a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d0a-138">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="65d0a-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

