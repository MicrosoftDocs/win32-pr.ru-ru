---
title: 'Функция Битеаддрессбуффер:: Load (int)'
description: 'Возвращает одно значение. | Функция Битеаддрессбуффер:: Load (int)'
ms.assetid: a63f4099-2c3b-4d37-9135-b8c63df30824
keywords:
- Загрузить функцию HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0de7d1a8ef8a7fe3173016fe07a433a930c3d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998059"
---
# <a name="byteaddressbufferloadint-function"></a><span data-ttu-id="614c7-105">Функция Битеаддрессбуффер:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="614c7-105">ByteAddressBuffer::Load(int) function</span></span>

<span data-ttu-id="614c7-106">Возвращает одно значение.</span><span class="sxs-lookup"><span data-stu-id="614c7-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="614c7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="614c7-107">Syntax</span></span>

``` syntax
uint Load(
  in int address
);
```

## <a name="parameters"></a><span data-ttu-id="614c7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="614c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="614c7-109">*адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="614c7-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614c7-110">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="614c7-110">Type: **int**</span></span>

<span data-ttu-id="614c7-111">Входной адрес в байтах, который должен быть кратным 4.</span><span class="sxs-lookup"><span data-stu-id="614c7-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="614c7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="614c7-112">Return value</span></span>

<span data-ttu-id="614c7-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="614c7-113">Type: **uint**</span></span>

<span data-ttu-id="614c7-114">Одно значение.</span><span class="sxs-lookup"><span data-stu-id="614c7-114">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="614c7-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="614c7-115">Remarks</span></span>

<span data-ttu-id="614c7-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="614c7-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="614c7-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="614c7-117">Vertex</span></span> | <span data-ttu-id="614c7-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="614c7-118">Hull</span></span> | <span data-ttu-id="614c7-119">Домен</span><span class="sxs-lookup"><span data-stu-id="614c7-119">Domain</span></span> | <span data-ttu-id="614c7-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="614c7-120">Geometry</span></span> | <span data-ttu-id="614c7-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="614c7-121">Pixel</span></span> | <span data-ttu-id="614c7-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="614c7-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="614c7-123">x</span><span class="sxs-lookup"><span data-stu-id="614c7-123">x</span></span>      | <span data-ttu-id="614c7-124">x</span><span class="sxs-lookup"><span data-stu-id="614c7-124">x</span></span>    | <span data-ttu-id="614c7-125">x</span><span class="sxs-lookup"><span data-stu-id="614c7-125">x</span></span>      | <span data-ttu-id="614c7-126">x</span><span class="sxs-lookup"><span data-stu-id="614c7-126">x</span></span>        | <span data-ttu-id="614c7-127">x</span><span class="sxs-lookup"><span data-stu-id="614c7-127">x</span></span>     | <span data-ttu-id="614c7-128">x</span><span class="sxs-lookup"><span data-stu-id="614c7-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="614c7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="614c7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="614c7-130">Методы Load</span><span class="sxs-lookup"><span data-stu-id="614c7-130">Load methods</span></span>](byteaddressbuffer-load.md)
</dt> <dt>

[<span data-ttu-id="614c7-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="614c7-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




