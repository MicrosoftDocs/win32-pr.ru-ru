---
title: 'Функция Рвбитеаддрессбуффер:: Dimension'
description: 'Возвращает длину буфера. | Функция Рвбитеаддрессбуффер:: Dimension'
ms.assetid: 7d78aa0d-75b8-43d5-85d9-0a6fb04ae64f
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
ms.openlocfilehash: 0d22b6f655802d77a92611fe8699a405aa323873
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353582"
---
# <a name="rwbyteaddressbuffergetdimensions-function"></a><span data-ttu-id="48b43-105">Функция Рвбитеаддрессбуффер:: Dimension</span><span class="sxs-lookup"><span data-stu-id="48b43-105">RWByteAddressBuffer::GetDimensions function</span></span>

<span data-ttu-id="48b43-106">Возвращает длину буфера.</span><span class="sxs-lookup"><span data-stu-id="48b43-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b43-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48b43-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="48b43-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="48b43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48b43-109">*затемнение* \[\]</span><span class="sxs-lookup"><span data-stu-id="48b43-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48b43-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="48b43-110">Type: **uint**</span></span>

<span data-ttu-id="48b43-111">Длина буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="48b43-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48b43-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48b43-112">Return value</span></span>

<span data-ttu-id="48b43-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="48b43-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48b43-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="48b43-114">Remarks</span></span>

<span data-ttu-id="48b43-115">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="48b43-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="48b43-116">Вершина</span><span class="sxs-lookup"><span data-stu-id="48b43-116">Vertex</span></span> | <span data-ttu-id="48b43-117">Поверхности</span><span class="sxs-lookup"><span data-stu-id="48b43-117">Hull</span></span> | <span data-ttu-id="48b43-118">Домен</span><span class="sxs-lookup"><span data-stu-id="48b43-118">Domain</span></span> | <span data-ttu-id="48b43-119">Геометрия</span><span class="sxs-lookup"><span data-stu-id="48b43-119">Geometry</span></span> | <span data-ttu-id="48b43-120">Пиксель</span><span class="sxs-lookup"><span data-stu-id="48b43-120">Pixel</span></span> | <span data-ttu-id="48b43-121">Вычисления</span><span class="sxs-lookup"><span data-stu-id="48b43-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="48b43-122">x</span><span class="sxs-lookup"><span data-stu-id="48b43-122">x</span></span>     | <span data-ttu-id="48b43-123">x</span><span class="sxs-lookup"><span data-stu-id="48b43-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="48b43-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48b43-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48b43-125">рвбитеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="48b43-125">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="48b43-126">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="48b43-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




