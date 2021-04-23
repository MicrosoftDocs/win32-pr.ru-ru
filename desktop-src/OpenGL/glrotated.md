---
title: Функция Глротатед (GL. h)
description: Функция Глротатед Умножает текущую матрицу на матрицу вращения.
ms.assetid: 9adfeb5b-8c2a-4acf-a251-6ba23cc4c3a6
keywords:
- Функция Глротатед OpenGL
topic_type:
- apiref
api_name:
- glRotated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d0678e9da6f0b68047708f45fda1c9da66d8139
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535417"
---
# <a name="glrotated-function"></a><span data-ttu-id="786d1-104">Функция Глротатед</span><span class="sxs-lookup"><span data-stu-id="786d1-104">glRotated function</span></span>

<span data-ttu-id="786d1-105">Функция **глротатед** Умножает текущую матрицу на матрицу вращения.</span><span class="sxs-lookup"><span data-stu-id="786d1-105">The **glRotated** function multiplies the current matrix by a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="786d1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="786d1-106">Syntax</span></span>


```C++
void WINAPI glRotated(
   GLdouble angle,
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="786d1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="786d1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="786d1-108">*angle*</span><span class="sxs-lookup"><span data-stu-id="786d1-108">*angle*</span></span> 
</dt> <dd>

<span data-ttu-id="786d1-109">Угол поворота (в градусах).</span><span class="sxs-lookup"><span data-stu-id="786d1-109">The angle of rotation, in degrees.</span></span>

</dd> <dt>

<span data-ttu-id="786d1-110">*x*</span><span class="sxs-lookup"><span data-stu-id="786d1-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="786d1-111">Координата *x* вектора.</span><span class="sxs-lookup"><span data-stu-id="786d1-111">The *x* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="786d1-112">*y*</span><span class="sxs-lookup"><span data-stu-id="786d1-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="786d1-113">Координата *y* вектора.</span><span class="sxs-lookup"><span data-stu-id="786d1-113">The *y* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="786d1-114">*гармошкой*</span><span class="sxs-lookup"><span data-stu-id="786d1-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="786d1-115">Координата *z* вектора.</span><span class="sxs-lookup"><span data-stu-id="786d1-115">The *z* coordinate of a vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="786d1-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="786d1-116">Return value</span></span>

<span data-ttu-id="786d1-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="786d1-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="786d1-118">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="786d1-118">Error codes</span></span>

<span data-ttu-id="786d1-119">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="786d1-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="786d1-120">Имя</span><span class="sxs-lookup"><span data-stu-id="786d1-120">Name</span></span>                                                                                                  | <span data-ttu-id="786d1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="786d1-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="786d1-122"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="786d1-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="786d1-123">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="786d1-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="786d1-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="786d1-124">Remarks</span></span>

<span data-ttu-id="786d1-125">Функция **глротатед** выдает матрицу, которая выполняет поворот *угла* в градусах против часовой стрелки относительно вектора от начала координат до точки (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="786d1-125">The **glRotated** function computes a matrix that performs a counterclockwise rotation of *angle* degrees about the vector from the origin through the point (*x*, *y*, *z*).</span></span>

<span data-ttu-id="786d1-126">Текущая матрица (см. [**глматриксмоде**](glmatrixmode.md)) умножается на эту матрицу вращения, при этом продукт заменяется текущей матрицей.</span><span class="sxs-lookup"><span data-stu-id="786d1-126">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this rotation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="786d1-127">То есть, если M — это текущая матрица, а R — матрица перевода, то M заменяется на M R.</span><span class="sxs-lookup"><span data-stu-id="786d1-127">That is, if M is the current matrix and R is the translation matrix, then M is replaced with M   R.</span></span>

<span data-ttu-id="786d1-128">Если режим матрицы — GL \_ моделвиев или GL \_ , то вызывается поворот всех объектов, нарисованных после **глротатед** .</span><span class="sxs-lookup"><span data-stu-id="786d1-128">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glRotated** is called are rotated.</span></span> <span data-ttu-id="786d1-129">Используйте [**глпушматрикс**](glpushmatrix.md) и [**глпопматрикс**](glpopmatrix.md) , чтобы сохранить и восстановить повернутую систему координат.</span><span class="sxs-lookup"><span data-stu-id="786d1-129">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unrotated coordinate system.</span></span>

<span data-ttu-id="786d1-130">Следующие функции извлекают сведения, относящиеся к **глротатед**:</span><span class="sxs-lookup"><span data-stu-id="786d1-130">The following functions retrieve information related to **glRotated**:</span></span>

<span data-ttu-id="786d1-131">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ режим рендеринга GL \_</span><span class="sxs-lookup"><span data-stu-id="786d1-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

<span data-ttu-id="786d1-132">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в \_ режиме матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="786d1-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="786d1-133">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ МОДЕЛВИЕВ \_ Матрица GL</span><span class="sxs-lookup"><span data-stu-id="786d1-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="786d1-134">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ матрица проекции главной книги \_</span><span class="sxs-lookup"><span data-stu-id="786d1-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="786d1-135">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ \_ Матрица текстуры GL</span><span class="sxs-lookup"><span data-stu-id="786d1-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="786d1-136">Требования</span><span class="sxs-lookup"><span data-stu-id="786d1-136">Requirements</span></span>



| <span data-ttu-id="786d1-137">Требование</span><span class="sxs-lookup"><span data-stu-id="786d1-137">Requirement</span></span> | <span data-ttu-id="786d1-138">Значение</span><span class="sxs-lookup"><span data-stu-id="786d1-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="786d1-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="786d1-139">Minimum supported client</span></span><br/> | <span data-ttu-id="786d1-140">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="786d1-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="786d1-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="786d1-141">Minimum supported server</span></span><br/> | <span data-ttu-id="786d1-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="786d1-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="786d1-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="786d1-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="786d1-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="786d1-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="786d1-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="786d1-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="786d1-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="786d1-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="786d1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="786d1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="786d1-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="786d1-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="786d1-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="786d1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="786d1-150">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="786d1-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="786d1-151">**гленд**</span><span class="sxs-lookup"><span data-stu-id="786d1-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="786d1-152">**глматриксмоде**</span><span class="sxs-lookup"><span data-stu-id="786d1-152">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="786d1-153">**глмултматрикс**</span><span class="sxs-lookup"><span data-stu-id="786d1-153">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="786d1-154">**глпопматрикс**</span><span class="sxs-lookup"><span data-stu-id="786d1-154">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="786d1-155">**глпушматрикс**</span><span class="sxs-lookup"><span data-stu-id="786d1-155">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="786d1-156">**глскале**</span><span class="sxs-lookup"><span data-stu-id="786d1-156">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="786d1-157">**глтранслате**</span><span class="sxs-lookup"><span data-stu-id="786d1-157">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





