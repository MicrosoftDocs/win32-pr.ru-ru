---
title: Функция glVertex4dv (GL. h)
description: Указывает вершину. | Функция glVertex4dv (GL. h)
ms.assetid: af0a3c69-0d71-4cbb-9494-561033d99ac1
keywords:
- Функция glVertex4dv OpenGL
topic_type:
- apiref
api_name:
- glVertex4dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 532a71c576ca0b49dd645afe8b501f0e718a827b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684880"
---
# <a name="glvertex4dv-function"></a><span data-ttu-id="bd273-105">Функция glVertex4dv</span><span class="sxs-lookup"><span data-stu-id="bd273-105">glVertex4dv function</span></span>

<span data-ttu-id="bd273-106">Указывает вершину.</span><span class="sxs-lookup"><span data-stu-id="bd273-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd273-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd273-107">Syntax</span></span>


```C++
void WINAPI glVertex4dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="bd273-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd273-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd273-109">*3,3*</span><span class="sxs-lookup"><span data-stu-id="bd273-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="bd273-110">Указатель на массив из четырех элементов.</span><span class="sxs-lookup"><span data-stu-id="bd273-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="bd273-111">Элементы — это координаты x, y, z и w вершины.</span><span class="sxs-lookup"><span data-stu-id="bd273-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd273-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd273-112">Return value</span></span>

<span data-ttu-id="bd273-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bd273-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd273-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bd273-114">Requirements</span></span>



| <span data-ttu-id="bd273-115">Требование</span><span class="sxs-lookup"><span data-stu-id="bd273-115">Requirement</span></span> | <span data-ttu-id="bd273-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bd273-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd273-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd273-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bd273-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bd273-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bd273-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd273-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bd273-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bd273-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd273-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bd273-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd273-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd273-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bd273-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bd273-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="bd273-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd273-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bd273-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bd273-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd273-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd273-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd273-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd273-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd273-128">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="bd273-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bd273-129">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="bd273-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="bd273-130">**глколор**</span><span class="sxs-lookup"><span data-stu-id="bd273-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="bd273-131">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="bd273-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="bd273-132">**гленд**</span><span class="sxs-lookup"><span data-stu-id="bd273-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bd273-133">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="bd273-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="bd273-134">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="bd273-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="bd273-135">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="bd273-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="bd273-136">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="bd273-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="bd273-137">**глрект**</span><span class="sxs-lookup"><span data-stu-id="bd273-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="bd273-138">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="bd273-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





