---
title: Функция glEvalPoint2 (GL. h)
description: Функции glEvalPoint1 и glEvalPoint2 создают и оценивают единую точку в сетке. | Функция glEvalPoint2 (GL. h)
ms.assetid: babae9c7-84a8-4a7e-b6f9-97c4e8bd42fe
keywords:
- Функция glEvalPoint2 OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fafe728249f988462b0929873bbb195fed1e7c9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684957"
---
# <a name="glevalpoint2-function"></a><span data-ttu-id="5dc7c-105">Функция glEvalPoint2</span><span class="sxs-lookup"><span data-stu-id="5dc7c-105">glEvalPoint2 function</span></span>

<span data-ttu-id="5dc7c-106">Функции [**glEvalPoint1**](glevalpoint.md) и **glEvalPoint2** создают и оценивают единую точку в сетке.</span><span class="sxs-lookup"><span data-stu-id="5dc7c-106">The [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2** functions generate and evaluate a single point in a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dc7c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dc7c-107">Syntax</span></span>


```C++
void glEvalPoint2(
   GLint i,
   GLint j
);
```



## <a name="parameters"></a><span data-ttu-id="5dc7c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5dc7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dc7c-109">*i*</span><span class="sxs-lookup"><span data-stu-id="5dc7c-109">*i*</span></span> 
</dt> <dd>

<span data-ttu-id="5dc7c-110">Целочисленное значение для переменной домена сетки *i*.</span><span class="sxs-lookup"><span data-stu-id="5dc7c-110">The integer value for grid domain variable *i*.</span></span>

</dd> <dt>

<span data-ttu-id="5dc7c-111">*б*</span><span class="sxs-lookup"><span data-stu-id="5dc7c-111">*j*</span></span> 
</dt> <dd>

<span data-ttu-id="5dc7c-112">Целочисленное значение для переменной домена сетки *j* .</span><span class="sxs-lookup"><span data-stu-id="5dc7c-112">The integer value for grid domain variable *j* .</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dc7c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5dc7c-113">Return value</span></span>

<span data-ttu-id="5dc7c-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5dc7c-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dc7c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5dc7c-115">Remarks</span></span>

<span data-ttu-id="5dc7c-116">Функции [**глмапгрид**](glmapgrid-functions.md) и [**глевалмеш**](glevalmesh-functions.md) используются совместно для эффективного создания и вычисления ряда значений домена сопоставлений с равными пробелами.</span><span class="sxs-lookup"><span data-stu-id="5dc7c-116">The [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="5dc7c-117">**Глевалпоинт** можно использовать для вычисления одной точки сетки в том же гридспаце, которая проходит через **глевалмеш**.</span><span class="sxs-lookup"><span data-stu-id="5dc7c-117">You can use **glEvalPoint** to evaluate a single grid point in the same gridspace that is traversed by **glEvalMesh**.</span></span> <span data-ttu-id="5dc7c-118">Вызов [**glEvalPoint1**](glevalpoint.md) эквивалентен вызову</span><span class="sxs-lookup"><span data-stu-id="5dc7c-118">Calling [**glEvalPoint1**](glevalpoint.md) is equivalent to calling</span></span>

<span data-ttu-id="5dc7c-119">**glEvalCoord1** (*i* ?*u*  + *u* 1);</span><span class="sxs-lookup"><span data-stu-id="5dc7c-119">**glEvalCoord1** (*i* ?*u* +*u* 1 );</span></span>

<span data-ttu-id="5dc7c-120">where</span><span class="sxs-lookup"><span data-stu-id="5dc7c-120">where</span></span>

<span data-ttu-id="5dc7c-121">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="5dc7c-121">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="5dc7c-122">и *n*, *u* 1 и *u* 2 являются аргументами самой последней функции **glMapGrid1** .</span><span class="sxs-lookup"><span data-stu-id="5dc7c-122">and *n*, *u* 1 , and *u* 2 are the arguments to the most recent **glMapGrid1** function.</span></span> <span data-ttu-id="5dc7c-123">Одно абсолютное числовое требование заключается в том, что если *я*  =  *n*, то значение, вычисленное из (*i* ?*u* + U1) представляет собой ровно *u* 2.</span><span class="sxs-lookup"><span data-stu-id="5dc7c-123">The one absolute numeric requirement is that if *i* = *n*, then the value computed from (*i* ?*u* + u1 ) is exactly *u* 2 .</span></span>

<span data-ttu-id="5dc7c-124">В двухмерном регистре **glEvalPoint2**, Let</span><span class="sxs-lookup"><span data-stu-id="5dc7c-124">In the two-dimensional case, **glEvalPoint2**, let</span></span>

<span data-ttu-id="5dc7c-125">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="5dc7c-125">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="5dc7c-126">? *v* = (*v* 2 *v* 1)/*m*</span><span class="sxs-lookup"><span data-stu-id="5dc7c-126">?*v* = (*v* 2 *v* 1 )/*m*</span></span>

<span data-ttu-id="5dc7c-127">где *n*, *u* 1, *u* 2, *m*, *v* 1 и *v* 2 являются аргументами самой последней функции **glMapGrid2** .</span><span class="sxs-lookup"><span data-stu-id="5dc7c-127">where *n*, *u* 1 , *u* 2 , *m*, *v* 1 , and *v* 2  are the arguments to the most recent **glMapGrid2** function.</span></span> <span data-ttu-id="5dc7c-128">Затем функция **glEvalPoint2** эквивалентна вызову</span><span class="sxs-lookup"><span data-stu-id="5dc7c-128">Then the **glEvalPoint2** function is equivalent to calling</span></span>

<span data-ttu-id="5dc7c-129">**glEvalCoord2** (*i* ?*u*  +  *u* 1, *j* ?*v*  +  *v* 1);</span><span class="sxs-lookup"><span data-stu-id="5dc7c-129">**glEvalCoord2** (*i* ?*u* + *u* 1 , *j* ?*v* + *v* 1 );</span></span>

<span data-ttu-id="5dc7c-130">Единственными абсолютными числовыми требованиями является то, что если *я* = *n*, то значение, вычисленное из (*i* ?*u*  +  *u* 1) является ровно U2, и если *j*  =  *m*, то значение, вычисленное на основе (*j* ?*v*  +  *v* 1) является ровно *v* 2.</span><span class="sxs-lookup"><span data-stu-id="5dc7c-130">The only absolute numeric requirements are that if *i*=*n*, then the value computed from (*i* ?*u* + *u* 1 ) is exactly u2 , and if *j* = *m*, then the value computed from (*j* ?*v* + *v* 1  ) is exactly *v* 2 .</span></span>

<span data-ttu-id="5dc7c-131">Следующие функции извлекают сведения, относящиеся к [**glEvalPoint1**](glevalpoint.md) и **glEvalPoint2**:</span><span class="sxs-lookup"><span data-stu-id="5dc7c-131">The following functions retrieve information relating to [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2**:</span></span>

<span data-ttu-id="5dc7c-132">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ GL \_ «Карта1» \_ домен Grid</span><span class="sxs-lookup"><span data-stu-id="5dc7c-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="5dc7c-133">**глжет** с аргументом \_ GL \_ MAP2 \_ домен Grid</span><span class="sxs-lookup"><span data-stu-id="5dc7c-133">**glGet** with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="5dc7c-134">**глжет** с аргументами \_ \_ сегментами сетки GL «Карта1» \_</span><span class="sxs-lookup"><span data-stu-id="5dc7c-134">**glGet** with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="5dc7c-135">**глжет** с аргументами \_ \_ сегментами сетки GL MAP2 \_</span><span class="sxs-lookup"><span data-stu-id="5dc7c-135">**glGet** with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="5dc7c-136">Требования</span><span class="sxs-lookup"><span data-stu-id="5dc7c-136">Requirements</span></span>



| <span data-ttu-id="5dc7c-137">Требование</span><span class="sxs-lookup"><span data-stu-id="5dc7c-137">Requirement</span></span> | <span data-ttu-id="5dc7c-138">Значение</span><span class="sxs-lookup"><span data-stu-id="5dc7c-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dc7c-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5dc7c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5dc7c-140">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5dc7c-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5dc7c-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5dc7c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5dc7c-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5dc7c-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5dc7c-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5dc7c-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dc7c-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dc7c-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5dc7c-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5dc7c-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="5dc7c-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5dc7c-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5dc7c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="5dc7c-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dc7c-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dc7c-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dc7c-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5dc7c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dc7c-150">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="5dc7c-150">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="5dc7c-151">**глевалмеш**</span><span class="sxs-lookup"><span data-stu-id="5dc7c-151">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="5dc7c-152">**глжет**</span><span class="sxs-lookup"><span data-stu-id="5dc7c-152">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="5dc7c-153">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="5dc7c-153">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="5dc7c-154">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="5dc7c-154">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="5dc7c-155">**глмапгрид**</span><span class="sxs-lookup"><span data-stu-id="5dc7c-155">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> </dl>

 

 





