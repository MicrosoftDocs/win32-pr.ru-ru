---
description: Описывает значения цвета.
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
ms.openlocfilehash: 1fe2f187921749207bbbf51d7fcfd75357a70858
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354410"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a><span data-ttu-id="9d139-103">Структура D3DCOLORVALUE (D3D9Types. h)</span><span class="sxs-lookup"><span data-stu-id="9d139-103">D3DCOLORVALUE structure (D3D9Types.h)</span></span>

<span data-ttu-id="9d139-104">Описывает значения цвета.</span><span class="sxs-lookup"><span data-stu-id="9d139-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d139-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d139-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="9d139-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9d139-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d139-107">**r**</span><span class="sxs-lookup"><span data-stu-id="9d139-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="9d139-108">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9d139-108">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="9d139-109">Значение с плавающей запятой, указывающее красный компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="9d139-109">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="9d139-110">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="9d139-110">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="9d139-111">Значение 0,0 указывает на полное отсутствие красного компонента, а значение 1,0 означает, что красный элемент полностью представлен.</span><span class="sxs-lookup"><span data-stu-id="9d139-111">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="9d139-112">**g**</span><span class="sxs-lookup"><span data-stu-id="9d139-112">**g**</span></span>
</dt> <dd>

<span data-ttu-id="9d139-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9d139-113">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="9d139-114">Значение с плавающей запятой, указывающее зеленый компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="9d139-114">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="9d139-115">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="9d139-115">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="9d139-116">Значение 0,0 указывает на полное отсутствие зеленого компонента, а значение 1,0 указывает на то, что зеленый объект имеется.</span><span class="sxs-lookup"><span data-stu-id="9d139-116">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="9d139-117">**b**</span><span class="sxs-lookup"><span data-stu-id="9d139-117">**b**</span></span>
</dt> <dd>

<span data-ttu-id="9d139-118">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9d139-118">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="9d139-119">Значение с плавающей запятой, указывающее синий компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="9d139-119">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="9d139-120">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="9d139-120">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="9d139-121">Значение 0,0 указывает на полное отсутствие синего компонента, а значение 1,0 указывает на то, что синий цвет имеется.</span><span class="sxs-lookup"><span data-stu-id="9d139-121">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="9d139-122">**конкретного**</span><span class="sxs-lookup"><span data-stu-id="9d139-122">**a**</span></span>
</dt> <dd>

<span data-ttu-id="9d139-123">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9d139-123">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="9d139-124">Значение с плавающей запятой, указывающее альфа-компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="9d139-124">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="9d139-125">Обычно это значение находится в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="9d139-125">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="9d139-126">Значение 0,0 означает полностью прозрачное, а значение 1,0 — полностью непрозрачный.</span><span class="sxs-lookup"><span data-stu-id="9d139-126">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d139-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d139-127">Remarks</span></span>

<span data-ttu-id="9d139-128">Членам этой структуры можно присвоить значения вне диапазона от 0 до 1, чтобы реализовать необычные эффекты.</span><span class="sxs-lookup"><span data-stu-id="9d139-128">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="9d139-129">Значения больше 1 создают сильные лампочки, которые обычно заменяют сцену.</span><span class="sxs-lookup"><span data-stu-id="9d139-129">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="9d139-130">Отрицательные значения создают темные огни, которые фактически удаляют свет из сцены.</span><span class="sxs-lookup"><span data-stu-id="9d139-130">Negative values produce dark lights that actually remove light from a scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d139-131">Требования</span><span class="sxs-lookup"><span data-stu-id="9d139-131">Requirements</span></span>



| <span data-ttu-id="9d139-132">Требование</span><span class="sxs-lookup"><span data-stu-id="9d139-132">Requirement</span></span> | <span data-ttu-id="9d139-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9d139-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d139-134">Header</span><span class="sxs-lookup"><span data-stu-id="9d139-134">Header</span></span><br/> | <dl> <span data-ttu-id="9d139-135"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d139-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d139-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d139-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d139-137">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="9d139-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




