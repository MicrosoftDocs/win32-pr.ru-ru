---
title: 'Функция Битеаддрессбуффер:: Load4 (UINT)'
description: 'Возвращает четыре значения. | Функция Битеаддрессбуффер:: Load4 (UINT)'
ms.assetid: bc74bf29-1c22-4e47-bafc-ecef194f54b8
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
ms.openlocfilehash: 18ce27e7d02a414165aab169e40a6ab14cdd8c4c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986624"
---
# <a name="byteaddressbufferload4uint-function"></a><span data-ttu-id="9d1c0-105">Функция Битеаддрессбуффер:: Load4 (UINT)</span><span class="sxs-lookup"><span data-stu-id="9d1c0-105">ByteAddressBuffer::Load4(uint) function</span></span>

<span data-ttu-id="9d1c0-106">Возвращает четыре значения.</span><span class="sxs-lookup"><span data-stu-id="9d1c0-106">Gets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d1c0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d1c0-107">Syntax</span></span>

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="9d1c0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d1c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d1c0-109">*адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d1c0-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d1c0-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="9d1c0-110">Type: **uint**</span></span>

<span data-ttu-id="9d1c0-111">Входной адрес в байтах, который должен быть кратным 4.</span><span class="sxs-lookup"><span data-stu-id="9d1c0-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d1c0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d1c0-112">Return value</span></span>

<span data-ttu-id="9d1c0-113">Тип: **uint4**</span><span class="sxs-lookup"><span data-stu-id="9d1c0-113">Type: **uint4**</span></span>

<span data-ttu-id="9d1c0-114">Четыре значения.</span><span class="sxs-lookup"><span data-stu-id="9d1c0-114">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d1c0-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="9d1c0-115">Remarks</span></span>

<span data-ttu-id="9d1c0-116">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="9d1c0-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9d1c0-117">Вершина</span><span class="sxs-lookup"><span data-stu-id="9d1c0-117">Vertex</span></span> | <span data-ttu-id="9d1c0-118">Поверхности</span><span class="sxs-lookup"><span data-stu-id="9d1c0-118">Hull</span></span> | <span data-ttu-id="9d1c0-119">Домен</span><span class="sxs-lookup"><span data-stu-id="9d1c0-119">Domain</span></span> | <span data-ttu-id="9d1c0-120">Геометрия</span><span class="sxs-lookup"><span data-stu-id="9d1c0-120">Geometry</span></span> | <span data-ttu-id="9d1c0-121">Пиксель</span><span class="sxs-lookup"><span data-stu-id="9d1c0-121">Pixel</span></span> | <span data-ttu-id="9d1c0-122">Вычисления</span><span class="sxs-lookup"><span data-stu-id="9d1c0-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9d1c0-123">x</span><span class="sxs-lookup"><span data-stu-id="9d1c0-123">x</span></span>      | <span data-ttu-id="9d1c0-124">x</span><span class="sxs-lookup"><span data-stu-id="9d1c0-124">x</span></span>    | <span data-ttu-id="9d1c0-125">x</span><span class="sxs-lookup"><span data-stu-id="9d1c0-125">x</span></span>      | <span data-ttu-id="9d1c0-126">x</span><span class="sxs-lookup"><span data-stu-id="9d1c0-126">x</span></span>        | <span data-ttu-id="9d1c0-127">x</span><span class="sxs-lookup"><span data-stu-id="9d1c0-127">x</span></span>     | <span data-ttu-id="9d1c0-128">x</span><span class="sxs-lookup"><span data-stu-id="9d1c0-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9d1c0-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d1c0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d1c0-130">Методы Load4</span><span class="sxs-lookup"><span data-stu-id="9d1c0-130">Load4 methods</span></span>](byteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="9d1c0-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="9d1c0-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




