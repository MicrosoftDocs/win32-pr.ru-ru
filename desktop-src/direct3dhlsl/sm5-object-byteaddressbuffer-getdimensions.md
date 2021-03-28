---
title: 'Функция Битеаддрессбуффер:: Dimension'
description: 'Возвращает длину буфера. | Функция Битеаддрессбуффер:: Dimension'
ms.assetid: 32099118-8d8a-440e-96ba-2580d905f068
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
ms.openlocfilehash: 1cbb705789e444a6fa54aeb87190912996f65621
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998014"
---
# <a name="byteaddressbuffergetdimensions-function"></a><span data-ttu-id="defdd-105">Функция Битеаддрессбуффер:: Dimension</span><span class="sxs-lookup"><span data-stu-id="defdd-105">ByteAddressBuffer::GetDimensions function</span></span>

<span data-ttu-id="defdd-106">Возвращает длину буфера.</span><span class="sxs-lookup"><span data-stu-id="defdd-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="defdd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="defdd-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="defdd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="defdd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="defdd-109">*затемнение* \[\]</span><span class="sxs-lookup"><span data-stu-id="defdd-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="defdd-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="defdd-110">Type: **uint**</span></span>

<span data-ttu-id="defdd-111">Длина буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="defdd-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="defdd-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="defdd-112">Return value</span></span>

<span data-ttu-id="defdd-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="defdd-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="defdd-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="defdd-114">Remarks</span></span>

<span data-ttu-id="defdd-115">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="defdd-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="defdd-116">Вершина</span><span class="sxs-lookup"><span data-stu-id="defdd-116">Vertex</span></span> | <span data-ttu-id="defdd-117">Поверхности</span><span class="sxs-lookup"><span data-stu-id="defdd-117">Hull</span></span> | <span data-ttu-id="defdd-118">Домен</span><span class="sxs-lookup"><span data-stu-id="defdd-118">Domain</span></span> | <span data-ttu-id="defdd-119">Геометрия</span><span class="sxs-lookup"><span data-stu-id="defdd-119">Geometry</span></span> | <span data-ttu-id="defdd-120">Пиксель</span><span class="sxs-lookup"><span data-stu-id="defdd-120">Pixel</span></span> | <span data-ttu-id="defdd-121">Вычисления</span><span class="sxs-lookup"><span data-stu-id="defdd-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="defdd-122">x</span><span class="sxs-lookup"><span data-stu-id="defdd-122">x</span></span>      | <span data-ttu-id="defdd-123">x</span><span class="sxs-lookup"><span data-stu-id="defdd-123">x</span></span>    | <span data-ttu-id="defdd-124">x</span><span class="sxs-lookup"><span data-stu-id="defdd-124">x</span></span>      | <span data-ttu-id="defdd-125">x</span><span class="sxs-lookup"><span data-stu-id="defdd-125">x</span></span>        | <span data-ttu-id="defdd-126">x</span><span class="sxs-lookup"><span data-stu-id="defdd-126">x</span></span>     | <span data-ttu-id="defdd-127">x</span><span class="sxs-lookup"><span data-stu-id="defdd-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="defdd-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="defdd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="defdd-129">битеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="defdd-129">ByteAddressBuffer</span></span>](sm5-object-byteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="defdd-130">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="defdd-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




