---
title: Функция glVertex3s (GL. h)
description: Указывает вершину. | Функция glVertex3s (GL. h)
ms.assetid: ee970440-3eb3-46d6-80d2-e23649585510
keywords:
- Функция glVertex3s OpenGL
topic_type:
- apiref
api_name:
- glVertex3s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a167ded1510c0c5d9b430e59fb81b1625d5c199f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081797"
---
# <a name="glvertex3s-function"></a><span data-ttu-id="496f8-105">Функция glVertex3s</span><span class="sxs-lookup"><span data-stu-id="496f8-105">glVertex3s function</span></span>

<span data-ttu-id="496f8-106">Указывает вершину.</span><span class="sxs-lookup"><span data-stu-id="496f8-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="496f8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="496f8-107">Syntax</span></span>


```C++
void WINAPI glVertex3s(
   GLshort x,
   GLshort y,
   GLshort z
);
```



## <a name="parameters"></a><span data-ttu-id="496f8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="496f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="496f8-109">*x*</span><span class="sxs-lookup"><span data-stu-id="496f8-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="496f8-110">Задает координату x вершины.</span><span class="sxs-lookup"><span data-stu-id="496f8-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="496f8-111">*y*</span><span class="sxs-lookup"><span data-stu-id="496f8-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="496f8-112">Указывает координату y вершины.</span><span class="sxs-lookup"><span data-stu-id="496f8-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="496f8-113">*гармошкой*</span><span class="sxs-lookup"><span data-stu-id="496f8-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="496f8-114">Задает z-координату вершины.</span><span class="sxs-lookup"><span data-stu-id="496f8-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="496f8-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="496f8-115">Return value</span></span>

<span data-ttu-id="496f8-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="496f8-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="496f8-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="496f8-117">Remarks</span></span>

<span data-ttu-id="496f8-118">Команды функции глвертекс используются в парах [**глбегин**](glbegin.md) / [**гленд**](glend.md) для указания вершин, линий и многоугольников.</span><span class="sxs-lookup"><span data-stu-id="496f8-118">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="496f8-119">Текущие координаты цвета, нормали и текстуры связаны с вершиной при вызове Глвертекс.</span><span class="sxs-lookup"><span data-stu-id="496f8-119">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="496f8-120">Если указаны только значения *x* и *y* , по умолчанию для *z* используется значение 0,0, а для параметров *w* — 1,0.</span><span class="sxs-lookup"><span data-stu-id="496f8-120">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="496f8-121">При указании *x*, *y* и *z* значение *w* по умолчанию равно 1,0.</span><span class="sxs-lookup"><span data-stu-id="496f8-121">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="496f8-122">Вызов глвертекс за пределами пары **глбегин** / **гленд** приводит к неопределенному поведению.</span><span class="sxs-lookup"><span data-stu-id="496f8-122">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="496f8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="496f8-123">Requirements</span></span>



| <span data-ttu-id="496f8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="496f8-124">Requirement</span></span> | <span data-ttu-id="496f8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="496f8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="496f8-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="496f8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="496f8-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="496f8-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="496f8-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="496f8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="496f8-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="496f8-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="496f8-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="496f8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="496f8-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="496f8-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="496f8-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="496f8-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="496f8-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="496f8-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="496f8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="496f8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="496f8-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="496f8-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="496f8-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="496f8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="496f8-137">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="496f8-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="496f8-138">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="496f8-138">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="496f8-139">**глколор**</span><span class="sxs-lookup"><span data-stu-id="496f8-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="496f8-140">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="496f8-140">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="496f8-141">**гленд**</span><span class="sxs-lookup"><span data-stu-id="496f8-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="496f8-142">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="496f8-142">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="496f8-143">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="496f8-143">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="496f8-144">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="496f8-144">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="496f8-145">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="496f8-145">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="496f8-146">**глрект**</span><span class="sxs-lookup"><span data-stu-id="496f8-146">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="496f8-147">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="496f8-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





