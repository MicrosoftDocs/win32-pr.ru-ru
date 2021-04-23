---
title: 'Функция Консуместруктуредбуффер:: Dimension'
description: 'Возвращает размеры ресурсов. | Функция Консуместруктуредбуффер:: Dimension'
ms.assetid: 0710a4fb-23b0-4b19-b9ed-21bbb9874d33
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
ms.openlocfilehash: a204ed44c90c60b327ceb201037c6758763b3a05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998026"
---
# <a name="consumestructuredbuffergetdimensions-function"></a><span data-ttu-id="684d2-105">Функция Консуместруктуредбуффер:: Dimension</span><span class="sxs-lookup"><span data-stu-id="684d2-105">ConsumeStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="684d2-106">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="684d2-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="684d2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="684d2-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="684d2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="684d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="684d2-109">*нумструктс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="684d2-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="684d2-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="684d2-110">Type: **uint**</span></span>

<span data-ttu-id="684d2-111">Число структур.</span><span class="sxs-lookup"><span data-stu-id="684d2-111">The number of structures.</span></span>

</dd> <dt>

<span data-ttu-id="684d2-112">*Шаг с шагом* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="684d2-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="684d2-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="684d2-113">Type: **uint**</span></span>

<span data-ttu-id="684d2-114">Шаг (в байтах) каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="684d2-114">The stride, in bytes, of each element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="684d2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="684d2-115">Return value</span></span>

<span data-ttu-id="684d2-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="684d2-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="684d2-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="684d2-117">Remarks</span></span>

<span data-ttu-id="684d2-118">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="684d2-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="684d2-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="684d2-119">Vertex</span></span> | <span data-ttu-id="684d2-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="684d2-120">Hull</span></span> | <span data-ttu-id="684d2-121">Домен</span><span class="sxs-lookup"><span data-stu-id="684d2-121">Domain</span></span> | <span data-ttu-id="684d2-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="684d2-122">Geometry</span></span> | <span data-ttu-id="684d2-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="684d2-123">Pixel</span></span> | <span data-ttu-id="684d2-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="684d2-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="684d2-125">x</span><span class="sxs-lookup"><span data-stu-id="684d2-125">x</span></span>      | <span data-ttu-id="684d2-126">x</span><span class="sxs-lookup"><span data-stu-id="684d2-126">x</span></span>    | <span data-ttu-id="684d2-127">x</span><span class="sxs-lookup"><span data-stu-id="684d2-127">x</span></span>      | <span data-ttu-id="684d2-128">x</span><span class="sxs-lookup"><span data-stu-id="684d2-128">x</span></span>        | <span data-ttu-id="684d2-129">x</span><span class="sxs-lookup"><span data-stu-id="684d2-129">x</span></span>     | <span data-ttu-id="684d2-130">x</span><span class="sxs-lookup"><span data-stu-id="684d2-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="684d2-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="684d2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="684d2-132">консуместруктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="684d2-132">ConsumeStructuredBuffer</span></span>](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="684d2-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="684d2-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




