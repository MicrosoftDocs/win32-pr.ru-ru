---
title: 'Функция Рвбитеаддрессбуффер:: Store'
description: Задает одно значение.
ms.assetid: edfda955-602c-44f4-adc3-77b61c9dcd05
keywords:
- Функция Store HLSL
topic_type:
- apiref
api_name:
- Store
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e161e4fb64d09e41c6529954e63b2ace55207e9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "104983773"
---
# <a name="store-function"></a><span data-ttu-id="83842-104">Функция Store</span><span class="sxs-lookup"><span data-stu-id="83842-104">Store function</span></span>

<span data-ttu-id="83842-105">Задает одно значение.</span><span class="sxs-lookup"><span data-stu-id="83842-105">Sets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="83842-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83842-106">Syntax</span></span>

``` syntax
void Store(
  in uint address,
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="83842-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="83842-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83842-108">*адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83842-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83842-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="83842-109">Type: **uint**</span></span>

<span data-ttu-id="83842-110">Входной адрес в байтах, который должен быть кратным 4.</span><span class="sxs-lookup"><span data-stu-id="83842-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="83842-111">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83842-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83842-112">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="83842-112">Type: **uint**</span></span>

<span data-ttu-id="83842-113">Одно входное значение.</span><span class="sxs-lookup"><span data-stu-id="83842-113">One input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83842-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83842-114">Return value</span></span>

<span data-ttu-id="83842-115">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="83842-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83842-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="83842-116">Remarks</span></span>

<span data-ttu-id="83842-117">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="83842-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="83842-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="83842-118">Vertex</span></span> | <span data-ttu-id="83842-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="83842-119">Hull</span></span> | <span data-ttu-id="83842-120">Домен</span><span class="sxs-lookup"><span data-stu-id="83842-120">Domain</span></span> | <span data-ttu-id="83842-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="83842-121">Geometry</span></span> | <span data-ttu-id="83842-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="83842-122">Pixel</span></span> | <span data-ttu-id="83842-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="83842-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="83842-124">x</span><span class="sxs-lookup"><span data-stu-id="83842-124">x</span></span>     | <span data-ttu-id="83842-125">x</span><span class="sxs-lookup"><span data-stu-id="83842-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="83842-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83842-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83842-127">рвбитеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="83842-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="83842-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="83842-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




