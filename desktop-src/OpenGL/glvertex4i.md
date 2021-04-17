---
title: Функция glVertex4i (GL. h)
description: Указывает вершину. | Функция glVertex4i (GL. h)
ms.assetid: eb73c5eb-c03d-489f-b323-bb2245d9b34c
keywords:
- Функция glVertex4i OpenGL
topic_type:
- apiref
api_name:
- glVertex4i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a354c5b1f386147a55bb94c5bcdacd862c1c41b2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684981"
---
# <a name="glvertex4i-function"></a><span data-ttu-id="50723-105">Функция glVertex4i</span><span class="sxs-lookup"><span data-stu-id="50723-105">glVertex4i function</span></span>

<span data-ttu-id="50723-106">Указывает вершину.</span><span class="sxs-lookup"><span data-stu-id="50723-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="50723-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50723-107">Syntax</span></span>


```C++
void WINAPI glVertex4i(
   GLint x,
   GLint y,
   GLint z,
   GLint w
);
```



## <a name="parameters"></a><span data-ttu-id="50723-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="50723-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50723-109">*x*</span><span class="sxs-lookup"><span data-stu-id="50723-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="50723-110">Задает координату x вершины.</span><span class="sxs-lookup"><span data-stu-id="50723-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="50723-111">*y*</span><span class="sxs-lookup"><span data-stu-id="50723-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="50723-112">Указывает координату y вершины.</span><span class="sxs-lookup"><span data-stu-id="50723-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="50723-113">*гармошкой*</span><span class="sxs-lookup"><span data-stu-id="50723-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="50723-114">Задает z-координату вершины.</span><span class="sxs-lookup"><span data-stu-id="50723-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="50723-115">*w*</span><span class="sxs-lookup"><span data-stu-id="50723-115">*w*</span></span> 
</dt> <dd>

<span data-ttu-id="50723-116">Задает w-координату вершины.</span><span class="sxs-lookup"><span data-stu-id="50723-116">Specifies the w-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50723-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50723-117">Return value</span></span>

<span data-ttu-id="50723-118">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="50723-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50723-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50723-119">Remarks</span></span>

<span data-ttu-id="50723-120">Команды функции глвертекс используются в парах [**глбегин**](glbegin.md) / [**гленд**](glend.md) для указания вершин, линий и многоугольников.</span><span class="sxs-lookup"><span data-stu-id="50723-120">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="50723-121">Текущие координаты цвета, нормали и текстуры связаны с вершиной при вызове Глвертекс.</span><span class="sxs-lookup"><span data-stu-id="50723-121">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="50723-122">Если указаны только значения *x* и *y* , по умолчанию для *z* используется значение 0,0, а для параметров *w* — 1,0.</span><span class="sxs-lookup"><span data-stu-id="50723-122">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="50723-123">При указании *x*, *y* и *z* значение *w* по умолчанию равно 1,0.</span><span class="sxs-lookup"><span data-stu-id="50723-123">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="50723-124">Вызов глвертекс за пределами пары **глбегин** / **гленд** приводит к неопределенному поведению.</span><span class="sxs-lookup"><span data-stu-id="50723-124">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="50723-125">Требования</span><span class="sxs-lookup"><span data-stu-id="50723-125">Requirements</span></span>



| <span data-ttu-id="50723-126">Требование</span><span class="sxs-lookup"><span data-stu-id="50723-126">Requirement</span></span> | <span data-ttu-id="50723-127">Значение</span><span class="sxs-lookup"><span data-stu-id="50723-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50723-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50723-128">Minimum supported client</span></span><br/> | <span data-ttu-id="50723-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50723-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="50723-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50723-130">Minimum supported server</span></span><br/> | <span data-ttu-id="50723-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50723-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="50723-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="50723-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="50723-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="50723-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="50723-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="50723-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="50723-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50723-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="50723-136">DLL</span><span class="sxs-lookup"><span data-stu-id="50723-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50723-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50723-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50723-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50723-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50723-139">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="50723-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="50723-140">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="50723-140">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="50723-141">**глколор**</span><span class="sxs-lookup"><span data-stu-id="50723-141">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="50723-142">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="50723-142">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="50723-143">**гленд**</span><span class="sxs-lookup"><span data-stu-id="50723-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="50723-144">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="50723-144">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="50723-145">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="50723-145">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="50723-146">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="50723-146">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="50723-147">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="50723-147">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="50723-148">**глрект**</span><span class="sxs-lookup"><span data-stu-id="50723-148">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="50723-149">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="50723-149">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





