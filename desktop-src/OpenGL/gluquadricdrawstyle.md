---
title: Функция Глукуадрикдравстиле (GLU. h)
description: Функция Глукуадрикдравстиле задает стиль рисования, необходимый для куадрикс.
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- Функция Глукуадрикдравстиле OpenGL
topic_type:
- apiref
api_name:
- gluQuadricDrawStyle
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a1b44b7894ea9762b450c5a5d6c2b022c5e02f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989036"
---
# <a name="gluquadricdrawstyle-function"></a><span data-ttu-id="8c6b4-104">Функция Глукуадрикдравстиле</span><span class="sxs-lookup"><span data-stu-id="8c6b4-104">gluQuadricDrawStyle function</span></span>

<span data-ttu-id="8c6b4-105">Функция **глукуадрикдравстиле** задает стиль рисования, необходимый для куадрикс.</span><span class="sxs-lookup"><span data-stu-id="8c6b4-105">The **gluQuadricDrawStyle** function specifies the draw style desired for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c6b4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c6b4-106">Syntax</span></span>


```C++
void WINAPI gluQuadricDrawStyle(
   GLUquadric *quadObject,
   GLenum     drawStyle
);
```



## <a name="parameters"></a><span data-ttu-id="8c6b4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c6b4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c6b4-108">*куадобжект*</span><span class="sxs-lookup"><span data-stu-id="8c6b4-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="8c6b4-109">Объект куадрик (созданный с помощью [**глуневкуадрик**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="8c6b4-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="8c6b4-110">*дравстиле*</span><span class="sxs-lookup"><span data-stu-id="8c6b4-110">*drawStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="8c6b4-111">Требуемый стиль рисования.</span><span class="sxs-lookup"><span data-stu-id="8c6b4-111">The desired draw style.</span></span> <span data-ttu-id="8c6b4-112">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="8c6b4-112">The following values are valid.</span></span>



| <span data-ttu-id="8c6b4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="8c6b4-113">Value</span></span>                                                                                                                                                            | <span data-ttu-id="8c6b4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8c6b4-114">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <span data-ttu-id="8c6b4-115"><dt>**GLU \_ Заливка**</dt></span><span class="sxs-lookup"><span data-stu-id="8c6b4-115"><dt>**GLU\_FILL**</dt></span></span> </dl>                   | <span data-ttu-id="8c6b4-116">Куадрикс подготавливаются к просмотру с помощью примитивов многоугольников.</span><span class="sxs-lookup"><span data-stu-id="8c6b4-116">Quadrics are rendered with polygon primitives.</span></span> <span data-ttu-id="8c6b4-117">Многоугольники рисуются против часовой стрелки по отношению к их нормальным значениям (как определено с помощью [**глукуадрикориентатион**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="8c6b4-117">The polygons are drawn in a counterclockwise fashion with respect to their normals (as defined with [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span><br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <span data-ttu-id="8c6b4-118"><dt>**GLU \_ строка**</dt></span><span class="sxs-lookup"><span data-stu-id="8c6b4-118"><dt>**GLU\_LINE**</dt></span></span> </dl>                   | <span data-ttu-id="8c6b4-119">Куадрикс подготавливаются к просмотру как набор строк.</span><span class="sxs-lookup"><span data-stu-id="8c6b4-119">Quadrics are rendered as a set of lines.</span></span><br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <span data-ttu-id="8c6b4-120"><dt>**GLU \_ силуэт**</dt></span><span class="sxs-lookup"><span data-stu-id="8c6b4-120"><dt>**GLU\_SILHOUETTE**</dt></span></span> </dl> | <span data-ttu-id="8c6b4-121">Куадрикс подготавливаются к просмотру как набор строк, за исключением того, что границы, разделяющие копланар грани, не рисуются.</span><span class="sxs-lookup"><span data-stu-id="8c6b4-121">Quadrics are rendered as a set of lines, except that edges separating coplanar faces will not be drawn.</span></span><br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <span data-ttu-id="8c6b4-122"><dt>**\_точка Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="8c6b4-122"><dt>**GLU\_POINT**</dt></span></span> </dl>                | <span data-ttu-id="8c6b4-123">Куадрикс подготавливаются к просмотру как набор точек.</span><span class="sxs-lookup"><span data-stu-id="8c6b4-123">Quadrics are rendered as a set of points.</span></span><br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c6b4-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c6b4-124">Return value</span></span>

<span data-ttu-id="8c6b4-125">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8c6b4-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c6b4-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c6b4-126">Remarks</span></span>

<span data-ttu-id="8c6b4-127">Функция **глукуадрикдравстиле** задает стиль рисования для куадрикс, отображаемого с помощью **куадобжект**.</span><span class="sxs-lookup"><span data-stu-id="8c6b4-127">The **gluQuadricDrawStyle** function specifies the draw style for quadrics rendered with **quadObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c6b4-128">Требования</span><span class="sxs-lookup"><span data-stu-id="8c6b4-128">Requirements</span></span>



| <span data-ttu-id="8c6b4-129">Требование</span><span class="sxs-lookup"><span data-stu-id="8c6b4-129">Requirement</span></span> | <span data-ttu-id="8c6b4-130">Значение</span><span class="sxs-lookup"><span data-stu-id="8c6b4-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8c6b4-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c6b4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8c6b4-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8c6b4-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8c6b4-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c6b4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8c6b4-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8c6b4-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8c6b4-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8c6b4-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c6b4-136"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c6b4-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="8c6b4-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8c6b4-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="8c6b4-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c6b4-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8c6b4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8c6b4-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c6b4-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c6b4-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c6b4-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c6b4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c6b4-142">**глуневкуадрик**</span><span class="sxs-lookup"><span data-stu-id="8c6b4-142">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="8c6b4-143">**глукуадрикнормалс**</span><span class="sxs-lookup"><span data-stu-id="8c6b4-143">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="8c6b4-144">**глукуадрикориентатион**</span><span class="sxs-lookup"><span data-stu-id="8c6b4-144">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="8c6b4-145">**глукуадриктекстуре**</span><span class="sxs-lookup"><span data-stu-id="8c6b4-145">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





