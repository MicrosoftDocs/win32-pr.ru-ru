---
title: Функция Глклипплане (GL. h)
description: Функция Глклипплане указывает плоскость, в которой обрезана Вся геометрия.
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- Функция Глклипплане OpenGL
topic_type:
- apiref
api_name:
- glClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33380203b30b7a3a2e37ee5d58a47fec845cbc1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681950"
---
# <a name="glclipplane-function"></a><span data-ttu-id="0f906-104">Функция Глклипплане</span><span class="sxs-lookup"><span data-stu-id="0f906-104">glClipPlane function</span></span>

<span data-ttu-id="0f906-105">Функция **глклипплане** указывает плоскость, в которой обрезана Вся геометрия.</span><span class="sxs-lookup"><span data-stu-id="0f906-105">The **glClipPlane** function specifies a plane against which all geometry is clipped.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f906-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f906-106">Syntax</span></span>


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a><span data-ttu-id="0f906-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f906-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f906-108">*плоскости*</span><span class="sxs-lookup"><span data-stu-id="0f906-108">*plane*</span></span> 
</dt> <dd>

<span data-ttu-id="0f906-109">Размещается плоскость обрезки.</span><span class="sxs-lookup"><span data-stu-id="0f906-109">The clipping plane that is being positioned.</span></span> <span data-ttu-id="0f906-110">Символьные имена в виде плоскости Clip в виде главной области \_ \_ *i*, где *i* — целое число от 0 до \_ максимального количества \_ \_ плоскостей, равное 1, принимаются.</span><span class="sxs-lookup"><span data-stu-id="0f906-110">Symbolic names of the form GL\_CLIP\_PLANE *i*, where *i* is an integer between 0 and GL\_MAX\_CLIP\_PLANES - 1, are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="0f906-111">*Дробь*</span><span class="sxs-lookup"><span data-stu-id="0f906-111">*equation*</span></span> 
</dt> <dd>

<span data-ttu-id="0f906-112">Адрес массива из четырех значений с плавающей запятой двойной точности.</span><span class="sxs-lookup"><span data-stu-id="0f906-112">The address of an array of four double-precision floating-point values.</span></span> <span data-ttu-id="0f906-113">Эти значения интерпретируется как уравнение плоскости.</span><span class="sxs-lookup"><span data-stu-id="0f906-113">These values are interpreted as a plane equation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f906-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f906-114">Return value</span></span>

<span data-ttu-id="0f906-115">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0f906-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0f906-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="0f906-116">Error codes</span></span>

<span data-ttu-id="0f906-117">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="0f906-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0f906-118">Имя</span><span class="sxs-lookup"><span data-stu-id="0f906-118">Name</span></span>                                                                                                  | <span data-ttu-id="0f906-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0f906-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f906-120"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="0f906-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="0f906-121">*плоскость* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="0f906-121">*plane* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="0f906-122"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="0f906-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0f906-123">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="0f906-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0f906-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f906-124">Remarks</span></span>

<span data-ttu-id="0f906-125">Геометрия всегда обрезается относительно границ шести плоскостей фрустум в *x*, *y* и *z*.</span><span class="sxs-lookup"><span data-stu-id="0f906-125">Geometry is always clipped against the boundaries of a six-plane frustum in *x*, *y*, and *z*.</span></span> <span data-ttu-id="0f906-126">Функция **глклипплане** позволяет определить дополнительные плоскости, не обязательно Перпендикулярные оси *x*, оси *y* или оси *z*, для которых обрезается Вся геометрия.</span><span class="sxs-lookup"><span data-stu-id="0f906-126">The **glClipPlane** function allows the specification of additional planes, not necessarily perpendicular to the *x-* axis, *y-* axis, or *z*-axis, against which all geometry is clipped.</span></span> <span data-ttu-id="0f906-127">Можно указать до GL максимальных плоскостей для \_ \_ вырезок \_ , где \_ GL \_ \_ не менее шести плоскостей.</span><span class="sxs-lookup"><span data-stu-id="0f906-127">Up to GL\_MAX\_CLIP\_PLANES planes can be specified, where GL\_MAX\_CLIP\_PLANES is at least six in all implementations.</span></span> <span data-ttu-id="0f906-128">Так как результирующая область обрезки является пересечением определенных половинных пробелов, оно всегда выпуклой.</span><span class="sxs-lookup"><span data-stu-id="0f906-128">Because the resulting clipping region is the intersection of the defined half-spaces, it is always convex.</span></span>

<span data-ttu-id="0f906-129">Функция **глклипплане** задает половину пространства, используя уравнение плоскости из четырех компонентов.</span><span class="sxs-lookup"><span data-stu-id="0f906-129">The **glClipPlane** function specifies a half-space using a four-component plane equation.</span></span> <span data-ttu-id="0f906-130">При вызове \**глклипплане\*\*\*Формула* преобразуется инверсией матрицы моделвиев и хранится в результирующих координатах глаза.</span><span class="sxs-lookup"><span data-stu-id="0f906-130">When you call **glClipPlane**,*equation* is transformed by the inverse of the modelview matrix and stored in the resulting eye coordinates.</span></span> <span data-ttu-id="0f906-131">Последующие изменения матрицы моделвиев не оказывают влияния на хранимые компоненты уравнений плоскости.</span><span class="sxs-lookup"><span data-stu-id="0f906-131">Subsequent changes to the modelview matrix have no effect on the stored plane-equation components.</span></span> <span data-ttu-id="0f906-132">Если скалярное произведение координат глаза для вершины с компонентами уравнения в хранимой плоскости имеет положительный или нулевое значение, вершина находится в относительно этой плоскости обрезки.</span><span class="sxs-lookup"><span data-stu-id="0f906-132">If the dot product of the eye coordinates of a vertex with the stored plane equation components is positive or zero, the vertex is in with respect to that clipping plane.</span></span> <span data-ttu-id="0f906-133">В противном случае он истекает.</span><span class="sxs-lookup"><span data-stu-id="0f906-133">Otherwise, it is out.</span></span>

<span data-ttu-id="0f906-134">Используйте функции [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) для включения и отключения отсечения плоскостей.</span><span class="sxs-lookup"><span data-stu-id="0f906-134">Use the [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) functions to enable and disable clipping planes.</span></span> <span data-ttu-id="0f906-135">Вызовите обтравочные плоскости с аргументом GL \_ - \_ плоскостью *i*, где *i* — это номер плоскости.</span><span class="sxs-lookup"><span data-stu-id="0f906-135">Call clipping planes with the argument GL\_CLIP\_PLANE *i*, where *i* is the plane number.</span></span>

<span data-ttu-id="0f906-136">По умолчанию все обтравочные плоскости определены как (0, 0, 0, 0) в координатах глаза и отключены.</span><span class="sxs-lookup"><span data-stu-id="0f906-136">By default, all clipping planes are defined as (0,0,0,0) in eye coordinates and are disabled.</span></span>

<span data-ttu-id="0f906-137">Это всегда так, что GL — это « \_ \_  \_ \_ PLANE0». </span><span class="sxs-lookup"><span data-stu-id="0f906-137">It is always the case that GL\_CLIP\_PLANE *i* = GL\_CLIP\_PLANE0 + *i*.</span></span>

<span data-ttu-id="0f906-138">Следующие функции извлекают сведения, относящиеся к **глклипплане**:</span><span class="sxs-lookup"><span data-stu-id="0f906-138">The following functions retrieve information related to **glClipPlane**:</span></span>

[<span data-ttu-id="0f906-139">**глжетклипплане**</span><span class="sxs-lookup"><span data-stu-id="0f906-139">**glGetClipPlane**</span></span>](glgetclipplane.md)

<span data-ttu-id="0f906-140">[**глисенаблед**](glisenabled.md) с аргументом GL \_ Clip \_ плоскость *i*</span><span class="sxs-lookup"><span data-stu-id="0f906-140">[**glIsEnabled**](glisenabled.md) with argument GL\_CLIP\_PLANE *i*</span></span>

## <a name="requirements"></a><span data-ttu-id="0f906-141">Требования</span><span class="sxs-lookup"><span data-stu-id="0f906-141">Requirements</span></span>



| <span data-ttu-id="0f906-142">Требование</span><span class="sxs-lookup"><span data-stu-id="0f906-142">Requirement</span></span> | <span data-ttu-id="0f906-143">Значение</span><span class="sxs-lookup"><span data-stu-id="0f906-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f906-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f906-144">Minimum supported client</span></span><br/> | <span data-ttu-id="0f906-145">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f906-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0f906-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f906-146">Minimum supported server</span></span><br/> | <span data-ttu-id="0f906-147">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f906-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0f906-148">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0f906-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f906-149"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f906-149"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0f906-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0f906-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f906-151"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f906-151"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0f906-152">DLL</span><span class="sxs-lookup"><span data-stu-id="0f906-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f906-153"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f906-153"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f906-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f906-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f906-155">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="0f906-155">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0f906-156">**глдисабле**</span><span class="sxs-lookup"><span data-stu-id="0f906-156">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="0f906-157">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="0f906-157">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="0f906-158">**гленд**</span><span class="sxs-lookup"><span data-stu-id="0f906-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0f906-159">**глжетклипплане**</span><span class="sxs-lookup"><span data-stu-id="0f906-159">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="0f906-160">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="0f906-160">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





