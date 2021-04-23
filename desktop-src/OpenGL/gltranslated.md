---
title: Функция Глтранслатед (GL. h)
description: Функция Глтранслатед Умножает текущую матрицу на матрицу перевода.
ms.assetid: 9f066a92-ee78-44d1-b8f8-0eacde0e1a47
keywords:
- Функция Глтранслатед OpenGL
topic_type:
- apiref
api_name:
- glTranslated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705c8dd0635294b066897db99c0770b5f6622c75
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105684728"
---
# <a name="gltranslated-function"></a><span data-ttu-id="94992-104">Функция Глтранслатед</span><span class="sxs-lookup"><span data-stu-id="94992-104">glTranslated function</span></span>

<span data-ttu-id="94992-105">Функция **глтранслатед** Умножает текущую матрицу на матрицу перевода.</span><span class="sxs-lookup"><span data-stu-id="94992-105">The **glTranslated** function multiplies the current matrix by a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="94992-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94992-106">Syntax</span></span>


```C++
void WINAPI glTranslated(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="94992-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="94992-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94992-108">*x*</span><span class="sxs-lookup"><span data-stu-id="94992-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="94992-109">Координата *x* вектора перевода.</span><span class="sxs-lookup"><span data-stu-id="94992-109">The *x* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="94992-110">*y*</span><span class="sxs-lookup"><span data-stu-id="94992-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="94992-111">Координата *y* вектора перевода.</span><span class="sxs-lookup"><span data-stu-id="94992-111">The *y* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="94992-112">*гармошкой*</span><span class="sxs-lookup"><span data-stu-id="94992-112">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="94992-113">Координата *z* вектора перевода.</span><span class="sxs-lookup"><span data-stu-id="94992-113">The *z* coordinate of a translation vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94992-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94992-114">Return value</span></span>

<span data-ttu-id="94992-115">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="94992-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94992-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94992-116">Remarks</span></span>

<span data-ttu-id="94992-117">Функция **глтранслатед** создает перевод, указанный в (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="94992-117">The **glTranslated** function produces the translation specified by (*x*, *y*, *z*).</span></span> <span data-ttu-id="94992-118">Вектор перевода используется для расчета матрицы перевода 4x4:</span><span class="sxs-lookup"><span data-stu-id="94992-118">The translation vector is used to compute a 4x4 translation matrix:</span></span>

![Схема, показывающая матрицу перевода 4x4, указанную x, y, z.](images/trans01.png)

<span data-ttu-id="94992-120">Текущая матрица (см. [**глматриксмоде**](glmatrixmode.md)) умножается на эту матрицу преобразования, при этом продукт заменяется текущей матрицей.</span><span class="sxs-lookup"><span data-stu-id="94992-120">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this translation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="94992-121">То есть, если M — это текущая матрица, а T — матрица перевода, то M заменяется на M T.</span><span class="sxs-lookup"><span data-stu-id="94992-121">That is, if M is the current matrix and T is the translation matrix, then M is replaced with M T.</span></span>

<span data-ttu-id="94992-122">Если режим матрицы — GL \_ моделвиев или GL \_ , то будут переведены все объекты, нарисованные после **глтранслатед** .</span><span class="sxs-lookup"><span data-stu-id="94992-122">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glTranslated** is called are translated.</span></span> <span data-ttu-id="94992-123">Используйте [**глпушматрикс**](glpushmatrix.md) и **глпопматрикс** для сохранения и восстановления непреобразованной системы координат.</span><span class="sxs-lookup"><span data-stu-id="94992-123">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the untranslated coordinate system.</span></span>

<span data-ttu-id="94992-124">Следующие функции извлекают сведения, относящиеся к [**глтранслатед**](gltranslate.md):</span><span class="sxs-lookup"><span data-stu-id="94992-124">The following functions retrieve information related to [**glTranslated**](gltranslate.md):</span></span>

<span data-ttu-id="94992-125">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом в \_ режиме матрицы GL \_</span><span class="sxs-lookup"><span data-stu-id="94992-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="94992-126">**глжет** с аргументом \_ МОДЕЛВИЕВ \_ Матрица GL</span><span class="sxs-lookup"><span data-stu-id="94992-126">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="94992-127">**глжет** с аргументом \_ матрица проекции главной книги \_</span><span class="sxs-lookup"><span data-stu-id="94992-127">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="94992-128">**глжет** с аргументом \_ \_ Матрица текстуры GL</span><span class="sxs-lookup"><span data-stu-id="94992-128">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="94992-129">Требования</span><span class="sxs-lookup"><span data-stu-id="94992-129">Requirements</span></span>



| <span data-ttu-id="94992-130">Требование</span><span class="sxs-lookup"><span data-stu-id="94992-130">Requirement</span></span> | <span data-ttu-id="94992-131">Значение</span><span class="sxs-lookup"><span data-stu-id="94992-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94992-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94992-132">Minimum supported client</span></span><br/> | <span data-ttu-id="94992-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="94992-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="94992-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94992-134">Minimum supported server</span></span><br/> | <span data-ttu-id="94992-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="94992-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="94992-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="94992-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="94992-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="94992-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="94992-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="94992-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="94992-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94992-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="94992-140">DLL</span><span class="sxs-lookup"><span data-stu-id="94992-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94992-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94992-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94992-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94992-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94992-143">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="94992-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="94992-144">**гленд**</span><span class="sxs-lookup"><span data-stu-id="94992-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="94992-145">**глматриксмоде**</span><span class="sxs-lookup"><span data-stu-id="94992-145">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="94992-146">**глмултматрикс**</span><span class="sxs-lookup"><span data-stu-id="94992-146">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="94992-147">**глпушматрикс**</span><span class="sxs-lookup"><span data-stu-id="94992-147">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="94992-148">**глротате**</span><span class="sxs-lookup"><span data-stu-id="94992-148">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="94992-149">**глскале**</span><span class="sxs-lookup"><span data-stu-id="94992-149">**glScale**</span></span>](glscale.md)
</dt> </dl>

 

 





