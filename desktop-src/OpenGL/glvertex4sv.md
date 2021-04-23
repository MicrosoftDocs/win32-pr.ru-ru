---
title: Функция glVertex4sv (GL. h)
description: Указывает вершину. | Функция glVertex4sv (GL. h)
ms.assetid: 969ecb41-7e72-4b95-9d84-2d995f60f2a3
keywords:
- Функция glVertex4sv OpenGL
topic_type:
- apiref
api_name:
- glVertex4sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c0497fa55b43b22e4649e7ece3eb17f6f9e5339
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914680"
---
# <a name="glvertex4sv-function"></a><span data-ttu-id="2c722-105">Функция glVertex4sv</span><span class="sxs-lookup"><span data-stu-id="2c722-105">glVertex4sv function</span></span>

<span data-ttu-id="2c722-106">Указывает вершину.</span><span class="sxs-lookup"><span data-stu-id="2c722-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c722-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c722-107">Syntax</span></span>


```C++
void WINAPI glVertex4sv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="2c722-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c722-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c722-109">*3,3*</span><span class="sxs-lookup"><span data-stu-id="2c722-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="2c722-110">Указатель на массив из четырех элементов.</span><span class="sxs-lookup"><span data-stu-id="2c722-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="2c722-111">Элементы — это координаты x, y, z и w вершины.</span><span class="sxs-lookup"><span data-stu-id="2c722-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c722-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c722-112">Return value</span></span>

<span data-ttu-id="2c722-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2c722-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c722-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2c722-114">Requirements</span></span>



| <span data-ttu-id="2c722-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2c722-115">Requirement</span></span> | <span data-ttu-id="2c722-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2c722-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c722-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c722-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2c722-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c722-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2c722-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c722-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2c722-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c722-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2c722-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2c722-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c722-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c722-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2c722-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2c722-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="2c722-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c722-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2c722-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2c722-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c722-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c722-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c722-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c722-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c722-128">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="2c722-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2c722-129">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="2c722-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="2c722-130">**глколор**</span><span class="sxs-lookup"><span data-stu-id="2c722-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="2c722-131">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="2c722-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="2c722-132">**гленд**</span><span class="sxs-lookup"><span data-stu-id="2c722-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2c722-133">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="2c722-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="2c722-134">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="2c722-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="2c722-135">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="2c722-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="2c722-136">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="2c722-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="2c722-137">**глрект**</span><span class="sxs-lookup"><span data-stu-id="2c722-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="2c722-138">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="2c722-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





