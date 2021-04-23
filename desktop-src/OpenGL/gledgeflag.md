---
title: Функция Гледжефлаг (GL. h)
description: Помечает границы как границы или неграницы. | Функция Гледжефлаг (GL. h)
ms.assetid: cebaa4af-a3bc-4396-9ee0-8cc10bcaf256
keywords:
- Функция Гледжефлаг OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlag
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 599a0b539e32d0e457f92c256e2cb0b678b05b59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684850"
---
# <a name="gledgeflag-function"></a><span data-ttu-id="e959c-105">Функция Гледжефлаг</span><span class="sxs-lookup"><span data-stu-id="e959c-105">glEdgeFlag function</span></span>

<span data-ttu-id="e959c-106">Помечает границы как границы или неграницы.</span><span class="sxs-lookup"><span data-stu-id="e959c-106">Flags edges as either boundary or nonboundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="e959c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e959c-107">Syntax</span></span>


```C++
void WINAPI glEdgeFlag(
   GLboolean flag
);
```



## <a name="parameters"></a><span data-ttu-id="e959c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e959c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e959c-109">*flag*</span><span class="sxs-lookup"><span data-stu-id="e959c-109">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="e959c-110">Задает текущее значение флага ребра: **true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="e959c-110">Specifies the current edge flag value, either **TRUE** or **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e959c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e959c-111">Return value</span></span>

<span data-ttu-id="e959c-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e959c-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e959c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e959c-113">Remarks</span></span>

<span data-ttu-id="e959c-114">Каждая вершина многоугольника, отдельный треугольник или отдельный грани четырехсторонней, заданный между парой [**глбегин**](/windows/desktop/OpenGL/glbegin) / [**гленд**](/windows/desktop/OpenGL/glend) , помечается как начало границы или неграничного края.</span><span class="sxs-lookup"><span data-stu-id="e959c-114">Each vertex of a polygon, separate triangle, or separate quadrilateral specified between a [**glBegin**](/windows/desktop/OpenGL/glbegin)/[**glEnd**](/windows/desktop/OpenGL/glend) pair is marked as the start of either a boundary or nonboundary edge.</span></span> <span data-ttu-id="e959c-115">Если текущий флаг границы имеет **значение true** , если указана вершина, то вершина помечается как начало границ границы.</span><span class="sxs-lookup"><span data-stu-id="e959c-115">If the current edge flag is **TRUE** when the vertex is specified, the vertex is marked as the start of a boundary edge.</span></span> <span data-ttu-id="e959c-116">Если текущий флаг границы имеет **значение false**, вершина помечается как начало неграничного края.</span><span class="sxs-lookup"><span data-stu-id="e959c-116">If the current edge flag is **FALSE**, the vertex is marked as the start of a nonboundary edge.</span></span> <span data-ttu-id="e959c-117">Функция **гледжефлаг** устанавливает для флага ребра **значение true** , если флаг имеет ненулевое значение, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e959c-117">The **glEdgeFlag** function sets the edge flag to **TRUE** if flag is nonzero, **FALSE** otherwise.</span></span>

<span data-ttu-id="e959c-118">Вершины Соединенных треугольников и подключенных куадрилатералс всегда помечаются как границы, независимо от значения флага ребра.</span><span class="sxs-lookup"><span data-stu-id="e959c-118">The vertices of connected triangles and connected quadrilaterals are always marked as boundary, regardless of the value of the edge flag.</span></span>

<span data-ttu-id="e959c-119">Флаги граничных и неграничных краев в вершинах являются значимыми только в том случае, если \_ для режима многоугольника GL \_ задано значение «GL \_ » или « \_ линия GL».</span><span class="sxs-lookup"><span data-stu-id="e959c-119">Boundary and nonboundary edge flags on vertices are significant only if GL\_POLYGON\_MODE is set to GL\_POINT or GL\_LINE.</span></span> <span data-ttu-id="e959c-120">См. [**глполигонмоде**](/windows/desktop/OpenGL/glpolygonmode).</span><span class="sxs-lookup"><span data-stu-id="e959c-120">See [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span></span>

<span data-ttu-id="e959c-121">Изначально бит флага ребра имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="e959c-121">Initially, the edge flag bit is **TRUE**.</span></span>

<span data-ttu-id="e959c-122">Текущий флаг границы можно обновить в любое время.</span><span class="sxs-lookup"><span data-stu-id="e959c-122">The current edge flag can be updated at any time.</span></span> <span data-ttu-id="e959c-123">В частности, **гледжефлаг** можно вызывать между вызовом [**глбегин**](/windows/desktop/OpenGL/glbegin) и соответствующим вызовом [**гленд**](/windows/desktop/OpenGL/glend).</span><span class="sxs-lookup"><span data-stu-id="e959c-123">In particular, **glEdgeFlag** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](/windows/desktop/OpenGL/glend).</span></span>

<span data-ttu-id="e959c-124">Следующие функции извлекают сведения, относящиеся к **гледжефлаг**:</span><span class="sxs-lookup"><span data-stu-id="e959c-124">The following functions retrieve information related to **glEdgeFlag**:</span></span>

<span data-ttu-id="e959c-125">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ ребра \_</span><span class="sxs-lookup"><span data-stu-id="e959c-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG</span></span>

## <a name="requirements"></a><span data-ttu-id="e959c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e959c-126">Requirements</span></span>



| <span data-ttu-id="e959c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e959c-127">Requirement</span></span> | <span data-ttu-id="e959c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e959c-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e959c-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e959c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e959c-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e959c-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e959c-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e959c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e959c-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e959c-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e959c-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e959c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e959c-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e959c-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e959c-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e959c-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="e959c-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e959c-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e959c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e959c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e959c-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e959c-138"><dt>Opengl32.dll</dt></span></span> </dl> |



 

