---
description: Определяет константы, описывающие поддерживаемые режимы заливки.
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: Перечисление D3DSHADEMODE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSHADEMODE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9950e0074bef7a7b0c211177b3902cd69e2e112c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354540"
---
# <a name="d3dshademode-enumeration"></a><span data-ttu-id="592ba-103">Перечисление D3DSHADEMODE</span><span class="sxs-lookup"><span data-stu-id="592ba-103">D3DSHADEMODE enumeration</span></span>

<span data-ttu-id="592ba-104">Определяет константы, описывающие поддерживаемые режимы заливки.</span><span class="sxs-lookup"><span data-stu-id="592ba-104">Defines constants that describe the supported shading modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="592ba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="592ba-105">Syntax</span></span>


```C++
typedef enum D3DSHADEMODE { 
  D3DSHADE_FLAT         = 1,
  D3DSHADE_GOURAUD      = 2,
  D3DSHADE_PHONG        = 3,
  D3DSHADE_FORCE_DWORD  = 0x7fffffff
} D3DSHADEMODE, *LPD3DSHADEMODE;
```



## <a name="constants"></a><span data-ttu-id="592ba-106">Константы</span><span class="sxs-lookup"><span data-stu-id="592ba-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="592ba-107"><span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ бемоль**</span><span class="sxs-lookup"><span data-stu-id="592ba-107"><span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE\_FLAT**</span></span>
</dt> <dd>

<span data-ttu-id="592ba-108">Режим плоской заливки.</span><span class="sxs-lookup"><span data-stu-id="592ba-108">Flat shading mode.</span></span> <span data-ttu-id="592ba-109">Цвет и отражающий компонент первой вершины в треугольнике используются для определения цвета и отраженного компонента грани.</span><span class="sxs-lookup"><span data-stu-id="592ba-109">The color and specular component of the first vertex in the triangle are used to determine the color and specular component of the face.</span></span> <span data-ttu-id="592ba-110">Эти цвета остаются постоянными в пределах треугольника; то есть они не интерполируются.</span><span class="sxs-lookup"><span data-stu-id="592ba-110">These colors remain constant across the triangle; that is, they are not interpolated.</span></span> <span data-ttu-id="592ba-111">Отражающая альфа-составляющая интерполяция.</span><span class="sxs-lookup"><span data-stu-id="592ba-111">The specular alpha is interpolated.</span></span> <span data-ttu-id="592ba-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="592ba-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="592ba-113"><span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE метод \_ Гуро**</span><span class="sxs-lookup"><span data-stu-id="592ba-113"><span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE\_GOURAUD**</span></span>
</dt> <dd>

<span data-ttu-id="592ba-114">Режим заливки Гуро.</span><span class="sxs-lookup"><span data-stu-id="592ba-114">Gouraud shading mode.</span></span> <span data-ttu-id="592ba-115">Цвет и отражающие компоненты грани определяются линейной интерполяцией между всеми тремя вершинами треугольника.</span><span class="sxs-lookup"><span data-stu-id="592ba-115">The color and specular components of the face are determined by a linear interpolation between all three of the triangle's vertices.</span></span>

</dd> <dt>

<span data-ttu-id="592ba-116"><span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ по методу Фонга**</span><span class="sxs-lookup"><span data-stu-id="592ba-116"><span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE\_PHONG**</span></span>
</dt> <dd>

<span data-ttu-id="592ba-117">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="592ba-117">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="592ba-118"><span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="592ba-118"><span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="592ba-119">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="592ba-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="592ba-120">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="592ba-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="592ba-121">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="592ba-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="592ba-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="592ba-122">Remarks</span></span>

<span data-ttu-id="592ba-123">Первая вершина треугольника для режима плоской заливки определяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="592ba-123">The first vertex of a triangle for flat shading mode is defined in the following manner.</span></span>

-   <span data-ttu-id="592ba-124">Для списка треугольников первая вершина треугольника i имеет значение \* 3.</span><span class="sxs-lookup"><span data-stu-id="592ba-124">For a triangle list, the first vertex of the triangle i is i \* 3.</span></span>
-   <span data-ttu-id="592ba-125">Для полосы треугольника первая вершина треугольника i является вершиной i.</span><span class="sxs-lookup"><span data-stu-id="592ba-125">For a triangle strip, the first vertex of the triangle i is vertex i.</span></span>
-   <span data-ttu-id="592ba-126">Для вентилятора треугольника первая вершина треугольника i — вершина i + 1.</span><span class="sxs-lookup"><span data-stu-id="592ba-126">For a triangle fan, the first vertex of the triangle i is vertex i + 1.</span></span>

<span data-ttu-id="592ba-127">Члены этого перечислимого типа определяют а также корректируются для \_ состояния отрисовки D3DRS шадемоде.</span><span class="sxs-lookup"><span data-stu-id="592ba-127">The members of this enumerated type define the vales for the D3DRS\_SHADEMODE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="592ba-128">Требования</span><span class="sxs-lookup"><span data-stu-id="592ba-128">Requirements</span></span>



| <span data-ttu-id="592ba-129">Требование</span><span class="sxs-lookup"><span data-stu-id="592ba-129">Requirement</span></span> | <span data-ttu-id="592ba-130">Значение</span><span class="sxs-lookup"><span data-stu-id="592ba-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="592ba-131">Header</span><span class="sxs-lookup"><span data-stu-id="592ba-131">Header</span></span><br/> | <dl> <span data-ttu-id="592ba-132"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="592ba-132"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="592ba-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="592ba-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="592ba-134">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="592ba-134">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="592ba-135">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="592ba-135">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
