---
title: 'Функция Битеаддрессбуффер:: Load3 (UINT)'
description: 'Возвращает три значения. | Функция Битеаддрессбуффер:: Load3 (UINT)'
ms.assetid: 79afeb36-e0e7-44a2-b252-8e3577f4c1a5
keywords:
- Функция Load3 HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e3975d454fcbb8c5dfa8cdef8d7f5718143546f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986625"
---
# <a name="byteaddressbufferload3uint-function"></a><span data-ttu-id="ca0ef-105">Функция Битеаддрессбуффер:: Load3 (UINT)</span><span class="sxs-lookup"><span data-stu-id="ca0ef-105">ByteAddressBuffer::Load3(uint) function</span></span>

<span data-ttu-id="ca0ef-106">Возвращает три значения.</span><span class="sxs-lookup"><span data-stu-id="ca0ef-106">Gets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca0ef-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca0ef-107">Syntax</span></span>

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="ca0ef-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca0ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca0ef-109">*адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca0ef-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca0ef-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="ca0ef-110">Type: **uint**</span></span>

<span data-ttu-id="ca0ef-111">Входной адрес в байтах, который должен быть кратным 4.</span><span class="sxs-lookup"><span data-stu-id="ca0ef-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca0ef-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca0ef-112">Return value</span></span>

<span data-ttu-id="ca0ef-113">Тип: **uint3**</span><span class="sxs-lookup"><span data-stu-id="ca0ef-113">Type: **uint3**</span></span>

<span data-ttu-id="ca0ef-114">Три значения.</span><span class="sxs-lookup"><span data-stu-id="ca0ef-114">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca0ef-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="ca0ef-115">Remarks</span></span>

<span data-ttu-id="ca0ef-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ca0ef-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ca0ef-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="ca0ef-117">Vertex</span></span> | <span data-ttu-id="ca0ef-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ca0ef-118">Hull</span></span> | <span data-ttu-id="ca0ef-119">Домен</span><span class="sxs-lookup"><span data-stu-id="ca0ef-119">Domain</span></span> | <span data-ttu-id="ca0ef-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ca0ef-120">Geometry</span></span> | <span data-ttu-id="ca0ef-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ca0ef-121">Pixel</span></span> | <span data-ttu-id="ca0ef-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ca0ef-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ca0ef-123">x</span><span class="sxs-lookup"><span data-stu-id="ca0ef-123">x</span></span>      | <span data-ttu-id="ca0ef-124">x</span><span class="sxs-lookup"><span data-stu-id="ca0ef-124">x</span></span>    | <span data-ttu-id="ca0ef-125">x</span><span class="sxs-lookup"><span data-stu-id="ca0ef-125">x</span></span>      | <span data-ttu-id="ca0ef-126">x</span><span class="sxs-lookup"><span data-stu-id="ca0ef-126">x</span></span>        | <span data-ttu-id="ca0ef-127">x</span><span class="sxs-lookup"><span data-stu-id="ca0ef-127">x</span></span>     | <span data-ttu-id="ca0ef-128">x</span><span class="sxs-lookup"><span data-stu-id="ca0ef-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ca0ef-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca0ef-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca0ef-130">Методы Load3</span><span class="sxs-lookup"><span data-stu-id="ca0ef-130">Load3 methods</span></span>](byteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="ca0ef-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ca0ef-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




