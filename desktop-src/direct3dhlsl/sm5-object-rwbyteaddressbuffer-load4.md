---
title: 'Функция Рвбитеаддрессбуффер:: Load4 (UINT)'
description: 'Возвращает четыре значения. | Функция Рвбитеаддрессбуффер:: Load4 (UINT)'
ms.assetid: b46cd119-75be-4c2d-82f9-5dcabd7e4400
keywords:
- Функция Load4 HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2bdc5adf3b3d95c68871a14c9382891a59ad52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986723"
---
# <a name="rwbyteaddressbufferload4uint-function"></a><span data-ttu-id="17783-105">Функция Рвбитеаддрессбуффер:: Load4 (UINT)</span><span class="sxs-lookup"><span data-stu-id="17783-105">RWByteAddressBuffer::Load4(uint) function</span></span>

<span data-ttu-id="17783-106">Возвращает четыре значения.</span><span class="sxs-lookup"><span data-stu-id="17783-106">Gets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="17783-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17783-107">Syntax</span></span>

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="17783-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="17783-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17783-109">*адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17783-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17783-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="17783-110">Type: **uint**</span></span>

<span data-ttu-id="17783-111">Входной адрес в байтах, который должен быть кратным 4.</span><span class="sxs-lookup"><span data-stu-id="17783-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17783-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17783-112">Return value</span></span>

<span data-ttu-id="17783-113">Тип: **uint4**</span><span class="sxs-lookup"><span data-stu-id="17783-113">Type: **uint4**</span></span>

<span data-ttu-id="17783-114">Четыре значения.</span><span class="sxs-lookup"><span data-stu-id="17783-114">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="17783-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="17783-115">Remarks</span></span>

<span data-ttu-id="17783-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="17783-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="17783-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="17783-117">Vertex</span></span> | <span data-ttu-id="17783-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="17783-118">Hull</span></span> | <span data-ttu-id="17783-119">Домен</span><span class="sxs-lookup"><span data-stu-id="17783-119">Domain</span></span> | <span data-ttu-id="17783-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="17783-120">Geometry</span></span> | <span data-ttu-id="17783-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="17783-121">Pixel</span></span> | <span data-ttu-id="17783-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="17783-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="17783-123">x</span><span class="sxs-lookup"><span data-stu-id="17783-123">x</span></span>     | <span data-ttu-id="17783-124">x</span><span class="sxs-lookup"><span data-stu-id="17783-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="17783-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17783-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17783-126">Методы Load4</span><span class="sxs-lookup"><span data-stu-id="17783-126">Load4 methods</span></span>](rwbyteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="17783-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="17783-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




