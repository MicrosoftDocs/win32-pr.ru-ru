---
title: 'Функция Texture2DMS:: Жетсамплепоситион'
description: Возвращает расположение образца для указанного индекса.
ms.assetid: b7821112-9b40-4302-b5c1-03bab531a0ab
keywords:
- Функция Жетсамплепоситион HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 532411e333023ff61df0b7f9fbf0336dc11d1586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533710"
---
# <a name="texture2dmsgetsampleposition-function"></a><span data-ttu-id="b9d4f-104">Функция Texture2DMS:: Жетсамплепоситион</span><span class="sxs-lookup"><span data-stu-id="b9d4f-104">Texture2DMS::GetSamplePosition function</span></span>

<span data-ttu-id="b9d4f-105">Возвращает расположение образца для указанного индекса.</span><span class="sxs-lookup"><span data-stu-id="b9d4f-105">Returns the sample position for the sample index provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9d4f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9d4f-106">Syntax</span></span>

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="b9d4f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9d4f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9d4f-108">*sampleindex* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b9d4f-108">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9d4f-109">Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9d4f-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b9d4f-110">Отсчитываемый от нуля индекс образца расположения.</span><span class="sxs-lookup"><span data-stu-id="b9d4f-110">The zero-based index of a sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9d4f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9d4f-111">Return value</span></span>

<span data-ttu-id="b9d4f-112">Тип: **float2**</span><span class="sxs-lookup"><span data-stu-id="b9d4f-112">Type: **float2**</span></span>

<span data-ttu-id="b9d4f-113">Пример расположения.</span><span class="sxs-lookup"><span data-stu-id="b9d4f-113">A sample location.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9d4f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9d4f-114">Remarks</span></span>

<span data-ttu-id="b9d4f-115">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="b9d4f-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b9d4f-116">Вершина</span><span class="sxs-lookup"><span data-stu-id="b9d4f-116">Vertex</span></span> | <span data-ttu-id="b9d4f-117">Поверхности</span><span class="sxs-lookup"><span data-stu-id="b9d4f-117">Hull</span></span> | <span data-ttu-id="b9d4f-118">Домен</span><span class="sxs-lookup"><span data-stu-id="b9d4f-118">Domain</span></span> | <span data-ttu-id="b9d4f-119">Геометрия</span><span class="sxs-lookup"><span data-stu-id="b9d4f-119">Geometry</span></span> | <span data-ttu-id="b9d4f-120">Пиксель</span><span class="sxs-lookup"><span data-stu-id="b9d4f-120">Pixel</span></span> | <span data-ttu-id="b9d4f-121">Вычисления</span><span class="sxs-lookup"><span data-stu-id="b9d4f-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b9d4f-122">x</span><span class="sxs-lookup"><span data-stu-id="b9d4f-122">x</span></span>      | <span data-ttu-id="b9d4f-123">x</span><span class="sxs-lookup"><span data-stu-id="b9d4f-123">x</span></span>    | <span data-ttu-id="b9d4f-124">x</span><span class="sxs-lookup"><span data-stu-id="b9d4f-124">x</span></span>      | <span data-ttu-id="b9d4f-125">x</span><span class="sxs-lookup"><span data-stu-id="b9d4f-125">x</span></span>        | <span data-ttu-id="b9d4f-126">x</span><span class="sxs-lookup"><span data-stu-id="b9d4f-126">x</span></span>     | <span data-ttu-id="b9d4f-127">x</span><span class="sxs-lookup"><span data-stu-id="b9d4f-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b9d4f-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9d4f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9d4f-129">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="b9d4f-129">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="b9d4f-130">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="b9d4f-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
