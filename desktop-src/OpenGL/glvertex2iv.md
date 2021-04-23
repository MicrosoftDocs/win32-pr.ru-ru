---
title: Функция glVertex2iv (GL. h)
description: Указывает вершину. | Функция glVertex2iv (GL. h)
ms.assetid: 3b88bf7d-5743-4ac0-a79f-5f450b488bd2
keywords:
- Функция glVertex2iv OpenGL
topic_type:
- apiref
api_name:
- glVertex2iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594c50ff1e30184d5a7292c5b639f16a48f0820b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081818"
---
# <a name="glvertex2iv-function"></a><span data-ttu-id="77407-105">Функция glVertex2iv</span><span class="sxs-lookup"><span data-stu-id="77407-105">glVertex2iv function</span></span>

<span data-ttu-id="77407-106">Указывает вершину.</span><span class="sxs-lookup"><span data-stu-id="77407-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="77407-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77407-107">Syntax</span></span>


```C++
void WINAPI glVertex2iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="77407-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="77407-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77407-109">*3,3*</span><span class="sxs-lookup"><span data-stu-id="77407-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="77407-110">Указатель на массив из двух элементов.</span><span class="sxs-lookup"><span data-stu-id="77407-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="77407-111">Элементы являются координатами x и y вершины.</span><span class="sxs-lookup"><span data-stu-id="77407-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77407-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77407-112">Return value</span></span>

<span data-ttu-id="77407-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="77407-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="77407-114">Требования</span><span class="sxs-lookup"><span data-stu-id="77407-114">Requirements</span></span>



| <span data-ttu-id="77407-115">Требование</span><span class="sxs-lookup"><span data-stu-id="77407-115">Requirement</span></span> | <span data-ttu-id="77407-116">Значение</span><span class="sxs-lookup"><span data-stu-id="77407-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77407-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77407-117">Minimum supported client</span></span><br/> | <span data-ttu-id="77407-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="77407-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="77407-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77407-119">Minimum supported server</span></span><br/> | <span data-ttu-id="77407-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="77407-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77407-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="77407-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="77407-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="77407-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="77407-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="77407-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="77407-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77407-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="77407-125">DLL</span><span class="sxs-lookup"><span data-stu-id="77407-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77407-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77407-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77407-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77407-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77407-128">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="77407-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="77407-129">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="77407-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="77407-130">**глколор**</span><span class="sxs-lookup"><span data-stu-id="77407-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="77407-131">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="77407-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="77407-132">**гленд**</span><span class="sxs-lookup"><span data-stu-id="77407-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="77407-133">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="77407-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="77407-134">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="77407-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="77407-135">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="77407-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="77407-136">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="77407-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="77407-137">**глрект**</span><span class="sxs-lookup"><span data-stu-id="77407-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="77407-138">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="77407-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





