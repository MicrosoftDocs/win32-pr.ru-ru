---
title: Функция glVertex2dv (GL. h)
description: Указывает вершину. | Функция glVertex2dv (GL. h)
ms.assetid: b685d0aa-2874-4ad9-a20c-86823e9ad00b
keywords:
- Функция glVertex2dv OpenGL
topic_type:
- apiref
api_name:
- glVertex2dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4839fa650302a67c98a0aef3d227dfafa8ddb688
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000119"
---
# <a name="glvertex2dv-function"></a><span data-ttu-id="c71d2-105">Функция glVertex2dv</span><span class="sxs-lookup"><span data-stu-id="c71d2-105">glVertex2dv function</span></span>

<span data-ttu-id="c71d2-106">Указывает вершину.</span><span class="sxs-lookup"><span data-stu-id="c71d2-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="c71d2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c71d2-107">Syntax</span></span>


```C++
void WINAPI glVertex2dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="c71d2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c71d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c71d2-109">*3,3*</span><span class="sxs-lookup"><span data-stu-id="c71d2-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="c71d2-110">Указатель на массив из двух элементов.</span><span class="sxs-lookup"><span data-stu-id="c71d2-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="c71d2-111">Элементы являются координатами x и y вершины.</span><span class="sxs-lookup"><span data-stu-id="c71d2-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c71d2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c71d2-112">Return value</span></span>

<span data-ttu-id="c71d2-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c71d2-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c71d2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c71d2-114">Requirements</span></span>



| <span data-ttu-id="c71d2-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c71d2-115">Requirement</span></span> | <span data-ttu-id="c71d2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c71d2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c71d2-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c71d2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c71d2-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c71d2-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c71d2-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c71d2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c71d2-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c71d2-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c71d2-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c71d2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c71d2-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c71d2-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c71d2-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c71d2-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c71d2-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c71d2-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c71d2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c71d2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c71d2-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c71d2-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c71d2-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c71d2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c71d2-128">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="c71d2-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c71d2-129">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="c71d2-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="c71d2-130">**глколор**</span><span class="sxs-lookup"><span data-stu-id="c71d2-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="c71d2-131">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="c71d2-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="c71d2-132">**гленд**</span><span class="sxs-lookup"><span data-stu-id="c71d2-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c71d2-133">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="c71d2-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="c71d2-134">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="c71d2-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="c71d2-135">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="c71d2-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="c71d2-136">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="c71d2-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="c71d2-137">**глрект**</span><span class="sxs-lookup"><span data-stu-id="c71d2-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="c71d2-138">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="c71d2-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





