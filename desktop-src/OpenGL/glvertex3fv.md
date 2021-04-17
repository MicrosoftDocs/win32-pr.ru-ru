---
title: Функция glVertex3fv (GL. h)
description: Указывает вершину. | Функция glVertex3fv (GL. h)
ms.assetid: d8790ffe-73b1-49d8-a7f5-2117177573ac
keywords:
- Функция glVertex3fv OpenGL
topic_type:
- apiref
api_name:
- glVertex3fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f3bcbe73d071bc18e3a1a58ef2f505fa9bd6a3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684884"
---
# <a name="glvertex3fv-function"></a><span data-ttu-id="11302-105">Функция glVertex3fv</span><span class="sxs-lookup"><span data-stu-id="11302-105">glVertex3fv function</span></span>

<span data-ttu-id="11302-106">Указывает вершину.</span><span class="sxs-lookup"><span data-stu-id="11302-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="11302-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11302-107">Syntax</span></span>


```C++
void WINAPI glVertex3fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="11302-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="11302-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11302-109">*3,3*</span><span class="sxs-lookup"><span data-stu-id="11302-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="11302-110">Указатель на массив из трех элементов.</span><span class="sxs-lookup"><span data-stu-id="11302-110">A pointer to an array of three elements.</span></span> <span data-ttu-id="11302-111">Элементы — это координаты x, y и z вершины.</span><span class="sxs-lookup"><span data-stu-id="11302-111">The elements are the x, y, and z coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11302-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11302-112">Return value</span></span>

<span data-ttu-id="11302-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="11302-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="11302-114">Требования</span><span class="sxs-lookup"><span data-stu-id="11302-114">Requirements</span></span>



| <span data-ttu-id="11302-115">Требование</span><span class="sxs-lookup"><span data-stu-id="11302-115">Requirement</span></span> | <span data-ttu-id="11302-116">Значение</span><span class="sxs-lookup"><span data-stu-id="11302-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11302-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11302-117">Minimum supported client</span></span><br/> | <span data-ttu-id="11302-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11302-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="11302-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11302-119">Minimum supported server</span></span><br/> | <span data-ttu-id="11302-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11302-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="11302-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="11302-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="11302-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="11302-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="11302-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="11302-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="11302-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11302-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="11302-125">DLL</span><span class="sxs-lookup"><span data-stu-id="11302-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11302-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11302-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11302-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11302-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11302-128">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="11302-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="11302-129">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="11302-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="11302-130">**глколор**</span><span class="sxs-lookup"><span data-stu-id="11302-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="11302-131">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="11302-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="11302-132">**гленд**</span><span class="sxs-lookup"><span data-stu-id="11302-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="11302-133">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="11302-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="11302-134">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="11302-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="11302-135">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="11302-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="11302-136">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="11302-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="11302-137">**глрект**</span><span class="sxs-lookup"><span data-stu-id="11302-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="11302-138">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="11302-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





