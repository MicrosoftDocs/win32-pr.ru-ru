---
description: Описывает текущее состояние отсечения.
ms.assetid: 3ea8631c-a967-4d24-a49a-1751b3ee6077
title: Структура D3DCLIPSTATUS9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPSTATUS9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3b22fdfcc136c05ec8fe03ae491612606b2df62f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713575"
---
# <a name="d3dclipstatus9-structure"></a><span data-ttu-id="37532-103">Структура D3DCLIPSTATUS9</span><span class="sxs-lookup"><span data-stu-id="37532-103">D3DCLIPSTATUS9 structure</span></span>

<span data-ttu-id="37532-104">Описывает текущее состояние отсечения.</span><span class="sxs-lookup"><span data-stu-id="37532-104">Describes the current clip status.</span></span>

## <a name="syntax"></a><span data-ttu-id="37532-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37532-105">Syntax</span></span>


```C++
typedef struct D3DCLIPSTATUS9 {
  DWORD ClipUnion;
  DWORD ClipIntersection;
} D3DCLIPSTATUS9, *LPD3DCLIPSTATUS9;
```



## <a name="members"></a><span data-ttu-id="37532-106">Члены</span><span class="sxs-lookup"><span data-stu-id="37532-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="37532-107">**клипунион**</span><span class="sxs-lookup"><span data-stu-id="37532-107">**ClipUnion**</span></span>
</dt> <dd>

<span data-ttu-id="37532-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37532-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="37532-109">Флаги объединения клипов, описывающие текущее состояние отсечения.</span><span class="sxs-lookup"><span data-stu-id="37532-109">Clip union flags that describe the current clip status.</span></span> <span data-ttu-id="37532-110">Этот элемент может иметь один или несколько следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="37532-110">This member can be one or more of the following flags:</span></span>



| <span data-ttu-id="37532-111">Значение</span><span class="sxs-lookup"><span data-stu-id="37532-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="37532-112">Значение</span><span class="sxs-lookup"><span data-stu-id="37532-112">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <span data-ttu-id="37532-113"><dt>**D3DCS \_ все**</dt></span><span class="sxs-lookup"><span data-stu-id="37532-113"><dt>**D3DCS\_ALL**</dt></span></span> </dl>          | <span data-ttu-id="37532-114">Сочетание всех флагов клипа.</span><span class="sxs-lookup"><span data-stu-id="37532-114">Combination of all clip flags.</span></span><br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <span data-ttu-id="37532-115"><dt>**D3DCS \_ слева**</dt></span><span class="sxs-lookup"><span data-stu-id="37532-115"><dt>**D3DCS\_LEFT**</dt></span></span> </dl>       | <span data-ttu-id="37532-116">Все вершины обрезаются левой плоскостью просмотра фрустум.</span><span class="sxs-lookup"><span data-stu-id="37532-116">All vertices are clipped by the left plane of the viewing frustum.</span></span><br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <span data-ttu-id="37532-117"><dt>**D3DCS \_ вправо**</dt></span><span class="sxs-lookup"><span data-stu-id="37532-117"><dt>**D3DCS\_RIGHT**</dt></span></span> </dl>    | <span data-ttu-id="37532-118">Все вершины обрезаются правой плоскостью просмотра фрустум.</span><span class="sxs-lookup"><span data-stu-id="37532-118">All vertices are clipped by the right plane of the viewing frustum.</span></span><br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <span data-ttu-id="37532-119"><dt>**D3DCS \_ сверху**</dt></span><span class="sxs-lookup"><span data-stu-id="37532-119"><dt>**D3DCS\_TOP**</dt></span></span> </dl>          | <span data-ttu-id="37532-120">Все вершины обрезаются верхней плоскостью фрустум просмотра.</span><span class="sxs-lookup"><span data-stu-id="37532-120">All vertices are clipped by the top plane of the viewing frustum.</span></span><br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <span data-ttu-id="37532-121"><dt>**D3DCS \_ снизу**</dt></span><span class="sxs-lookup"><span data-stu-id="37532-121"><dt>**D3DCS\_BOTTOM**</dt></span></span> </dl> | <span data-ttu-id="37532-122">Все вершины обрезаются нижней плоскостью фрустум просмотра.</span><span class="sxs-lookup"><span data-stu-id="37532-122">All vertices are clipped by the bottom plane of the viewing frustum.</span></span><br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <span data-ttu-id="37532-123"><dt>**D3DCS \_ спереди**</dt></span><span class="sxs-lookup"><span data-stu-id="37532-123"><dt>**D3DCS\_FRONT**</dt></span></span> </dl>    | <span data-ttu-id="37532-124">Все вершины обрезаются передней плоскостью просмотра фрустум.</span><span class="sxs-lookup"><span data-stu-id="37532-124">All vertices are clipped by the front plane of the viewing frustum.</span></span><br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <span data-ttu-id="37532-125"><dt>**D3DCS \_ назад**</dt></span><span class="sxs-lookup"><span data-stu-id="37532-125"><dt>**D3DCS\_BACK**</dt></span></span> </dl>       | <span data-ttu-id="37532-126">Все вершины обрезаются на задней плоскости фрустум просмотра.</span><span class="sxs-lookup"><span data-stu-id="37532-126">All vertices are clipped by the back plane of the viewing frustum.</span></span><br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <span data-ttu-id="37532-127"><dt>**D3DCS \_ PLANE0**</dt></span><span class="sxs-lookup"><span data-stu-id="37532-127"><dt>**D3DCS\_PLANE0**</dt></span></span> </dl> | <span data-ttu-id="37532-128">Определяемые приложением отрезкиные плоскости.</span><span class="sxs-lookup"><span data-stu-id="37532-128">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <span data-ttu-id="37532-129"><dt>**D3DCS \_ PLANE1**</dt></span><span class="sxs-lookup"><span data-stu-id="37532-129"><dt>**D3DCS\_PLANE1**</dt></span></span> </dl> | <span data-ttu-id="37532-130">Определяемые приложением отрезкиные плоскости.</span><span class="sxs-lookup"><span data-stu-id="37532-130">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <span data-ttu-id="37532-131"><dt>**D3DCS \_ PLANE2**</dt></span><span class="sxs-lookup"><span data-stu-id="37532-131"><dt>**D3DCS\_PLANE2**</dt></span></span> </dl> | <span data-ttu-id="37532-132">Определяемые приложением отрезкиные плоскости.</span><span class="sxs-lookup"><span data-stu-id="37532-132">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <span data-ttu-id="37532-133"><dt>**D3DCS \_ PLANE3**</dt></span><span class="sxs-lookup"><span data-stu-id="37532-133"><dt>**D3DCS\_PLANE3**</dt></span></span> </dl> | <span data-ttu-id="37532-134">Определяемые приложением отрезкиные плоскости.</span><span class="sxs-lookup"><span data-stu-id="37532-134">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <span data-ttu-id="37532-135"><dt>**D3DCS \_ PLANE4**</dt></span><span class="sxs-lookup"><span data-stu-id="37532-135"><dt>**D3DCS\_PLANE4**</dt></span></span> </dl> | <span data-ttu-id="37532-136">Определяемые приложением отрезкиные плоскости.</span><span class="sxs-lookup"><span data-stu-id="37532-136">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <span data-ttu-id="37532-137"><dt>**D3DCS \_ PLANE5**</dt></span><span class="sxs-lookup"><span data-stu-id="37532-137"><dt>**D3DCS\_PLANE5**</dt></span></span> </dl> | <span data-ttu-id="37532-138">Определяемые приложением отрезкиные плоскости.</span><span class="sxs-lookup"><span data-stu-id="37532-138">Application-defined clipping planes.</span></span><br/>                                 |



 

</dd> <dt>

<span data-ttu-id="37532-139">**клипинтерсектион**</span><span class="sxs-lookup"><span data-stu-id="37532-139">**ClipIntersection**</span></span>
</dt> <dd>

<span data-ttu-id="37532-140">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37532-140">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="37532-141">Флаги пересечения фрагментов клипов, описывающие текущее состояние отсечения.</span><span class="sxs-lookup"><span data-stu-id="37532-141">Clip intersection flags that describe the current clip status.</span></span> <span data-ttu-id="37532-142">Этот элемент может принимать те же флаги, что и Клипунион.</span><span class="sxs-lookup"><span data-stu-id="37532-142">This member can take the same flags as ClipUnion.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37532-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37532-143">Remarks</span></span>

<span data-ttu-id="37532-144">При включении обрезки во время обработки вершин (с помощью [**процессвертицес**](/windows/desktop/api), [**дравпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)или других функций рисования) Direct3D вычислит код обрезки для каждой вершины.</span><span class="sxs-lookup"><span data-stu-id="37532-144">When clipping is enabled during vertex processing (by [**ProcessVertices**](/windows/desktop/api), [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), or other drawing functions), Direct3D computes a clip code for every vertex.</span></span> <span data-ttu-id="37532-145">Фрагмент кода обрезки представляет собой сочетание \_ \* битов D3DCS.</span><span class="sxs-lookup"><span data-stu-id="37532-145">The clip code is a combination of D3DCS\_\* bits.</span></span> <span data-ttu-id="37532-146">Если вершина находится за пределами определенной плоскости обрезки, соответствующий бит задается в коде обрезки.</span><span class="sxs-lookup"><span data-stu-id="37532-146">When a vertex is outside a particular clipping plane, the corresponding bit is set in the clipping code.</span></span> <span data-ttu-id="37532-147">Direct3D поддерживает состояние отсечения с помощью **D3DCLIPSTATUS9**, который содержит элементы Клипунион и клипинтерсектион.</span><span class="sxs-lookup"><span data-stu-id="37532-147">Direct3D maintains the clip status using **D3DCLIPSTATUS9**, which has ClipUnion and ClipIntersection members.</span></span> <span data-ttu-id="37532-148">Клипунион — это побитовое или из всех кодов зажимов вершин, а Клипинтерсектион — это побитовое и из всех кодов фрагментов вершин.</span><span class="sxs-lookup"><span data-stu-id="37532-148">ClipUnion is a bitwise OR of all vertex clip codes and ClipIntersection is a bitwise AND of all vertex clip codes.</span></span> <span data-ttu-id="37532-149">Начальные значения для Клипунион и 0xFFFFFFFF для Клипинтерсектион равны нулю.</span><span class="sxs-lookup"><span data-stu-id="37532-149">Initial values are zero for ClipUnion and 0xFFFFFFFF for ClipIntersection.</span></span> <span data-ttu-id="37532-150">Если \_ для D3DRS обрезки задано **значение false**, то для клипунион и клипинтерсектион устанавливается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="37532-150">When D3DRS\_CLIPPING is set to **FALSE**, ClipUnion and ClipIntersection are set to zero.</span></span> <span data-ttu-id="37532-151">Direct3D обновляет состояние отсечения во время вызовов рисования.</span><span class="sxs-lookup"><span data-stu-id="37532-151">Direct3D updates the clip status during drawing calls.</span></span> <span data-ttu-id="37532-152">Чтобы вычислить состояние отсечения для определенного объекта, задайте для Клипунион и Клипинтерсектион начальное значение и продолжайте рисование.</span><span class="sxs-lookup"><span data-stu-id="37532-152">To compute clip status for a particular object, set ClipUnion and ClipIntersection to their initial value and continue drawing.</span></span>

<span data-ttu-id="37532-153">Состояние обрезки не обновляется [**дравректпатч**](/windows/desktop/api) и [**дравтрипатч**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) , так как для них отсутствует Эмуляция программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="37532-153">Clip status is not updated by [**DrawRectPatch**](/windows/desktop/api) and [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) because there is no software emulation for them.</span></span>

## <a name="requirements"></a><span data-ttu-id="37532-154">Требования</span><span class="sxs-lookup"><span data-stu-id="37532-154">Requirements</span></span>



| <span data-ttu-id="37532-155">Требование</span><span class="sxs-lookup"><span data-stu-id="37532-155">Requirement</span></span> | <span data-ttu-id="37532-156">Значение</span><span class="sxs-lookup"><span data-stu-id="37532-156">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37532-157">Header</span><span class="sxs-lookup"><span data-stu-id="37532-157">Header</span></span><br/> | <dl> <span data-ttu-id="37532-158"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="37532-158"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37532-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37532-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37532-160">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="37532-160">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="37532-161">**жетклипстатус**</span><span class="sxs-lookup"><span data-stu-id="37532-161">**GetClipStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[<span data-ttu-id="37532-162">**сетклипстатус**</span><span class="sxs-lookup"><span data-stu-id="37532-162">**SetClipStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
