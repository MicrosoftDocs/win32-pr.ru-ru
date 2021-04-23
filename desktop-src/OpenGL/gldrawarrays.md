---
title: Функция Глдраваррайс (GL. h)
description: Функция Глдраваррайс указывает несколько примитивов для отображения.
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- Функция Глдраваррайс OpenGL
topic_type:
- apiref
api_name:
- glDrawArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88b20cf3a3e3b2c96a8172f53f8126815efe16d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988787"
---
# <a name="gldrawarrays-function"></a><span data-ttu-id="9f39f-104">Функция Глдраваррайс</span><span class="sxs-lookup"><span data-stu-id="9f39f-104">glDrawArrays function</span></span>

<span data-ttu-id="9f39f-105">Функция **глдраваррайс** указывает несколько примитивов для отображения.</span><span class="sxs-lookup"><span data-stu-id="9f39f-105">The **glDrawArrays** function specifies multiple primitives to render.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f39f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f39f-106">Syntax</span></span>


```C++
void WINAPI glDrawArrays(
   GLenum  mode,
   GLint   first,
   GLsizei count
);
```



## <a name="parameters"></a><span data-ttu-id="9f39f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f39f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f39f-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="9f39f-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="9f39f-109">Тип отображаемых примитивов.</span><span class="sxs-lookup"><span data-stu-id="9f39f-109">The kind of primitives to render.</span></span> <span data-ttu-id="9f39f-110">Следующие константы задают допустимые типы примитивов: \_ точки GL, \_ Линейная \_ полоса строк GL, \_ линейный \_ цикл строки, строки GL, ленту с треугольным треугольником, \_ \_ \_ \_ \_ \_ вершинный Вентилятор, треугольники GL, \_ четыре чередующихся элемента, четыре неметрических элемента \_ \_ и \_ многоугольник GL.</span><span class="sxs-lookup"><span data-stu-id="9f39f-110">The following constants specify acceptable types of primitives: GL\_POINTS, GL\_LINE\_STRIP, GL\_LINE\_LOOP, GL\_LINES, GL\_TRIANGLE\_STRIP, GL\_TRIANGLE\_FAN, GL\_TRIANGLES, GL\_QUAD\_STRIP, GL\_QUADS, and GL\_POLYGON.</span></span>

</dd> <dt>

<span data-ttu-id="9f39f-111">*first*</span><span class="sxs-lookup"><span data-stu-id="9f39f-111">*first*</span></span> 
</dt> <dd>

<span data-ttu-id="9f39f-112">Начальный индекс в включенных массивах.</span><span class="sxs-lookup"><span data-stu-id="9f39f-112">The starting index in the enabled arrays.</span></span>

</dd> <dt>

<span data-ttu-id="9f39f-113">*count*</span><span class="sxs-lookup"><span data-stu-id="9f39f-113">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="9f39f-114">Число индексов для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="9f39f-114">The number of indexes to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f39f-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f39f-115">Return value</span></span>

<span data-ttu-id="9f39f-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9f39f-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9f39f-117">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="9f39f-117">Error codes</span></span>

<span data-ttu-id="9f39f-118">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="9f39f-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9f39f-119">Имя</span><span class="sxs-lookup"><span data-stu-id="9f39f-119">Name</span></span>                                                                                                  | <span data-ttu-id="9f39f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9f39f-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9f39f-121"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="9f39f-121"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="9f39f-122">*число* было отрицательным.</span><span class="sxs-lookup"><span data-stu-id="9f39f-122">*count* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="9f39f-123"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="9f39f-123"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="9f39f-124">*режим* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="9f39f-124">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="9f39f-125"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="9f39f-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9f39f-126">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9f39f-126">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9f39f-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f39f-127">Remarks</span></span>

<span data-ttu-id="9f39f-128">С помощью **глдраваррайс** можно указать несколько геометрических примитивов для отображения.</span><span class="sxs-lookup"><span data-stu-id="9f39f-128">With **glDrawArrays**, you can specify multiple geometric primitives to render.</span></span> <span data-ttu-id="9f39f-129">Вместо вызова отдельных функций OpenGL для передачи каждой отдельной вершины, обычной или цветовой области можно указать отдельные массивы вершин, нормалей и цветов, чтобы определить последовательность примитивов (одинаковый тип) с одним вызовом **глдраваррайс**.</span><span class="sxs-lookup"><span data-stu-id="9f39f-129">Instead of calling separate OpenGL functions to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors to define a sequence of primitives (all the same kind) with a single call to **glDrawArrays**.</span></span>

<span data-ttu-id="9f39f-130">При вызове **глдраваррайс** *число* последовательных элементов из каждого разрешенного массива используется для создания последовательности геометрических примитивов, начиная с *первого* элемента.</span><span class="sxs-lookup"><span data-stu-id="9f39f-130">When you call **glDrawArrays**, *count* sequential elements from each enabled array are used to construct a sequence of geometric primitives, beginning with the *first* element.</span></span> <span data-ttu-id="9f39f-131">Параметр *mode* определяет тип создаваемого примитива и использование элементов массива для создания примитивов.</span><span class="sxs-lookup"><span data-stu-id="9f39f-131">The *mode* parameter specifies what kind of primitive to construct and how to use the array elements to construct the primitives.</span></span>

<span data-ttu-id="9f39f-132">После возврата **глдраваррайс** значения атрибутов вершин, измененных **глдраваррайс** , не определены.</span><span class="sxs-lookup"><span data-stu-id="9f39f-132">After **glDrawArrays** returns, the values of vertex attributes that are modified by **glDrawArrays** are undefined.</span></span> <span data-ttu-id="9f39f-133">Например, если \_ \_ включен массив цветов GL, значение текущего цвета не определено после возврата **глдраваррайс** .</span><span class="sxs-lookup"><span data-stu-id="9f39f-133">For example, if GL\_COLOR\_ARRAY is enabled, the value of the current color is undefined after **glDrawArrays** returns.</span></span> <span data-ttu-id="9f39f-134">Атрибуты, не измененные **глдраваррайс** , остаются определенными.</span><span class="sxs-lookup"><span data-stu-id="9f39f-134">Attributes not modified by **glDrawArrays** remain defined.</span></span> <span data-ttu-id="9f39f-135">Если \_ массив ВЕРШИН GL \_ не включен, геометрические примитивы не создаются, но атрибуты, соответствующие включенным массивам, изменяются.</span><span class="sxs-lookup"><span data-stu-id="9f39f-135">When GL\_VERTEX\_ARRAY is not enabled, no geometric primitives are generated but the attributes corresponding to enabled arrays are modified.</span></span>

<span data-ttu-id="9f39f-136">**Глдраваррайс** можно включить в списки вывода.</span><span class="sxs-lookup"><span data-stu-id="9f39f-136">You can include **glDrawArrays** in display lists.</span></span> <span data-ttu-id="9f39f-137">При включении **глдраваррайс** в список отображений необходимые данные массива, определяемые указателями на массивы и включенными, создаются и записываются в список отображаемых данных.</span><span class="sxs-lookup"><span data-stu-id="9f39f-137">When you include **glDrawArrays** in a display list, the necessary array data, determined by the array pointers and the enables, are generated and entered in the display list.</span></span> <span data-ttu-id="9f39f-138">Значения указателей на массивы и включения определяются во время создания списков вывода.</span><span class="sxs-lookup"><span data-stu-id="9f39f-138">The values of array pointers and enables are determined during the creation of display lists.</span></span>

<span data-ttu-id="9f39f-139">Данные статического массива можно считывать в любое время.</span><span class="sxs-lookup"><span data-stu-id="9f39f-139">You can read static array data at any time.</span></span> <span data-ttu-id="9f39f-140">Если какие-либо статические элементы массива изменяются и массив не указан снова, результаты всех последующих вызовов **глдраваррайс** будут неопределенными.</span><span class="sxs-lookup"><span data-stu-id="9f39f-140">If any static array elements are modified and the array is not specified again, the results of any subsequent calls to **glDrawArrays** are undefined.</span></span>

<span data-ttu-id="9f39f-141">Хотя при указании массива несколько раз в пределах пар [**глбегин**](glbegin.md) и [**гленд**](glend.md) не возникает ошибок, результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="9f39f-141">Although no error is generated when you specify an array more than once within [**glBegin**](glbegin.md) and [**glend**](glend.md) pairs, the results are undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f39f-142">Требования</span><span class="sxs-lookup"><span data-stu-id="9f39f-142">Requirements</span></span>



| <span data-ttu-id="9f39f-143">Требование</span><span class="sxs-lookup"><span data-stu-id="9f39f-143">Requirement</span></span> | <span data-ttu-id="9f39f-144">Значение</span><span class="sxs-lookup"><span data-stu-id="9f39f-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f39f-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f39f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="9f39f-146">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f39f-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9f39f-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f39f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="9f39f-148">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f39f-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9f39f-149">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9f39f-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f39f-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f39f-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9f39f-151">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f39f-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f39f-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f39f-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9f39f-153">DLL</span><span class="sxs-lookup"><span data-stu-id="9f39f-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f39f-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f39f-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f39f-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f39f-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f39f-156">**гларрайелемент**</span><span class="sxs-lookup"><span data-stu-id="9f39f-156">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="9f39f-157">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="9f39f-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9f39f-158">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="9f39f-158">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="9f39f-159">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="9f39f-159">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="9f39f-160">**гленд**</span><span class="sxs-lookup"><span data-stu-id="9f39f-160">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9f39f-161">**глжетпоинтерв**</span><span class="sxs-lookup"><span data-stu-id="9f39f-161">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="9f39f-162">**глжетстринг**</span><span class="sxs-lookup"><span data-stu-id="9f39f-162">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="9f39f-163">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="9f39f-163">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="9f39f-164">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="9f39f-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="9f39f-165">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="9f39f-165">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="9f39f-166">**глвертекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="9f39f-166">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





