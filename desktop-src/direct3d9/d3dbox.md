---
description: Определяет том.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: Структура D3DBOX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 882f6aadf0d49284b30132d4f08a9c583e5c9d73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273727"
---
# <a name="d3dbox-structure"></a><span data-ttu-id="56a3b-103">Структура D3DBOX</span><span class="sxs-lookup"><span data-stu-id="56a3b-103">D3DBOX structure</span></span>

<span data-ttu-id="56a3b-104">Определяет том.</span><span class="sxs-lookup"><span data-stu-id="56a3b-104">Defines a volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="56a3b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56a3b-105">Syntax</span></span>


```C++
typedef struct D3DBOX {
  UINT Left;
  UINT Top;
  UINT Right;
  UINT Bottom;
  UINT Front;
  UINT Back;
} D3DBOX, *LPD3DBOX;
```



## <a name="members"></a><span data-ttu-id="56a3b-106">Члены</span><span class="sxs-lookup"><span data-stu-id="56a3b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="56a3b-107">**Слева**</span><span class="sxs-lookup"><span data-stu-id="56a3b-107">**Left**</span></span>
</dt> <dd>

<span data-ttu-id="56a3b-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56a3b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="56a3b-109">Расположение левой стороны поля на оси x.</span><span class="sxs-lookup"><span data-stu-id="56a3b-109">Position of the left side of the box on the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="56a3b-110">**Top**</span><span class="sxs-lookup"><span data-stu-id="56a3b-110">**Top**</span></span>
</dt> <dd>

<span data-ttu-id="56a3b-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56a3b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="56a3b-112">Расположение верхней части бокса на оси y.</span><span class="sxs-lookup"><span data-stu-id="56a3b-112">Position of the top of the box on the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="56a3b-113">**Right**</span><span class="sxs-lookup"><span data-stu-id="56a3b-113">**Right**</span></span>
</dt> <dd>

<span data-ttu-id="56a3b-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56a3b-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="56a3b-115">Расположение правой части бокса на оси x.</span><span class="sxs-lookup"><span data-stu-id="56a3b-115">Position of the right side of the box on the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="56a3b-116">**Нижнее**</span><span class="sxs-lookup"><span data-stu-id="56a3b-116">**Bottom**</span></span>
</dt> <dd>

<span data-ttu-id="56a3b-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56a3b-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="56a3b-118">Расположение нижней части бокса на оси y.</span><span class="sxs-lookup"><span data-stu-id="56a3b-118">Position of the bottom of the box on the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="56a3b-119">**Front**</span><span class="sxs-lookup"><span data-stu-id="56a3b-119">**Front**</span></span>
</dt> <dd>

<span data-ttu-id="56a3b-120">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56a3b-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="56a3b-121">Расположение передней части бокса на оси z.</span><span class="sxs-lookup"><span data-stu-id="56a3b-121">Position of the front of the box on the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="56a3b-122">**Назад**</span><span class="sxs-lookup"><span data-stu-id="56a3b-122">**Back**</span></span>
</dt> <dd>

<span data-ttu-id="56a3b-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56a3b-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="56a3b-124">Расположение задней части поля на оси z.</span><span class="sxs-lookup"><span data-stu-id="56a3b-124">Position of the back of the box on the z-axis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56a3b-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56a3b-125">Remarks</span></span>

<span data-ttu-id="56a3b-126">**D3DBOX** включает в себя левый, верхний и передний края; Однако правый, нижний и задние края не включены.</span><span class="sxs-lookup"><span data-stu-id="56a3b-126">**D3DBOX** includes the left, top, and front edges; however, the right, bottom, and back edges are not included.</span></span> <span data-ttu-id="56a3b-127">Например, поле шириной в 100 единиц и начинается с 0 (таким образом, включая точки вплоть до 99) будет выражаться значением 0 для левого элемента и значением 100 для правого члена.</span><span class="sxs-lookup"><span data-stu-id="56a3b-127">For example, a box that is 100 units wide and begins at 0 (thus, including the points up to and including 99) would be expressed with a value of 0 for the Left member and a value of 100 for the Right member.</span></span> <span data-ttu-id="56a3b-128">Обратите внимание, что для правого члена не используется значение 99.</span><span class="sxs-lookup"><span data-stu-id="56a3b-128">Note that a value of 99 is not used for the Right member.</span></span>

<span data-ttu-id="56a3b-129">Для **D3DBOX** наблюдаются ограничения на сторону, расположенные слева направо, сверху вниз и с начала до конца.</span><span class="sxs-lookup"><span data-stu-id="56a3b-129">The restrictions on side ordering observed for **D3DBOX** are left to right, top to bottom, and front to back.</span></span>

## <a name="requirements"></a><span data-ttu-id="56a3b-130">Требования</span><span class="sxs-lookup"><span data-stu-id="56a3b-130">Requirements</span></span>



| <span data-ttu-id="56a3b-131">Требование</span><span class="sxs-lookup"><span data-stu-id="56a3b-131">Requirement</span></span> | <span data-ttu-id="56a3b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="56a3b-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56a3b-133">Header</span><span class="sxs-lookup"><span data-stu-id="56a3b-133">Header</span></span><br/> | <dl> <span data-ttu-id="56a3b-134"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="56a3b-134"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56a3b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56a3b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56a3b-136">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="56a3b-136">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
