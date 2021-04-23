---
description: Описывает анимацию и задает толщину, скорость и позиции смешения для записи в заданный момент времени.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: Структура D3DXTRACK_DESC (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRACK_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12f1604cf954bcdd6a2a898fec5410804112e498
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713633"
---
# <a name="d3dxtrack_desc-structure"></a><span data-ttu-id="4aeaf-103">\_Структура D3DXTRACK DESC</span><span class="sxs-lookup"><span data-stu-id="4aeaf-103">D3DXTRACK\_DESC structure</span></span>

<span data-ttu-id="4aeaf-104">Описывает анимацию и задает толщину, скорость и позиции смешения для записи в заданный момент времени.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-104">Describes an animation track and specifies blending weight, speed, and position for the track at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aeaf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4aeaf-105">Syntax</span></span>


```C++
typedef struct D3DXTRACK_DESC {
  D3DXPRIORITY_TYPE Priority;
  FLOAT             Weight;
  FLOAT             Speed;
  DOUBLE            Position;
  BOOL              Enable;
} D3DXTRACK_DESC, *LPD3DXTRACK_DESC;
```



## <a name="members"></a><span data-ttu-id="4aeaf-106">Члены</span><span class="sxs-lookup"><span data-stu-id="4aeaf-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4aeaf-107">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="4aeaf-107">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="4aeaf-108">Тип: **[ **D3DXPRIORITY \_ тип**](./d3dxpriority-type.md)**</span><span class="sxs-lookup"><span data-stu-id="4aeaf-108">Type: **[**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4aeaf-109">Тип приоритета, как определено в [**\_ типе D3DXPRIORITY**](./d3dxpriority-type.md).</span><span class="sxs-lookup"><span data-stu-id="4aeaf-109">Priority type, as defined in [**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aeaf-110">**Weight**</span><span class="sxs-lookup"><span data-stu-id="4aeaf-110">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="4aeaf-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4aeaf-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4aeaf-112">Значение веса.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-112">Weight value.</span></span> <span data-ttu-id="4aeaf-113">Вес определяет долю этой дорожки для смешения с другими дорожками.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-113">The weight determines the proportion of this track to blend with other tracks.</span></span>

</dd> <dt>

<span data-ttu-id="4aeaf-114">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="4aeaf-114">**Speed**</span></span>
</dt> <dd>

<span data-ttu-id="4aeaf-115">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4aeaf-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4aeaf-116">Значение скорости.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-116">Speed value.</span></span> <span data-ttu-id="4aeaf-117">Он используется аналогично множителю для масштабирования периода курса.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-117">This is used similarly to a multiplier to scale the period of the track.</span></span>

</dd> <dt>

<span data-ttu-id="4aeaf-118">**Позиция**</span><span class="sxs-lookup"><span data-stu-id="4aeaf-118">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="4aeaf-119">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4aeaf-119">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4aeaf-120">Время, на которое ведется трассировка, в локальной временной области текущего набора анимации.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-120">Time position of the track, in the local timeframe of its current animation set.</span></span>

</dd> <dt>

<span data-ttu-id="4aeaf-121">**Разрешить**</span><span class="sxs-lookup"><span data-stu-id="4aeaf-121">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="4aeaf-122">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4aeaf-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4aeaf-123">Следите за включением и отключением.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-123">Track enable/disable.</span></span> <span data-ttu-id="4aeaf-124">Чтобы включить, установите значение **true**.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-124">To enable, set to **TRUE**.</span></span> <span data-ttu-id="4aeaf-125">Чтобы отключить, задайте для параметра значение **false**.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-125">To disable, set to **FALSE**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4aeaf-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4aeaf-126">Remarks</span></span>

<span data-ttu-id="4aeaf-127">Курсы с одинаковым приоритетом смешиваются друг с другом, а два результирующих значения смешиваются с использованием коэффициента смешения приоритетов.</span><span class="sxs-lookup"><span data-stu-id="4aeaf-127">Tracks with the same priority are blended together, and the two resulting values are then blended using the priority blend factor.</span></span> <span data-ttu-id="4aeaf-128">С дорожкой должен быть связан набор анимации (хранящийся отдельно).</span><span class="sxs-lookup"><span data-stu-id="4aeaf-128">A track must have an animation set (stored separately) associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aeaf-129">Требования</span><span class="sxs-lookup"><span data-stu-id="4aeaf-129">Requirements</span></span>



| <span data-ttu-id="4aeaf-130">Требование</span><span class="sxs-lookup"><span data-stu-id="4aeaf-130">Requirement</span></span> | <span data-ttu-id="4aeaf-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4aeaf-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4aeaf-132">Header</span><span class="sxs-lookup"><span data-stu-id="4aeaf-132">Header</span></span><br/> | <dl> <span data-ttu-id="4aeaf-133"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4aeaf-133"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aeaf-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4aeaf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aeaf-135">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="4aeaf-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
