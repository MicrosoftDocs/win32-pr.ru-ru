---
title: Функция Глуневкуадрик (GLU. h)
description: Функция Глуневкуадрик создает объект куадрик.
ms.assetid: 5a4289bf-b57a-4c74-b0e3-b7536671e4df
keywords:
- Функция Глуневкуадрик OpenGL
topic_type:
- apiref
api_name:
- gluNewQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: affedc7dcebd2b7925449e22cc1b902e88d936f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988883"
---
# <a name="glunewquadric-function"></a><span data-ttu-id="46652-104">Функция Глуневкуадрик</span><span class="sxs-lookup"><span data-stu-id="46652-104">gluNewQuadric function</span></span>

<span data-ttu-id="46652-105">Функция **глуневкуадрик** создает объект куадрик.</span><span class="sxs-lookup"><span data-stu-id="46652-105">The **gluNewQuadric** function creates a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="46652-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46652-106">Syntax</span></span>


```C++
GLUquadric* WINAPI gluNewQuadric(void);
```



## <a name="parameters"></a><span data-ttu-id="46652-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="46652-107">Parameters</span></span>

<span data-ttu-id="46652-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="46652-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="46652-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46652-109">Remarks</span></span>

<span data-ttu-id="46652-110">Функция **глуневкуадрик** создает и возвращает указатель на новый объект куадрик.</span><span class="sxs-lookup"><span data-stu-id="46652-110">The **gluNewQuadric** function creates and returns a pointer to a new quadric object.</span></span> <span data-ttu-id="46652-111">Используйте этот объект при вызове функций отрисовки куадрик и управления.</span><span class="sxs-lookup"><span data-stu-id="46652-111">Refer to this object when calling quadric rendering and control functions.</span></span> <span data-ttu-id="46652-112">Возвращаемое значение, равное нулю, означает, что недостаточно памяти для выделения объекту.</span><span class="sxs-lookup"><span data-stu-id="46652-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="46652-113">Требования</span><span class="sxs-lookup"><span data-stu-id="46652-113">Requirements</span></span>



| <span data-ttu-id="46652-114">Требование</span><span class="sxs-lookup"><span data-stu-id="46652-114">Requirement</span></span> | <span data-ttu-id="46652-115">Значение</span><span class="sxs-lookup"><span data-stu-id="46652-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="46652-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46652-116">Minimum supported client</span></span><br/> | <span data-ttu-id="46652-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="46652-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="46652-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46652-118">Minimum supported server</span></span><br/> | <span data-ttu-id="46652-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="46652-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="46652-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="46652-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="46652-121"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="46652-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="46652-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="46652-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="46652-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46652-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="46652-124">DLL</span><span class="sxs-lookup"><span data-stu-id="46652-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46652-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46652-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46652-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46652-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46652-127">**глуцилиндер**</span><span class="sxs-lookup"><span data-stu-id="46652-127">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="46652-128">**глуделетекуадрик**</span><span class="sxs-lookup"><span data-stu-id="46652-128">**gluDeleteQuadric**</span></span>](gludeletequadric.md)
</dt> <dt>

[<span data-ttu-id="46652-129">**глудиск**</span><span class="sxs-lookup"><span data-stu-id="46652-129">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="46652-130">**глупартиалдиск**</span><span class="sxs-lookup"><span data-stu-id="46652-130">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="46652-131">*глукуадриккаллбакк*</span><span class="sxs-lookup"><span data-stu-id="46652-131">*gluQuadricCallback*</span></span>](gluquadric.md)
</dt> <dt>

[<span data-ttu-id="46652-132">**глукуадрикдравстиле**</span><span class="sxs-lookup"><span data-stu-id="46652-132">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="46652-133">**глукуадрикнормалс**</span><span class="sxs-lookup"><span data-stu-id="46652-133">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="46652-134">**глукуадрикориентатион**</span><span class="sxs-lookup"><span data-stu-id="46652-134">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="46652-135">**глукуадриктекстуре**</span><span class="sxs-lookup"><span data-stu-id="46652-135">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="46652-136">**глусфере**</span><span class="sxs-lookup"><span data-stu-id="46652-136">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





