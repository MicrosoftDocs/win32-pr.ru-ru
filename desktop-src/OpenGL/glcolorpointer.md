---
title: Функция Глколорпоинтер (GL. h)
description: Функция Глколорпоинтер определяет массив цветов.
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- Функция Глколорпоинтер OpenGL
topic_type:
- apiref
api_name:
- glColorPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abced52f0d0664e998ad8380e33d43d4af36bcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489738"
---
# <a name="glcolorpointer-function"></a><span data-ttu-id="4bd2c-104">Функция Глколорпоинтер</span><span class="sxs-lookup"><span data-stu-id="4bd2c-104">glColorPointer function</span></span>

<span data-ttu-id="4bd2c-105">Функция **глколорпоинтер** определяет массив цветов.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-105">The **glColorPointer** function defines an array of colors.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bd2c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4bd2c-106">Syntax</span></span>


```C++
void WINAPI glColorPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="4bd2c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bd2c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bd2c-108">*size*</span><span class="sxs-lookup"><span data-stu-id="4bd2c-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="4bd2c-109">Число компонентов на цвет.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-109">The number of components per color.</span></span> <span data-ttu-id="4bd2c-110">Значение должно быть либо 3, либо 4.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-110">The value must be either 3 or 4.</span></span>

</dd> <dt>

<span data-ttu-id="4bd2c-111">*type*</span><span class="sxs-lookup"><span data-stu-id="4bd2c-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="4bd2c-112">Тип данных каждого компонента цвета в массиве цветов.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-112">The data type of each color component in a color array.</span></span> <span data-ttu-id="4bd2c-113">Допустимые типы данных задаются со следующими константами: GL \_ , \_ неподписанный байт, формат GL, короткий, GL без знака, "short int", "Неподписанное целое число", некоторая с \_ \_ \_ \_ \_ \_ \_ \_ плавающей запятой или значение \_ типа "double".</span><span class="sxs-lookup"><span data-stu-id="4bd2c-113">Acceptable data types are specified with the following constants: GL\_BYTE, GL\_UNSIGNED\_BYTE, GL\_SHORT, GL\_UNSIGNED\_SHORT, GL\_INT, GL\_UNSIGNED\_INT, GL\_FLOAT, or GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="4bd2c-114">*шага*</span><span class="sxs-lookup"><span data-stu-id="4bd2c-114">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="4bd2c-115">Смещение в байтах между последовательными цветами.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-115">The byte offset between consecutive colors.</span></span> <span data-ttu-id="4bd2c-116">Если *шаг* равен нулю, цвета жестко упакованы в массив.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-116">When *stride* is zero, the colors are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="4bd2c-117">*указатель*</span><span class="sxs-lookup"><span data-stu-id="4bd2c-117">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="4bd2c-118">Указатель на первый компонент первого элемента Color в массиве цветов.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-118">A pointer to the first component of the first color element in a color array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bd2c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4bd2c-119">Return value</span></span>

<span data-ttu-id="4bd2c-120">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4bd2c-121">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4bd2c-121">Error codes</span></span>

<span data-ttu-id="4bd2c-122">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4bd2c-123">Имя</span><span class="sxs-lookup"><span data-stu-id="4bd2c-123">Name</span></span>                                                                                              | <span data-ttu-id="4bd2c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4bd2c-124">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4bd2c-125"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4bd2c-125"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="4bd2c-126">*Размер* не был 3 или 4.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-126">*size* was not 3 or 4.</span></span><br/>            |
| <dl> <span data-ttu-id="4bd2c-127"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4bd2c-127"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="4bd2c-128">*тип* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-128">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="4bd2c-129"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4bd2c-129"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="4bd2c-130">*шаг* или *число* были отрицательными.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-130">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4bd2c-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4bd2c-131">Remarks</span></span>

<span data-ttu-id="4bd2c-132">Функция **глколорпоинтер** задает расположение и формат данных для массива компонентов цвета, используемых при подготовке к просмотру.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-132">The **glColorPointer** function specifies the location and data format of an array of color components to use when rendering.</span></span> <span data-ttu-id="4bd2c-133">Параметр *stride* определяет смещение в байтах от одного цвета к другому, позволяя использовать упаковку атрибутов вершин в одном массиве или хранилище в отдельных массивах.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-133">The *stride* parameter determines the byte offset from one color to the next, enabling the packing of vertex attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="4bd2c-134">В некоторых реализациях хранение атрибутов вершин в одном массиве может оказаться более эффективным, чем использование отдельных массивов.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-134">In some implementations, storing vertex attributes in a single array can be more efficient than the use of separate arrays.</span></span>

<span data-ttu-id="4bd2c-135">Включить массив цветов, указав \_ \_ константу массива цветов GL с [**гленаблеклиентстате**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="4bd2c-135">Enabled the color array by specifying the GL\_COLOR\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="4bd2c-136">При вызове [**гларрайелемент**](glarrayelement.md), [**глдравелементс**](gldrawelements.md)или [**глдраваррайс**](gldrawarrays.md) используется массив цветов, который, таким же, включен.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-136">Calling [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md) uses the color array that is thus enabled.</span></span> <span data-ttu-id="4bd2c-137">По умолчанию массив цветов отключен.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-137">By default, the color array is disabled.</span></span> <span data-ttu-id="4bd2c-138">Вызовы **глколорпоинтер** не могут быть указаны в списках вывода.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-138">The **glColorPointer** calls cannot by entered in display lists.</span></span>

<span data-ttu-id="4bd2c-139">При указании массива цветов с помощью **глколорпоинтер** значения всех параметров массива цветов функции сохраняются в состоянии на стороне клиента, а также можно кэшировать статические элементы массива.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-139">When you specify a color array using **glColorPointer**, the values of all the function's color array parameters are saved in a client-side state, and you can cache static array elements.</span></span> <span data-ttu-id="4bd2c-140">Так как параметры массива цветов находятся в состоянии на стороне клиента, [**глпушаттриб**](glpushattrib.md) и [**глпопаттриб**](glpopattrib.md) не сохраняют и не восстанавливают значения параметров.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-140">Because the color array parameters are in a client-side state, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) do not save or restore the parameters' values.</span></span>

<span data-ttu-id="4bd2c-141">Хотя указание массива цветов в парах [**глбегин**](glbegin.md) и [**гленд**](glend.md) не приводит к формированию ошибки, результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="4bd2c-141">Although specifying the color array within [**glBegin**](glbegin.md) and [**glend**](glend.md) pairs does not generate an error, the results are undefined.</span></span>

<span data-ttu-id="4bd2c-142">Следующие функции извлекают сведения, относящиеся к функции **глколорпоинтер** :</span><span class="sxs-lookup"><span data-stu-id="4bd2c-142">The following functions retrieve information related to the **glColorPointer** function:</span></span>

<span data-ttu-id="4bd2c-143">[**глисенаблед**](glisenabled.md) с аргументом \_ массива цветов GL \_</span><span class="sxs-lookup"><span data-stu-id="4bd2c-143">[**glIsEnabled**](glisenabled.md) with argument GL\_COLOR\_ARRAY</span></span>

<span data-ttu-id="4bd2c-144">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ \_ Размер массива \_ цветов GL</span><span class="sxs-lookup"><span data-stu-id="4bd2c-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_ARRAY\_SIZE</span></span>

<span data-ttu-id="4bd2c-145">**глжет** с аргументом \_ \_ тип массива \_ цветов GL</span><span class="sxs-lookup"><span data-stu-id="4bd2c-145">**glGet** with argument GL\_COLOR\_ARRAY\_TYPE</span></span>

<span data-ttu-id="4bd2c-146">**глжет** с аргументом \_ массива цветов GL \_ \_ stride</span><span class="sxs-lookup"><span data-stu-id="4bd2c-146">**glGet** with argument GL\_COLOR\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="4bd2c-147">**глжет** с аргументом \_ \_ число массивов цветов GL \_</span><span class="sxs-lookup"><span data-stu-id="4bd2c-147">**glGet** with argument GL\_COLOR\_ARRAY\_COUNT</span></span>

<span data-ttu-id="4bd2c-148">[**глжетпоинтерв**](glgetpointerv.md) с аргументом \_ \_ указатель на массив цветов GL \_</span><span class="sxs-lookup"><span data-stu-id="4bd2c-148">[**glGetPointerv**](glgetpointerv.md) with argument GL\_COLOR\_ARRAY\_POINTER</span></span>

## <a name="requirements"></a><span data-ttu-id="4bd2c-149">Требования</span><span class="sxs-lookup"><span data-stu-id="4bd2c-149">Requirements</span></span>



| <span data-ttu-id="4bd2c-150">Требование</span><span class="sxs-lookup"><span data-stu-id="4bd2c-150">Requirement</span></span> | <span data-ttu-id="4bd2c-151">Значение</span><span class="sxs-lookup"><span data-stu-id="4bd2c-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bd2c-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4bd2c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4bd2c-153">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4bd2c-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4bd2c-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4bd2c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4bd2c-155">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4bd2c-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4bd2c-156">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4bd2c-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bd2c-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bd2c-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4bd2c-158">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4bd2c-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="4bd2c-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bd2c-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4bd2c-160">DLL</span><span class="sxs-lookup"><span data-stu-id="4bd2c-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bd2c-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bd2c-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bd2c-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4bd2c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bd2c-163">**гларрайелемент**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-163">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="4bd2c-164">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-164">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4bd2c-165">**глдраваррайс**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-165">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="4bd2c-166">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-166">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="4bd2c-167">**гленаблеклиентстате**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-167">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="4bd2c-168">**гленд**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4bd2c-169">**глжет**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-169">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="4bd2c-170">**глжетстринг**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-170">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="4bd2c-171">**глжетпоинтерв**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-171">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="4bd2c-172">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-172">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="4bd2c-173">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-173">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="4bd2c-174">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-174">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="4bd2c-175">**глпопаттриб**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-175">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="4bd2c-176">**глпушаттриб**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-176">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="4bd2c-177">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-177">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="4bd2c-178">**глвертекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="4bd2c-178">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





