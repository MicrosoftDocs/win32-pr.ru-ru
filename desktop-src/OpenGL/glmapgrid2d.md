---
title: Функция glMapGrid2d (GL. h)
description: Определяет одномерный сетку. | Функция glMapGrid2d (GL. h)
ms.assetid: 5e5887d1-e137-434b-a1f3-b3f10d462823
keywords:
- Функция glMapGrid2d OpenGL
topic_type:
- apiref
api_name:
- glMapGrid2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6992a904528cf961f27335e7241c50fbd14f058b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664853"
---
# <a name="glmapgrid2d-function"></a><span data-ttu-id="881d8-105">Функция glMapGrid2d</span><span class="sxs-lookup"><span data-stu-id="881d8-105">glMapGrid2d function</span></span>

<span data-ttu-id="881d8-106">Определяет одномерный сетку.</span><span class="sxs-lookup"><span data-stu-id="881d8-106">Defines a one-dimensional mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="881d8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="881d8-107">Syntax</span></span>


```C++
void WINAPI glMapGrid2d(
   GLint    un,
   GLdouble u1,
   GLdouble u2,
   GLint    vn,
   GLdouble v1,
   GLdouble v2
);
```



## <a name="parameters"></a><span data-ttu-id="881d8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="881d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="881d8-109">*понижен*</span><span class="sxs-lookup"><span data-stu-id="881d8-109">*un*</span></span> 
</dt> <dd>

<span data-ttu-id="881d8-110">Число секций в диапазоне диапазонов сетки \[ : U1, U2 \] .</span><span class="sxs-lookup"><span data-stu-id="881d8-110">The number of partitions in the grid range interval \[u1, u2\].</span></span> <span data-ttu-id="881d8-111">Это значение должно быть положительным.</span><span class="sxs-lookup"><span data-stu-id="881d8-111">This value must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="881d8-112">*U1*</span><span class="sxs-lookup"><span data-stu-id="881d8-112">*u1*</span></span> 
</dt> <dd>

<span data-ttu-id="881d8-113">Значение, используемое в качестве сопоставления для значения домена целочисленной сетки i = 0.</span><span class="sxs-lookup"><span data-stu-id="881d8-113">A value used as the mapping for integer grid domain value i = 0.</span></span>

</dd> <dt>

<span data-ttu-id="881d8-114">*U2*</span><span class="sxs-lookup"><span data-stu-id="881d8-114">*u2*</span></span> 
</dt> <dd>

<span data-ttu-id="881d8-115">Значение, используемое в качестве сопоставления для значения домена целочисленной сетки i = un.</span><span class="sxs-lookup"><span data-stu-id="881d8-115">A value used as the mapping for integer grid domain value i = un.</span></span>

</dd> <dt>

<span data-ttu-id="881d8-116">*VN*</span><span class="sxs-lookup"><span data-stu-id="881d8-116">*vn*</span></span> 
</dt> <dd>

<span data-ttu-id="881d8-117">Число секций в диапазоне от 1 до \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="881d8-117">The number of partitions in the grid range interval \[v1, v2\].</span></span>

</dd> <dt>

<span data-ttu-id="881d8-118">*Версия 1*</span><span class="sxs-lookup"><span data-stu-id="881d8-118">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="881d8-119">Значение, используемое в качестве сопоставления для значения домена целочисленной сетки j = 0.</span><span class="sxs-lookup"><span data-stu-id="881d8-119">A value used as the mapping for integer grid domain value j = 0.</span></span>

</dd> <dt>

<span data-ttu-id="881d8-120">*Версия 2*</span><span class="sxs-lookup"><span data-stu-id="881d8-120">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="881d8-121">Значение, используемое в качестве сопоставления для значения домена целочисленной сетки j = VN.</span><span class="sxs-lookup"><span data-stu-id="881d8-121">A value used as the mapping for integer grid domain value j = vn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="881d8-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="881d8-122">Return value</span></span>

<span data-ttu-id="881d8-123">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="881d8-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="881d8-124">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="881d8-124">Error codes</span></span>

<span data-ttu-id="881d8-125">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="881d8-125">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="881d8-126">Имя</span><span class="sxs-lookup"><span data-stu-id="881d8-126">Name</span></span>                                                                                                  | <span data-ttu-id="881d8-127">Значение</span><span class="sxs-lookup"><span data-stu-id="881d8-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="881d8-128"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="881d8-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="881d8-129">Либо *un* , либо *VN* не были положительными.</span><span class="sxs-lookup"><span data-stu-id="881d8-129">Either *un* or *vn* was not positive.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="881d8-130"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="881d8-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="881d8-131">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="881d8-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="881d8-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="881d8-132">Remarks</span></span>

<span data-ttu-id="881d8-133">Функции **глмапгрид** и [глевалмеш](glevalmesh-functions.md) используются совместно для эффективного создания и вычисления ряда значений домена сопоставлений с равными пробелами.</span><span class="sxs-lookup"><span data-stu-id="881d8-133">The **glMapGrid** and [glEvalMesh](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="881d8-134">Функция Глевалмеш выполняет шаг с целым доменом одномерной или двухмерной сетки, диапазон которого представляет собой домен карт оценки, заданных в [**glMap1**](glmap1.md) и [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="881d8-134">The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="881d8-135">Функции [**glMapGrid1**](glmapgrid1d.md) и **glMapGrid2** определяют сопоставления линейной сетки между координатами сетки i (или i и j) целого числа с координатами карты вычисления числа с плавающей запятой u (или a и v).</span><span class="sxs-lookup"><span data-stu-id="881d8-135">The [**glMapGrid1**](glmapgrid1d.md) and **glMapGrid2** functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates.</span></span> <span data-ttu-id="881d8-136">Сведения о том, как оцениваются координаты, см. в разделе [**glMap1**](glmap1.md) и [**glMap2**](glmap2.md) .</span><span class="sxs-lookup"><span data-stu-id="881d8-136">See [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md) for details of how u and v coordinates are evaluated.</span></span>

<span data-ttu-id="881d8-137">Функция [**glMapGrid1**](glmapgrid1d.md) задает одно линейное сопоставление таким, *что координата* целочисленной сетки 0 сопоставляется только с U1, а целочисленная сетка целых чисел отменяет сопоставление ровно с *U2*.</span><span class="sxs-lookup"><span data-stu-id="881d8-137">The [**glMapGrid1**](glmapgrid1d.md) function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate *un* maps exactly to *u2*.</span></span> <span data-ttu-id="881d8-138">Все остальные координаты целочисленной сетки *я* сопоставил таким образом, что:</span><span class="sxs-lookup"><span data-stu-id="881d8-138">All other integer grid coordinates *i* are mapped such that:</span></span>

<span data-ttu-id="881d8-139">*u = i (U2 U1)/Ун + U1*</span><span class="sxs-lookup"><span data-stu-id="881d8-139">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="881d8-140">Функция **glMapGrid2** указывает два таких линейных сопоставления.</span><span class="sxs-lookup"><span data-stu-id="881d8-140">The **glMapGrid2** function specifies two such linear mappings.</span></span> <span data-ttu-id="881d8-141">Одна карта сопоставляет целочисленную сетку *i = 0* ровно с *U1*, а целочисленная сетка — координата *i =* в точности до *U2*.</span><span class="sxs-lookup"><span data-stu-id="881d8-141">One maps integer grid coordinate *i = 0* exactly to *u1*, and integer grid coordinate *i = un* exactly to *u2*.</span></span> <span data-ttu-id="881d8-142">Вторая сопоставляет сетку целых чисел *j = 0* ровно с *v1*, а целочисленная сетка с координатами « *j = VN» —* только *v2*.</span><span class="sxs-lookup"><span data-stu-id="881d8-142">The other maps integer grid coordinate *j = 0* exactly to *v1*, and integer grid coordinate *j = vn* exactly to *v2*.</span></span> <span data-ttu-id="881d8-143">Другие координаты целочисленных сеток i и j сопоставлены таким, что</span><span class="sxs-lookup"><span data-stu-id="881d8-143">Other integer grid coordinates i and j are mapped such that</span></span>

<span data-ttu-id="881d8-144">*u = i (U2 U1)/Ун + U1*</span><span class="sxs-lookup"><span data-stu-id="881d8-144">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="881d8-145">*v = j (V2 v1)/VN + v1*</span><span class="sxs-lookup"><span data-stu-id="881d8-145">*v = j (v2 v1)/vn + v1*</span></span>

<span data-ttu-id="881d8-146">Сопоставления, заданные параметром [**глмапгрид**](glmapgrid1d.md) , используются одинаково в [глевалмеш](glevalmesh-functions.md) и [**глевалпоинт**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="881d8-146">The mappings specified by [**glMapGrid**](glmapgrid1d.md) are used identically by [glEvalMesh](glevalmesh-functions.md) and [**glEvalPoint**](glevalpoint.md).</span></span>

<span data-ttu-id="881d8-147">Следующие функции извлекают сведения, относящиеся к [**глмапгрид**](glmapgrid1d.md):</span><span class="sxs-lookup"><span data-stu-id="881d8-147">The following functions retrieve information related to [**glMapGrid**](glmapgrid1d.md):</span></span>

<dl>

<span data-ttu-id="881d8-148">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ GL \_ «Карта1» \_ домен Grid</span><span class="sxs-lookup"><span data-stu-id="881d8-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="881d8-149">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ GL \_ MAP2 \_ домен Grid</span><span class="sxs-lookup"><span data-stu-id="881d8-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="881d8-150">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументами \_ \_ сегментами сетки GL «Карта1» \_</span><span class="sxs-lookup"><span data-stu-id="881d8-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>  
<span data-ttu-id="881d8-151">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументами \_ \_ сегментами сетки GL MAP2 \_</span><span class="sxs-lookup"><span data-stu-id="881d8-151">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="881d8-152">Требования</span><span class="sxs-lookup"><span data-stu-id="881d8-152">Requirements</span></span>



| <span data-ttu-id="881d8-153">Требование</span><span class="sxs-lookup"><span data-stu-id="881d8-153">Requirement</span></span> | <span data-ttu-id="881d8-154">Значение</span><span class="sxs-lookup"><span data-stu-id="881d8-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="881d8-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="881d8-155">Minimum supported client</span></span><br/> | <span data-ttu-id="881d8-156">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="881d8-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="881d8-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="881d8-157">Minimum supported server</span></span><br/> | <span data-ttu-id="881d8-158">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="881d8-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="881d8-159">Заголовок</span><span class="sxs-lookup"><span data-stu-id="881d8-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="881d8-160"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="881d8-160"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="881d8-161">Библиотека</span><span class="sxs-lookup"><span data-stu-id="881d8-161">Library</span></span><br/>                  | <dl> <span data-ttu-id="881d8-162"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="881d8-162"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="881d8-163">DLL</span><span class="sxs-lookup"><span data-stu-id="881d8-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="881d8-164"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="881d8-164"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="881d8-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="881d8-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="881d8-166">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="881d8-166">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="881d8-167">**гленд**</span><span class="sxs-lookup"><span data-stu-id="881d8-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="881d8-168">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="881d8-168">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="881d8-169">глевалмеш</span><span class="sxs-lookup"><span data-stu-id="881d8-169">glEvalMesh</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="881d8-170">**глевалпоинт**</span><span class="sxs-lookup"><span data-stu-id="881d8-170">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="881d8-171">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="881d8-171">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="881d8-172">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="881d8-172">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





