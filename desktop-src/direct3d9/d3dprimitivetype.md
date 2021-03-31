---
description: Определяет примитивы, поддерживаемые Direct3D.
ms.assetid: 89e697f9-02b9-4ae1-9e86-6178da0cb008
title: Перечисление D3DPRIMITIVETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRIMITIVETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 933bbec72950bd2c73fda8b3781dd46393ca4c96
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157203"
---
# <a name="d3dprimitivetype-enumeration"></a><span data-ttu-id="e1d8e-103">Перечисление D3DPRIMITIVETYPE</span><span class="sxs-lookup"><span data-stu-id="e1d8e-103">D3DPRIMITIVETYPE enumeration</span></span>

<span data-ttu-id="e1d8e-104">Определяет примитивы, поддерживаемые Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e1d8e-104">Defines the primitives supported by Direct3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d8e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1d8e-105">Syntax</span></span>


```C++
typedef enum D3DPRIMITIVETYPE { 
  D3DPT_POINTLIST      = 1,
  D3DPT_LINELIST       = 2,
  D3DPT_LINESTRIP      = 3,
  D3DPT_TRIANGLELIST   = 4,
  D3DPT_TRIANGLESTRIP  = 5,
  D3DPT_TRIANGLEFAN    = 6,
  D3DPT_FORCE_DWORD    = 0x7fffffff
} D3DPRIMITIVETYPE, *LPD3DPRIMITIVETYPE;
```



## <a name="constants"></a><span data-ttu-id="e1d8e-106">Константы</span><span class="sxs-lookup"><span data-stu-id="e1d8e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e1d8e-107"><span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT \_ поинтлист**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-107"><span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT\_POINTLIST**</span></span>
</dt> <dd>

<span data-ttu-id="e1d8e-108">Отображает вершины в виде коллекции изолированных точек.</span><span class="sxs-lookup"><span data-stu-id="e1d8e-108">Renders the vertices as a collection of isolated points.</span></span> <span data-ttu-id="e1d8e-109">Это значение не поддерживается для индексированных примитивов.</span><span class="sxs-lookup"><span data-stu-id="e1d8e-109">This value is unsupported for indexed primitives.</span></span>

</dd> <dt>

<span data-ttu-id="e1d8e-110"><span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT \_ линелист**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-110"><span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT\_LINELIST**</span></span>
</dt> <dd>

<span data-ttu-id="e1d8e-111">Отображает вершины в виде списка изолированных сегментов прямой линии.</span><span class="sxs-lookup"><span data-stu-id="e1d8e-111">Renders the vertices as a list of isolated straight line segments.</span></span>

</dd> <dt>

<span data-ttu-id="e1d8e-112"><span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT \_ линестрип**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-112"><span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT\_LINESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="e1d8e-113">Отображает вершины в виде одной ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="e1d8e-113">Renders the vertices as a single polyline.</span></span>

</dd> <dt>

<span data-ttu-id="e1d8e-114"><span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT \_ трианглелист**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-114"><span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT\_TRIANGLELIST**</span></span>
</dt> <dd>

<span data-ttu-id="e1d8e-115">Отображает указанные вершины как последовательность изолированных треугольников.</span><span class="sxs-lookup"><span data-stu-id="e1d8e-115">Renders the specified vertices as a sequence of isolated triangles.</span></span> <span data-ttu-id="e1d8e-116">Каждая группа из трех вершин определяет отдельный треугольник.</span><span class="sxs-lookup"><span data-stu-id="e1d8e-116">Each group of three vertices defines a separate triangle.</span></span>

<span data-ttu-id="e1d8e-117">На возврат к обратной стороне влияет текущее состояние отображения "обмотка".</span><span class="sxs-lookup"><span data-stu-id="e1d8e-117">Back-face culling is affected by the current winding-order render state.</span></span>

</dd> <dt>

<span data-ttu-id="e1d8e-118"><span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT \_ трианглестрип**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-118"><span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT\_TRIANGLESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="e1d8e-119">Отображает вершины в виде полосы треугольника.</span><span class="sxs-lookup"><span data-stu-id="e1d8e-119">Renders the vertices as a triangle strip.</span></span> <span data-ttu-id="e1d8e-120">Флаг отбора задних граней автоматически передается на треугольники с четным числом.</span><span class="sxs-lookup"><span data-stu-id="e1d8e-120">The backface-culling flag is automatically flipped on even-numbered triangles.</span></span>

</dd> <dt>

<span data-ttu-id="e1d8e-121"><span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT \_ трианглефан**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-121"><span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT\_TRIANGLEFAN**</span></span>
</dt> <dd>

<span data-ttu-id="e1d8e-122">Отображает вершины в качестве вентилятора треугольника.</span><span class="sxs-lookup"><span data-stu-id="e1d8e-122">Renders the vertices as a triangle fan.</span></span>

</dd> <dt>

<span data-ttu-id="e1d8e-123"><span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-123"><span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="e1d8e-124">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="e1d8e-124">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="e1d8e-125">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="e1d8e-125">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="e1d8e-126">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="e1d8e-126">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1d8e-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1d8e-127">Remarks</span></span>

<span data-ttu-id="e1d8e-128">Использование [лент треугольников](triangle-strips.md) или вершинных [вентиляторов (Direct3D 9)](triangle-fans.md) зачастую более эффективно, чем использование списков треугольников, поскольку дублируется меньшее число вершин.</span><span class="sxs-lookup"><span data-stu-id="e1d8e-128">Using [Triangle Strips](triangle-strips.md) or [Triangle Fans (Direct3D 9)](triangle-fans.md) is often more efficient than using triangle lists because fewer vertices are duplicated.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1d8e-129">Требования</span><span class="sxs-lookup"><span data-stu-id="e1d8e-129">Requirements</span></span>



| <span data-ttu-id="e1d8e-130">Требование</span><span class="sxs-lookup"><span data-stu-id="e1d8e-130">Requirement</span></span> | <span data-ttu-id="e1d8e-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e1d8e-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d8e-132">Header</span><span class="sxs-lookup"><span data-stu-id="e1d8e-132">Header</span></span><br/> | <dl> <span data-ttu-id="e1d8e-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1d8e-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1d8e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1d8e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d8e-135">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="e1d8e-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="e1d8e-136">**IDirect3DDevice9::DrawIndexedPrimitive**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-136">**IDirect3DDevice9::DrawIndexedPrimitive**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)
</dt> <dt>

[<span data-ttu-id="e1d8e-137">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-137">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)
</dt> <dt>

[<span data-ttu-id="e1d8e-138">**IDirect3DDevice9::DrawPrimitive**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-138">**IDirect3DDevice9::DrawPrimitive**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)
</dt> <dt>

[<span data-ttu-id="e1d8e-139">**IDirect3DDevice9::DrawPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-139">**IDirect3DDevice9::DrawPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
</dt> </dl>

 

 
