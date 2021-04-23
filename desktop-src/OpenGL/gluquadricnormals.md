---
title: Функция Глукуадрикнормалс (GLU. h)
description: Функция Глукуадрикнормалс указывает, какие нормали будут использоваться для куадрикс.
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
keywords:
- Функция Глукуадрикнормалс OpenGL
topic_type:
- apiref
api_name:
- gluQuadricNormals
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11f9d8cd1884d7a5d1bc4cd03797517ba484126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491910"
---
# <a name="gluquadricnormals-function"></a><span data-ttu-id="6420c-104">Функция Глукуадрикнормалс</span><span class="sxs-lookup"><span data-stu-id="6420c-104">gluQuadricNormals function</span></span>

<span data-ttu-id="6420c-105">Функция **глукуадрикнормалс** указывает, какие нормали будут использоваться для куадрикс.</span><span class="sxs-lookup"><span data-stu-id="6420c-105">The **gluQuadricNormals** function specifies what kind of normals are to be used for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="6420c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6420c-106">Syntax</span></span>


```C++
void WINAPI gluQuadricNormals(
   GLUquadric *quadObject,
   GLenum     normals
);
```



## <a name="parameters"></a><span data-ttu-id="6420c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6420c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6420c-108">*куадобжект*</span><span class="sxs-lookup"><span data-stu-id="6420c-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="6420c-109">Объект куадрик (созданный с помощью [**глуневкуадрик**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="6420c-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6420c-110">*Normals*</span><span class="sxs-lookup"><span data-stu-id="6420c-110">*normals*</span></span> 
</dt> <dd>

<span data-ttu-id="6420c-111">Требуемый тип нормалй.</span><span class="sxs-lookup"><span data-stu-id="6420c-111">The desired type of normals.</span></span> <span data-ttu-id="6420c-112">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="6420c-112">The following values are valid.</span></span>



| <span data-ttu-id="6420c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6420c-113">Value</span></span>                                                                                                                                                | <span data-ttu-id="6420c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="6420c-114">Meaning</span></span>                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="GLU_NONE"></span><span id="glu_none"></span><dl> <span data-ttu-id="6420c-115"><dt>**GLU \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="6420c-115"><dt>**GLU\_NONE**</dt></span></span> </dl>       | <span data-ttu-id="6420c-116">Нормали не создаются.</span><span class="sxs-lookup"><span data-stu-id="6420c-116">No normals are generated.</span></span><br/>                                                         |
| <span id="GLU_FLAT"></span><span id="glu_flat"></span><dl> <span data-ttu-id="6420c-117"><dt>**GLU \_ бемоль**</dt></span><span class="sxs-lookup"><span data-stu-id="6420c-117"><dt>**GLU\_FLAT**</dt></span></span> </dl>       | <span data-ttu-id="6420c-118">Для каждого аспекта куадрик создается один нормальный.</span><span class="sxs-lookup"><span data-stu-id="6420c-118">One normal is generated for every facet of a quadric.</span></span><br/>                             |
| <span id="GLU_SMOOTH"></span><span id="glu_smooth"></span><dl> <span data-ttu-id="6420c-119"><dt>**GLU \_ гладкий**</dt></span><span class="sxs-lookup"><span data-stu-id="6420c-119"><dt>**GLU\_SMOOTH**</dt></span></span> </dl> | <span data-ttu-id="6420c-120">Для каждой вершины куадрик создается один нормальный.</span><span class="sxs-lookup"><span data-stu-id="6420c-120">One normal is generated for every vertex of a quadric.</span></span> <span data-ttu-id="6420c-121">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6420c-121">This is the default value.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6420c-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6420c-122">Return value</span></span>

<span data-ttu-id="6420c-123">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6420c-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6420c-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6420c-124">Remarks</span></span>

<span data-ttu-id="6420c-125">Функция **глукуадрикнормалс** указывает, какие нормали должны использоваться для куадрикс, отображаемого с помощью **куадобжект**.</span><span class="sxs-lookup"><span data-stu-id="6420c-125">The **gluQuadricNormals** function specifies what kind of normals are to be used for quadrics rendered with **quadObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6420c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="6420c-126">Requirements</span></span>



| <span data-ttu-id="6420c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6420c-127">Requirement</span></span> | <span data-ttu-id="6420c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6420c-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6420c-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6420c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6420c-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6420c-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6420c-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6420c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6420c-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6420c-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6420c-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6420c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6420c-134"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="6420c-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="6420c-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6420c-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="6420c-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6420c-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6420c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6420c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6420c-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6420c-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6420c-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6420c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6420c-140">**глуневкуадрик**</span><span class="sxs-lookup"><span data-stu-id="6420c-140">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="6420c-141">**глукуадрикдравстиле**</span><span class="sxs-lookup"><span data-stu-id="6420c-141">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="6420c-142">**глукуадрикориентатион**</span><span class="sxs-lookup"><span data-stu-id="6420c-142">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="6420c-143">**глукуадриктекстуре**</span><span class="sxs-lookup"><span data-stu-id="6420c-143">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





