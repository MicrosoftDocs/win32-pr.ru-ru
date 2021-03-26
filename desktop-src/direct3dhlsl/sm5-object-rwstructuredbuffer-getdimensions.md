---
title: 'Функция Рвструктуредбуффер:: Dimension'
description: 'Возвращает размеры ресурсов. | Функция Рвструктуредбуффер:: Dimension'
ms.assetid: 842b3d21-2e2b-4906-93ee-0252b2e8cf85
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
ms.openlocfilehash: 0e3868f33e372472999c29bffdd8e12bc8ef09b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986201"
---
# <a name="rwstructuredbuffergetdimensions-function"></a><span data-ttu-id="abf8c-105">Функция Рвструктуредбуффер:: Dimension</span><span class="sxs-lookup"><span data-stu-id="abf8c-105">RWStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="abf8c-106">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="abf8c-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="abf8c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abf8c-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="abf8c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="abf8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abf8c-109">*нумструктс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="abf8c-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abf8c-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="abf8c-110">Type: **uint**</span></span>

<span data-ttu-id="abf8c-111">Число структур в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="abf8c-111">The number of structures in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="abf8c-112">*Шаг с шагом* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="abf8c-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abf8c-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="abf8c-113">Type: **uint**</span></span>

<span data-ttu-id="abf8c-114">Шаг в байтах для каждого элемента структуры.</span><span class="sxs-lookup"><span data-stu-id="abf8c-114">The stride, in bytes, of each structure element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abf8c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="abf8c-115">Return value</span></span>

<span data-ttu-id="abf8c-116">Nothing</span><span class="sxs-lookup"><span data-stu-id="abf8c-116">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="abf8c-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="abf8c-117">Remarks</span></span>

<span data-ttu-id="abf8c-118">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="abf8c-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="abf8c-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="abf8c-119">Vertex</span></span> | <span data-ttu-id="abf8c-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="abf8c-120">Hull</span></span> | <span data-ttu-id="abf8c-121">Домен</span><span class="sxs-lookup"><span data-stu-id="abf8c-121">Domain</span></span> | <span data-ttu-id="abf8c-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="abf8c-122">Geometry</span></span> | <span data-ttu-id="abf8c-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="abf8c-123">Pixel</span></span> | <span data-ttu-id="abf8c-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="abf8c-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="abf8c-125">x</span><span class="sxs-lookup"><span data-stu-id="abf8c-125">x</span></span>     | <span data-ttu-id="abf8c-126">x</span><span class="sxs-lookup"><span data-stu-id="abf8c-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="abf8c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abf8c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abf8c-128">рвструктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="abf8c-128">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="abf8c-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="abf8c-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




