---
title: Функция Глутесснормал (GLU. h)
description: Функция Глутесснормал задает значение нормали для многоугольника.
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- Функция Глутесснормал OpenGL
topic_type:
- apiref
api_name:
- gluTessNormal
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af04ab2364fafcea709ca36cab2f10a8bea1a96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989262"
---
# <a name="glutessnormal-function"></a><span data-ttu-id="9a2f1-104">Функция Глутесснормал</span><span class="sxs-lookup"><span data-stu-id="9a2f1-104">gluTessNormal function</span></span>

<span data-ttu-id="9a2f1-105">Функция **глутесснормал** задает значение нормали для многоугольника.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-105">The **gluTessNormal** function specifies a normal for a polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a2f1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a2f1-106">Syntax</span></span>


```C++
void WINAPI gluTessNormal(
   GLUtesselator *tess,
   GLdouble      x,
   GLdouble      y,
   GLdouble      z
);
```



## <a name="parameters"></a><span data-ttu-id="9a2f1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a2f1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a2f1-108">*тесс*</span><span class="sxs-lookup"><span data-stu-id="9a2f1-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="9a2f1-109">Объект тесселяции (созданный с помощью [**глуневтесс**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="9a2f1-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9a2f1-110">*x*</span><span class="sxs-lookup"><span data-stu-id="9a2f1-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="9a2f1-111">Компонент координат x нормали.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-111">The x-coordinate component of a normal.</span></span>

</dd> <dt>

<span data-ttu-id="9a2f1-112">*y*</span><span class="sxs-lookup"><span data-stu-id="9a2f1-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="9a2f1-113">Компонент координат y обычного.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-113">The y-coordinate component of a normal.</span></span>

</dd> <dt>

<span data-ttu-id="9a2f1-114">*гармошкой*</span><span class="sxs-lookup"><span data-stu-id="9a2f1-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="9a2f1-115">Компонент z-координаты нормали.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-115">The z-coordinate component of a normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a2f1-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a2f1-116">Return value</span></span>

<span data-ttu-id="9a2f1-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a2f1-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a2f1-118">Remarks</span></span>

<span data-ttu-id="9a2f1-119">Функция **глутесснормал** описывает нормальную работу с определенным многоугольником.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-119">The **gluTessNormal** function describes a normal for a polygon that you define.</span></span> <span data-ttu-id="9a2f1-120">Все входные данные проецируются на плоскость, перпендикулярную одной из трех осей координат, перед тесселяцией, а все выходные треугольники ориентированы против часовой стрелки относительно обычного.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-120">All input data is projected onto a plane perpendicular to one of the three coordinate axes before tessellation, and all output triangles are oriented counterclockwise with respect to the normal.</span></span> <span data-ttu-id="9a2f1-121">(Чтобы получить ориентацию по часовой стрелке, измените знак предоставленного нормального режима на обратный.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-121">(To obtain clockwise orientation, reverse the sign of the supplied normal).</span></span> <span data-ttu-id="9a2f1-122">Например, если известно, что все многоугольники находятся в плоскости x-y, вызовите **глутесснормал**(тесс, 0,0, 0,0, 1,0) перед отрисовкой многоугольников.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-122">For example, if you know that all polygons lie in the x-y plane, call **gluTessNormal**(tess, 0.0, 0.0, 1.0) before rendering any polygons.</span></span>

<span data-ttu-id="9a2f1-123">Если в качестве нормального значения используется (0,0, 0,0, 0,0) (значение по умолчанию), то нормальная ситуация определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9a2f1-123">If the supplied normal is (0.0, 0.0, 0.0) (the default value), the normal is determined as follows:</span></span>

1.  <span data-ttu-id="9a2f1-124">Направление нормальной работы до его знака найдется путем подгонки плоскости к вершинам без учета того, как будут соединены вершины.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-124">The direction of the normal, up to its sign, is found by fitting a plane to the vertexes, without regard to how the vertexes are connected.</span></span> <span data-ttu-id="9a2f1-125">Ожидается, что входные данные полагаются на плоскость примерно в плоскости; в противном случае проекция, перпендикулярная одной из трех осей координат, может существенно изменить геометрию.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-125">It is expected that the input data lies approximately in the plane; otherwise projection perpendicular to one of the three coordinate axes can change the geometry substantially.</span></span>
2.  <span data-ttu-id="9a2f1-126">Знак нормали выбирается таким образом, что сумма всех подписанных областей всех входных данных не отрицательна (где профиль с против часовой стрелки имеет положительную область).</span><span class="sxs-lookup"><span data-stu-id="9a2f1-126">The sign of the normal is chosen so that the sum of the signed areas of all input contours is nonnegative (where a counterclockwise contour has positive area).</span></span>

<span data-ttu-id="9a2f1-127">Заданная нормальная ситуация сохраняется до тех пор, пока другой вызов **глутесснормал** не изменит его.</span><span class="sxs-lookup"><span data-stu-id="9a2f1-127">The supplied normal persists until another call to **gluTessNormal** changes it.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a2f1-128">Требования</span><span class="sxs-lookup"><span data-stu-id="9a2f1-128">Requirements</span></span>



| <span data-ttu-id="9a2f1-129">Требование</span><span class="sxs-lookup"><span data-stu-id="9a2f1-129">Requirement</span></span> | <span data-ttu-id="9a2f1-130">Значение</span><span class="sxs-lookup"><span data-stu-id="9a2f1-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9a2f1-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a2f1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9a2f1-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9a2f1-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9a2f1-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a2f1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9a2f1-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9a2f1-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9a2f1-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9a2f1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a2f1-136"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a2f1-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9a2f1-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9a2f1-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a2f1-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a2f1-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9a2f1-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9a2f1-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a2f1-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a2f1-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a2f1-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a2f1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a2f1-142">**глуневтесс**</span><span class="sxs-lookup"><span data-stu-id="9a2f1-142">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="9a2f1-143">**глутессбегинполигон**</span><span class="sxs-lookup"><span data-stu-id="9a2f1-143">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="9a2f1-144">**глутессендполигон**</span><span class="sxs-lookup"><span data-stu-id="9a2f1-144">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> </dl>

 

 





