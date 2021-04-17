---
title: Функция glVertex3sv (GL. h)
description: Указывает вершину. | Функция glVertex3sv (GL. h)
ms.assetid: 8b819a95-f834-4c6e-b88a-a96ae9b36c71
keywords:
- Функция glVertex3sv OpenGL
topic_type:
- apiref
api_name:
- glVertex3sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa808f76beefa440c3fa4a93a2301cf8b40dfcb2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684886"
---
# <a name="glvertex3sv-function"></a><span data-ttu-id="2e23f-105">Функция glVertex3sv</span><span class="sxs-lookup"><span data-stu-id="2e23f-105">glVertex3sv function</span></span>

<span data-ttu-id="2e23f-106">Указывает вершину.</span><span class="sxs-lookup"><span data-stu-id="2e23f-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e23f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e23f-107">Syntax</span></span>


```C++
void WINAPI glVertex3sv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="2e23f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e23f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e23f-109">*3,3*</span><span class="sxs-lookup"><span data-stu-id="2e23f-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="2e23f-110">Указатель на массив из трех элементов.</span><span class="sxs-lookup"><span data-stu-id="2e23f-110">A pointer to an array of three elements.</span></span> <span data-ttu-id="2e23f-111">Элементы — это координаты x, y и z вершины.</span><span class="sxs-lookup"><span data-stu-id="2e23f-111">The elements are the x, y, and z coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e23f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e23f-112">Return value</span></span>

<span data-ttu-id="2e23f-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2e23f-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e23f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2e23f-114">Requirements</span></span>



| <span data-ttu-id="2e23f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2e23f-115">Requirement</span></span> | <span data-ttu-id="2e23f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2e23f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e23f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e23f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2e23f-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2e23f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2e23f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e23f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2e23f-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2e23f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2e23f-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2e23f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e23f-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e23f-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2e23f-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2e23f-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="2e23f-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e23f-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2e23f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2e23f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e23f-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e23f-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e23f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e23f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e23f-128">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="2e23f-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2e23f-129">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="2e23f-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="2e23f-130">**глколор**</span><span class="sxs-lookup"><span data-stu-id="2e23f-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="2e23f-131">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="2e23f-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="2e23f-132">**гленд**</span><span class="sxs-lookup"><span data-stu-id="2e23f-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2e23f-133">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="2e23f-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="2e23f-134">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="2e23f-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="2e23f-135">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="2e23f-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="2e23f-136">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="2e23f-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="2e23f-137">**глрект**</span><span class="sxs-lookup"><span data-stu-id="2e23f-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="2e23f-138">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="2e23f-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





