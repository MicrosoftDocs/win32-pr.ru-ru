---
title: Функция glVertex4fv (GL. h)
description: Указывает вершину. | Функция glVertex4fv (GL. h)
ms.assetid: c2a766fd-3ad8-463b-8f09-36d0673e6716
keywords:
- Функция glVertex4fv OpenGL
topic_type:
- apiref
api_name:
- glVertex4fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e05551268b697ba4444c29d5f2b9bdfb0e832e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684879"
---
# <a name="glvertex4fv-function"></a><span data-ttu-id="4b958-105">Функция glVertex4fv</span><span class="sxs-lookup"><span data-stu-id="4b958-105">glVertex4fv function</span></span>

<span data-ttu-id="4b958-106">Указывает вершину.</span><span class="sxs-lookup"><span data-stu-id="4b958-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b958-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b958-107">Syntax</span></span>


```C++
void WINAPI glVertex4fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="4b958-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b958-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b958-109">*3,3*</span><span class="sxs-lookup"><span data-stu-id="4b958-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="4b958-110">Указатель на массив из четырех элементов.</span><span class="sxs-lookup"><span data-stu-id="4b958-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="4b958-111">Элементы — это координаты x, y, z и w вершины.</span><span class="sxs-lookup"><span data-stu-id="4b958-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b958-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b958-112">Return value</span></span>

<span data-ttu-id="4b958-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4b958-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b958-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4b958-114">Requirements</span></span>



| <span data-ttu-id="4b958-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4b958-115">Requirement</span></span> | <span data-ttu-id="4b958-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4b958-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b958-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b958-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4b958-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4b958-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4b958-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b958-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4b958-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4b958-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b958-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4b958-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b958-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b958-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4b958-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4b958-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="4b958-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b958-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4b958-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4b958-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b958-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b958-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b958-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b958-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b958-128">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="4b958-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4b958-129">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="4b958-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="4b958-130">**глколор**</span><span class="sxs-lookup"><span data-stu-id="4b958-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="4b958-131">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="4b958-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="4b958-132">**гленд**</span><span class="sxs-lookup"><span data-stu-id="4b958-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4b958-133">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="4b958-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="4b958-134">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="4b958-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="4b958-135">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="4b958-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="4b958-136">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="4b958-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="4b958-137">**глрект**</span><span class="sxs-lookup"><span data-stu-id="4b958-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="4b958-138">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="4b958-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





