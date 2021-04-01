---
title: Функция Глжетпикселмапфв (GL. h)
description: Функции Глжетпикселмапфв, Глжетпикселмапуив и Глжетпикселмапусв возвращают указанную карту в пикселях. | Функция Глжетпикселмапфв (GL. h)
ms.assetid: b09f4799-8e36-4d4f-90d8-4a8ed3d15718
keywords:
- Функция Глжетпикселмапфв OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f73fb817c347832dfc6a09636173641e5c869b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914400"
---
# <a name="glgetpixelmapfv-function"></a><span data-ttu-id="bb591-105">Функция Глжетпикселмапфв</span><span class="sxs-lookup"><span data-stu-id="bb591-105">glGetPixelMapfv function</span></span>

<span data-ttu-id="bb591-106">Функции **глжетпикселмапфв**, [**глжетпикселмапуив**](glgetpixelmapuiv.md)и [**глжетпикселмапусв**](glgetpixelmapusv.md) возвращают указанную карту в пикселях.</span><span class="sxs-lookup"><span data-stu-id="bb591-106">The **glGetPixelMapfv**, [**glGetPixelMapuiv**](glgetpixelmapuiv.md), and [**glGetPixelMapusv**](glgetpixelmapusv.md) functions return the specified pixel map.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb591-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb591-107">Syntax</span></span>


```C++
void WINAPI glGetPixelMapfv(
   GLenum  map,
   GLfloat *values
);
```



## <a name="parameters"></a><span data-ttu-id="bb591-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb591-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb591-109">*map*</span><span class="sxs-lookup"><span data-stu-id="bb591-109">*map*</span></span> 
</dt> <dd>

<span data-ttu-id="bb591-110">Имя возвращаемой схемы пикселей.</span><span class="sxs-lookup"><span data-stu-id="bb591-110">The name of the pixel map to return.</span></span> <span data-ttu-id="bb591-111">Допустимые значения: "таблица с картой" i "1", "1" \_ \_ \_ \_ \_ , \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ "с", "с", "с", "с", "с", "с", "с", "с", "на 1", "Таблица 1".</span><span class="sxs-lookup"><span data-stu-id="bb591-111">Accepted values are GL\_PIXEL\_MAP\_I\_TO\_I, GL\_PIXEL\_MAP\_S\_TO\_S, GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, GL\_PIXEL\_MAP\_I\_TO\_A, GL\_PIXEL\_MAP\_R\_TO\_R, GL\_PIXEL\_MAP\_G\_TO\_G, GL\_PIXEL\_MAP\_B\_TO\_B, and GL\_PIXEL\_MAP\_A\_TO\_A.</span></span>

</dd> <dt>

<span data-ttu-id="bb591-112">*Значения*</span><span class="sxs-lookup"><span data-stu-id="bb591-112">*values*</span></span> 
</dt> <dd>

<span data-ttu-id="bb591-113">Возвращает содержимое схемы пикселей.</span><span class="sxs-lookup"><span data-stu-id="bb591-113">Returns the pixel map contents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb591-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb591-114">Return value</span></span>

<span data-ttu-id="bb591-115">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bb591-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bb591-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="bb591-116">Error codes</span></span>

<span data-ttu-id="bb591-117">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="bb591-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="bb591-118">Имя</span><span class="sxs-lookup"><span data-stu-id="bb591-118">Name</span></span>                                                                                                  | <span data-ttu-id="bb591-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bb591-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb591-120"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="bb591-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="bb591-121">значение *Map* не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="bb591-121">*map* was not an accepted value.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="bb591-122"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="bb591-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="bb591-123">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="bb591-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bb591-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb591-124">Remarks</span></span>

<span data-ttu-id="bb591-125">Описание допустимых значений параметра *Map* см. в разделе [**глпикселмап**](glpixelmap.md) .</span><span class="sxs-lookup"><span data-stu-id="bb591-125">See [**glPixelMap**](glpixelmap.md) for a description of the acceptable values for the *map* parameter.</span></span> <span data-ttu-id="bb591-126">Функция **глжетпикселмап** возвращает в виде *значений* содержимое точечной гиперкарты, указанной в *Map*.</span><span class="sxs-lookup"><span data-stu-id="bb591-126">The **glGetPixelMap** function returns in *values* the contents of the pixel map specified in *map*.</span></span> <span data-ttu-id="bb591-127">Используйте карты пикселей во время выполнения [**глреадпикселс**](glreadpixels.md), [**глдравпикселс**](gldrawpixels.md), [**глкопипикселс**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)и [**glTexImage2D**](glteximage2d.md) для сопоставления цветовых индексов, индексов наборов элементов, цветовых компонентов и компонентов глубины с другими значениями.</span><span class="sxs-lookup"><span data-stu-id="bb591-127">Use pixel maps during the execution of [**glReadPixels**](glreadpixels.md), [**glDrawPixels**](gldrawpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md), and [**glTexImage2D**](glteximage2d.md) to map color indexes, stencil indexes, color components, and depth components to other values.</span></span>

<span data-ttu-id="bb591-128">Целочисленные значения без знака, если они запрошены, линейно сопоставляются с внутренним представлением фиксированной или плавающей запятой, которое 1,0 сопоставляется с максимальным значением типа Integer, а 0,0 сопоставляется с нулем.</span><span class="sxs-lookup"><span data-stu-id="bb591-128">Unsigned integer values, if requested, are linearly mapped from the internal fixed or floating-point representation such that 1.0 maps to the largest representable integer value, and 0.0 maps to zero.</span></span> <span data-ttu-id="bb591-129">Возврат целочисленных значений без знака не определен, если значение сопоставлений не находится в диапазоне \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="bb591-129">Return unsigned integer values are undefined if the map value was not in the range \[0,1\].</span></span>

<span data-ttu-id="bb591-130">Чтобы определить требуемый размер *Map*, вызовите [**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с соответствующей символьной константой.</span><span class="sxs-lookup"><span data-stu-id="bb591-130">To determine the required size of *map*, call [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with the appropriate symbolic constant.</span></span>

<span data-ttu-id="bb591-131">Если возникает ошибка, содержимое *значений* не изменяется.</span><span class="sxs-lookup"><span data-stu-id="bb591-131">If an error is generated, no change is made to the contents of *values*.</span></span>

<span data-ttu-id="bb591-132">Следующие функции извлекают сведения, относящиеся к **глжетпикселмап**:</span><span class="sxs-lookup"><span data-stu-id="bb591-132">The following functions retrieve information related to **glGetPixelMap**:</span></span>

<span data-ttu-id="bb591-133">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ пиксель \_ Map \_ i \_ , \_ \_ Размер</span><span class="sxs-lookup"><span data-stu-id="bb591-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PIXEL\_MAP\_I\_TO\_I\_SIZE</span></span>

<span data-ttu-id="bb591-134">**глжет** с аргументом \_ GL \_ пиксель \_ Map \_ с \_ \_ размером s</span><span class="sxs-lookup"><span data-stu-id="bb591-134">**glGet** with argument GL\_PIXEL\_MAP\_S\_TO\_S\_SIZE</span></span>

<span data-ttu-id="bb591-135">**глжет** с аргументом \_ GL \_ пиксель \_ Map \_ с I на \_ R \_ size</span><span class="sxs-lookup"><span data-stu-id="bb591-135">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_R\_SIZE</span></span>

<span data-ttu-id="bb591-136">**глжет** с аргументом GL \_ пиксель \_ Map \_ I \_ на \_ G \_ size</span><span class="sxs-lookup"><span data-stu-id="bb591-136">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_G\_SIZE</span></span>

<span data-ttu-id="bb591-137">**глжет** с аргументом GL \_ пиксель \_ Map \_ I \_ на \_ B \_ size</span><span class="sxs-lookup"><span data-stu-id="bb591-137">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_B\_SIZE</span></span>

<span data-ttu-id="bb591-138">**глжет** с аргументом GL \_ пиксель \_ Map \_ I \_ на \_ \_ Размер</span><span class="sxs-lookup"><span data-stu-id="bb591-138">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_A\_SIZE</span></span>

<span data-ttu-id="bb591-139">**глжет** с аргументом GL \_ пиксель \_ Map \_ r \_ to \_ r \_ size</span><span class="sxs-lookup"><span data-stu-id="bb591-139">**glGet** with argument GL\_PIXEL\_MAP\_R\_TO\_R\_SIZE</span></span>

<span data-ttu-id="bb591-140">**глжет** с аргументом GL \_ пиксель \_ Map \_ g \_ к \_ g \_ size</span><span class="sxs-lookup"><span data-stu-id="bb591-140">**glGet** with argument GL\_PIXEL\_MAP\_G\_TO\_G\_SIZE</span></span>

<span data-ttu-id="bb591-141">**глжет** с аргументом GL \_ пиксель \_ Map \_ b \_ к \_ b \_ size</span><span class="sxs-lookup"><span data-stu-id="bb591-141">**glGet** with argument GL\_PIXEL\_MAP\_B\_TO\_B\_SIZE</span></span>

<span data-ttu-id="bb591-142">**глжет** с аргументом GL \_ пиксель \_ сопоставьте \_ a \_ с \_ \_ размером</span><span class="sxs-lookup"><span data-stu-id="bb591-142">**glGet** with argument GL\_PIXEL\_MAP\_A\_TO\_A\_SIZE</span></span>

<span data-ttu-id="bb591-143">**глжет** с аргументом GL \_ максимальный размер \_ \_ \_ таблицы карт</span><span class="sxs-lookup"><span data-stu-id="bb591-143">**glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE</span></span>

## <a name="requirements"></a><span data-ttu-id="bb591-144">Требования</span><span class="sxs-lookup"><span data-stu-id="bb591-144">Requirements</span></span>



| <span data-ttu-id="bb591-145">Требование</span><span class="sxs-lookup"><span data-stu-id="bb591-145">Requirement</span></span> | <span data-ttu-id="bb591-146">Значение</span><span class="sxs-lookup"><span data-stu-id="bb591-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb591-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb591-147">Minimum supported client</span></span><br/> | <span data-ttu-id="bb591-148">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bb591-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bb591-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb591-149">Minimum supported server</span></span><br/> | <span data-ttu-id="bb591-150">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bb591-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bb591-151">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bb591-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb591-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb591-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bb591-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bb591-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb591-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb591-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bb591-155">DLL</span><span class="sxs-lookup"><span data-stu-id="bb591-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb591-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb591-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb591-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb591-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb591-158">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="bb591-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bb591-159">**глкопипикселс**</span><span class="sxs-lookup"><span data-stu-id="bb591-159">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="bb591-160">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="bb591-160">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="bb591-161">**гленд**</span><span class="sxs-lookup"><span data-stu-id="bb591-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bb591-162">**глжет**</span><span class="sxs-lookup"><span data-stu-id="bb591-162">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="bb591-163">**глпикселмап**</span><span class="sxs-lookup"><span data-stu-id="bb591-163">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="bb591-164">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="bb591-164">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="bb591-165">**глреадпикселс**</span><span class="sxs-lookup"><span data-stu-id="bb591-165">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="bb591-166">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="bb591-166">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="bb591-167">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="bb591-167">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





