---
title: 'Функция Битеаддрессбуффер:: Load2 (UINT)'
description: 'Возвращает два значения. | Функция Битеаддрессбуффер:: Load2 (UINT)'
ms.assetid: 696ce310-4d65-4382-97ec-046160197c67
keywords:
- Функция Load2 HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78204fc3d41daf07a54974fbf103685e718ab79d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820509"
---
# <a name="byteaddressbufferload2uint-function"></a><span data-ttu-id="9dbe0-105">Функция Битеаддрессбуффер:: Load2 (UINT)</span><span class="sxs-lookup"><span data-stu-id="9dbe0-105">ByteAddressBuffer::Load2(uint) function</span></span>

<span data-ttu-id="9dbe0-106">Возвращает два значения.</span><span class="sxs-lookup"><span data-stu-id="9dbe0-106">Gets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dbe0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9dbe0-107">Syntax</span></span>

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="9dbe0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9dbe0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dbe0-109">*адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9dbe0-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dbe0-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="9dbe0-110">Type: **uint**</span></span>

<span data-ttu-id="9dbe0-111">Входной адрес в байтах, который должен быть кратным 4.</span><span class="sxs-lookup"><span data-stu-id="9dbe0-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dbe0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9dbe0-112">Return value</span></span>

<span data-ttu-id="9dbe0-113">Тип: **uint2**</span><span class="sxs-lookup"><span data-stu-id="9dbe0-113">Type: **uint2**</span></span>

<span data-ttu-id="9dbe0-114">Два значения.</span><span class="sxs-lookup"><span data-stu-id="9dbe0-114">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dbe0-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="9dbe0-115">Remarks</span></span>

<span data-ttu-id="9dbe0-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="9dbe0-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9dbe0-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="9dbe0-117">Vertex</span></span> | <span data-ttu-id="9dbe0-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="9dbe0-118">Hull</span></span> | <span data-ttu-id="9dbe0-119">Домен</span><span class="sxs-lookup"><span data-stu-id="9dbe0-119">Domain</span></span> | <span data-ttu-id="9dbe0-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="9dbe0-120">Geometry</span></span> | <span data-ttu-id="9dbe0-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="9dbe0-121">Pixel</span></span> | <span data-ttu-id="9dbe0-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="9dbe0-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9dbe0-123">x</span><span class="sxs-lookup"><span data-stu-id="9dbe0-123">x</span></span>      | <span data-ttu-id="9dbe0-124">x</span><span class="sxs-lookup"><span data-stu-id="9dbe0-124">x</span></span>    | <span data-ttu-id="9dbe0-125">x</span><span class="sxs-lookup"><span data-stu-id="9dbe0-125">x</span></span>      | <span data-ttu-id="9dbe0-126">x</span><span class="sxs-lookup"><span data-stu-id="9dbe0-126">x</span></span>        | <span data-ttu-id="9dbe0-127">x</span><span class="sxs-lookup"><span data-stu-id="9dbe0-127">x</span></span>     | <span data-ttu-id="9dbe0-128">x</span><span class="sxs-lookup"><span data-stu-id="9dbe0-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9dbe0-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9dbe0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dbe0-130">Методы Load2</span><span class="sxs-lookup"><span data-stu-id="9dbe0-130">Load2 methods</span></span>](byteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="9dbe0-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="9dbe0-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




