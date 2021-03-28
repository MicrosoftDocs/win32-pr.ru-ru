---
title: 'Функция Рвбуффер:: Dimension'
description: 'Возвращает длину буфера. | Функция Рвбуффер:: Dimension'
ms.assetid: 600147cb-9513-4b74-a873-1ed22b31cdf7
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
ms.openlocfilehash: 98e419d3e77a27f211f0e063573caffcd6c61ce8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998210"
---
# <a name="rwbuffergetdimensions-function"></a><span data-ttu-id="d5eba-105">Функция Рвбуффер:: Dimension</span><span class="sxs-lookup"><span data-stu-id="d5eba-105">RWBuffer::GetDimensions function</span></span>

<span data-ttu-id="d5eba-106">Возвращает длину буфера.</span><span class="sxs-lookup"><span data-stu-id="d5eba-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5eba-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5eba-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="d5eba-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5eba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5eba-109">*затемнение* \[\]</span><span class="sxs-lookup"><span data-stu-id="d5eba-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5eba-110">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="d5eba-110">Type: **uint**</span></span>

<span data-ttu-id="d5eba-111">Длина буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="d5eba-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5eba-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5eba-112">Return value</span></span>

<span data-ttu-id="d5eba-113">Nothing</span><span class="sxs-lookup"><span data-stu-id="d5eba-113">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="d5eba-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d5eba-114">Remarks</span></span>

<span data-ttu-id="d5eba-115">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="d5eba-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d5eba-116">Вершина</span><span class="sxs-lookup"><span data-stu-id="d5eba-116">Vertex</span></span> | <span data-ttu-id="d5eba-117">Поверхности</span><span class="sxs-lookup"><span data-stu-id="d5eba-117">Hull</span></span> | <span data-ttu-id="d5eba-118">Домен</span><span class="sxs-lookup"><span data-stu-id="d5eba-118">Domain</span></span> | <span data-ttu-id="d5eba-119">Геометрия</span><span class="sxs-lookup"><span data-stu-id="d5eba-119">Geometry</span></span> | <span data-ttu-id="d5eba-120">Пиксель</span><span class="sxs-lookup"><span data-stu-id="d5eba-120">Pixel</span></span> | <span data-ttu-id="d5eba-121">Вычисления</span><span class="sxs-lookup"><span data-stu-id="d5eba-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d5eba-122">x</span><span class="sxs-lookup"><span data-stu-id="d5eba-122">x</span></span>     | <span data-ttu-id="d5eba-123">x</span><span class="sxs-lookup"><span data-stu-id="d5eba-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d5eba-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5eba-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5eba-125">рвбуффер</span><span class="sxs-lookup"><span data-stu-id="d5eba-125">RWBuffer</span></span>](sm5-object-rwbuffer.md)
</dt> <dt>

[<span data-ttu-id="d5eba-126">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="d5eba-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




