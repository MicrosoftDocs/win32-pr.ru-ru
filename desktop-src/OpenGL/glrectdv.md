---
title: Функция Глректдв (GL. h)
description: Функция Глректдв рисует прямоугольник.
ms.assetid: 53000734-bfc3-42c3-aa80-0a54e3dd36ec
keywords:
- Функция Глректдв OpenGL
topic_type:
- apiref
api_name:
- glRectdv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2956a1f658101a384ae69b05ed50418492d264
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414784"
---
# <a name="glrectdv-function"></a><span data-ttu-id="3b619-104">Функция Глректдв</span><span class="sxs-lookup"><span data-stu-id="3b619-104">glRectdv function</span></span>

<span data-ttu-id="3b619-105">Функция **глректдв** рисует прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="3b619-105">The **glRectdv** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b619-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b619-106">Syntax</span></span>


```C++
void WINAPI glRectdv(
   const GLdouble *v1,
   const GLdouble *v2
);
```



## <a name="parameters"></a><span data-ttu-id="3b619-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b619-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b619-108">*Версия 1*</span><span class="sxs-lookup"><span data-stu-id="3b619-108">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="3b619-109">Указатель на одну вершину прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="3b619-109">A pointer to one vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="3b619-110">*Версия 2*</span><span class="sxs-lookup"><span data-stu-id="3b619-110">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="3b619-111">Указатель на противоположную вершину прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="3b619-111">a pointer to the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b619-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b619-112">Return value</span></span>

<span data-ttu-id="3b619-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3b619-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3b619-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3b619-114">Error codes</span></span>

<span data-ttu-id="3b619-115">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="3b619-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3b619-116">Имя</span><span class="sxs-lookup"><span data-stu-id="3b619-116">Name</span></span>                                                                                                  | <span data-ttu-id="3b619-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3b619-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3b619-118"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="3b619-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3b619-119">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3b619-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3b619-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b619-120">Remarks</span></span>

<span data-ttu-id="3b619-121">Функция **глректд** поддерживает эффективную спецификацию прямоугольников в двух угловых точках.</span><span class="sxs-lookup"><span data-stu-id="3b619-121">The **glRectd** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="3b619-122">Каждая команда Rectangle принимает четыре аргумента, организованные как две последовательные пары (*x*, *y*) или как два указателя на массивы, каждый из которых содержит пару (*x*, *y*).</span><span class="sxs-lookup"><span data-stu-id="3b619-122">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="3b619-123">Полученный прямоугольник определяется в плоскости *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="3b619-123">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="3b619-124">Функция **глректд**(*x1,* *Y1,* *x2,* *Y2*) в точности эквивалентна следующей последовательности:</span><span class="sxs-lookup"><span data-stu-id="3b619-124">The **glRectd**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="3b619-125">**глбегин**( \_ многоугольник GL);</span><span class="sxs-lookup"><span data-stu-id="3b619-125">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="3b619-126">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="3b619-126">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="3b619-127">**glVertex2**( *x2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="3b619-127">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="3b619-128">**glVertex2**( *x2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="3b619-128">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="3b619-129">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="3b619-129">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="3b619-130">**гленд**();</span><span class="sxs-lookup"><span data-stu-id="3b619-130">**glEnd**( );</span></span>

<span data-ttu-id="3b619-131">Обратите внимание, что если вторая вершина находится выше и правее первой вершины, прямоугольник создается с поворотом против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="3b619-131">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b619-132">Требования</span><span class="sxs-lookup"><span data-stu-id="3b619-132">Requirements</span></span>



| <span data-ttu-id="3b619-133">Требование</span><span class="sxs-lookup"><span data-stu-id="3b619-133">Requirement</span></span> | <span data-ttu-id="3b619-134">Значение</span><span class="sxs-lookup"><span data-stu-id="3b619-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b619-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b619-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3b619-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b619-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3b619-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b619-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3b619-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b619-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3b619-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3b619-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b619-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b619-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3b619-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3b619-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b619-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b619-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3b619-143">DLL</span><span class="sxs-lookup"><span data-stu-id="3b619-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b619-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b619-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b619-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b619-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b619-146">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="3b619-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3b619-147">**гленд**</span><span class="sxs-lookup"><span data-stu-id="3b619-147">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3b619-148">**глвертекс**</span><span class="sxs-lookup"><span data-stu-id="3b619-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





