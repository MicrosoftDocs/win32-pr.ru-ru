---
title: Функция Глротатеф (GL. h)
description: Функция Глротатеф Умножает текущую матрицу на матрицу вращения.
ms.assetid: 8216a125-de8c-44e5-afb3-3d4e5ffc600d
keywords:
- Функция Глротатеф OpenGL
topic_type:
- apiref
api_name:
- glRotatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 953b8ffc5f89e5a4cf9901e4cb5fb5afb4c8dfdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493221"
---
# <a name="glrotatef-function"></a><span data-ttu-id="c9d48-104">Функция Глротатеф</span><span class="sxs-lookup"><span data-stu-id="c9d48-104">glRotatef function</span></span>

<span data-ttu-id="c9d48-105">Функция **глротатеф** Умножает текущую матрицу на матрицу вращения.</span><span class="sxs-lookup"><span data-stu-id="c9d48-105">The **glRotatef** function multiplies the current matrix by a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d48-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9d48-106">Syntax</span></span>


```C++
void WINAPI glRotatef(
   GLfloat angle,
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a><span data-ttu-id="c9d48-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9d48-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9d48-108">*angle*</span><span class="sxs-lookup"><span data-stu-id="c9d48-108">*angle*</span></span> 
</dt> <dd>

<span data-ttu-id="c9d48-109">Угол поворота (в градусах).</span><span class="sxs-lookup"><span data-stu-id="c9d48-109">The angle of rotation, in degrees.</span></span>

</dd> <dt>

<span data-ttu-id="c9d48-110">*x*</span><span class="sxs-lookup"><span data-stu-id="c9d48-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="c9d48-111">Координата *x* вектора.</span><span class="sxs-lookup"><span data-stu-id="c9d48-111">The *x* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="c9d48-112">*y*</span><span class="sxs-lookup"><span data-stu-id="c9d48-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="c9d48-113">Координата *y* вектора.</span><span class="sxs-lookup"><span data-stu-id="c9d48-113">The *y* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="c9d48-114">*гармошкой*</span><span class="sxs-lookup"><span data-stu-id="c9d48-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="c9d48-115">Координата *z* вектора.</span><span class="sxs-lookup"><span data-stu-id="c9d48-115">The *z* coordinate of a vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9d48-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9d48-116">Return value</span></span>

<span data-ttu-id="c9d48-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c9d48-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c9d48-118">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c9d48-118">Error codes</span></span>

<span data-ttu-id="c9d48-119">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="c9d48-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c9d48-120">Имя</span><span class="sxs-lookup"><span data-stu-id="c9d48-120">Name</span></span>                                                                                                  | <span data-ttu-id="c9d48-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c9d48-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9d48-122"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c9d48-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c9d48-123">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c9d48-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c9d48-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9d48-124">Remarks</span></span>

<span data-ttu-id="c9d48-125">Функция **глротатеф** выдает матрицу, которая выполняет поворот *угла* в градусах против часовой стрелки относительно вектора от начала координат до точки (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="c9d48-125">The **glRotatef** function computes a matrix that performs a counterclockwise rotation of *angle* degrees about the vector from the origin through the point (*x*, *y*, *z*).</span></span>

<span data-ttu-id="c9d48-126">Текущая матрица (см. [**глматриксмоде**](glmatrixmode.md)) умножается на эту матрицу вращения, при этом продукт заменяется текущей матрицей.</span><span class="sxs-lookup"><span data-stu-id="c9d48-126">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this rotation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="c9d48-127">То есть, если M — это текущая матрица, а R — матрица перевода, то M заменяется на M R.</span><span class="sxs-lookup"><span data-stu-id="c9d48-127">That is, if M is the current matrix and R is the translation matrix, then M is replaced with M   R.</span></span>

<span data-ttu-id="c9d48-128">Если режим матрицы — GL \_ моделвиев или GL \_ , то вызывается поворот всех объектов, нарисованных после **глротатеф** .</span><span class="sxs-lookup"><span data-stu-id="c9d48-128">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glRotatef** is called are rotated.</span></span> <span data-ttu-id="c9d48-129">Используйте [**глпушматрикс**](glpushmatrix.md) и [**глпопматрикс**](glpopmatrix.md) , чтобы сохранить и восстановить повернутую систему координат.</span><span class="sxs-lookup"><span data-stu-id="c9d48-129">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unrotated coordinate system.</span></span>

<span data-ttu-id="c9d48-130">Следующие функции извлекают сведения, относящиеся к **глротатеф**:</span><span class="sxs-lookup"><span data-stu-id="c9d48-130">The following functions retrieve information related to **glRotatef**:</span></span>

<span data-ttu-id="c9d48-131">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ режим рендеринга GL \_</span><span class="sxs-lookup"><span data-stu-id="c9d48-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

<span data-ttu-id="c9d48-132">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в \_ режиме матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="c9d48-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="c9d48-133">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ МОДЕЛВИЕВ \_ Матрица GL</span><span class="sxs-lookup"><span data-stu-id="c9d48-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="c9d48-134">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ матрица проекции главной книги \_</span><span class="sxs-lookup"><span data-stu-id="c9d48-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="c9d48-135">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ \_ Матрица текстуры GL</span><span class="sxs-lookup"><span data-stu-id="c9d48-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="c9d48-136">Требования</span><span class="sxs-lookup"><span data-stu-id="c9d48-136">Requirements</span></span>



| <span data-ttu-id="c9d48-137">Требование</span><span class="sxs-lookup"><span data-stu-id="c9d48-137">Requirement</span></span> | <span data-ttu-id="c9d48-138">Значение</span><span class="sxs-lookup"><span data-stu-id="c9d48-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d48-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9d48-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c9d48-140">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c9d48-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c9d48-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9d48-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c9d48-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c9d48-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c9d48-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c9d48-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9d48-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9d48-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c9d48-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9d48-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="c9d48-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9d48-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c9d48-147">DLL</span><span class="sxs-lookup"><span data-stu-id="c9d48-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9d48-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9d48-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9d48-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9d48-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d48-150">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="c9d48-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c9d48-151">**гленд**</span><span class="sxs-lookup"><span data-stu-id="c9d48-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c9d48-152">**глматриксмоде**</span><span class="sxs-lookup"><span data-stu-id="c9d48-152">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="c9d48-153">**глмултматрикс**</span><span class="sxs-lookup"><span data-stu-id="c9d48-153">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="c9d48-154">**глпопматрикс**</span><span class="sxs-lookup"><span data-stu-id="c9d48-154">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="c9d48-155">**глпушматрикс**</span><span class="sxs-lookup"><span data-stu-id="c9d48-155">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="c9d48-156">**глскале**</span><span class="sxs-lookup"><span data-stu-id="c9d48-156">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="c9d48-157">**глтранслате**</span><span class="sxs-lookup"><span data-stu-id="c9d48-157">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





