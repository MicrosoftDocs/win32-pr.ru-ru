---
title: 'Функция buffer:: Dimension'
description: 'Возвращает длину буфера. | Функция buffer:: Dimension'
ms.assetid: 704890e8-43e4-4e72-b7e2-eeef331bef1c
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
ms.openlocfilehash: c7f1ad1da7600e65d7442c1b2431535e2fdcf38c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986205"
---
# <a name="buffergetdimensions-function"></a><span data-ttu-id="31d4c-105">Функция buffer:: Dimension</span><span class="sxs-lookup"><span data-stu-id="31d4c-105">Buffer::GetDimensions function</span></span>

<span data-ttu-id="31d4c-106">Возвращает длину буфера.</span><span class="sxs-lookup"><span data-stu-id="31d4c-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="31d4c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31d4c-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="31d4c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="31d4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31d4c-109">*затемнение* \[\]</span><span class="sxs-lookup"><span data-stu-id="31d4c-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31d4c-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="31d4c-110">Type: **uint**</span></span>

<span data-ttu-id="31d4c-111">Длина буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="31d4c-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31d4c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31d4c-112">Return value</span></span>

<span data-ttu-id="31d4c-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="31d4c-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31d4c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="31d4c-114">Remarks</span></span>

<span data-ttu-id="31d4c-115">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="31d4c-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="31d4c-116">Вершина</span><span class="sxs-lookup"><span data-stu-id="31d4c-116">Vertex</span></span> | <span data-ttu-id="31d4c-117">Поверхности</span><span class="sxs-lookup"><span data-stu-id="31d4c-117">Hull</span></span> | <span data-ttu-id="31d4c-118">Домен</span><span class="sxs-lookup"><span data-stu-id="31d4c-118">Domain</span></span> | <span data-ttu-id="31d4c-119">Геометрия</span><span class="sxs-lookup"><span data-stu-id="31d4c-119">Geometry</span></span> | <span data-ttu-id="31d4c-120">Пиксель</span><span class="sxs-lookup"><span data-stu-id="31d4c-120">Pixel</span></span> | <span data-ttu-id="31d4c-121">Вычисления</span><span class="sxs-lookup"><span data-stu-id="31d4c-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="31d4c-122">x</span><span class="sxs-lookup"><span data-stu-id="31d4c-122">x</span></span>      | <span data-ttu-id="31d4c-123">x</span><span class="sxs-lookup"><span data-stu-id="31d4c-123">x</span></span>    | <span data-ttu-id="31d4c-124">x</span><span class="sxs-lookup"><span data-stu-id="31d4c-124">x</span></span>      | <span data-ttu-id="31d4c-125">x</span><span class="sxs-lookup"><span data-stu-id="31d4c-125">x</span></span>        | <span data-ttu-id="31d4c-126">x</span><span class="sxs-lookup"><span data-stu-id="31d4c-126">x</span></span>     | <span data-ttu-id="31d4c-127">x</span><span class="sxs-lookup"><span data-stu-id="31d4c-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="31d4c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31d4c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d4c-129">Буфер</span><span class="sxs-lookup"><span data-stu-id="31d4c-129">Buffer</span></span>](sm5-object-buffer.md)
</dt> <dt>

[<span data-ttu-id="31d4c-130">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="31d4c-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




