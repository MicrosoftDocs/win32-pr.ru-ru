---
title: 'Функция Структуредбуффер:: Dimension'
description: 'Возвращает размеры ресурсов. | Функция Структуредбуффер:: Dimension'
ms.assetid: 423ea79c-4440-4837-b637-95180a1d5019
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
ms.openlocfilehash: 2b3d7c879c77386ddee80a63053711b8ae34ee8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352962"
---
# <a name="structuredbuffergetdimensions-function"></a><span data-ttu-id="9b1ea-105">Функция Структуредбуффер:: Dimension</span><span class="sxs-lookup"><span data-stu-id="9b1ea-105">StructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="9b1ea-106">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b1ea-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b1ea-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b1ea-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="9b1ea-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b1ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b1ea-109">*нумструктс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9b1ea-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b1ea-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="9b1ea-110">Type: **uint**</span></span>

<span data-ttu-id="9b1ea-111">Число структур в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="9b1ea-111">The number of structures in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="9b1ea-112">*Шаг с шагом* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9b1ea-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b1ea-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="9b1ea-113">Type: **uint**</span></span>

<span data-ttu-id="9b1ea-114">Шаг в байтах для каждого элемента структуры.</span><span class="sxs-lookup"><span data-stu-id="9b1ea-114">The stride, in bytes, of each structure element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b1ea-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b1ea-115">Return value</span></span>

<span data-ttu-id="9b1ea-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9b1ea-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b1ea-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="9b1ea-117">Remarks</span></span>

<span data-ttu-id="9b1ea-118">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="9b1ea-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9b1ea-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="9b1ea-119">Vertex</span></span> | <span data-ttu-id="9b1ea-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="9b1ea-120">Hull</span></span> | <span data-ttu-id="9b1ea-121">Домен</span><span class="sxs-lookup"><span data-stu-id="9b1ea-121">Domain</span></span> | <span data-ttu-id="9b1ea-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="9b1ea-122">Geometry</span></span> | <span data-ttu-id="9b1ea-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="9b1ea-123">Pixel</span></span> | <span data-ttu-id="9b1ea-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="9b1ea-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9b1ea-125">x</span><span class="sxs-lookup"><span data-stu-id="9b1ea-125">x</span></span>      | <span data-ttu-id="9b1ea-126">x</span><span class="sxs-lookup"><span data-stu-id="9b1ea-126">x</span></span>    | <span data-ttu-id="9b1ea-127">x</span><span class="sxs-lookup"><span data-stu-id="9b1ea-127">x</span></span>      | <span data-ttu-id="9b1ea-128">x</span><span class="sxs-lookup"><span data-stu-id="9b1ea-128">x</span></span>        | <span data-ttu-id="9b1ea-129">x</span><span class="sxs-lookup"><span data-stu-id="9b1ea-129">x</span></span>     | <span data-ttu-id="9b1ea-130">x</span><span class="sxs-lookup"><span data-stu-id="9b1ea-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9b1ea-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b1ea-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b1ea-132">структуредбуффер</span><span class="sxs-lookup"><span data-stu-id="9b1ea-132">StructuredBuffer</span></span>](sm5-object-structuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="9b1ea-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="9b1ea-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




