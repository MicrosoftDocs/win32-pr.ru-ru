---
title: Функция glVertex3iv (GL. h)
description: Указывает вершину. | Функция glVertex3iv (GL. h)
ms.assetid: db7e6a93-aaa2-402b-acd5-971c17451314
keywords:
- Функция glVertex3iv OpenGL
topic_type:
- apiref
api_name:
- glVertex3iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bb0a5db3ebf30722573c9f7d0143b92046c8cb6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684906"
---
# <a name="glvertex3iv-function"></a><span data-ttu-id="8b946-105">Функция glVertex3iv</span><span class="sxs-lookup"><span data-stu-id="8b946-105">glVertex3iv function</span></span>

<span data-ttu-id="8b946-106">Указывает вершину.</span><span class="sxs-lookup"><span data-stu-id="8b946-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b946-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b946-107">Syntax</span></span>


```C++
void WINAPI glVertex3iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="8b946-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b946-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b946-109">*3,3*</span><span class="sxs-lookup"><span data-stu-id="8b946-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="8b946-110">Указатель на массив из трех элементов.</span><span class="sxs-lookup"><span data-stu-id="8b946-110">A pointer to an array of three elements.</span></span> <span data-ttu-id="8b946-111">Элементы — это координаты x, y и z вершины.</span><span class="sxs-lookup"><span data-stu-id="8b946-111">The elements are the x, y, and z coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b946-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b946-112">Return value</span></span>

<span data-ttu-id="8b946-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8b946-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b946-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8b946-114">Requirements</span></span>



| <span data-ttu-id="8b946-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8b946-115">Requirement</span></span> | <span data-ttu-id="8b946-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8b946-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b946-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b946-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8b946-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8b946-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8b946-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b946-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8b946-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8b946-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8b946-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8b946-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b946-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b946-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8b946-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8b946-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b946-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b946-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8b946-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8b946-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b946-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b946-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b946-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b946-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b946-128">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="8b946-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8b946-129">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="8b946-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="8b946-130">**глколор**</span><span class="sxs-lookup"><span data-stu-id="8b946-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="8b946-131">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="8b946-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="8b946-132">**гленд**</span><span class="sxs-lookup"><span data-stu-id="8b946-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8b946-133">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="8b946-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="8b946-134">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="8b946-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="8b946-135">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="8b946-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="8b946-136">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="8b946-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="8b946-137">**глрект**</span><span class="sxs-lookup"><span data-stu-id="8b946-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="8b946-138">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="8b946-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





