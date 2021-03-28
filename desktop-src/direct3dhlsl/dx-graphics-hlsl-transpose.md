---
title: переставить
description: Переставит указанную входную матрицу.
ms.assetid: 2a2ff2fb-73f0-4bb8-af83-38fe0567d122
keywords:
- переставить HLSL
topic_type:
- apiref
api_name:
- transpose
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44f129a87edaff260de87136954be7598ee3acb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413072"
---
# <a name="transpose"></a><span data-ttu-id="e5aa8-104">переставить</span><span class="sxs-lookup"><span data-stu-id="e5aa8-104">transpose</span></span>

<span data-ttu-id="e5aa8-105">Переставит указанную входную матрицу.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-105">Transposes the specified input matrix.</span></span>



| <span data-ttu-id="e5aa8-106">RET-транспонировать (*x*)</span><span class="sxs-lookup"><span data-stu-id="e5aa8-106">ret transpose(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="e5aa8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5aa8-107">Parameters</span></span>



| <span data-ttu-id="e5aa8-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="e5aa8-108">Item</span></span>                                                   | <span data-ttu-id="e5aa8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e5aa8-109">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="e5aa8-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="e5aa8-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="e5aa8-111">\[в \] указанной матрице.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-111">\[in\] The specified matrix.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="e5aa8-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5aa8-112">Return Value</span></span>

<span data-ttu-id="e5aa8-113">Переданное значение параметра *x* .</span><span class="sxs-lookup"><span data-stu-id="e5aa8-113">The transposed value of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5aa8-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5aa8-114">Remarks</span></span>

<span data-ttu-id="e5aa8-115">Если измерения исходной матрицы являются *столбцами* *строк* , то результирующая матрица будет *строкой* *столбцов* .</span><span class="sxs-lookup"><span data-stu-id="e5aa8-115">If the dimensions of the source matrix are *rows* *columns*, the resulting matrix is *columns* *rows*.</span></span>

## <a name="type-description"></a><span data-ttu-id="e5aa8-116">Описание типа</span><span class="sxs-lookup"><span data-stu-id="e5aa8-116">Type Description</span></span>



| <span data-ttu-id="e5aa8-117">Имя</span><span class="sxs-lookup"><span data-stu-id="e5aa8-117">Name</span></span> | [<span data-ttu-id="e5aa8-118">**Тип шаблона**</span><span class="sxs-lookup"><span data-stu-id="e5aa8-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="e5aa8-119">**Тип компонента**</span><span class="sxs-lookup"><span data-stu-id="e5aa8-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="e5aa8-120">Размер</span><span class="sxs-lookup"><span data-stu-id="e5aa8-120">Size</span></span>                                                                                   |
|------|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5aa8-121">*x*</span><span class="sxs-lookup"><span data-stu-id="e5aa8-121">*x*</span></span>  | [<span data-ttu-id="e5aa8-122">**таблицу**</span><span class="sxs-lookup"><span data-stu-id="e5aa8-122">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e5aa8-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="e5aa8-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="e5aa8-124">any</span><span class="sxs-lookup"><span data-stu-id="e5aa8-124">any</span></span>                                                                                    |
| <span data-ttu-id="e5aa8-125">обратно</span><span class="sxs-lookup"><span data-stu-id="e5aa8-125">ret</span></span>  | [<span data-ttu-id="e5aa8-126">**таблицу**</span><span class="sxs-lookup"><span data-stu-id="e5aa8-126">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e5aa8-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="e5aa8-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="e5aa8-128">строки — одинаковое число столбцов в качестве входных данных *x*, Columns = одинаковое число строк в качестве входных данных *x*</span><span class="sxs-lookup"><span data-stu-id="e5aa8-128">rows = same number of columns as input *x*, columns = same number of rows as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e5aa8-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e5aa8-129">Minimum Shader Model</span></span>

<span data-ttu-id="e5aa8-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e5aa8-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e5aa8-131">Shader Model</span></span>                                                                       | <span data-ttu-id="e5aa8-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="e5aa8-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e5aa8-133">[Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) и более высокие модели шейдеров</span><span class="sxs-lookup"><span data-stu-id="e5aa8-133">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="e5aa8-134">да</span><span class="sxs-lookup"><span data-stu-id="e5aa8-134">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e5aa8-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5aa8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5aa8-136">**Встроенные функции (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e5aa8-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

