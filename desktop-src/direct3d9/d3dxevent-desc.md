---
description: Описывает событие анимации.
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: Структура D3DXEVENT_DESC (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 32e02e75d3d73569b60c466f45dace2c074a6b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694157"
---
# <a name="d3dxevent_desc-structure"></a><span data-ttu-id="ef63a-103">\_Структура D3DXEVENT DESC</span><span class="sxs-lookup"><span data-stu-id="ef63a-103">D3DXEVENT\_DESC structure</span></span>

<span data-ttu-id="ef63a-104">Описывает событие анимации.</span><span class="sxs-lookup"><span data-stu-id="ef63a-104">Describes an animation event.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef63a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef63a-105">Syntax</span></span>


```C++
typedef struct D3DXEVENT_DESC {
  D3DXEVENT_TYPE      Type;
  UINT                Track;
  DOUBLE              StartTime;
  DOUBLE              Duration;
  D3DXTRANSITION_TYPE Transition;
  union {
    FLOAT  Weight;
    FLOAT  Speed;
    DOUBLE Position;
    BOOL   Enable;
  };
} D3DXEVENT_DESC, *LPD3DXEVENT_DESC;
```



## <a name="members"></a><span data-ttu-id="ef63a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="ef63a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ef63a-107">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ef63a-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="ef63a-108">Тип: **[ **D3DXEVENT \_ тип**](./d3dxevent-type.md)**</span><span class="sxs-lookup"><span data-stu-id="ef63a-108">Type: **[**D3DXEVENT\_TYPE**](./d3dxevent-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ef63a-109">Тип события, как определено [**в \_ типе D3DXEVENT**](./d3dxevent-type.md).</span><span class="sxs-lookup"><span data-stu-id="ef63a-109">Event type, as defined in [**D3DXEVENT\_TYPE**](./d3dxevent-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef63a-110">**Track**</span><span class="sxs-lookup"><span data-stu-id="ef63a-110">**Track**</span></span>
</dt> <dd>

<span data-ttu-id="ef63a-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef63a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ef63a-112">Идентификатор трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="ef63a-112">Event track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ef63a-113">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="ef63a-113">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="ef63a-114">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef63a-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ef63a-115">Время начала события в глобальном времени.</span><span class="sxs-lookup"><span data-stu-id="ef63a-115">Start time of the event in global time.</span></span>

</dd> <dt>

<span data-ttu-id="ef63a-116">**Длительность**</span><span class="sxs-lookup"><span data-stu-id="ef63a-116">**Duration**</span></span>
</dt> <dd>

<span data-ttu-id="ef63a-117">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef63a-117">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ef63a-118">Длительность события в глобальном времени.</span><span class="sxs-lookup"><span data-stu-id="ef63a-118">Duration of the event in global time.</span></span>

</dd> <dt>

<span data-ttu-id="ef63a-119">**Переход**</span><span class="sxs-lookup"><span data-stu-id="ef63a-119">**Transition**</span></span>
</dt> <dd>

<span data-ttu-id="ef63a-120">Тип: **[ **D3DXTRANSITION \_ тип**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="ef63a-120">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ef63a-121">Стиль перехода для события, как определено в [**\_ типе D3DXTRANSITION**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="ef63a-121">Transition style of the event, as defined in [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef63a-122">**Weight**</span><span class="sxs-lookup"><span data-stu-id="ef63a-122">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="ef63a-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef63a-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ef63a-124">Отслеживание веса для события.</span><span class="sxs-lookup"><span data-stu-id="ef63a-124">Track weight for the event.</span></span>

</dd> <dt>

<span data-ttu-id="ef63a-125">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="ef63a-125">**Speed**</span></span>
</dt> <dd>

<span data-ttu-id="ef63a-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef63a-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ef63a-127">Скорость записи для события.</span><span class="sxs-lookup"><span data-stu-id="ef63a-127">Track speed for the event.</span></span>

</dd> <dt>

<span data-ttu-id="ef63a-128">**Позиция**</span><span class="sxs-lookup"><span data-stu-id="ef63a-128">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="ef63a-129">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef63a-129">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ef63a-130">Отслеживание расположения для события.</span><span class="sxs-lookup"><span data-stu-id="ef63a-130">Track position for the event.</span></span>

</dd> <dt>

<span data-ttu-id="ef63a-131">**Разрешить**</span><span class="sxs-lookup"><span data-stu-id="ef63a-131">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="ef63a-132">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef63a-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ef63a-133">Включить флаг.</span><span class="sxs-lookup"><span data-stu-id="ef63a-133">Enable flag.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef63a-134">Требования</span><span class="sxs-lookup"><span data-stu-id="ef63a-134">Requirements</span></span>



| <span data-ttu-id="ef63a-135">Требование</span><span class="sxs-lookup"><span data-stu-id="ef63a-135">Requirement</span></span> | <span data-ttu-id="ef63a-136">Значение</span><span class="sxs-lookup"><span data-stu-id="ef63a-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef63a-137">Header</span><span class="sxs-lookup"><span data-stu-id="ef63a-137">Header</span></span><br/> | <dl> <span data-ttu-id="ef63a-138"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef63a-138"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef63a-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef63a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef63a-140">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="ef63a-140">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
