---
description: Определяет константы, описывающие режим заполнения.
ms.assetid: be835432-e8d5-4afb-a810-2dac25bdc9dc
title: Перечисление D3DFILLMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFILLMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 33cf03258933055aa18aecb42fffe4d8f33b1e51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704033"
---
# <a name="d3dfillmode-enumeration"></a><span data-ttu-id="a274f-103">Перечисление D3DFILLMODE</span><span class="sxs-lookup"><span data-stu-id="a274f-103">D3DFILLMODE enumeration</span></span>

<span data-ttu-id="a274f-104">Определяет константы, описывающие режим заполнения.</span><span class="sxs-lookup"><span data-stu-id="a274f-104">Defines constants describing the fill mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="a274f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a274f-105">Syntax</span></span>


```C++
typedef enum D3DFILLMODE { 
  D3DFILL_POINT        = 1,
  D3DFILL_WIREFRAME    = 2,
  D3DFILL_SOLID        = 3,
  D3DFILL_FORCE_DWORD  = 0x7fffffff
} D3DFILLMODE, *LPD3DFILLMODE;
```



## <a name="constants"></a><span data-ttu-id="a274f-106">Константы</span><span class="sxs-lookup"><span data-stu-id="a274f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a274f-107"><span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**\_Точка D3DFILL**</span><span class="sxs-lookup"><span data-stu-id="a274f-107"><span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**D3DFILL\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="a274f-108">Точки заполнения.</span><span class="sxs-lookup"><span data-stu-id="a274f-108">Fill points.</span></span>

</dd> <dt>

<span data-ttu-id="a274f-109"><span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**\_Каркасная схема D3DFILL**</span><span class="sxs-lookup"><span data-stu-id="a274f-109"><span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**D3DFILL\_WIREFRAME**</span></span>
</dt> <dd>

<span data-ttu-id="a274f-110">Заполнить каркасы.</span><span class="sxs-lookup"><span data-stu-id="a274f-110">Fill wireframes.</span></span>

</dd> <dt>

<span data-ttu-id="a274f-111"><span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL \_**</span><span class="sxs-lookup"><span data-stu-id="a274f-111"><span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL\_SOLID**</span></span>
</dt> <dd>

<span data-ttu-id="a274f-112">Заливка сплошным.</span><span class="sxs-lookup"><span data-stu-id="a274f-112">Fill solids.</span></span>

</dd> <dt>

<span data-ttu-id="a274f-113"><span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a274f-113"><span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a274f-114">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="a274f-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a274f-115">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="a274f-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a274f-116">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="a274f-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a274f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a274f-117">Remarks</span></span>

<span data-ttu-id="a274f-118">Значения в этом перечислимом типе используются \_ состоянием визуализации D3DRS филлмоде.</span><span class="sxs-lookup"><span data-stu-id="a274f-118">The values in this enumerated type are used by the D3DRS\_FILLMODE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="a274f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a274f-119">Requirements</span></span>



| <span data-ttu-id="a274f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a274f-120">Requirement</span></span> | <span data-ttu-id="a274f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a274f-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a274f-122">Header</span><span class="sxs-lookup"><span data-stu-id="a274f-122">Header</span></span><br/> | <dl> <span data-ttu-id="a274f-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a274f-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a274f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a274f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a274f-125">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="a274f-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="a274f-126">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="a274f-126">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
