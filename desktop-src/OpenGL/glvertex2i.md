---
title: Функция glVertex2i (GL. h)
description: Указывает вершину. | Функция glVertex2i (GL. h)
ms.assetid: 13dc175b-9382-4266-962d-6dcf23ff5949
keywords:
- Функция glVertex2i OpenGL
topic_type:
- apiref
api_name:
- glVertex2i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f810083c61fbd04d1c61349d57e7abd72ab95a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684956"
---
# <a name="glvertex2i-function"></a><span data-ttu-id="3f22e-105">Функция glVertex2i</span><span class="sxs-lookup"><span data-stu-id="3f22e-105">glVertex2i function</span></span>

<span data-ttu-id="3f22e-106">Указывает вершину.</span><span class="sxs-lookup"><span data-stu-id="3f22e-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f22e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f22e-107">Syntax</span></span>


```C++
void WINAPI glVertex2i(
   GLint x,
   GLint y
);
```



## <a name="parameters"></a><span data-ttu-id="3f22e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f22e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f22e-109">*x*</span><span class="sxs-lookup"><span data-stu-id="3f22e-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="3f22e-110">Задает координату x вершины.</span><span class="sxs-lookup"><span data-stu-id="3f22e-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="3f22e-111">*y*</span><span class="sxs-lookup"><span data-stu-id="3f22e-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="3f22e-112">Указывает координату y вершины.</span><span class="sxs-lookup"><span data-stu-id="3f22e-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f22e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f22e-113">Return value</span></span>

<span data-ttu-id="3f22e-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3f22e-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f22e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f22e-115">Remarks</span></span>

<span data-ttu-id="3f22e-116">Команды функции глвертекс используются в парах [**глбегин**](glbegin.md) / [**гленд**](glend.md) для указания вершин, линий и многоугольников.</span><span class="sxs-lookup"><span data-stu-id="3f22e-116">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="3f22e-117">Текущие координаты цвета, нормали и текстуры связаны с вершиной при вызове Глвертекс.</span><span class="sxs-lookup"><span data-stu-id="3f22e-117">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="3f22e-118">Если указаны только значения *x* и *y* , по умолчанию для *z* используется значение 0,0, а для параметров *w* — 1,0.</span><span class="sxs-lookup"><span data-stu-id="3f22e-118">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="3f22e-119">При указании *x*, *y* и *z* значение *w* по умолчанию равно 1,0.</span><span class="sxs-lookup"><span data-stu-id="3f22e-119">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="3f22e-120">Вызов глвертекс за пределами пары **глбегин** / **гленд** приводит к неопределенному поведению.</span><span class="sxs-lookup"><span data-stu-id="3f22e-120">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f22e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="3f22e-121">Requirements</span></span>



| <span data-ttu-id="3f22e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="3f22e-122">Requirement</span></span> | <span data-ttu-id="3f22e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="3f22e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f22e-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f22e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3f22e-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3f22e-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3f22e-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f22e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3f22e-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3f22e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f22e-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3f22e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f22e-129"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f22e-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3f22e-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3f22e-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f22e-131"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f22e-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3f22e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3f22e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f22e-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f22e-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f22e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f22e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f22e-135">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="3f22e-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3f22e-136">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="3f22e-136">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="3f22e-137">**глколор**</span><span class="sxs-lookup"><span data-stu-id="3f22e-137">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="3f22e-138">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="3f22e-138">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="3f22e-139">**гленд**</span><span class="sxs-lookup"><span data-stu-id="3f22e-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3f22e-140">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="3f22e-140">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="3f22e-141">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="3f22e-141">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="3f22e-142">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="3f22e-142">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="3f22e-143">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="3f22e-143">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="3f22e-144">**глрект**</span><span class="sxs-lookup"><span data-stu-id="3f22e-144">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="3f22e-145">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="3f22e-145">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





