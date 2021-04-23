---
description: Определяет размеры окон для целевой поверхности рендеринга, на которых проекты трехмерных томов.
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: Структура D3DVIEWPORT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVIEWPORT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3d96000de50934ebdc893ffc3866dd3252703bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713792"
---
# <a name="d3dviewport9-structure"></a><span data-ttu-id="82218-103">Структура D3DVIEWPORT9</span><span class="sxs-lookup"><span data-stu-id="82218-103">D3DVIEWPORT9 structure</span></span>

<span data-ttu-id="82218-104">Определяет размеры окон для целевой поверхности рендеринга, на которых проекты трехмерных томов.</span><span class="sxs-lookup"><span data-stu-id="82218-104">Defines the window dimensions of a render-target surface onto which a 3D volume projects.</span></span>

## <a name="syntax"></a><span data-ttu-id="82218-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82218-105">Syntax</span></span>


```C++
typedef struct D3DVIEWPORT9 {
  DWORD X;
  DWORD Y;
  DWORD Width;
  DWORD Height;
  float MinZ;
  float MaxZ;
} D3DVIEWPORT9, *LPD3DVIEWPORT9;
```



## <a name="members"></a><span data-ttu-id="82218-106">Члены</span><span class="sxs-lookup"><span data-stu-id="82218-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="82218-107">**X**</span><span class="sxs-lookup"><span data-stu-id="82218-107">**X**</span></span>
</dt> <dd>

<span data-ttu-id="82218-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82218-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82218-109">Пиксельная координата верхнего левого угла окна просмотра на поверхности целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="82218-109">Pixel coordinate of the upper-left corner of the viewport on the render-target surface.</span></span> <span data-ttu-id="82218-110">Если вы не хотите выполнять рендеринг в подмножестве поверхности, этот элемент может иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="82218-110">Unless you want to render to a subset of the surface, this member can be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="82218-111">**да**</span><span class="sxs-lookup"><span data-stu-id="82218-111">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="82218-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82218-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82218-113">Пиксельная координата верхнего левого угла окна просмотра на поверхности целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="82218-113">Pixel coordinate of the upper-left corner of the viewport on the render-target surface.</span></span> <span data-ttu-id="82218-114">Если вы не хотите выполнять рендеринг в подмножестве поверхности, этот элемент может иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="82218-114">Unless you want to render to a subset of the surface, this member can be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="82218-115">**Width**</span><span class="sxs-lookup"><span data-stu-id="82218-115">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="82218-116">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82218-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82218-117">Размерность объема обрезки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="82218-117">Width dimension of the clip volume, in pixels.</span></span> <span data-ttu-id="82218-118">Если только не выполняется отрисовка только в подмножестве поверхности, этому элементу должно быть присвоено значение ширины, равное поверхности целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="82218-118">Unless you are rendering only to a subset of the surface, this member should be set to the width dimension of the render-target surface.</span></span>

</dd> <dt>

<span data-ttu-id="82218-119">**Height**</span><span class="sxs-lookup"><span data-stu-id="82218-119">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="82218-120">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82218-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82218-121">Размерность изображения для тома обрезки (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="82218-121">Height dimension of the clip volume, in pixels.</span></span> <span data-ttu-id="82218-122">Если только не выполняется отрисовка только в подмножестве поверхности, этот элемент должен иметь размерность, равную высоте поверхности целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="82218-122">Unless you are rendering only to a subset of the surface, this member should be set to the height dimension of the render-target surface.</span></span>

</dd> <dt>

<span data-ttu-id="82218-123">**минз**</span><span class="sxs-lookup"><span data-stu-id="82218-123">**MinZ**</span></span>
</dt> <dd>

<span data-ttu-id="82218-124">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="82218-124">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="82218-125">Вместе с Максз, значение, описывающее диапазон значений глубины, в которых должна быть визуализирована сцена, минимальное и максимальное значения громкости клипа.</span><span class="sxs-lookup"><span data-stu-id="82218-125">Together with MaxZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume.</span></span> <span data-ttu-id="82218-126">Большинство приложений присвойте этому параметру значение 0,0.</span><span class="sxs-lookup"><span data-stu-id="82218-126">Most applications set this value to 0.0.</span></span> <span data-ttu-id="82218-127">Обрезка выполняется после применения матрицы проекции.</span><span class="sxs-lookup"><span data-stu-id="82218-127">Clipping is performed after applying the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="82218-128">**максз**</span><span class="sxs-lookup"><span data-stu-id="82218-128">**MaxZ**</span></span>
</dt> <dd>

<span data-ttu-id="82218-129">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="82218-129">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="82218-130">Вместе с Минз, значение, описывающее диапазон значений глубины, в которых должна быть визуализирована сцена, минимальное и максимальное значения громкости клипа.</span><span class="sxs-lookup"><span data-stu-id="82218-130">Together with MinZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume.</span></span> <span data-ttu-id="82218-131">Большинство приложений присвойте этому параметру значение 1,0.</span><span class="sxs-lookup"><span data-stu-id="82218-131">Most applications set this value to 1.0.</span></span> <span data-ttu-id="82218-132">Обрезка выполняется после применения матрицы проекции.</span><span class="sxs-lookup"><span data-stu-id="82218-132">Clipping is performed after applying the projection matrix.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82218-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82218-133">Remarks</span></span>

<span data-ttu-id="82218-134">Элементы X, Y, Width и Height описывают расположение и размеры окна просмотра на поверхности целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="82218-134">The X, Y, Width, and Height members describe the position and dimensions of the viewport on the render-target surface.</span></span> <span data-ttu-id="82218-135">Как правило, приложения подготавливаются ко всей целевой поверхности; при подготовке к просмотру на поверхности 640 x 480 эти элементы должны быть равны 0, 0, 640 и 480 соответственно.</span><span class="sxs-lookup"><span data-stu-id="82218-135">Usually, applications render to the entire target surface; when rendering on a 640 x 480 surface, these members should be 0, 0, 640, and 480, respectively.</span></span> <span data-ttu-id="82218-136">Для Минз и Максз обычно устанавливается значение 0,0 и 1,0, но для достижения конкретных эффектов можно задать другие значения.</span><span class="sxs-lookup"><span data-stu-id="82218-136">The MinZ and MaxZ are typically set to 0.0 and 1.0 but can be set to other values to achieve specific effects.</span></span> <span data-ttu-id="82218-137">Например, можно задать для них значение 0,0, чтобы заставить систему визуализировать объекты на передний план сцены или как 1,0 для принудительного применения объектов в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="82218-137">For example, you might set them both to 0.0 to force the system to render objects to the foreground of a scene, or both to 1.0 to force the objects into the background.</span></span>

<span data-ttu-id="82218-138">При изменении параметров окна просмотра устройства (из-за вызова метода [**сетвиевпорт**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) ) драйвер создает новую матрицу преобразования.</span><span class="sxs-lookup"><span data-stu-id="82218-138">When the viewport parameters for a device change (because of a call to the [**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) method), the driver builds a new transformation matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="82218-139">Требования</span><span class="sxs-lookup"><span data-stu-id="82218-139">Requirements</span></span>



| <span data-ttu-id="82218-140">Требование</span><span class="sxs-lookup"><span data-stu-id="82218-140">Requirement</span></span> | <span data-ttu-id="82218-141">Значение</span><span class="sxs-lookup"><span data-stu-id="82218-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82218-142">Header</span><span class="sxs-lookup"><span data-stu-id="82218-142">Header</span></span><br/> | <dl> <span data-ttu-id="82218-143"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="82218-143"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82218-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82218-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82218-145">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="82218-145">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="82218-146">**Окно просмотра**</span><span class="sxs-lookup"><span data-stu-id="82218-146">**GetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[<span data-ttu-id="82218-147">**сетвиевпорт**</span><span class="sxs-lookup"><span data-stu-id="82218-147">**SetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
