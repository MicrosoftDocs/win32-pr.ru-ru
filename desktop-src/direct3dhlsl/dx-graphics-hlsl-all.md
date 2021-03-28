---
title: все
description: Определяет, являются ли все компоненты указанного значения ненулевыми.
ms.assetid: 9ee079ff-cd2c-41f5-98cd-ea1f4215e7d5
keywords:
- все HLSL
topic_type:
- apiref
api_name:
- all
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59d59e18655aab10d13af998f4e2aa94da3fa08b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984085"
---
# <a name="all"></a><span data-ttu-id="d799f-104">все</span><span class="sxs-lookup"><span data-stu-id="d799f-104">all</span></span>

<span data-ttu-id="d799f-105">Определяет, являются ли все компоненты указанного значения ненулевыми.</span><span class="sxs-lookup"><span data-stu-id="d799f-105">Determines if all components of the specified value are non-zero.</span></span>



| <span data-ttu-id="d799f-106">*RET* все (*x*)</span><span class="sxs-lookup"><span data-stu-id="d799f-106">*ret* all(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="d799f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d799f-107">Parameters</span></span>



| <span data-ttu-id="d799f-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="d799f-108">Item</span></span>                                                   | <span data-ttu-id="d799f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d799f-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="d799f-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="d799f-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d799f-111">\[в \] указанном значении.</span><span class="sxs-lookup"><span data-stu-id="d799f-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d799f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d799f-112">Return Value</span></span>

<span data-ttu-id="d799f-113">**Значение true** , если все компоненты параметра *x* не равны нулю; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="d799f-113">**True** if all components of the *x* parameter are non-zero; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d799f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d799f-114">Remarks</span></span>

<span data-ttu-id="d799f-115">Эта функция аналогична [**любой**](dx-graphics-hlsl-any.md) встроенной функции HLSL.</span><span class="sxs-lookup"><span data-stu-id="d799f-115">This function is similar to the [**any**](dx-graphics-hlsl-any.md) HLSL intrinsic function.</span></span> <span data-ttu-id="d799f-116">Функция **ANY** определяет, являются ли какие-либо компоненты указанного значения ненулевыми, тогда как функция **ALL** определяет, являются ли все компоненты указанного значения ненулевыми.</span><span class="sxs-lookup"><span data-stu-id="d799f-116">The **any** function determines if any components of the specified value are non-zero, while the **all** function determines if all components of the specified value are non-zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="d799f-117">Описание типа</span><span class="sxs-lookup"><span data-stu-id="d799f-117">Type Description</span></span>



| <span data-ttu-id="d799f-118">Имя</span><span class="sxs-lookup"><span data-stu-id="d799f-118">Name</span></span>  | [<span data-ttu-id="d799f-119">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="d799f-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="d799f-120">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="d799f-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="d799f-121">Размер</span><span class="sxs-lookup"><span data-stu-id="d799f-121">Size</span></span> |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="d799f-122">*x*</span><span class="sxs-lookup"><span data-stu-id="d799f-122">*x*</span></span>   | <span data-ttu-id="d799f-123">[**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица**</span><span class="sxs-lookup"><span data-stu-id="d799f-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="d799f-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d799f-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="d799f-125">any</span><span class="sxs-lookup"><span data-stu-id="d799f-125">any</span></span>  |
| <span data-ttu-id="d799f-126">*обратно*</span><span class="sxs-lookup"><span data-stu-id="d799f-126">*ret*</span></span> | [<span data-ttu-id="d799f-127">**скаляр**</span><span class="sxs-lookup"><span data-stu-id="d799f-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                            | [<span data-ttu-id="d799f-128">**bool**</span><span class="sxs-lookup"><span data-stu-id="d799f-128">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                 | <span data-ttu-id="d799f-129">1</span><span class="sxs-lookup"><span data-stu-id="d799f-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d799f-130">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d799f-130">Minimum Shader Model</span></span>

<span data-ttu-id="d799f-131">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="d799f-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d799f-132">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d799f-132">Shader Model</span></span>                                                                       | <span data-ttu-id="d799f-133">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d799f-133">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="d799f-134">[Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="d799f-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d799f-135">да</span><span class="sxs-lookup"><span data-stu-id="d799f-135">yes</span></span>                   |
| [<span data-ttu-id="d799f-136">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d799f-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d799f-137">VS \_ 1 \_ 1 и PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="d799f-137">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="d799f-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d799f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d799f-139">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d799f-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

