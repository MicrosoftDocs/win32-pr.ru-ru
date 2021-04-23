---
title: Функция Глжетмапфв (GL. h)
description: Функции Глжетмапдв, Глжетмапфв и Глжетмапив возвращают параметры оценщика. | Функция Глжетмапфв (GL. h)
ms.assetid: dc93e468-7b76-4b5d-a46c-63920ed05568
keywords:
- Функция Глжетмапфв OpenGL
topic_type:
- apiref
api_name:
- glGetMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02129e9637333fb36265ce9f7b631d6cb3377d0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684866"
---
# <a name="glgetmapfv-function"></a><span data-ttu-id="535b5-105">Функция Глжетмапфв</span><span class="sxs-lookup"><span data-stu-id="535b5-105">glGetMapfv function</span></span>

<span data-ttu-id="535b5-106">Функции [**глжетмапдв**](glgetmapdv.md), **глжетмапфв** и [**глжетмапив**](glgetmapiv.md) возвращают параметры оценщика.</span><span class="sxs-lookup"><span data-stu-id="535b5-106">The [**glGetMapdv**](glgetmapdv.md), **glGetMapfv**, and [**glGetMapiv**](glgetmapiv.md) functions return evaluator parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="535b5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="535b5-107">Syntax</span></span>


```C++
void WINAPI glGetMapfv(
   GLenum  target,
   GLenum  query,
   GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="535b5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="535b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="535b5-109">*target*</span><span class="sxs-lookup"><span data-stu-id="535b5-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="535b5-110">Символическое имя объекта Map.</span><span class="sxs-lookup"><span data-stu-id="535b5-110">The symbolic name of a map.</span></span> <span data-ttu-id="535b5-111">Ниже приведены допустимые значения: GL \_ «Карта1» \_ Color \_ 4, GL \_ «Карта1» \_ index, GL \_ «Карта1» \_ нормаль, GL \_ «Карта1» \_ текстура \_ курд \_ 1, GL \_ «Карта1» \_ текстура \_ курд \_ 2, GL \_ «Карта1» \_ текстура \_ курд \_ 3, GL \_ «Карта1» \_ текстура \_ курд \_ 4, GL \_ «Карта1» \_ вершина \_ , GL \_ «Карта1» \_ вершина \_ , GL \_ MAP2 \_ Color \_ 4, ГК MAP2 \_ \_ index, GL \_ MAP2 \_ Обычная, GL MAP2 текстуры курд 1, GL MAP2 текстуры курд 2, GL MAP2 текстура курд 3, GL MAP2 текстуры \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ курд \_ 4, GL \_ MAP2 \_ вершина \_ и GL \_ MAP2 \_ Vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="535b5-111">The following are accepted values: GL\_MAP1\_COLOR\_4, GL\_MAP1\_INDEX, GL\_MAP1\_NORMAL, GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP1\_VERTEX\_3, GL\_MAP1\_VERTEX\_4, GL\_MAP2\_COLOR\_4, GL\_MAP2\_INDEX, GL\_MAP2\_NORMAL, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, GL\_MAP2\_TEXTURE\_COORD\_4, GL\_MAP2\_VERTEX\_3, and GL\_MAP2\_VERTEX\_4.</span></span>

</dd> <dt>

<span data-ttu-id="535b5-112">*запрос*</span><span class="sxs-lookup"><span data-stu-id="535b5-112">*query*</span></span> 
</dt> <dd>

<span data-ttu-id="535b5-113">Указывает возвращаемый параметр.</span><span class="sxs-lookup"><span data-stu-id="535b5-113">Specifies which parameter to return.</span></span> <span data-ttu-id="535b5-114">Допустимы следующие символьные имена.</span><span class="sxs-lookup"><span data-stu-id="535b5-114">The following symbolic names are accepted.</span></span>



| <span data-ttu-id="535b5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="535b5-115">Value</span></span>                                                                                                                                             | <span data-ttu-id="535b5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="535b5-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <span data-ttu-id="535b5-117"><dt>**\_КОЕФФ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="535b5-117"><dt>**GL\_COEFF**</dt></span></span> </dl>    | <span data-ttu-id="535b5-118">Параметр *v* возвращает контрольные точки для функции оценщика.</span><span class="sxs-lookup"><span data-stu-id="535b5-118">The *v* parameter returns the control points for the evaluator function.</span></span> <span data-ttu-id="535b5-119">Одномерные средства оценки возвращают контрольные точки, а двухмерные оценивающие *возвращают* контрольные точки *Уордер* *x* *вордер* .</span><span class="sxs-lookup"><span data-stu-id="535b5-119">One-dimensional evaluators return *order* control points, and two-dimensional evaluators return *uorder* *x* *vorder* control points.</span></span> <span data-ttu-id="535b5-120">Каждая контрольная точка состоит из одного, двух, трех или четырех целочисленных значений с плавающей запятой одиночной точности или двойной точности, в зависимости от типа оценщика.</span><span class="sxs-lookup"><span data-stu-id="535b5-120">Each control point consists of one, two, three, or four integer, single-precision floating-point, or double-precision floating-point values, depending on the type of the evaluator.</span></span> <span data-ttu-id="535b5-121">Двумерные контрольные точки возвращаются в основном порядке строк, быстро увеличивают индекс *Уордер* и индекс *вордер* после каждой строки.</span><span class="sxs-lookup"><span data-stu-id="535b5-121">Two-dimensional control points are returned in row-major order, incrementing the *uorder* index quickly, and the *vorder* index after each row.</span></span> <span data-ttu-id="535b5-122">При запросе целочисленные значения вычисляются путем округления внутренних значений с плавающей запятой до ближайших целочисленных значений.</span><span class="sxs-lookup"><span data-stu-id="535b5-122">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <span data-ttu-id="535b5-123"><dt>**заказ в ГК \_**</dt></span><span class="sxs-lookup"><span data-stu-id="535b5-123"><dt>**GL\_ORDER**</dt></span></span> </dl>    | <span data-ttu-id="535b5-124">Параметр *v* Возвращает порядок функции оценщика.</span><span class="sxs-lookup"><span data-stu-id="535b5-124">The *v* parameter returns the order of the evaluator function.</span></span> <span data-ttu-id="535b5-125">Одномерные средства оценки возвращают одно значение, *Order*.</span><span class="sxs-lookup"><span data-stu-id="535b5-125">One-dimensional evaluators return a single value, *order*.</span></span> <span data-ttu-id="535b5-126">Одномерные средства оценки возвращают два значения: *Уордер* и *вордер*.</span><span class="sxs-lookup"><span data-stu-id="535b5-126">Two-dimensional evaluators return two values, *uorder* and *vorder*.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <span data-ttu-id="535b5-127"><dt>**\_домен GL**</dt></span><span class="sxs-lookup"><span data-stu-id="535b5-127"><dt>**GL\_DOMAIN**</dt></span></span> </dl> | <span data-ttu-id="535b5-128">Параметр *v* возвращает линейные параметры сопоставления *u* и *v* .</span><span class="sxs-lookup"><span data-stu-id="535b5-128">The *v* parameter returns the linear *u* and *v* mapping parameters.</span></span> <span data-ttu-id="535b5-129">Одномерные средства оценки возвращают два значения: *u* 1 и *u* 2, как указано в [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="535b5-129">One-dimensional evaluators return two values, *u* 1 and *u* 2, as specified by [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="535b5-130">Двумерные оценивающие возвращают четыре значения (*U1*, *U2*, *v1* и *v2*), как указано в [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="535b5-130">Two-dimensional evaluators return four values (*u1*, *u2*, *v1*, and *v2*) as specified by [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="535b5-131">При запросе целочисленные значения вычисляются путем округления внутренних значений с плавающей запятой до ближайших целочисленных значений.</span><span class="sxs-lookup"><span data-stu-id="535b5-131">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="535b5-132">*3,3*</span><span class="sxs-lookup"><span data-stu-id="535b5-132">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="535b5-133">Возвращает запрошенные данные.</span><span class="sxs-lookup"><span data-stu-id="535b5-133">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="535b5-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="535b5-134">Return value</span></span>

<span data-ttu-id="535b5-135">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="535b5-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="535b5-136">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="535b5-136">Error codes</span></span>

<span data-ttu-id="535b5-137">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="535b5-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="535b5-138">Имя</span><span class="sxs-lookup"><span data-stu-id="535b5-138">Name</span></span>                                                                                                  | <span data-ttu-id="535b5-139">Значение</span><span class="sxs-lookup"><span data-stu-id="535b5-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="535b5-140"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="535b5-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="535b5-141">*целевой объект* или *запрос* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="535b5-141">*target* or *query* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="535b5-142"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="535b5-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="535b5-143">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="535b5-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="535b5-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="535b5-144">Remarks</span></span>

<span data-ttu-id="535b5-145">Функция **глжетмап** Возвращает параметры оценщика.</span><span class="sxs-lookup"><span data-stu-id="535b5-145">The **glGetMap** function returns evaluator parameters.</span></span> <span data-ttu-id="535b5-146">(Функции **glMap1** и **glMap2** определяют оценивающие.) *Целевой* параметр указывает карту, *запрос* выбирает конкретный параметр, а *v* указывает на хранилище, в котором будут возвращаться значения.</span><span class="sxs-lookup"><span data-stu-id="535b5-146">(The **glMap1** and **glMap2** functions define evaluators.) The *target* parameter specifies a map, *query* selects a specific parameter, and *v* points to storage where the values will be returned.</span></span>

<span data-ttu-id="535b5-147">Допустимые значения для *целевого* параметра описаны в [**glMap1**](glmap1.md) и [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="535b5-147">The acceptable values for the *target* parameter are described in [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="535b5-148">Если возникает ошибка, содержимое *v* не вносится никаких изменений.</span><span class="sxs-lookup"><span data-stu-id="535b5-148">If an error is generated, no change is made to the contents of *v*.</span></span>

## <a name="requirements"></a><span data-ttu-id="535b5-149">Требования</span><span class="sxs-lookup"><span data-stu-id="535b5-149">Requirements</span></span>



| <span data-ttu-id="535b5-150">Требование</span><span class="sxs-lookup"><span data-stu-id="535b5-150">Requirement</span></span> | <span data-ttu-id="535b5-151">Значение</span><span class="sxs-lookup"><span data-stu-id="535b5-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="535b5-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="535b5-152">Minimum supported client</span></span><br/> | <span data-ttu-id="535b5-153">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="535b5-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="535b5-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="535b5-154">Minimum supported server</span></span><br/> | <span data-ttu-id="535b5-155">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="535b5-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="535b5-156">Заголовок</span><span class="sxs-lookup"><span data-stu-id="535b5-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="535b5-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="535b5-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="535b5-158">Библиотека</span><span class="sxs-lookup"><span data-stu-id="535b5-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="535b5-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="535b5-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="535b5-160">DLL</span><span class="sxs-lookup"><span data-stu-id="535b5-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="535b5-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="535b5-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="535b5-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="535b5-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="535b5-163">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="535b5-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="535b5-164">**гленд**</span><span class="sxs-lookup"><span data-stu-id="535b5-164">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="535b5-165">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="535b5-165">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="535b5-166">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="535b5-166">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="535b5-167">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="535b5-167">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





