---
title: 'Функция Рвбитеаддрессбуффер:: Load2 (UINT)'
description: 'Возвращает два значения. | Функция Рвбитеаддрессбуффер:: Load2 (UINT)'
ms.assetid: a00396cb-e68d-479e-ab3f-4c52f2cfc3bc
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
ms.openlocfilehash: 7595477448deb087b94664100710690a6f386a94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986702"
---
# <a name="rwbyteaddressbufferload2uint-function"></a><span data-ttu-id="71d32-105">Функция Рвбитеаддрессбуффер:: Load2 (UINT)</span><span class="sxs-lookup"><span data-stu-id="71d32-105">RWByteAddressBuffer::Load2(uint) function</span></span>

<span data-ttu-id="71d32-106">Возвращает два значения.</span><span class="sxs-lookup"><span data-stu-id="71d32-106">Gets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d32-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71d32-107">Syntax</span></span>

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="71d32-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="71d32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71d32-109">*адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71d32-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71d32-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="71d32-110">Type: **uint**</span></span>

<span data-ttu-id="71d32-111">Входной адрес в байтах, который должен быть кратным 4.</span><span class="sxs-lookup"><span data-stu-id="71d32-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71d32-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71d32-112">Return value</span></span>

<span data-ttu-id="71d32-113">Тип: **uint2**</span><span class="sxs-lookup"><span data-stu-id="71d32-113">Type: **uint2**</span></span>

<span data-ttu-id="71d32-114">Два значения.</span><span class="sxs-lookup"><span data-stu-id="71d32-114">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="71d32-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="71d32-115">Remarks</span></span>

<span data-ttu-id="71d32-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="71d32-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="71d32-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="71d32-117">Vertex</span></span> | <span data-ttu-id="71d32-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="71d32-118">Hull</span></span> | <span data-ttu-id="71d32-119">Домен</span><span class="sxs-lookup"><span data-stu-id="71d32-119">Domain</span></span> | <span data-ttu-id="71d32-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="71d32-120">Geometry</span></span> | <span data-ttu-id="71d32-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="71d32-121">Pixel</span></span> | <span data-ttu-id="71d32-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="71d32-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="71d32-123">x</span><span class="sxs-lookup"><span data-stu-id="71d32-123">x</span></span>     | <span data-ttu-id="71d32-124">x</span><span class="sxs-lookup"><span data-stu-id="71d32-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="71d32-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71d32-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d32-126">Методы Load2</span><span class="sxs-lookup"><span data-stu-id="71d32-126">Load2 methods</span></span>](rwbyteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="71d32-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="71d32-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




