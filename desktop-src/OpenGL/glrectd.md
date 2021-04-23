---
title: Функция Глректд (GL. h)
description: Функция Глректд рисует прямоугольник.
ms.assetid: d5574c22-7ae1-4040-9b95-769693fa41e3
keywords:
- Функция Глректд OpenGL
topic_type:
- apiref
api_name:
- glRectd
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad37f2d21891ee47182b484741caabda906b20f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681764"
---
# <a name="glrectd-function"></a><span data-ttu-id="3380c-104">Функция Глректд</span><span class="sxs-lookup"><span data-stu-id="3380c-104">glRectd function</span></span>

<span data-ttu-id="3380c-105">Функция **глректд** рисует прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="3380c-105">The **glRectd** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="3380c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3380c-106">Syntax</span></span>


```C++
void WINAPI glRectd(
   GLdouble x1,
   GLdouble y1,
   GLdouble x2,
   GLdouble y2
);
```



## <a name="parameters"></a><span data-ttu-id="3380c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3380c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3380c-108">*x1*</span><span class="sxs-lookup"><span data-stu-id="3380c-108">*x1*</span></span> 
</dt> <dd>

<span data-ttu-id="3380c-109">Координата *x* вершины прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="3380c-109">The *x* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="3380c-110">*Y1*</span><span class="sxs-lookup"><span data-stu-id="3380c-110">*y1*</span></span> 
</dt> <dd>

<span data-ttu-id="3380c-111">Координата *y* вершины прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="3380c-111">The *y* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="3380c-112">*штук*</span><span class="sxs-lookup"><span data-stu-id="3380c-112">*x2*</span></span> 
</dt> <dd>

<span data-ttu-id="3380c-113">Координата *x* противоположной вершины прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="3380c-113">The *x* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="3380c-114">*Y2*</span><span class="sxs-lookup"><span data-stu-id="3380c-114">*y2*</span></span> 
</dt> <dd>

<span data-ttu-id="3380c-115">Координата *y* противоположной вершины прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="3380c-115">The *y* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3380c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3380c-116">Return value</span></span>

<span data-ttu-id="3380c-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3380c-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3380c-118">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3380c-118">Error codes</span></span>

<span data-ttu-id="3380c-119">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="3380c-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3380c-120">Имя</span><span class="sxs-lookup"><span data-stu-id="3380c-120">Name</span></span>                                                                                                  | <span data-ttu-id="3380c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3380c-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3380c-122"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="3380c-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3380c-123">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3380c-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3380c-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3380c-124">Remarks</span></span>

<span data-ttu-id="3380c-125">Функция **глректд** поддерживает эффективную спецификацию прямоугольников в двух угловых точках.</span><span class="sxs-lookup"><span data-stu-id="3380c-125">The **glRectd** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="3380c-126">Каждая команда Rectangle принимает четыре аргумента, организованные как две последовательные пары (*x*, *y*) или как два указателя на массивы, каждый из которых содержит пару (*x*, *y*).</span><span class="sxs-lookup"><span data-stu-id="3380c-126">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="3380c-127">Полученный прямоугольник определяется в плоскости *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="3380c-127">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="3380c-128">Функция **глректд**(*x1,* *Y1,* *x2,* *Y2*) в точности эквивалентна следующей последовательности:</span><span class="sxs-lookup"><span data-stu-id="3380c-128">The **glRectd**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="3380c-129">**глбегин**( \_ многоугольник GL);</span><span class="sxs-lookup"><span data-stu-id="3380c-129">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="3380c-130">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="3380c-130">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="3380c-131">**glVertex2**( *x2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="3380c-131">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="3380c-132">**glVertex2**( *x2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="3380c-132">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="3380c-133">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="3380c-133">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="3380c-134">**гленд**();</span><span class="sxs-lookup"><span data-stu-id="3380c-134">**glEnd**( );</span></span>

<span data-ttu-id="3380c-135">Обратите внимание, что если вторая вершина находится выше и правее первой вершины, прямоугольник создается с поворотом против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="3380c-135">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="3380c-136">Требования</span><span class="sxs-lookup"><span data-stu-id="3380c-136">Requirements</span></span>



| <span data-ttu-id="3380c-137">Требование</span><span class="sxs-lookup"><span data-stu-id="3380c-137">Requirement</span></span> | <span data-ttu-id="3380c-138">Значение</span><span class="sxs-lookup"><span data-stu-id="3380c-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3380c-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3380c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3380c-140">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3380c-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3380c-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3380c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3380c-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3380c-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3380c-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3380c-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="3380c-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3380c-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3380c-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3380c-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="3380c-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3380c-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3380c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="3380c-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3380c-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3380c-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3380c-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3380c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3380c-150">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="3380c-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3380c-151">**гленд**</span><span class="sxs-lookup"><span data-stu-id="3380c-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3380c-152">**глвертекс**</span><span class="sxs-lookup"><span data-stu-id="3380c-152">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





