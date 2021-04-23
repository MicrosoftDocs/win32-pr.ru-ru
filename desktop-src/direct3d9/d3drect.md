---
description: Определяет прямоугольник.
ms.assetid: a8590411-fd34-4048-a41f-b4155d955573
title: Структура D3DRECT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9a22b74869afa16ca0c55ac50975eb36ba590c7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821156"
---
# <a name="d3drect-structure"></a><span data-ttu-id="ddaae-103">Структура D3DRECT</span><span class="sxs-lookup"><span data-stu-id="ddaae-103">D3DRECT structure</span></span>

<span data-ttu-id="ddaae-104">Определяет прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="ddaae-104">Defines a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddaae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ddaae-105">Syntax</span></span>


```C++
typedef struct D3DRECT {
  LONG x1;
  LONG y1;
  LONG x2;
  LONG y2;
} D3DRECT;
```



## <a name="members"></a><span data-ttu-id="ddaae-106">Члены</span><span class="sxs-lookup"><span data-stu-id="ddaae-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ddaae-107">**x1**</span><span class="sxs-lookup"><span data-stu-id="ddaae-107">**x1**</span></span>
</dt> <dd>

<span data-ttu-id="ddaae-108">Тип: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ddaae-108">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ddaae-109">Координата по оси X верхнего левого угла прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="ddaae-109">The x-coordinate of the upper-left corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="ddaae-110">**Y1**</span><span class="sxs-lookup"><span data-stu-id="ddaae-110">**y1**</span></span>
</dt> <dd>

<span data-ttu-id="ddaae-111">Тип: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ddaae-111">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ddaae-112">Координата по оси Y верхнего левого угла прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="ddaae-112">The y-coordinate of the upper-left corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="ddaae-113">**штук**</span><span class="sxs-lookup"><span data-stu-id="ddaae-113">**x2**</span></span>
</dt> <dd>

<span data-ttu-id="ddaae-114">Тип: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ddaae-114">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ddaae-115">Координата по оси x правого нижнего угла прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="ddaae-115">The x-coordinate of the lower-right corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="ddaae-116">**Y2**</span><span class="sxs-lookup"><span data-stu-id="ddaae-116">**y2**</span></span>
</dt> <dd>

<span data-ttu-id="ddaae-117">Тип: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ddaae-117">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ddaae-118">Координата по оси y правого нижнего угла прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="ddaae-118">The y-coordinate of the lower-right corner of the rectangle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ddaae-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ddaae-119">Requirements</span></span>



| <span data-ttu-id="ddaae-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ddaae-120">Requirement</span></span> | <span data-ttu-id="ddaae-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ddaae-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddaae-122">Header</span><span class="sxs-lookup"><span data-stu-id="ddaae-122">Header</span></span><br/> | <dl> <span data-ttu-id="ddaae-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddaae-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddaae-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddaae-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddaae-125">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="ddaae-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="ddaae-126">**Открытым**</span><span class="sxs-lookup"><span data-stu-id="ddaae-126">**Clear**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 
