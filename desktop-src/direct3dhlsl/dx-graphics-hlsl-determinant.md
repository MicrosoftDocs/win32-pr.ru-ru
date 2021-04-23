---
title: определяющих
description: Возвращает определитель заданной квадратной матрицы с плавающей запятой.
ms.assetid: 9062b6f1-8518-4ee4-8d57-5aa9e2176d05
keywords:
- определителная HLSL
topic_type:
- apiref
api_name:
- determinant
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb010a0c0d0868afcb3dff488daf7926ec6c5e03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984017"
---
# <a name="determinant"></a><span data-ttu-id="0000d-104">определяющих</span><span class="sxs-lookup"><span data-stu-id="0000d-104">determinant</span></span>

<span data-ttu-id="0000d-105">Возвращает определитель заданной квадратной матрицы с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0000d-105">Returns the determinant of the specified floating-point, square matrix.</span></span>



| <span data-ttu-id="0000d-106">определитель " *RET* " (*m*)</span><span class="sxs-lookup"><span data-stu-id="0000d-106">*ret* determinant(*m*)</span></span> |
|------------------------|



 

## <a name="parameters"></a><span data-ttu-id="0000d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0000d-107">Parameters</span></span>



| <span data-ttu-id="0000d-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="0000d-108">Item</span></span>                                                   | <span data-ttu-id="0000d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0000d-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="0000d-110"><span id="m"></span><span id="M"></span>*Пн*</span><span class="sxs-lookup"><span data-stu-id="0000d-110"><span id="m"></span><span id="M"></span>*m*</span></span><br/> | <span data-ttu-id="0000d-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="0000d-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0000d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0000d-112">Return Value</span></span>

<span data-ttu-id="0000d-113">Скалярное значение с плавающей запятой, представляющее определитель параметра *m* .</span><span class="sxs-lookup"><span data-stu-id="0000d-113">The floating-point, scalar value that represents the determinant of the *m* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="0000d-114">Описание типа</span><span class="sxs-lookup"><span data-stu-id="0000d-114">Type Description</span></span>



| <span data-ttu-id="0000d-115">Имя</span><span class="sxs-lookup"><span data-stu-id="0000d-115">Name</span></span>  | [<span data-ttu-id="0000d-116">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="0000d-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="0000d-117">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="0000d-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0000d-118">Размер</span><span class="sxs-lookup"><span data-stu-id="0000d-118">Size</span></span>                                     |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="0000d-119">*m*</span><span class="sxs-lookup"><span data-stu-id="0000d-119">*m*</span></span>   | [<span data-ttu-id="0000d-120">**таблицу**</span><span class="sxs-lookup"><span data-stu-id="0000d-120">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0000d-121">**float**</span><span class="sxs-lookup"><span data-stu-id="0000d-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0000d-122">Any (число строк = количество столбцов)</span><span class="sxs-lookup"><span data-stu-id="0000d-122">any (number of rows = number of columns)</span></span> |
| <span data-ttu-id="0000d-123">*обратно*</span><span class="sxs-lookup"><span data-stu-id="0000d-123">*ret*</span></span> | [<span data-ttu-id="0000d-124">**скаляр**</span><span class="sxs-lookup"><span data-stu-id="0000d-124">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0000d-125">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="0000d-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0000d-126">1</span><span class="sxs-lookup"><span data-stu-id="0000d-126">1</span></span>                                        |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0000d-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0000d-127">Minimum Shader Model</span></span>

<span data-ttu-id="0000d-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="0000d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0000d-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0000d-129">Shader Model</span></span>                                                                       | <span data-ttu-id="0000d-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="0000d-130">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="0000d-131">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="0000d-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="0000d-132">да</span><span class="sxs-lookup"><span data-stu-id="0000d-132">yes</span></span>                   |
| [<span data-ttu-id="0000d-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0000d-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="0000d-134">VS \_ 1 \_ 1 и PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="0000d-134">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="0000d-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0000d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0000d-136">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0000d-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

