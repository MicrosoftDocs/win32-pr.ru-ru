---
title: Функция Гллиневидс (GL. h)
description: Функция Гллиневидс задает ширину растровых линий.
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
keywords:
- Функция Гллиневидс OpenGL
topic_type:
- apiref
api_name:
- glLineWidth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa4cecafc9e5d8e0f55c6e9d0dbfe49924d54f14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661989"
---
# <a name="gllinewidth-function"></a><span data-ttu-id="24668-104">Функция Гллиневидс</span><span class="sxs-lookup"><span data-stu-id="24668-104">glLineWidth function</span></span>

<span data-ttu-id="24668-105">Функция **гллиневидс** задает ширину растровых линий.</span><span class="sxs-lookup"><span data-stu-id="24668-105">The **glLineWidth** function specifies the width of rasterized lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="24668-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24668-106">Syntax</span></span>


```C++
void WINAPI glLineWidth(
   GLfloat width
);
```



## <a name="parameters"></a><span data-ttu-id="24668-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="24668-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24668-108">*width*</span><span class="sxs-lookup"><span data-stu-id="24668-108">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="24668-109">Ширина растровых линий.</span><span class="sxs-lookup"><span data-stu-id="24668-109">The width of rasterized lines.</span></span> <span data-ttu-id="24668-110">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="24668-110">The default is 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24668-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24668-111">Return value</span></span>

<span data-ttu-id="24668-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="24668-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="24668-113">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="24668-113">Error codes</span></span>

<span data-ttu-id="24668-114">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="24668-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="24668-115">Имя</span><span class="sxs-lookup"><span data-stu-id="24668-115">Name</span></span>                                                                                                  | <span data-ttu-id="24668-116">Значение</span><span class="sxs-lookup"><span data-stu-id="24668-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="24668-117"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="24668-117"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="24668-118">*Ширина* меньше или равна нулю.</span><span class="sxs-lookup"><span data-stu-id="24668-118">*width* was less than or equal to zero.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="24668-119"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="24668-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="24668-120">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="24668-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="24668-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24668-121">Remarks</span></span>

<span data-ttu-id="24668-122">Функция **гллиневидс** задает растровую ширину для линий с псевдонимами и сглаженными.</span><span class="sxs-lookup"><span data-stu-id="24668-122">The **glLineWidth** function specifies the rasterized width of both aliased and antialiased lines.</span></span> <span data-ttu-id="24668-123">Использование толщины линии, отличной от 1,0, имеет различные эффекты в зависимости от того, включено ли сглаживание строк.</span><span class="sxs-lookup"><span data-stu-id="24668-123">Using a line width other than 1.0 has different effects, depending on whether line antialiasing is enabled.</span></span> <span data-ttu-id="24668-124">Сглаживание линии управляется путем вызова [**гленабле**](glenable.md) и **глдисабле** с аргументом GL \_ Line \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="24668-124">Line antialiasing is controlled by calling [**glEnable**](glenable.md) and **glDisable** with argument GL\_LINE\_SMOOTH.</span></span>

<span data-ttu-id="24668-125">Если сглаживание линии отключено, фактическая ширина определяется путем округления предоставленной ширины к ближайшему целому числу.</span><span class="sxs-lookup"><span data-stu-id="24668-125">If line antialiasing is disabled, the actual width is determined by rounding the supplied width to the nearest integer.</span></span> <span data-ttu-id="24668-126">(Если округление приводит к значению 0,0, то это так, как если бы толщина линии была 1,0). Если \| ?</span><span class="sxs-lookup"><span data-stu-id="24668-126">(If the rounding results in the value 0.0, it is as if the line width were 1.0) If \| ?</span></span> <span data-ttu-id="24668-127">x \|  =  \| ?</span><span class="sxs-lookup"><span data-stu-id="24668-127">x \| = \| ?</span></span> <span data-ttu-id="24668-128">y \| , *i* пикселей заполняются в каждом столбце, который является скругленным, где *i* — округленное значение *Width*.</span><span class="sxs-lookup"><span data-stu-id="24668-128">y \|, *i* pixels are filled in each column that is rasterized, where *i* is the rounded value of *width*.</span></span> <span data-ttu-id="24668-129">В противном случае *i* пикселей заполняют каждую строку, которая является растрирования.</span><span class="sxs-lookup"><span data-stu-id="24668-129">Otherwise, *i* pixels are filled in each row that is rasterized.</span></span>

<span data-ttu-id="24668-130">Если сглаживание линии включено, то при растрировании строки создается фрагмент для каждого квадрата пикселей, пересекающего область, которая имеет ширину прямоугольника, равную текущей ширине линии, длина равна фактической длине линии и по центру для математического сегмента линии.</span><span class="sxs-lookup"><span data-stu-id="24668-130">If antialiasing is enabled, line rasterization produces a fragment for each pixel square that intersects the region lying within the rectangle having width equal to the current line width, length equal to the actual length of the line, and centered on the mathematical line segment.</span></span> <span data-ttu-id="24668-131">Значение покрытия для каждого фрагмента является координатной областью окна пересечения прямоугольной области с соответствующим квадратом пикселей.</span><span class="sxs-lookup"><span data-stu-id="24668-131">The coverage value for each fragment is the window coordinate area of the intersection of the rectangular region with the corresponding pixel square.</span></span> <span data-ttu-id="24668-132">Это значение сохраняется и используется на заключительном шаге растрирования.</span><span class="sxs-lookup"><span data-stu-id="24668-132">This value is saved and used in the final rasterization step.</span></span>

<span data-ttu-id="24668-133">Если включено сглаживание строк, могут поддерживаться не все значения ширины.</span><span class="sxs-lookup"><span data-stu-id="24668-133">Not all widths can be supported when line antialiasing is enabled.</span></span> <span data-ttu-id="24668-134">Если запрошена неподдерживаемая ширина, используется Ближайшая поддерживаемая ширина.</span><span class="sxs-lookup"><span data-stu-id="24668-134">If an unsupported width is requested, the nearest supported width is used.</span></span> <span data-ttu-id="24668-135">Гарантируется, что поддерживается только ширина 1,0. другие зависят от реализации.</span><span class="sxs-lookup"><span data-stu-id="24668-135">Only width 1.0 is guaranteed to be supported; others depend on the implementation.</span></span> <span data-ttu-id="24668-136">Диапазон поддерживаемых ширины и разница между поддерживаемыми ширинами в пределах диапазона можно запросить, вызвав **глжет** с аргументами GL \_ Line \_ толщина \_ диапазона и \_ \_ \_ степенью детализации толщины линии GL.</span><span class="sxs-lookup"><span data-stu-id="24668-136">The range of supported widths and the size difference between supported widths within the range can be queried by calling **glGet** with arguments GL\_LINE\_WIDTH\_RANGE and GL\_LINE\_WIDTH\_GRANULARITY.</span></span>

<span data-ttu-id="24668-137">Ширина линии, заданная параметром **гллиневидс** , всегда возвращается \_ при \_ запросе ширины линии GL.</span><span class="sxs-lookup"><span data-stu-id="24668-137">The line width specified by **glLineWidth** is always returned when GL\_LINE\_WIDTH is queried.</span></span> <span data-ttu-id="24668-138">Фиксация и округление для строк с псевдонимами и сглаженных линий не влияют на указанное значение.</span><span class="sxs-lookup"><span data-stu-id="24668-138">Clamping and rounding for aliased and antialiased lines have no effect on the specified value.</span></span>

<span data-ttu-id="24668-139">Ширина линии без сглаживания может быть перенесена в максимальное значение, зависящее от реализации.</span><span class="sxs-lookup"><span data-stu-id="24668-139">Non-antialiased line width may be clamped to an implementation-dependent maximum.</span></span> <span data-ttu-id="24668-140">Хотя это максимальное значение не может быть запрошено, оно должно быть не меньше максимального значения для сглаженных строк, округленное до ближайшего целого значения.</span><span class="sxs-lookup"><span data-stu-id="24668-140">Although this maximum cannot be queried, it must be no less than the maximum value for antialiased lines, rounded to the nearest integer value.</span></span>

<span data-ttu-id="24668-141">Следующие функции извлекают сведения, относящиеся к **гллиневидс**:</span><span class="sxs-lookup"><span data-stu-id="24668-141">The following functions retrieve information related to **glLineWidth**:</span></span>

<span data-ttu-id="24668-142">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом " \_ толщина линии GL" \_</span><span class="sxs-lookup"><span data-stu-id="24668-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LINE\_WIDTH</span></span>

<span data-ttu-id="24668-143">**глжет** с аргументом \_ \_ диапазона толщины линии GL \_</span><span class="sxs-lookup"><span data-stu-id="24668-143">**glGet** with argument GL\_LINE\_WIDTH\_RANGE</span></span>

<span data-ttu-id="24668-144">**глжет** с аргументом \_ \_ ГРАНУЛЯРНОСТЬ толщины линии GL \_</span><span class="sxs-lookup"><span data-stu-id="24668-144">**glGet** with argument GL\_LINE\_WIDTH\_GRANULARITY</span></span>

<span data-ttu-id="24668-145">[**глисенаблед**](glisenabled.md) с аргументом GL \_ Line \_ Smooth</span><span class="sxs-lookup"><span data-stu-id="24668-145">[**glIsEnabled**](glisenabled.md) with argument GL\_LINE\_SMOOTH</span></span>

## <a name="requirements"></a><span data-ttu-id="24668-146">Требования</span><span class="sxs-lookup"><span data-stu-id="24668-146">Requirements</span></span>



| <span data-ttu-id="24668-147">Требование</span><span class="sxs-lookup"><span data-stu-id="24668-147">Requirement</span></span> | <span data-ttu-id="24668-148">Значение</span><span class="sxs-lookup"><span data-stu-id="24668-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24668-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24668-149">Minimum supported client</span></span><br/> | <span data-ttu-id="24668-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="24668-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="24668-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24668-151">Minimum supported server</span></span><br/> | <span data-ttu-id="24668-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="24668-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="24668-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="24668-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="24668-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="24668-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="24668-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="24668-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="24668-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24668-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="24668-157">DLL</span><span class="sxs-lookup"><span data-stu-id="24668-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24668-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24668-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24668-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24668-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24668-160">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="24668-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="24668-161">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="24668-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="24668-162">**гленд**</span><span class="sxs-lookup"><span data-stu-id="24668-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="24668-163">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="24668-163">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





