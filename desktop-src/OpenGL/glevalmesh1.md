---
title: Функция glEvalMesh1 (GL. h)
description: Вычисление одномерной сетки точек или линий.
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
keywords:
- Функция glEvalMesh1 OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8950dcf397816fca8eb5a6add45c45512c48866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534481"
---
# <a name="glevalmesh1-function"></a><span data-ttu-id="9f62e-104">Функция glEvalMesh1</span><span class="sxs-lookup"><span data-stu-id="9f62e-104">glEvalMesh1 function</span></span>

<span data-ttu-id="9f62e-105">Вычисление одномерной сетки точек или линий.</span><span class="sxs-lookup"><span data-stu-id="9f62e-105">Computes a one-dimensional grid of points or lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f62e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f62e-106">Syntax</span></span>


```C++
void WINAPI glEvalMesh1(
   GLenum mode,
   GLint  i1,
   GLint  i2
);
```



## <a name="parameters"></a><span data-ttu-id="9f62e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f62e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f62e-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="9f62e-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="9f62e-109">Значение типа, указывающее, следует ли вычислять одномерный сетку точек или линий.</span><span class="sxs-lookup"><span data-stu-id="9f62e-109">A value that specifies whether to compute a one-dimensional mesh of points or lines.</span></span> <span data-ttu-id="9f62e-110">Следующие символьные константы принимаются: GL \_ и \_ строка GL.</span><span class="sxs-lookup"><span data-stu-id="9f62e-110">The following symbolic constants are accepted: GL\_POINT and GL\_LINE.</span></span>

</dd> <dt>

<span data-ttu-id="9f62e-111">*I1*</span><span class="sxs-lookup"><span data-stu-id="9f62e-111">*i1*</span></span> 
</dt> <dd>

<span data-ttu-id="9f62e-112">Первое целое значение для переменной домена сетки i.</span><span class="sxs-lookup"><span data-stu-id="9f62e-112">The first integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="9f62e-113">*I2*</span><span class="sxs-lookup"><span data-stu-id="9f62e-113">*i2*</span></span> 
</dt> <dd>

<span data-ttu-id="9f62e-114">Последнее целочисленное значение для переменной домена сетки i.</span><span class="sxs-lookup"><span data-stu-id="9f62e-114">The last integer value for grid domain variable i.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f62e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f62e-115">Return value</span></span>

<span data-ttu-id="9f62e-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9f62e-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9f62e-117">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="9f62e-117">Error codes</span></span>

<span data-ttu-id="9f62e-118">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="9f62e-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9f62e-119">Имя</span><span class="sxs-lookup"><span data-stu-id="9f62e-119">Name</span></span>                                                                                                  | <span data-ttu-id="9f62e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9f62e-120">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9f62e-121"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="9f62e-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="9f62e-122">Указывает, что *режим* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="9f62e-122">Indicates that *mode* is not an accepted value.</span></span> <br/>                                                                            |
| <dl> <span data-ttu-id="9f62e-123"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="9f62e-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9f62e-124">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9f62e-124">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="9f62e-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f62e-125">Remarks</span></span>

<span data-ttu-id="9f62e-126">Используйте [**глмапгрид**](glmapgrid-functions.md) и [**глевалмеш**](glevalmesh-functions.md) вместе для эффективного создания и вычисления ряда значений домена с равными интервалами.</span><span class="sxs-lookup"><span data-stu-id="9f62e-126">Use [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) together to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="9f62e-127">Функция **глевалмеш** выполняет шаг с целым доменом одномерной или двухмерной сетки, диапазон которого представляет собой домен карт оценки, заданных в [**glMap1**](glmap1.md) и [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="9f62e-127">The **glEvalMesh** function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="9f62e-128">Параметр mode определяет, соединяются ли результирующие вершины как точки, линии или закрашенные многоугольники.</span><span class="sxs-lookup"><span data-stu-id="9f62e-128">The mode parameter determines whether the resulting vertices are connected as points, lines, or filled polygons.</span></span>

<span data-ttu-id="9f62e-129">В одномерном варианте **glEvalMesh1** сетка формируется так, как если бы выполнялся следующий фрагмент кода:</span><span class="sxs-lookup"><span data-stu-id="9f62e-129">In the one-dimensional case, **glEvalMesh1**, the mesh is generated as if the following code fragment were executed:</span></span>

<span data-ttu-id="9f62e-130">[**глбегин**](glbegin.md)(*тип*);</span><span class="sxs-lookup"><span data-stu-id="9f62e-130">[**glBegin**](glbegin.md)(*type*);</span></span>

<span data-ttu-id="9f62e-131">для (i = I1; я <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="9f62e-131">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="9f62e-132">{</span><span class="sxs-lookup"><span data-stu-id="9f62e-132">{</span></span>

<span data-ttu-id="9f62e-133">[**glEvalCoord1**](glevalcoord1d.md)(i? u + U1)</span><span class="sxs-lookup"><span data-stu-id="9f62e-133">[**glEvalCoord1**](glevalcoord1d.md)(i?u + u1)</span></span>

<span data-ttu-id="9f62e-134">}</span><span class="sxs-lookup"><span data-stu-id="9f62e-134">}</span></span>

<span data-ttu-id="9f62e-135">[**гленд**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="9f62e-135">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="9f62e-136">where</span><span class="sxs-lookup"><span data-stu-id="9f62e-136">where</span></span>

<span data-ttu-id="9f62e-137">? u = (U2 U1)/n</span><span class="sxs-lookup"><span data-stu-id="9f62e-137">?u = (u2 u1) / n</span></span>

<span data-ttu-id="9f62e-138">и n, U1 и U2 являются аргументами самой последней функции [**glMapGrid1**](glmapgrid1d.md) .</span><span class="sxs-lookup"><span data-stu-id="9f62e-138">and n, u1, and u2 are the arguments to the most recent [**glMapGrid1**](glmapgrid1d.md) function.</span></span> <span data-ttu-id="9f62e-139">Параметр *типа* — это \_ баллы GL, если режим является \_ точкой GL, или \_ строками GL, если режимом является \_ строка GL.</span><span class="sxs-lookup"><span data-stu-id="9f62e-139">The *type* parameter is GL\_POINTS if mode is GL\_POINT, or GL\_LINES if mode is GL\_LINE.</span></span> <span data-ttu-id="9f62e-140">Одно абсолютное числовое требование состоит в том, что если i = n, то значение, вычисленное от i? u + U1, равно U2.</span><span class="sxs-lookup"><span data-stu-id="9f62e-140">The one absolute numeric requirement is that if i = n, then the value computed from i?u + u1 is exactly u2.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f62e-141">Требования</span><span class="sxs-lookup"><span data-stu-id="9f62e-141">Requirements</span></span>



| <span data-ttu-id="9f62e-142">Требование</span><span class="sxs-lookup"><span data-stu-id="9f62e-142">Requirement</span></span> | <span data-ttu-id="9f62e-143">Значение</span><span class="sxs-lookup"><span data-stu-id="9f62e-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f62e-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f62e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9f62e-145">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f62e-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9f62e-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f62e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9f62e-147">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f62e-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9f62e-148">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9f62e-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f62e-149"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f62e-149"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9f62e-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f62e-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f62e-151"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f62e-151"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9f62e-152">DLL</span><span class="sxs-lookup"><span data-stu-id="9f62e-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f62e-153"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f62e-153"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f62e-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f62e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f62e-155">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="9f62e-155">**glBegin**</span></span>](glbegin.md)
</dt> </dl>

 

 





