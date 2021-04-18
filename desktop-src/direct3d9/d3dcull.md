---
description: Определяет поддерживаемые режимы отбора.
ms.assetid: b669307c-0d40-4ecb-8a2e-8bd1d9c65647
title: Перечисление D3DCULL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCULL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e88aa1baf86b2b03177cc686bf83299311065283
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703709"
---
# <a name="d3dcull-enumeration"></a><span data-ttu-id="64a55-103">Перечисление D3DCULL</span><span class="sxs-lookup"><span data-stu-id="64a55-103">D3DCULL enumeration</span></span>

<span data-ttu-id="64a55-104">Определяет поддерживаемые режимы отбора.</span><span class="sxs-lookup"><span data-stu-id="64a55-104">Defines the supported culling modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="64a55-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64a55-105">Syntax</span></span>


```C++
typedef enum D3DCULL { 
  D3DCULL_NONE         = 1,
  D3DCULL_CW           = 2,
  D3DCULL_CCW          = 3,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DCULL, *LPD3DCULL;
```



## <a name="constants"></a><span data-ttu-id="64a55-106">Константы</span><span class="sxs-lookup"><span data-stu-id="64a55-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="64a55-107"><span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL \_ None**</span><span class="sxs-lookup"><span data-stu-id="64a55-107"><span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="64a55-108">Не исключать задние грани.</span><span class="sxs-lookup"><span data-stu-id="64a55-108">Do not cull back faces.</span></span>

</dd> <dt>

<span data-ttu-id="64a55-109"><span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL \_ во вт.**</span><span class="sxs-lookup"><span data-stu-id="64a55-109"><span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL\_CW**</span></span>
</dt> <dd>

<span data-ttu-id="64a55-110">Исключать грани с отднем по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="64a55-110">Cull back faces with clockwise vertices.</span></span>

</dd> <dt>

<span data-ttu-id="64a55-111"><span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**D3DCULL \_ CCW**</span><span class="sxs-lookup"><span data-stu-id="64a55-111"><span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**D3DCULL\_CCW**</span></span>
</dt> <dd>

<span data-ttu-id="64a55-112">Возврат лицевых сторон с вершинами против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="64a55-112">Cull back faces with counterclockwise vertices.</span></span>

</dd> <dt>

<span data-ttu-id="64a55-113"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="64a55-113"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="64a55-114">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="64a55-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="64a55-115">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="64a55-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="64a55-116">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="64a55-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64a55-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64a55-117">Remarks</span></span>

<span data-ttu-id="64a55-118">Значения в этом перечислимом типе используются \_ состоянием визуализации D3DRS куллмоде.</span><span class="sxs-lookup"><span data-stu-id="64a55-118">The values in this enumerated type are used by the D3DRS\_CULLMODE render state.</span></span> <span data-ttu-id="64a55-119">Режимы отбора определяют, каким способом исключаются грани при подготовке к просмотру геометрии.</span><span class="sxs-lookup"><span data-stu-id="64a55-119">The culling modes define how back faces are culled when rendering a geometry.</span></span>

## <a name="requirements"></a><span data-ttu-id="64a55-120">Требования</span><span class="sxs-lookup"><span data-stu-id="64a55-120">Requirements</span></span>



| <span data-ttu-id="64a55-121">Требование</span><span class="sxs-lookup"><span data-stu-id="64a55-121">Requirement</span></span> | <span data-ttu-id="64a55-122">Значение</span><span class="sxs-lookup"><span data-stu-id="64a55-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64a55-123">Header</span><span class="sxs-lookup"><span data-stu-id="64a55-123">Header</span></span><br/> | <dl> <span data-ttu-id="64a55-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="64a55-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64a55-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64a55-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64a55-126">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="64a55-126">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="64a55-127">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="64a55-127">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="64a55-128">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="64a55-128">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
