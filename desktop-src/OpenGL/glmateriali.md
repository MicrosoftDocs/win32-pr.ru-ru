---
title: Функция Глматериали (GL. h)
description: Функция Сеглматериали задает параметры материала для модели освещения.
ms.assetid: e3722dfd-3bdd-4460-8226-e50580ca1d79
keywords:
- Функция Глматериали OpenGL
topic_type:
- apiref
api_name:
- glMateriali
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc4f1bf6628f1674cf9c3534b9f0c9d028246d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681822"
---
# <a name="glmateriali-function"></a><span data-ttu-id="5c2f4-104">Функция Глматериали</span><span class="sxs-lookup"><span data-stu-id="5c2f4-104">glMateriali function</span></span>

<span data-ttu-id="5c2f4-105">Функция **глматериали** задает параметры материала для модели освещения.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-105">The **glMateriali** function specifies material parameters for the lighting model.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c2f4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c2f4-106">Syntax</span></span>


```C++
void WINAPI glMateriali(
   GLenum face,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="5c2f4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c2f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c2f4-108">*личным*</span><span class="sxs-lookup"><span data-stu-id="5c2f4-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="5c2f4-109">Лицо или грани, которые обновляются.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-109">The face or faces that are being updated.</span></span> <span data-ttu-id="5c2f4-110">Должен быть одним из следующих: GL \_ спереди, GL \_ или GL \_ спереди и ГК \_ .</span><span class="sxs-lookup"><span data-stu-id="5c2f4-110">Must be one of the following: GL\_FRONT, GL\_BACK, or GL\_FRONT and GL\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="5c2f4-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="5c2f4-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="5c2f4-112">Однозначный параметр Material для обновляемого лица или граней.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-112">The single-valued material parameter of the face or faces being updated.</span></span> <span data-ttu-id="5c2f4-113">Необходимо указать GL \_ коэффициента блеска.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-113">Must be GL\_SHININESS.</span></span>



| <span data-ttu-id="5c2f4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="5c2f4-114">Value</span></span>                                                                                                                                                      | <span data-ttu-id="5c2f4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5c2f4-115">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="5c2f4-116"><dt>**\_коэффициента БЛЕСКА GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5c2f4-116"><dt>**GL\_SHININESS**</dt></span></span> </dl> | <span data-ttu-id="5c2f4-117">Параметр *param* — это одно целое число, которое указывает экспоненту RGBA для вещества.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-117">The *param* parameter is a single integer that specifies the RGBA specular exponent of the material.</span></span> <span data-ttu-id="5c2f4-118">Целочисленные значения сопоставляются напрямую.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-118">Integer values are mapped directly.</span></span> <span data-ttu-id="5c2f4-119">Принимаются только значения в диапазоне \[ 0, 128 \] .</span><span class="sxs-lookup"><span data-stu-id="5c2f4-119">Only values in the range \[0, 128\] are accepted.</span></span> <span data-ttu-id="5c2f4-120">По умолчанию отраженный экспонента для материалов с внешним и резервным интерфейсом — 0.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-120">The default specular exponent for both front-facing and back-facing materials is 0.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="5c2f4-121">*param*</span><span class="sxs-lookup"><span data-stu-id="5c2f4-121">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="5c2f4-122">Значение, для которого \_ будет задан параметр GL коэффициента блеска.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-122">The value to which parameter GL\_SHININESS will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c2f4-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c2f4-123">Return value</span></span>

<span data-ttu-id="5c2f4-124">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-124">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5c2f4-125">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5c2f4-125">Error codes</span></span>

<span data-ttu-id="5c2f4-126">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-126">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5c2f4-127">Имя</span><span class="sxs-lookup"><span data-stu-id="5c2f4-127">Name</span></span>                                                                                              | <span data-ttu-id="5c2f4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="5c2f4-128">Meaning</span></span>                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c2f4-129"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5c2f4-129"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="5c2f4-130">Pname  не является  допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-130">Either *face* or *pname* was not an accepted value.</span></span><br/>                |
| <dl> <span data-ttu-id="5c2f4-131"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5c2f4-131"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="5c2f4-132">Указана отражающая Экспонента за пределами диапазона \[ 0, 128 \] .</span><span class="sxs-lookup"><span data-stu-id="5c2f4-132">A specular exponent outside the range of \[0, 128\] was specified.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5c2f4-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c2f4-133">Remarks</span></span>

<span data-ttu-id="5c2f4-134">Функция **глматериали** присваивает значения материальным параметрам.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-134">The **glMateriali** function assigns values to material parameters.</span></span> <span data-ttu-id="5c2f4-135">Существует два соответствующих набора параметров материала.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-135">There are two matched sets of material parameters.</span></span> <span data-ttu-id="5c2f4-136">Первый, *внешний* набор, используется для затенения точек, линий, точечных рисунков и всех многоугольников (если двустороннее освещение отключено) или только для внешних многоугольников (если включено двустороннее освещение).</span><span class="sxs-lookup"><span data-stu-id="5c2f4-136">One, the *front-facing* set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled).</span></span> <span data-ttu-id="5c2f4-137">Другой набор, с *обратным переходом*, используется для затенения задних многоугольников только при включении двустороннего освещения.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-137">The other set, *back-facing*, is used to shade back-facing polygons only when two-sided lighting is enabled.</span></span> <span data-ttu-id="5c2f4-138">Дополнительные сведения об односторонним и двустороннем вычислениях освещения см. в разделе [**гллигхтмодел**](gllightmodel-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="5c2f4-138">Refer to [**glLightModel**](gllightmodel-functions.md) for details concerning one-sided and two-sided lighting calculations.</span></span>

<span data-ttu-id="5c2f4-139">Функция **глматериали** принимает три аргумента.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-139">The **glMateriali** function takes three arguments.</span></span> <span data-ttu-id="5c2f4-140">Первый, *лицевой стороной* указывает, будут ли изменены изначальные материалы, первоначальные \_ \_ \_ \_ и \_ задние плановые материалы GL.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-140">The first, *face*, specifies whether the GL\_FRONT materials, the GL\_BACK materials, or both GL\_FRONT\_AND\_BACK materials will be modified.</span></span> <span data-ttu-id="5c2f4-141">Второй параметр, *pname*, указывает, какое из нескольких параметров в одном или обоих наборах будет изменено.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-141">The second, *pname*, specifies which of several parameters in one or both sets will be modified.</span></span> <span data-ttu-id="5c2f4-142">Третья, *param*, указывает, какое значение будет присвоено указанному параметру.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-142">The third, *param*, specifies what value will be assigned to the specified parameter.</span></span>

<span data-ttu-id="5c2f4-143">Параметры материала используются в уравнении освещения, которое при необходимости применяется к каждой вершине.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-143">Material parameters are used in the lighting equation that is optionally applied to each vertex.</span></span> <span data-ttu-id="5c2f4-144">Уравнение рассматривается в [**гллигхтмодел**](gllightmodel-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5c2f4-144">The equation is discussed in [**glLightModel**](gllightmodel-functions.md).</span></span>

<span data-ttu-id="5c2f4-145">Параметры материала можно обновить в любое время.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-145">The material parameters can be updated at any time.</span></span> <span data-ttu-id="5c2f4-146">В частности, **глматериали** можно вызывать между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5c2f4-146">In particular, **glMateriali** can be called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="5c2f4-147">Если для каждой вершины необходимо изменить только один параметр материала, [**глколорматериал**](glcolormaterial.md) является предпочтительным по сравнению с **глматериали**.</span><span class="sxs-lookup"><span data-stu-id="5c2f4-147">If only a single material parameter is to be changed per vertex, however, [**glColorMaterial**](glcolormaterial.md) is preferred over **glMateriali**.</span></span>

<span data-ttu-id="5c2f4-148">Следующая функция получает сведения, связанные с **глматериали**:</span><span class="sxs-lookup"><span data-stu-id="5c2f4-148">The following function retrieves information related to **glMateriali**:</span></span>

[<span data-ttu-id="5c2f4-149">**глжетматериал**</span><span class="sxs-lookup"><span data-stu-id="5c2f4-149">**glGetMaterial**</span></span>](glgetmaterial.md)

## <a name="requirements"></a><span data-ttu-id="5c2f4-150">Требования</span><span class="sxs-lookup"><span data-stu-id="5c2f4-150">Requirements</span></span>



| <span data-ttu-id="5c2f4-151">Требование</span><span class="sxs-lookup"><span data-stu-id="5c2f4-151">Requirement</span></span> | <span data-ttu-id="5c2f4-152">Значение</span><span class="sxs-lookup"><span data-stu-id="5c2f4-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c2f4-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c2f4-153">Minimum supported client</span></span><br/> | <span data-ttu-id="5c2f4-154">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5c2f4-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5c2f4-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c2f4-155">Minimum supported server</span></span><br/> | <span data-ttu-id="5c2f4-156">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5c2f4-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5c2f4-157">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5c2f4-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c2f4-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c2f4-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5c2f4-159">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5c2f4-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="5c2f4-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c2f4-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5c2f4-161">DLL</span><span class="sxs-lookup"><span data-stu-id="5c2f4-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c2f4-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c2f4-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c2f4-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c2f4-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c2f4-164">**глколорматериал**</span><span class="sxs-lookup"><span data-stu-id="5c2f4-164">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="5c2f4-165">**гллигхт**</span><span class="sxs-lookup"><span data-stu-id="5c2f4-165">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="5c2f4-166">**гллигхтмодел**</span><span class="sxs-lookup"><span data-stu-id="5c2f4-166">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





