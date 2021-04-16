---
title: Функция glVertex2fv (GL. h)
description: Указывает вершину. | Функция glVertex2fv (GL. h)
ms.assetid: bae32d27-2a19-40d5-a3f7-0e7a41918034
keywords:
- Функция glVertex2fv OpenGL
topic_type:
- apiref
api_name:
- glVertex2fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecd7a57aff2166f3605d7007cd194f5cff04784
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664895"
---
# <a name="glvertex2fv-function"></a><span data-ttu-id="463c7-105">Функция glVertex2fv</span><span class="sxs-lookup"><span data-stu-id="463c7-105">glVertex2fv function</span></span>

<span data-ttu-id="463c7-106">Указывает вершину.</span><span class="sxs-lookup"><span data-stu-id="463c7-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="463c7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="463c7-107">Syntax</span></span>


```C++
void WINAPI glVertex2fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="463c7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="463c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="463c7-109">*3,3*</span><span class="sxs-lookup"><span data-stu-id="463c7-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="463c7-110">Указатель на массив из двух элементов.</span><span class="sxs-lookup"><span data-stu-id="463c7-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="463c7-111">Элементы являются координатами x и y вершины.</span><span class="sxs-lookup"><span data-stu-id="463c7-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="463c7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="463c7-112">Return value</span></span>

<span data-ttu-id="463c7-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="463c7-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="463c7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="463c7-114">Requirements</span></span>



| <span data-ttu-id="463c7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="463c7-115">Requirement</span></span> | <span data-ttu-id="463c7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="463c7-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="463c7-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="463c7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="463c7-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="463c7-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="463c7-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="463c7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="463c7-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="463c7-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="463c7-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="463c7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="463c7-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="463c7-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="463c7-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="463c7-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="463c7-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="463c7-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="463c7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="463c7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="463c7-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="463c7-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="463c7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="463c7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="463c7-128">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="463c7-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="463c7-129">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="463c7-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="463c7-130">**глколор**</span><span class="sxs-lookup"><span data-stu-id="463c7-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="463c7-131">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="463c7-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="463c7-132">**гленд**</span><span class="sxs-lookup"><span data-stu-id="463c7-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="463c7-133">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="463c7-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="463c7-134">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="463c7-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="463c7-135">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="463c7-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="463c7-136">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="463c7-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="463c7-137">**глрект**</span><span class="sxs-lookup"><span data-stu-id="463c7-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="463c7-138">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="463c7-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





