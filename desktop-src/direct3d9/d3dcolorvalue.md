---
description: Структура D3DCOLORVALUE (D3D9Types. h) — описывает значения цвета.
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: Структура D3DCOLORVALUE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c9b55fbf718382e9dca7e3999cce0cabe895a261
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116062"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a><span data-ttu-id="9d58f-103">Структура D3DCOLORVALUE (D3D9Types. h)</span><span class="sxs-lookup"><span data-stu-id="9d58f-103">D3DCOLORVALUE structure (D3D9Types.h)</span></span>

<span data-ttu-id="9d58f-104">Описывает значения цвета.</span><span class="sxs-lookup"><span data-stu-id="9d58f-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d58f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d58f-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="9d58f-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9d58f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d58f-107">**r**</span><span class="sxs-lookup"><span data-stu-id="9d58f-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="9d58f-108">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9d58f-108">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="9d58f-109">Значение с плавающей запятой, указывающее красный компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="9d58f-109">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="9d58f-110">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="9d58f-110">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="9d58f-111">Значение 0,0 указывает на полное отсутствие красного компонента, а значение 1,0 означает, что красный элемент полностью представлен.</span><span class="sxs-lookup"><span data-stu-id="9d58f-111">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="9d58f-112">**g**</span><span class="sxs-lookup"><span data-stu-id="9d58f-112">**g**</span></span>
</dt> <dd>

<span data-ttu-id="9d58f-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9d58f-113">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="9d58f-114">Значение с плавающей запятой, указывающее зеленый компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="9d58f-114">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="9d58f-115">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="9d58f-115">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="9d58f-116">Значение 0,0 указывает на полное отсутствие зеленого компонента, а значение 1,0 указывает на то, что зеленый объект имеется.</span><span class="sxs-lookup"><span data-stu-id="9d58f-116">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="9d58f-117">**b**</span><span class="sxs-lookup"><span data-stu-id="9d58f-117">**b**</span></span>
</dt> <dd>

<span data-ttu-id="9d58f-118">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9d58f-118">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="9d58f-119">Значение с плавающей запятой, указывающее синий компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="9d58f-119">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="9d58f-120">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="9d58f-120">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="9d58f-121">Значение 0,0 указывает на полное отсутствие синего компонента, а значение 1,0 указывает на то, что синий цвет имеется.</span><span class="sxs-lookup"><span data-stu-id="9d58f-121">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="9d58f-122">**конкретного**</span><span class="sxs-lookup"><span data-stu-id="9d58f-122">**a**</span></span>
</dt> <dd>

<span data-ttu-id="9d58f-123">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9d58f-123">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="9d58f-124">Значение с плавающей запятой, указывающее альфа-компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="9d58f-124">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="9d58f-125">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="9d58f-125">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="9d58f-126">Значение 0,0 означает полностью прозрачное, а значение 1,0 — полностью непрозрачный.</span><span class="sxs-lookup"><span data-stu-id="9d58f-126">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d58f-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="9d58f-127">Remarks</span></span>

<span data-ttu-id="9d58f-128">Членам этой структуры можно присвоить значения вне диапазона от 0 до 1, чтобы реализовать необычные эффекты.</span><span class="sxs-lookup"><span data-stu-id="9d58f-128">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="9d58f-129">Значения больше 1 создают сильные лампочки, которые обычно заменяют сцену.</span><span class="sxs-lookup"><span data-stu-id="9d58f-129">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="9d58f-130">Отрицательные значения создают темные огни, которые фактически удаляют свет из сцены.</span><span class="sxs-lookup"><span data-stu-id="9d58f-130">Negative values produce dark lights that actually remove light from a scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d58f-131">Требования</span><span class="sxs-lookup"><span data-stu-id="9d58f-131">Requirements</span></span>



| <span data-ttu-id="9d58f-132">Требование</span><span class="sxs-lookup"><span data-stu-id="9d58f-132">Requirement</span></span> | <span data-ttu-id="9d58f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9d58f-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d58f-134">Header</span><span class="sxs-lookup"><span data-stu-id="9d58f-134">Header</span></span><br/> | <dl> <span data-ttu-id="9d58f-135"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d58f-136">См. также</span><span class="sxs-lookup"><span data-stu-id="9d58f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d58f-137">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="9d58f-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




