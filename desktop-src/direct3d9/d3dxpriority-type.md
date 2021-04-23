---
description: Определяет тип приоритета, которому назначена анимация анимации.
ms.assetid: 7bd83e31-09c4-4376-a22d-ed8023b78e84
title: Перечисление D3DXPRIORITY_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPRIORITY_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5e6d82807cbd0e93e7a1127db80726c0ec06b5da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424377"
---
# <a name="d3dxpriority_type-enumeration"></a><span data-ttu-id="0019a-103">\_Перечисление типов D3DXPRIORITY</span><span class="sxs-lookup"><span data-stu-id="0019a-103">D3DXPRIORITY\_TYPE enumeration</span></span>

<span data-ttu-id="0019a-104">Определяет тип приоритета, которому назначена анимация анимации.</span><span class="sxs-lookup"><span data-stu-id="0019a-104">Defines the priority type to which an animation track is assigned.</span></span>

## <a name="syntax"></a><span data-ttu-id="0019a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0019a-105">Syntax</span></span>


```C++
typedef enum D3DXPRIORITY_TYPE { 
  D3DXPRIORITY_LOW          = 0,
  D3DXPRIORITY_HIGH         = 1,
  D3DXPRIORITY_FORCE_DWORD  = 0x7fffffff
} D3DXPRIORITY_TYPE, *LPD3DXPRIORITY_TYPE;
```



## <a name="constants"></a><span data-ttu-id="0019a-106">Константы</span><span class="sxs-lookup"><span data-stu-id="0019a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0019a-107"><span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY \_ низкий**</span><span class="sxs-lookup"><span data-stu-id="0019a-107"><span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="0019a-108">Отслеживание должно смешиваться со всеми дорожками с низким приоритетом, прежде чем смешивание с низким приоритетом будет смешиваться с высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="0019a-108">Track should be blended with all the low-priority tracks before the low-priority blend is mixed with the high-priority blend.</span></span>

</dd> <dt>

<span data-ttu-id="0019a-109"><span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY \_ высокий**</span><span class="sxs-lookup"><span data-stu-id="0019a-109"><span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY\_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="0019a-110">Отслеживание следует смешивать со всеми высокоприоритетными дорожками, прежде чем смешивание с высоким приоритетом будет смешиваться с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="0019a-110">Track should be blended with all the high-priority tracks before the high-priority blend is mixed with the low-priority blend.</span></span>

</dd> <dt>

<span data-ttu-id="0019a-111"><span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0019a-111"><span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0019a-112">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="0019a-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0019a-113">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="0019a-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0019a-114">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="0019a-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0019a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0019a-115">Remarks</span></span>

<span data-ttu-id="0019a-116">Курсы с одинаковым приоритетом смешиваются друг с другом, а два результирующих значения смешиваются с использованием коэффициента смешения приоритетов.</span><span class="sxs-lookup"><span data-stu-id="0019a-116">Tracks with the same priority are blended together, and the two resulting values are then blended using the priority blend factor.</span></span>

## <a name="requirements"></a><span data-ttu-id="0019a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0019a-117">Requirements</span></span>



| <span data-ttu-id="0019a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0019a-118">Requirement</span></span> | <span data-ttu-id="0019a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0019a-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0019a-120">Header</span><span class="sxs-lookup"><span data-stu-id="0019a-120">Header</span></span><br/> | <dl> <span data-ttu-id="0019a-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0019a-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0019a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0019a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0019a-123">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="0019a-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




