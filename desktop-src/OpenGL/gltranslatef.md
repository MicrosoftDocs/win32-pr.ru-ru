---
title: Функция Глтранслатеф (GL. h)
description: Функция Глтранслатеф Умножает текущую матрицу на матрицу перевода.
ms.assetid: 2354ad52-e80f-49fc-82e7-ac6c146aa59d
keywords:
- Функция Глтранслатеф OpenGL
topic_type:
- apiref
api_name:
- glTranslatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5b52c3890b70ecb931211af1788afe2b8e6ad4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "103914007"
---
# <a name="gltranslatef-function"></a><span data-ttu-id="a5ff8-104">Функция Глтранслатеф</span><span class="sxs-lookup"><span data-stu-id="a5ff8-104">glTranslatef function</span></span>

<span data-ttu-id="a5ff8-105">Функция [**глтранслатеф**](gltranslate.md) Умножает текущую матрицу на матрицу перевода.</span><span class="sxs-lookup"><span data-stu-id="a5ff8-105">The [**glTranslatef**](gltranslate.md) function multiplies the current matrix by a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5ff8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5ff8-106">Syntax</span></span>


```C++
void WINAPI glTranslatef(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a><span data-ttu-id="a5ff8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5ff8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5ff8-108">*x*</span><span class="sxs-lookup"><span data-stu-id="a5ff8-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="a5ff8-109">Координата *x* вектора перевода.</span><span class="sxs-lookup"><span data-stu-id="a5ff8-109">The *x* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="a5ff8-110">*y*</span><span class="sxs-lookup"><span data-stu-id="a5ff8-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="a5ff8-111">Координата *y* вектора перевода.</span><span class="sxs-lookup"><span data-stu-id="a5ff8-111">The *y* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="a5ff8-112">*гармошкой*</span><span class="sxs-lookup"><span data-stu-id="a5ff8-112">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="a5ff8-113">Координата *z* вектора перевода.</span><span class="sxs-lookup"><span data-stu-id="a5ff8-113">The *z* coordinate of a translation vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5ff8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5ff8-114">Return value</span></span>

<span data-ttu-id="a5ff8-115">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a5ff8-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5ff8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5ff8-116">Remarks</span></span>

<span data-ttu-id="a5ff8-117">Функция **глтранслатеф** создает перевод, указанный в (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="a5ff8-117">The **glTranslatef** function produces the translation specified by (*x*, *y*, *z*).</span></span> <span data-ttu-id="a5ff8-118">Вектор перевода используется для расчета матрицы перевода 4x4:</span><span class="sxs-lookup"><span data-stu-id="a5ff8-118">The translation vector is used to compute a 4x4 translation matrix:</span></span>

![Схема, показывающая матрицу перевода 4x4, указанную x, y, z.](images/trans01.png)

<span data-ttu-id="a5ff8-120">Текущая матрица (см. [**глматриксмоде**](glmatrixmode.md)) умножается на эту матрицу преобразования, при этом продукт заменяется текущей матрицей.</span><span class="sxs-lookup"><span data-stu-id="a5ff8-120">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this translation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="a5ff8-121">То есть, если M — это текущая матрица, а T — матрица перевода, то M заменяется на M T.</span><span class="sxs-lookup"><span data-stu-id="a5ff8-121">That is, if M is the current matrix and T is the translation matrix, then M is replaced with M T.</span></span>

<span data-ttu-id="a5ff8-122">Если режим матрицы — GL \_ моделвиев или GL \_ , то будут переведены все объекты, нарисованные после **глтранслатеф** .</span><span class="sxs-lookup"><span data-stu-id="a5ff8-122">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glTranslatef** is called are translated.</span></span> <span data-ttu-id="a5ff8-123">Используйте [**глпушматрикс**](glpushmatrix.md) и **глпопматрикс** для сохранения и восстановления непреобразованной системы координат.</span><span class="sxs-lookup"><span data-stu-id="a5ff8-123">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the untranslated coordinate system.</span></span>

<span data-ttu-id="a5ff8-124">Следующие функции извлекают сведения, относящиеся к [**глтранслатед**](gltranslate.md) и **глтранслатеф**:</span><span class="sxs-lookup"><span data-stu-id="a5ff8-124">The following functions retrieve information related to [**glTranslated**](gltranslate.md) and **glTranslatef**:</span></span>

<span data-ttu-id="a5ff8-125">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в \_ режиме матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="a5ff8-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="a5ff8-126">**глжет** с аргументом \_ МОДЕЛВИЕВ \_ Матрица GL</span><span class="sxs-lookup"><span data-stu-id="a5ff8-126">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="a5ff8-127">**глжет** с аргументом \_ матрица проекции главной книги \_</span><span class="sxs-lookup"><span data-stu-id="a5ff8-127">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="a5ff8-128">**глжет** с аргументом \_ \_ Матрица текстуры GL</span><span class="sxs-lookup"><span data-stu-id="a5ff8-128">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="a5ff8-129">Требования</span><span class="sxs-lookup"><span data-stu-id="a5ff8-129">Requirements</span></span>



| <span data-ttu-id="a5ff8-130">Требование</span><span class="sxs-lookup"><span data-stu-id="a5ff8-130">Requirement</span></span> | <span data-ttu-id="a5ff8-131">Значение</span><span class="sxs-lookup"><span data-stu-id="a5ff8-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5ff8-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5ff8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a5ff8-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a5ff8-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a5ff8-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5ff8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a5ff8-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a5ff8-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a5ff8-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a5ff8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5ff8-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5ff8-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a5ff8-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a5ff8-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5ff8-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5ff8-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a5ff8-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a5ff8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5ff8-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5ff8-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5ff8-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5ff8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5ff8-143">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="a5ff8-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a5ff8-144">**гленд**</span><span class="sxs-lookup"><span data-stu-id="a5ff8-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a5ff8-145">**глматриксмоде**</span><span class="sxs-lookup"><span data-stu-id="a5ff8-145">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="a5ff8-146">**глмултматрикс**</span><span class="sxs-lookup"><span data-stu-id="a5ff8-146">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="a5ff8-147">**глпушматрикс**</span><span class="sxs-lookup"><span data-stu-id="a5ff8-147">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="a5ff8-148">**глротате**</span><span class="sxs-lookup"><span data-stu-id="a5ff8-148">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="a5ff8-149">**глскале**</span><span class="sxs-lookup"><span data-stu-id="a5ff8-149">**glScale**</span></span>](glscale.md)
</dt> </dl>

 

 





