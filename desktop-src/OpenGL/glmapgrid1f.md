---
title: Функция glMapGrid1f (GL. h)
description: Определяет одномерный сетку. | Функция glMapGrid1f (GL. h)
ms.assetid: 242c0197-2fa6-4356-b536-627660ebd3a7
keywords:
- Функция glMapGrid1f OpenGL
topic_type:
- apiref
api_name:
- glMapGrid1f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75479e8e25098fbfc5b906ba1785913cba9f2e30
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684834"
---
# <a name="glmapgrid1f-function"></a><span data-ttu-id="65832-105">Функция glMapGrid1f</span><span class="sxs-lookup"><span data-stu-id="65832-105">glMapGrid1f function</span></span>

<span data-ttu-id="65832-106">Определяет одномерный сетку.</span><span class="sxs-lookup"><span data-stu-id="65832-106">Defines a one-dimensional mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="65832-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65832-107">Syntax</span></span>


```C++
void WINAPI glMapGrid1f(
   GLint   un,
   GLfloat u1,
   GLfloat u2
);
```



## <a name="parameters"></a><span data-ttu-id="65832-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="65832-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65832-109">*понижен*</span><span class="sxs-lookup"><span data-stu-id="65832-109">*un*</span></span> 
</dt> <dd>

<span data-ttu-id="65832-110">Число секций в диапазоне диапазонов сетки \[ : U1, U2 \] .</span><span class="sxs-lookup"><span data-stu-id="65832-110">The number of partitions in the grid range interval \[u1, u2\].</span></span> <span data-ttu-id="65832-111">Это значение должно быть положительным.</span><span class="sxs-lookup"><span data-stu-id="65832-111">This value must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="65832-112">*U1*</span><span class="sxs-lookup"><span data-stu-id="65832-112">*u1*</span></span> 
</dt> <dd>

<span data-ttu-id="65832-113">Значение, используемое в качестве сопоставления для значения домена целочисленной сетки i = 0.</span><span class="sxs-lookup"><span data-stu-id="65832-113">A value used as the mapping for integer grid domain value i = 0.</span></span>

</dd> <dt>

<span data-ttu-id="65832-114">*U2*</span><span class="sxs-lookup"><span data-stu-id="65832-114">*u2*</span></span> 
</dt> <dd>

<span data-ttu-id="65832-115">Значение, используемое в качестве сопоставления для значения домена целочисленной сетки i = un.</span><span class="sxs-lookup"><span data-stu-id="65832-115">A value used as the mapping for integer grid domain value i = un.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65832-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65832-116">Return value</span></span>

<span data-ttu-id="65832-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="65832-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="65832-118">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="65832-118">Error codes</span></span>

<span data-ttu-id="65832-119">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="65832-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="65832-120">Имя</span><span class="sxs-lookup"><span data-stu-id="65832-120">Name</span></span>                                                                                                  | <span data-ttu-id="65832-121">Значение</span><span class="sxs-lookup"><span data-stu-id="65832-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="65832-122"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="65832-122"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="65832-123">Либо *un* , либо *VN* не были положительными.</span><span class="sxs-lookup"><span data-stu-id="65832-123">Either *un* or *vn* was not positive.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="65832-124"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="65832-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="65832-125">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="65832-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="65832-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65832-126">Remarks</span></span>

<span data-ttu-id="65832-127">Функции **глмапгрид** и [глевалмеш](glevalmesh-functions.md) используются совместно для эффективного создания и вычисления ряда значений домена сопоставлений с равными пробелами.</span><span class="sxs-lookup"><span data-stu-id="65832-127">The **glMapGrid** and [glEvalMesh](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="65832-128">Функция Глевалмеш выполняет шаг с целым доменом одномерной или двухмерной сетки, диапазон которого представляет собой домен карт оценки, заданных в [**glMap1**](glmap1.md) и [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="65832-128">The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="65832-129">Функции [**glMapGrid1**](glmapgrid1d.md) и [**glMapGrid2**](glmapgrid2d.md) определяют сопоставления линейной сетки между координатами сетки i (или i и j) целого числа с координатами карты вычисления числа с плавающей запятой u (или a и v).</span><span class="sxs-lookup"><span data-stu-id="65832-129">The [**glMapGrid1**](glmapgrid1d.md) and [**glMapGrid2**](glmapgrid2d.md) functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates.</span></span> <span data-ttu-id="65832-130">Сведения о том, как оцениваются координаты, см. в разделе [**glMap1**](glmap1.md) и [**glMap2**](glmap2.md) .</span><span class="sxs-lookup"><span data-stu-id="65832-130">See [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md) for details of how u and v coordinates are evaluated.</span></span>

<span data-ttu-id="65832-131">Функция [**glMapGrid1**](glmapgrid1d.md) задает одно линейное сопоставление таким, *что координата* целочисленной сетки 0 сопоставляется только с U1, а целочисленная сетка целых чисел отменяет сопоставление ровно с *U2*.</span><span class="sxs-lookup"><span data-stu-id="65832-131">The [**glMapGrid1**](glmapgrid1d.md) function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate *un* maps exactly to *u2*.</span></span> <span data-ttu-id="65832-132">Все остальные координаты целочисленной сетки *я* сопоставил таким образом, что:</span><span class="sxs-lookup"><span data-stu-id="65832-132">All other integer grid coordinates *i* are mapped such that:</span></span>

<span data-ttu-id="65832-133">*u = i (U2 U1)/Ун + U1*</span><span class="sxs-lookup"><span data-stu-id="65832-133">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="65832-134">Функция [**glMapGrid2**](glmapgrid2d.md) указывает два таких линейных сопоставления.</span><span class="sxs-lookup"><span data-stu-id="65832-134">The [**glMapGrid2**](glmapgrid2d.md) function specifies two such linear mappings.</span></span> <span data-ttu-id="65832-135">Одна карта сопоставляет целочисленную сетку *i = 0* ровно с *U1*, а целочисленная сетка — координата *i =* в точности до *U2*.</span><span class="sxs-lookup"><span data-stu-id="65832-135">One maps integer grid coordinate *i = 0* exactly to *u1*, and integer grid coordinate *i = un* exactly to *u2*.</span></span> <span data-ttu-id="65832-136">Вторая сопоставляет сетку целых чисел *j = 0* ровно с *v1*, а целочисленная сетка с координатами « *j = VN» —* только *v2*.</span><span class="sxs-lookup"><span data-stu-id="65832-136">The other maps integer grid coordinate *j = 0* exactly to *v1*, and integer grid coordinate *j = vn* exactly to *v2*.</span></span> <span data-ttu-id="65832-137">Другие координаты целочисленных сеток i и j сопоставлены таким, что</span><span class="sxs-lookup"><span data-stu-id="65832-137">Other integer grid coordinates i and j are mapped such that</span></span>

<span data-ttu-id="65832-138">*u = i (U2 U1)/Ун + U1*</span><span class="sxs-lookup"><span data-stu-id="65832-138">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="65832-139">*v = j (V2 v1)/VN + v1*</span><span class="sxs-lookup"><span data-stu-id="65832-139">*v = j (v2 v1)/vn + v1*</span></span>

<span data-ttu-id="65832-140">Сопоставления, заданные параметром [**глмапгрид**](glmapgrid1d.md) , используются одинаково в [глевалмеш](glevalmesh-functions.md) и [**глевалпоинт**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="65832-140">The mappings specified by [**glMapGrid**](glmapgrid1d.md) are used identically by [glEvalMesh](glevalmesh-functions.md) and [**glEvalPoint**](glevalpoint.md).</span></span>

<span data-ttu-id="65832-141">Следующие функции извлекают сведения, относящиеся к [**глмапгрид**](glmapgrid1d.md):</span><span class="sxs-lookup"><span data-stu-id="65832-141">The following functions retrieve information related to [**glMapGrid**](glmapgrid1d.md):</span></span>

<dl>

<span data-ttu-id="65832-142">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ GL \_ «Карта1» \_ домен Grid</span><span class="sxs-lookup"><span data-stu-id="65832-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="65832-143">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ GL \_ MAP2 \_ домен Grid</span><span class="sxs-lookup"><span data-stu-id="65832-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="65832-144">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументами \_ \_ сегментами сетки GL «Карта1» \_</span><span class="sxs-lookup"><span data-stu-id="65832-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>  
<span data-ttu-id="65832-145">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументами \_ \_ сегментами сетки GL MAP2 \_</span><span class="sxs-lookup"><span data-stu-id="65832-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="65832-146">Требования</span><span class="sxs-lookup"><span data-stu-id="65832-146">Requirements</span></span>



| <span data-ttu-id="65832-147">Требование</span><span class="sxs-lookup"><span data-stu-id="65832-147">Requirement</span></span> | <span data-ttu-id="65832-148">Значение</span><span class="sxs-lookup"><span data-stu-id="65832-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65832-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65832-149">Minimum supported client</span></span><br/> | <span data-ttu-id="65832-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="65832-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="65832-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65832-151">Minimum supported server</span></span><br/> | <span data-ttu-id="65832-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="65832-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65832-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="65832-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="65832-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="65832-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="65832-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="65832-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="65832-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65832-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="65832-157">DLL</span><span class="sxs-lookup"><span data-stu-id="65832-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65832-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65832-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65832-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65832-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65832-160">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="65832-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="65832-161">**гленд**</span><span class="sxs-lookup"><span data-stu-id="65832-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="65832-162">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="65832-162">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="65832-163">глевалмеш</span><span class="sxs-lookup"><span data-stu-id="65832-163">glEvalMesh</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="65832-164">**глевалпоинт**</span><span class="sxs-lookup"><span data-stu-id="65832-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="65832-165">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="65832-165">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="65832-166">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="65832-166">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





