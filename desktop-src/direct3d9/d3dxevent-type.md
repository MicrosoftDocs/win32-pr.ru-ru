---
description: Описывает тип событий, которые могут быть разделены контроллером анимации.
ms.assetid: d98b398e-29e1-41b5-84eb-37983bac8d0a
title: Перечисление D3DXEVENT_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 97219478b898dc47e385e8e00a5cc9b5484730ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354880"
---
# <a name="d3dxevent_type-enumeration"></a><span data-ttu-id="1860b-103">\_Перечисление типов D3DXEVENT</span><span class="sxs-lookup"><span data-stu-id="1860b-103">D3DXEVENT\_TYPE enumeration</span></span>

<span data-ttu-id="1860b-104">Описывает тип событий, которые могут быть разделены контроллером анимации.</span><span class="sxs-lookup"><span data-stu-id="1860b-104">Describes the type of events that can be keyed by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="1860b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1860b-105">Syntax</span></span>


```C++
typedef enum D3DXEVENT_TYPE { 
  D3DXEVENT_TRACKSPEED     = 0,
  D3DXEVENT_TRACKWEIGHT    = 1,
  D3DXEVENT_TRACKPOSITION  = 2,
  D3DXEVENT_TRACKENABLE    = 3,
  D3DXEVENT_PRIORITYBLEND  = 4,
  D3DXEVENT_FORCE_DWORD    = 0x7fffffff
} D3DXEVENT_TYPE, *LPD3DXEVENT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="1860b-106">Константы</span><span class="sxs-lookup"><span data-stu-id="1860b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1860b-107"><span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**D3DXEVENT \_ траккспид**</span><span class="sxs-lookup"><span data-stu-id="1860b-107"><span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**D3DXEVENT\_TRACKSPEED**</span></span>
</dt> <dd>

<span data-ttu-id="1860b-108">Скорость записи.</span><span class="sxs-lookup"><span data-stu-id="1860b-108">Track speed.</span></span>

</dd> <dt>

<span data-ttu-id="1860b-109"><span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**D3DXEVENT \_ тракквеигхт**</span><span class="sxs-lookup"><span data-stu-id="1860b-109"><span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**D3DXEVENT\_TRACKWEIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="1860b-110">Вес трекинга.</span><span class="sxs-lookup"><span data-stu-id="1860b-110">Track weight.</span></span>

</dd> <dt>

<span data-ttu-id="1860b-111"><span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**D3DXEVENT \_ траккпоситион**</span><span class="sxs-lookup"><span data-stu-id="1860b-111"><span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**D3DXEVENT\_TRACKPOSITION**</span></span>
</dt> <dd>

<span data-ttu-id="1860b-112">Расположение Track.</span><span class="sxs-lookup"><span data-stu-id="1860b-112">Track position.</span></span>

</dd> <dt>

<span data-ttu-id="1860b-113"><span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**D3DXEVENT \_ траккенабле**</span><span class="sxs-lookup"><span data-stu-id="1860b-113"><span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**D3DXEVENT\_TRACKENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="1860b-114">Включить флаг.</span><span class="sxs-lookup"><span data-stu-id="1860b-114">Enable flag.</span></span>

</dd> <dt>

<span data-ttu-id="1860b-115"><span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**D3DXEVENT \_ приоритибленд**</span><span class="sxs-lookup"><span data-stu-id="1860b-115"><span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**D3DXEVENT\_PRIORITYBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="1860b-116">Значение приоритета смешения.</span><span class="sxs-lookup"><span data-stu-id="1860b-116">Priority blend value.</span></span>

</dd> <dt>

<span data-ttu-id="1860b-117"><span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1860b-117"><span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="1860b-118">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="1860b-118">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="1860b-119">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="1860b-119">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="1860b-120">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="1860b-120">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1860b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1860b-121">Requirements</span></span>



| <span data-ttu-id="1860b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="1860b-122">Requirement</span></span> | <span data-ttu-id="1860b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1860b-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1860b-124">Header</span><span class="sxs-lookup"><span data-stu-id="1860b-124">Header</span></span><br/> | <dl> <span data-ttu-id="1860b-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="1860b-125"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1860b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1860b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1860b-127">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="1860b-127">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




