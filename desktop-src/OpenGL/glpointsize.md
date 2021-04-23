---
title: Функция Глпоинтсизе (GL. h)
description: Функция Глпоинтсизе задает диаметр растровых точек.
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
keywords:
- Функция Глпоинтсизе OpenGL
topic_type:
- apiref
api_name:
- glPointSize
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6b9525e302cad1eb940184eb5eb83e11744bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661930"
---
# <a name="glpointsize-function"></a><span data-ttu-id="09f8d-104">Функция Глпоинтсизе</span><span class="sxs-lookup"><span data-stu-id="09f8d-104">glPointSize function</span></span>

<span data-ttu-id="09f8d-105">Функция **глпоинтсизе** задает диаметр растровых точек.</span><span class="sxs-lookup"><span data-stu-id="09f8d-105">The **glPointSize** function specifies the diameter of rasterized points.</span></span>

## <a name="syntax"></a><span data-ttu-id="09f8d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09f8d-106">Syntax</span></span>


```C++
void WINAPI glPointSize(
   GLfloat size
);
```



## <a name="parameters"></a><span data-ttu-id="09f8d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="09f8d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09f8d-108">*size*</span><span class="sxs-lookup"><span data-stu-id="09f8d-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="09f8d-109">Диаметр растровых точек.</span><span class="sxs-lookup"><span data-stu-id="09f8d-109">The diameter of rasterized points.</span></span> <span data-ttu-id="09f8d-110">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="09f8d-110">The default is 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09f8d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09f8d-111">Return value</span></span>

<span data-ttu-id="09f8d-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="09f8d-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="09f8d-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="09f8d-113">Error codes</span></span>

<span data-ttu-id="09f8d-114">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="09f8d-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="09f8d-115">Имя</span><span class="sxs-lookup"><span data-stu-id="09f8d-115">Name</span></span>                                                                                                  | <span data-ttu-id="09f8d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="09f8d-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09f8d-117"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="09f8d-117"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="09f8d-118">*Размер* меньше или равен нулю.</span><span class="sxs-lookup"><span data-stu-id="09f8d-118">*size* was less than or equal to zero.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="09f8d-119"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="09f8d-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="09f8d-120">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="09f8d-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="09f8d-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09f8d-121">Remarks</span></span>

<span data-ttu-id="09f8d-122">Функция **глпоинтсизе** задает растровый диаметр как псевдонимов, так и сглаженных точек.</span><span class="sxs-lookup"><span data-stu-id="09f8d-122">The **glPointSize** function specifies the rasterized diameter of both aliased and antialiased points.</span></span> <span data-ttu-id="09f8d-123">Использование кегля, отличного от 1,0, имеет различные эффекты в зависимости от того, включено ли сглаживание точек.</span><span class="sxs-lookup"><span data-stu-id="09f8d-123">Using a point size other than 1.0 has different effects, depending on whether point antialiasing is enabled.</span></span> <span data-ttu-id="09f8d-124">Сглаживание точек управляется путем вызова [**гленабле**](glenable.md) и **глдисабле** с аргументом GL в виде \_ точки \_ .</span><span class="sxs-lookup"><span data-stu-id="09f8d-124">Point antialiasing is controlled by calling [**glEnable**](glenable.md) and **glDisable** with argument GL\_POINT\_SMOOTH.</span></span>

<span data-ttu-id="09f8d-125">Если сглаживание точки отключено, фактический размер определяется путем округления предоставленного размера до ближайшего целого числа.</span><span class="sxs-lookup"><span data-stu-id="09f8d-125">If point antialiasing is disabled, the actual size is determined by rounding the supplied size to the nearest integer.</span></span> <span data-ttu-id="09f8d-126">(Если результат округления имеет значение 0, то это будет так, как если бы размер точки был равен 1.) Если округленный размер нечетный, то Центральная точка (*x*,*y*) фрагмента пикселя, представляющая точку, будет вычисляться как</span><span class="sxs-lookup"><span data-stu-id="09f8d-126">(If the rounding results in the value 0, it is as if the point size were 1.) If the rounded size is odd, then the center point (*x*,*y*) of the pixel fragment that represents the point is computed as</span></span>

<span data-ttu-id="09f8d-127">(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)</span><span class="sxs-lookup"><span data-stu-id="09f8d-127">(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)</span></span>

<span data-ttu-id="09f8d-128">где *w* подстрочные индексы обозначают координаты окна.</span><span class="sxs-lookup"><span data-stu-id="09f8d-128">where *w* subscripts indicate window coordinates.</span></span> <span data-ttu-id="09f8d-129">Все пиксели, находящиеся в квадратной сетке скругленного размера, расположенного в центре (*x*,*y*), составляют фрагмент.</span><span class="sxs-lookup"><span data-stu-id="09f8d-129">All pixels that lie within the square grid of the rounded size centered at (*x*,*y*) make up the fragment.</span></span> <span data-ttu-id="09f8d-130">Если размер четное, Центральная точка</span><span class="sxs-lookup"><span data-stu-id="09f8d-130">If the size is even, the center point is</span></span>

<span data-ttu-id="09f8d-131">(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)</span><span class="sxs-lookup"><span data-stu-id="09f8d-131">(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)</span></span>

<span data-ttu-id="09f8d-132">а центрированные центры фрагментов — это координаты окна половинного целого числа в квадрате округленного размера, расположенного в центре (*x*,*y*).</span><span class="sxs-lookup"><span data-stu-id="09f8d-132">and the rasterized fragment's centers are the half-integer window coordinates within the square of the rounded size centered at (*x*,*y*).</span></span> <span data-ttu-id="09f8d-133">Все фрагменты пикселов, созданные при растрировании точки нонантиалиасед, имеют одинаковые связанные данные. вершина, соответствующая точке.</span><span class="sxs-lookup"><span data-stu-id="09f8d-133">All pixel fragments produced in rasterizing a nonantialiased point are assigned the same associated data; that of the vertex corresponding to the point.</span></span>

<span data-ttu-id="09f8d-134">Если включено сглаживание, то точечная текстура создает фрагмент для каждого квадрата пикселей, пересекающего область, которая имеет диаметр, равный текущему размеру точки и центрированную в точках (*x*<sub>w</sub> ,*y*<sub>w</sub> ).</span><span class="sxs-lookup"><span data-stu-id="09f8d-134">If antialiasing is enabled, then point rasterization produces a fragment for each pixel square that intersects the region lying within the circle having diameter equal to the current point size and centered at the points (*x*<sub>w</sub> ,*y*<sub>w</sub> ).</span></span> <span data-ttu-id="09f8d-135">Значение покрытия для каждого фрагмента является координатной областью окна пересечения круговой области с соответствующим квадратом пикселей.</span><span class="sxs-lookup"><span data-stu-id="09f8d-135">The coverage value for each fragment is the window coordinate area of the intersection of the circular region with the corresponding pixel square.</span></span> <span data-ttu-id="09f8d-136">Это значение сохраняется и используется на заключительном шаге растрирования.</span><span class="sxs-lookup"><span data-stu-id="09f8d-136">This value is saved and used in the final rasterization step.</span></span> <span data-ttu-id="09f8d-137">Данные, связанные с каждым фрагментом, — это данные, связанные с растровой точкой.</span><span class="sxs-lookup"><span data-stu-id="09f8d-137">The data associated with each fragment is the data associated with the point being rasterized.</span></span>

<span data-ttu-id="09f8d-138">При включении сглаживания точек поддерживаются не все размеры.</span><span class="sxs-lookup"><span data-stu-id="09f8d-138">Not all sizes are supported when point antialiasing is enabled.</span></span> <span data-ttu-id="09f8d-139">Если запрошен неподдерживаемый размер, используется ближайший поддерживаемый размер.</span><span class="sxs-lookup"><span data-stu-id="09f8d-139">If an unsupported size is requested, the nearest supported size is used.</span></span> <span data-ttu-id="09f8d-140">Гарантируется, что поддерживается только размер 1,0. другие зависят от реализации.</span><span class="sxs-lookup"><span data-stu-id="09f8d-140">Only size 1.0 is guaranteed to be supported; others depend on the implementation.</span></span> <span data-ttu-id="09f8d-141">Диапазон поддерживаемых размеров и разница между поддерживаемыми размерами в пределах диапазона можно запросить, вызвав [**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументами \_ \_ диапазон размера главной точки \_ и \_ \_ гранулярность размера точки GL \_ .</span><span class="sxs-lookup"><span data-stu-id="09f8d-141">The range of supported sizes and the size difference between supported sizes within the range can be queried by calling [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with arguments GL\_POINT\_SIZE\_RANGE and GL\_POINT\_SIZE\_GRANULARITY.</span></span>

<span data-ttu-id="09f8d-142">Размер точки, указанный параметром **глпоинтсизе** , всегда возвращается, \_ когда \_ запрашивается размер точки GL.</span><span class="sxs-lookup"><span data-stu-id="09f8d-142">The point size specified by **glPointSize** is always returned when GL\_POINT\_SIZE is queried.</span></span> <span data-ttu-id="09f8d-143">Фиксация и округление для точек с псевдонимами и сглаживания не влияют на указанное значение.</span><span class="sxs-lookup"><span data-stu-id="09f8d-143">Clamping and rounding for aliased and antialiased points have no effect on the specified value.</span></span>

<span data-ttu-id="09f8d-144">Размер точки без сглаживания может относиться к максимуму, зависящему от реализации.</span><span class="sxs-lookup"><span data-stu-id="09f8d-144">Non-antialiased point size may be clamped to an implementation-dependent maximum.</span></span> <span data-ttu-id="09f8d-145">Хотя это максимальное значение не может быть запрошено, оно должно быть не меньше максимального значения для точек сглаживания, округленное до ближайшего целого значения.</span><span class="sxs-lookup"><span data-stu-id="09f8d-145">Although this maximum cannot be queried, it must be no less than the maximum value for antialiased points, rounded to the nearest integer value.</span></span>

<span data-ttu-id="09f8d-146">Следующие функции извлекают сведения, относящиеся к **глпоинтсизе**:</span><span class="sxs-lookup"><span data-stu-id="09f8d-146">The following functions retrieve information related to **glPointSize**:</span></span>

<span data-ttu-id="09f8d-147">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ Размер точки GL \_</span><span class="sxs-lookup"><span data-stu-id="09f8d-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POINT\_SIZE</span></span>

<span data-ttu-id="09f8d-148">**глжет** с аргументом \_ \_ диапазона размера \_ точки GL</span><span class="sxs-lookup"><span data-stu-id="09f8d-148">**glGet** with argument GL\_POINT\_SIZE\_RANGE</span></span>

<span data-ttu-id="09f8d-149">**глжет** с аргументом \_ \_ гранулярность размера \_ точки GL</span><span class="sxs-lookup"><span data-stu-id="09f8d-149">**glGet** with argument GL\_POINT\_SIZE\_GRANULARITY</span></span>

<span data-ttu-id="09f8d-150">[**глисенаблед**](glisenabled.md) с аргументом \_ " \_ Smooth пт"</span><span class="sxs-lookup"><span data-stu-id="09f8d-150">[**glIsEnabled**](glisenabled.md) with argument GL\_POINT\_SMOOTH</span></span>

## <a name="requirements"></a><span data-ttu-id="09f8d-151">Требования</span><span class="sxs-lookup"><span data-stu-id="09f8d-151">Requirements</span></span>



| <span data-ttu-id="09f8d-152">Требование</span><span class="sxs-lookup"><span data-stu-id="09f8d-152">Requirement</span></span> | <span data-ttu-id="09f8d-153">Значение</span><span class="sxs-lookup"><span data-stu-id="09f8d-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09f8d-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09f8d-154">Minimum supported client</span></span><br/> | <span data-ttu-id="09f8d-155">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="09f8d-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="09f8d-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09f8d-156">Minimum supported server</span></span><br/> | <span data-ttu-id="09f8d-157">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="09f8d-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="09f8d-158">Заголовок</span><span class="sxs-lookup"><span data-stu-id="09f8d-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="09f8d-159"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="09f8d-159"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="09f8d-160">Библиотека</span><span class="sxs-lookup"><span data-stu-id="09f8d-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="09f8d-161"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09f8d-161"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="09f8d-162">DLL</span><span class="sxs-lookup"><span data-stu-id="09f8d-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09f8d-163"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09f8d-163"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09f8d-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09f8d-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09f8d-165">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="09f8d-165">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="09f8d-166">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="09f8d-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="09f8d-167">**гленд**</span><span class="sxs-lookup"><span data-stu-id="09f8d-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="09f8d-168">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="09f8d-168">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





