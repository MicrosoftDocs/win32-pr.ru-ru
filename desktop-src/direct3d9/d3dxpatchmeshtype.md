---
description: Типы исправлений для сетки.
ms.assetid: 229d01b2-781c-48a8-93f2-9dd9dbd67f3e
title: Перечисление D3DXPATCHMESHTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHMESHTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d6a663e983b339d79ec89bf1b4ddfe7b4eaa9f1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713466"
---
# <a name="d3dxpatchmeshtype-enumeration"></a><span data-ttu-id="4ffac-103">Перечисление D3DXPATCHMESHTYPE</span><span class="sxs-lookup"><span data-stu-id="4ffac-103">D3DXPATCHMESHTYPE enumeration</span></span>

<span data-ttu-id="4ffac-104">Типы исправлений для сетки.</span><span class="sxs-lookup"><span data-stu-id="4ffac-104">Mesh patch types.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ffac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ffac-105">Syntax</span></span>


```C++
typedef enum D3DXPATCHMESHTYPE { 
  D3DXPATCHMESH_RECT         = 0x001,
  D3DXPATCHMESH_TRI          = 0x002,
  D3DXPATCHMESH_NPATCH       = 0x003,
  D3DXPATCHMESH_FORCE_DWORD  = 0x7fffffff
} D3DXPATCHMESHTYPE, *LPD3DXPATCHMESHTYPE;
```



## <a name="constants"></a><span data-ttu-id="4ffac-106">Константы</span><span class="sxs-lookup"><span data-stu-id="4ffac-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4ffac-107"><span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="4ffac-107"><span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH\_RECT**</span></span>
</dt> <dd>

<span data-ttu-id="4ffac-108">Тип сетки обновления прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4ffac-108">Rectangle patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="4ffac-109"><span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH \_**</span><span class="sxs-lookup"><span data-stu-id="4ffac-109"><span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH\_TRI**</span></span>
</dt> <dd>

<span data-ttu-id="4ffac-110">Тип сетки обновления треугольника.</span><span class="sxs-lookup"><span data-stu-id="4ffac-110">Triangle patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="4ffac-111"><span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH \_ нпатч**</span><span class="sxs-lookup"><span data-stu-id="4ffac-111"><span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH\_NPATCH**</span></span>
</dt> <dd>

<span data-ttu-id="4ffac-112">Тип сетки N-patch.</span><span class="sxs-lookup"><span data-stu-id="4ffac-112">N-patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="4ffac-113"><span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4ffac-113"><span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="4ffac-114">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="4ffac-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="4ffac-115">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="4ffac-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="4ffac-116">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="4ffac-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ffac-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ffac-117">Remarks</span></span>

<span data-ttu-id="4ffac-118">Обновления треугольников имеют три стороны и описаны в [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="4ffac-118">Triangle patches have three sides and are described in [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span> <span data-ttu-id="4ffac-119">Обновления прямоугольников являются четырьмя и описаны в [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="4ffac-119">Rectangle patches are four-sided and are described in [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ffac-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4ffac-120">Requirements</span></span>



| <span data-ttu-id="4ffac-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4ffac-121">Requirement</span></span> | <span data-ttu-id="4ffac-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4ffac-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ffac-123">Header</span><span class="sxs-lookup"><span data-stu-id="4ffac-123">Header</span></span><br/> | <dl> <span data-ttu-id="4ffac-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ffac-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ffac-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ffac-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ffac-126">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="4ffac-126">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="4ffac-127">Использование примитивов Higher-Order (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4ffac-127">Using Higher-Order Primitives (Direct3D 9)</span></span>](using-higher-order-primitives.md)
</dt> </dl>

 

 




