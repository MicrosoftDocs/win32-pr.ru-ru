---
title: 'Функция Рвбитеаддрессбуффер:: Load3 (UINT)'
description: 'Возвращает три значения. | Функция Рвбитеаддрессбуффер:: Load3 (UINT)'
ms.assetid: cf8c4c5d-4748-43d7-896e-33ed07c94b9e
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
ms.openlocfilehash: d6658b4929f09aa7296a284de1fdbf39c7c4f038
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986732"
---
# <a name="rwbyteaddressbufferload3uint-function"></a><span data-ttu-id="9fbd6-105">Функция Рвбитеаддрессбуффер:: Load3 (UINT)</span><span class="sxs-lookup"><span data-stu-id="9fbd6-105">RWByteAddressBuffer::Load3(uint) function</span></span>

<span data-ttu-id="9fbd6-106">Возвращает три значения.</span><span class="sxs-lookup"><span data-stu-id="9fbd6-106">Gets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fbd6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fbd6-107">Syntax</span></span>

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="9fbd6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9fbd6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fbd6-109">*адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9fbd6-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fbd6-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="9fbd6-110">Type: **uint**</span></span>

<span data-ttu-id="9fbd6-111">Входной адрес в байтах, который должен быть кратным 4.</span><span class="sxs-lookup"><span data-stu-id="9fbd6-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fbd6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9fbd6-112">Return value</span></span>

<span data-ttu-id="9fbd6-113">Тип: **uint3**</span><span class="sxs-lookup"><span data-stu-id="9fbd6-113">Type: **uint3**</span></span>

<span data-ttu-id="9fbd6-114">Три значения.</span><span class="sxs-lookup"><span data-stu-id="9fbd6-114">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fbd6-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="9fbd6-115">Remarks</span></span>

<span data-ttu-id="9fbd6-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="9fbd6-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9fbd6-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="9fbd6-117">Vertex</span></span> | <span data-ttu-id="9fbd6-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="9fbd6-118">Hull</span></span> | <span data-ttu-id="9fbd6-119">Домен</span><span class="sxs-lookup"><span data-stu-id="9fbd6-119">Domain</span></span> | <span data-ttu-id="9fbd6-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="9fbd6-120">Geometry</span></span> | <span data-ttu-id="9fbd6-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="9fbd6-121">Pixel</span></span> | <span data-ttu-id="9fbd6-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="9fbd6-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9fbd6-123">x</span><span class="sxs-lookup"><span data-stu-id="9fbd6-123">x</span></span>     | <span data-ttu-id="9fbd6-124">x</span><span class="sxs-lookup"><span data-stu-id="9fbd6-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9fbd6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fbd6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fbd6-126">Методы Load3</span><span class="sxs-lookup"><span data-stu-id="9fbd6-126">Load3 methods</span></span>](rwbyteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="9fbd6-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="9fbd6-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




