---
title: 'Функция Аппендструктуредбуффер:: Dimension'
description: 'Возвращает размеры ресурсов. | Функция Аппендструктуредбуффер:: Dimension'
ms.assetid: 41ed86d5-25c0-48bd-add9-792eb89605c3
keywords:
- Функция Dimension HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 93db905ae40f1bec7488eca292f4ea44d87950d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986208"
---
# <a name="appendstructuredbuffergetdimensions-function"></a><span data-ttu-id="ca222-105">Функция Аппендструктуредбуффер:: Dimension</span><span class="sxs-lookup"><span data-stu-id="ca222-105">AppendStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="ca222-106">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ca222-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca222-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca222-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="ca222-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca222-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca222-109">*нумструктс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ca222-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca222-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="ca222-110">Type: **uint**</span></span>

<span data-ttu-id="ca222-111">Число структур.</span><span class="sxs-lookup"><span data-stu-id="ca222-111">The number of structures.</span></span>

</dd> <dt>

<span data-ttu-id="ca222-112">*Шаг с шагом* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ca222-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca222-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="ca222-113">Type: **uint**</span></span>

<span data-ttu-id="ca222-114">Число байтов в каждом элементе.</span><span class="sxs-lookup"><span data-stu-id="ca222-114">The number of bytes in each element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca222-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca222-115">Return value</span></span>

<span data-ttu-id="ca222-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ca222-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca222-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ca222-117">Remarks</span></span>

<span data-ttu-id="ca222-118">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ca222-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ca222-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="ca222-119">Vertex</span></span> | <span data-ttu-id="ca222-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ca222-120">Hull</span></span> | <span data-ttu-id="ca222-121">Домен</span><span class="sxs-lookup"><span data-stu-id="ca222-121">Domain</span></span> | <span data-ttu-id="ca222-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ca222-122">Geometry</span></span> | <span data-ttu-id="ca222-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ca222-123">Pixel</span></span> | <span data-ttu-id="ca222-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ca222-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ca222-125">x</span><span class="sxs-lookup"><span data-stu-id="ca222-125">x</span></span>      | <span data-ttu-id="ca222-126">x</span><span class="sxs-lookup"><span data-stu-id="ca222-126">x</span></span>    | <span data-ttu-id="ca222-127">x</span><span class="sxs-lookup"><span data-stu-id="ca222-127">x</span></span>      | <span data-ttu-id="ca222-128">x</span><span class="sxs-lookup"><span data-stu-id="ca222-128">x</span></span>        | <span data-ttu-id="ca222-129">x</span><span class="sxs-lookup"><span data-stu-id="ca222-129">x</span></span>     | <span data-ttu-id="ca222-130">x</span><span class="sxs-lookup"><span data-stu-id="ca222-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ca222-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca222-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca222-132">аппендструктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="ca222-132">AppendStructuredBuffer</span></span>](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="ca222-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ca222-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




