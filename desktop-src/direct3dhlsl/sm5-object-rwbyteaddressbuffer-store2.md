---
title: 'Функция Рвбитеаддрессбуффер:: Store2'
description: Задает два значения.
ms.assetid: 7b32c84c-9ea2-47ae-a0f3-df6d95249163
keywords:
- Функция Store2 HLSL
topic_type:
- apiref
api_name:
- Store2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 574ad7fd59921767308e980e645bac966be87709
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "104069244"
---
# <a name="store2-function"></a><span data-ttu-id="79b3c-104">Функция Store2</span><span class="sxs-lookup"><span data-stu-id="79b3c-104">Store2 function</span></span>

<span data-ttu-id="79b3c-105">Задает два значения.</span><span class="sxs-lookup"><span data-stu-id="79b3c-105">Sets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="79b3c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79b3c-106">Syntax</span></span>

``` syntax
void Store2(
  in uint address,
  in uint2 values
);
```

## <a name="parameters"></a><span data-ttu-id="79b3c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="79b3c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79b3c-108">*адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79b3c-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79b3c-109">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="79b3c-109">Type: **uint**</span></span>

<span data-ttu-id="79b3c-110">Входной адрес в байтах, который должен быть кратным 4.</span><span class="sxs-lookup"><span data-stu-id="79b3c-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="79b3c-111">*значения* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79b3c-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79b3c-112">Тип: **uint2**</span><span class="sxs-lookup"><span data-stu-id="79b3c-112">Type: **uint2**</span></span>

<span data-ttu-id="79b3c-113">Два входных значения.</span><span class="sxs-lookup"><span data-stu-id="79b3c-113">Two input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79b3c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79b3c-114">Return value</span></span>

<span data-ttu-id="79b3c-115">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="79b3c-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79b3c-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="79b3c-116">Remarks</span></span>

<span data-ttu-id="79b3c-117">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="79b3c-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="79b3c-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="79b3c-118">Vertex</span></span> | <span data-ttu-id="79b3c-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="79b3c-119">Hull</span></span> | <span data-ttu-id="79b3c-120">Домен</span><span class="sxs-lookup"><span data-stu-id="79b3c-120">Domain</span></span> | <span data-ttu-id="79b3c-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="79b3c-121">Geometry</span></span> | <span data-ttu-id="79b3c-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="79b3c-122">Pixel</span></span> | <span data-ttu-id="79b3c-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="79b3c-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="79b3c-124">x</span><span class="sxs-lookup"><span data-stu-id="79b3c-124">x</span></span>     | <span data-ttu-id="79b3c-125">x</span><span class="sxs-lookup"><span data-stu-id="79b3c-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="79b3c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79b3c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79b3c-127">рвбитеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="79b3c-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="79b3c-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="79b3c-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




