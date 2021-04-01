---
title: Функция glEvalPoint1 (GL. h)
description: Функции glEvalPoint1 и glEvalPoint2 создают и оценивают единую точку в сетке. | Функция glEvalPoint1 (GL. h)
ms.assetid: 5ef1d2f0-d77b-4bb8-a0d4-45c1a6a91c18
keywords:
- Функция glEvalPoint1 OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b9c3b8e17f5a0554c1864a401ecf49343806c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914623"
---
# <a name="glevalpoint1-function"></a><span data-ttu-id="f547d-105">Функция glEvalPoint1</span><span class="sxs-lookup"><span data-stu-id="f547d-105">glEvalPoint1 function</span></span>

<span data-ttu-id="f547d-106">Функции [**glEvalPoint1**](glevalpoint.md) и **glEvalPoint2** создают и оценивают единую точку в сетке.</span><span class="sxs-lookup"><span data-stu-id="f547d-106">The [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2** functions generate and evaluate a single point in a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="f547d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f547d-107">Syntax</span></span>


```C++
void glEvalPoint1(
   GLint i
);
```



## <a name="parameters"></a><span data-ttu-id="f547d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f547d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f547d-109">*i*</span><span class="sxs-lookup"><span data-stu-id="f547d-109">*i*</span></span> 
</dt> <dd>

<span data-ttu-id="f547d-110">Целочисленное значение для переменной домена сетки *i*.</span><span class="sxs-lookup"><span data-stu-id="f547d-110">The integer value for grid domain variable *i*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f547d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f547d-111">Return value</span></span>

<span data-ttu-id="f547d-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f547d-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f547d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f547d-113">Remarks</span></span>

<span data-ttu-id="f547d-114">Функции [**глмапгрид**](glmapgrid-functions.md) и [**глевалмеш**](glevalmesh-functions.md) используются совместно для эффективного создания и вычисления ряда значений домена сопоставлений с равными пробелами.</span><span class="sxs-lookup"><span data-stu-id="f547d-114">The [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="f547d-115">**Глевалпоинт** можно использовать для вычисления одной точки сетки в том же гридспаце, которая проходит через **глевалмеш**.</span><span class="sxs-lookup"><span data-stu-id="f547d-115">You can use **glEvalPoint** to evaluate a single grid point in the same gridspace that is traversed by **glEvalMesh**.</span></span> <span data-ttu-id="f547d-116">Вызов [**glEvalPoint1**](glevalpoint.md) эквивалентен вызову</span><span class="sxs-lookup"><span data-stu-id="f547d-116">Calling [**glEvalPoint1**](glevalpoint.md) is equivalent to calling</span></span>

<span data-ttu-id="f547d-117">**glEvalCoord1** (*i* ?*u*  + *u* 1);</span><span class="sxs-lookup"><span data-stu-id="f547d-117">**glEvalCoord1** (*i* ?*u* +*u* 1 );</span></span>

<span data-ttu-id="f547d-118">where</span><span class="sxs-lookup"><span data-stu-id="f547d-118">where</span></span>

<span data-ttu-id="f547d-119">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="f547d-119">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="f547d-120">и *n*, *u* 1 и *u* 2 являются аргументами самой последней функции **glMapGrid1** .</span><span class="sxs-lookup"><span data-stu-id="f547d-120">and *n*, *u* 1 , and *u* 2 are the arguments to the most recent **glMapGrid1** function.</span></span> <span data-ttu-id="f547d-121">Одно абсолютное числовое требование заключается в том, что если *я*  =  *n*, то значение, вычисленное из (*i* ?*u* + U1) представляет собой ровно *u* 2.</span><span class="sxs-lookup"><span data-stu-id="f547d-121">The one absolute numeric requirement is that if *i* = *n*, then the value computed from (*i* ?*u* + u1 ) is exactly *u* 2 .</span></span>

<span data-ttu-id="f547d-122">В двухмерном регистре **glEvalPoint2**, Let</span><span class="sxs-lookup"><span data-stu-id="f547d-122">In the two-dimensional case, **glEvalPoint2**, let</span></span>

<span data-ttu-id="f547d-123">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="f547d-123">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="f547d-124">? *v* = (*v* 2 *v* 1)/*m*</span><span class="sxs-lookup"><span data-stu-id="f547d-124">?*v* = (*v* 2 *v* 1 )/*m*</span></span>

<span data-ttu-id="f547d-125">где *n*, *u* 1, *u* 2, *m*, *v* 1 и *v* 2 являются аргументами самой последней функции **glMapGrid2** .</span><span class="sxs-lookup"><span data-stu-id="f547d-125">where *n*, *u* 1 , *u* 2 , *m*, *v* 1 , and *v* 2  are the arguments to the most recent **glMapGrid2** function.</span></span> <span data-ttu-id="f547d-126">Затем функция **glEvalPoint2** эквивалентна вызову</span><span class="sxs-lookup"><span data-stu-id="f547d-126">Then the **glEvalPoint2** function is equivalent to calling</span></span>

<span data-ttu-id="f547d-127">**glEvalCoord2** (*i* ?*u*  +  *u* 1, *j* ?*v*  +  *v* 1);</span><span class="sxs-lookup"><span data-stu-id="f547d-127">**glEvalCoord2** (*i* ?*u* + *u* 1 , *j* ?*v* + *v* 1 );</span></span>

<span data-ttu-id="f547d-128">Единственными абсолютными числовыми требованиями является то, что если *я* = *n*, то значение, вычисленное из (*i* ?*u*  +  *u* 1) является ровно U2, и если *j*  =  *m*, то значение, вычисленное на основе (*j* ?*v*  +  *v* 1) является ровно *v* 2.</span><span class="sxs-lookup"><span data-stu-id="f547d-128">The only absolute numeric requirements are that if *i*=*n*, then the value computed from (*i* ?*u* + *u* 1 ) is exactly u2 , and if *j* = *m*, then the value computed from (*j* ?*v* + *v* 1  ) is exactly *v* 2 .</span></span>

<span data-ttu-id="f547d-129">Следующие функции извлекают сведения, относящиеся к [**glEvalPoint1**](glevalpoint.md) и **glEvalPoint2**:</span><span class="sxs-lookup"><span data-stu-id="f547d-129">The following functions retrieve information relating to [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2**:</span></span>

<span data-ttu-id="f547d-130">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ GL \_ «Карта1» \_ домен Grid</span><span class="sxs-lookup"><span data-stu-id="f547d-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="f547d-131">**глжет** с аргументом \_ GL \_ MAP2 \_ домен Grid</span><span class="sxs-lookup"><span data-stu-id="f547d-131">**glGet** with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="f547d-132">**глжет** с аргументами \_ \_ сегментами сетки GL «Карта1» \_</span><span class="sxs-lookup"><span data-stu-id="f547d-132">**glGet** with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="f547d-133">**глжет** с аргументами \_ \_ сегментами сетки GL MAP2 \_</span><span class="sxs-lookup"><span data-stu-id="f547d-133">**glGet** with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="f547d-134">Требования</span><span class="sxs-lookup"><span data-stu-id="f547d-134">Requirements</span></span>



| <span data-ttu-id="f547d-135">Требование</span><span class="sxs-lookup"><span data-stu-id="f547d-135">Requirement</span></span> | <span data-ttu-id="f547d-136">Значение</span><span class="sxs-lookup"><span data-stu-id="f547d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f547d-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f547d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f547d-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f547d-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f547d-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f547d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f547d-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f547d-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f547d-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f547d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f547d-142"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f547d-142"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f547d-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f547d-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="f547d-144"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f547d-144"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f547d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f547d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f547d-146"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f547d-146"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f547d-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f547d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f547d-148">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="f547d-148">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="f547d-149">**глевалмеш**</span><span class="sxs-lookup"><span data-stu-id="f547d-149">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="f547d-150">**глжет**</span><span class="sxs-lookup"><span data-stu-id="f547d-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="f547d-151">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="f547d-151">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="f547d-152">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="f547d-152">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="f547d-153">**глмапгрид**</span><span class="sxs-lookup"><span data-stu-id="f547d-153">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> </dl>

 

 





