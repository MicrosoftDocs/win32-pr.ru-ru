---
title: Функция Глиндекспоинтер (GL. h)
description: Функция Глиндекспоинтер определяет массив цветовых индексов.
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- Функция Глиндекспоинтер OpenGL
topic_type:
- apiref
api_name:
- glIndexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca6858d7d1e3f13e4155bd40307a53b22e80a56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489153"
---
# <a name="glindexpointer-function"></a><span data-ttu-id="3aa3f-104">Функция Глиндекспоинтер</span><span class="sxs-lookup"><span data-stu-id="3aa3f-104">glIndexPointer function</span></span>

<span data-ttu-id="3aa3f-105">Функция **глиндекспоинтер** определяет массив цветовых индексов.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-105">The **glIndexPointer** function defines an array of color indexes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa3f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3aa3f-106">Syntax</span></span>


```C++
void WINAPI glIndexPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="3aa3f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3aa3f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aa3f-108">*type*</span><span class="sxs-lookup"><span data-stu-id="3aa3f-108">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="3aa3f-109">Тип данных каждого цветового индекса в массиве, используя следующие символьные константы: GL \_ Short, GL \_ int, GL \_ с плавающей запятой, ГК \_ Double.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-109">The data type of each color index in the array using the following symbolic constants: GL\_SHORT, GL\_INT, GL\_FLOAT, GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="3aa3f-110">*шага*</span><span class="sxs-lookup"><span data-stu-id="3aa3f-110">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="3aa3f-111">Смещение в байтах между последовательными индексами цвета.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-111">The byte offset between consecutive color indexes.</span></span> <span data-ttu-id="3aa3f-112">Если *шаг* равен нулю, индексы цвета жестко упакованы в массив.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-112">When *stride* is zero, the color indexes are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="3aa3f-113">*указатель*</span><span class="sxs-lookup"><span data-stu-id="3aa3f-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="3aa3f-114">Указатель на первый цветовой индекс в массиве.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-114">A pointer to the first color index in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aa3f-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3aa3f-115">Return value</span></span>

<span data-ttu-id="3aa3f-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3aa3f-117">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3aa3f-117">Error codes</span></span>

<span data-ttu-id="3aa3f-118">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3aa3f-119">Имя</span><span class="sxs-lookup"><span data-stu-id="3aa3f-119">Name</span></span>                                                                                              | <span data-ttu-id="3aa3f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3aa3f-120">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3aa3f-121"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="3aa3f-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="3aa3f-122">*тип* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-122">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="3aa3f-123"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="3aa3f-123"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="3aa3f-124">*шаг* или *число* были отрицательными.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-124">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3aa3f-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3aa3f-125">Remarks</span></span>

<span data-ttu-id="3aa3f-126">Функция **глиндекспоинтер** задает расположение и данные массива цветовых индексов, используемых при подготовке к просмотру.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-126">The **glIndexPointer** function specifies the location and data of an array of color indexes to use when rendering.</span></span> <span data-ttu-id="3aa3f-127">Параметр *типа* задает тип данных каждого цветового индекса, а *шаг* смещения определяет смещение в байтах от одного цветового индекса к другому, позволяя использовать упаковку вершин и атрибуты в одном массиве или хранилище в отдельных массивах.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-127">The *type* parameter specifies the data type of each color index and *stride* determines the byte offset from one color index to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="3aa3f-128">В некоторых реализациях хранение вершин и атрибутов в одном массиве может быть более эффективным, чем использование отдельных массивов.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-128">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span> <span data-ttu-id="3aa3f-129">Дополнительные сведения см. в разделе [**глинтерлеаведаррайс**](glinterleavedarrays.md).</span><span class="sxs-lookup"><span data-stu-id="3aa3f-129">For more information, see [**glInterleavedArrays**](glinterleavedarrays.md).</span></span>

<span data-ttu-id="3aa3f-130">Массив цветового индекса включается при указании \_ \_ константы массива индекса GL с помощью [**гленаблеклиентстате**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="3aa3f-130">A color-index array is enabled when you specify the GL\_INDEX\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="3aa3f-131">Если этот параметр включен, [**глдраваррайс**](gldrawarrays.md) и [**гларрайелемент**](glarrayelement.md) используют массив цветового индекса.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-131">When enabled, [**glDrawArrays**](gldrawarrays.md) and [**glArrayElement**](glarrayelement.md) use the color-index array.</span></span> <span data-ttu-id="3aa3f-132">По умолчанию массив цветового индекса отключен.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-132">By default the color-index array is disabled.</span></span>

<span data-ttu-id="3aa3f-133">Невозможно включить **глиндекспоинтер** в списки вывода.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-133">You cannot include **glIndexPointer** in display lists.</span></span>

<span data-ttu-id="3aa3f-134">При указании массива цветового индекса с помощью **глиндекспоинтер** значения всех параметров массива цветового индекса функции сохраняются в состоянии на стороне клиента, а статические элементы массива могут быть кэшированы.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-134">When you specify a color-index array using **glIndexPointer**, the values of all the function's color-index array parameters are saved in a client-side state and static array elements can be cached.</span></span> <span data-ttu-id="3aa3f-135">Так как параметры массива цветового индекса являются состояниями на стороне клиента, их значения не сохраняются и не восстанавливаются [**глпушаттриб**](glpushattrib.md) и **глпопаттриб**.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-135">Because the color-index array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span>

<span data-ttu-id="3aa3f-136">Несмотря на то что ошибка не возникает при вызове **глиндекспоинтер** в парах [**глбегин**](glbegin.md) и **гленд** , результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="3aa3f-136">Although no error is generated when you call **glIndexPointer** within [**glBegin**](glbegin.md) and **glEnd** pairs, the results are undefined.</span></span>

<span data-ttu-id="3aa3f-137">Следующие функции извлекают сведения, относящиеся к **глиндекспоинтер**:</span><span class="sxs-lookup"><span data-stu-id="3aa3f-137">The following functions retrieve information related to **glIndexPointer**:</span></span>

<span data-ttu-id="3aa3f-138">[**глисенаблед**](glisenabled.md) с аргументом \_ Array индекса GL \_</span><span class="sxs-lookup"><span data-stu-id="3aa3f-138">[**glIsEnabled**](glisenabled.md) with argument GL\_INDEX\_ARRAY</span></span>

<span data-ttu-id="3aa3f-139">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ index \_ массива индекса \_ stride</span><span class="sxs-lookup"><span data-stu-id="3aa3f-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="3aa3f-140">**глжет** с аргументом \_ \_ число МАССИВов индексов GL \_</span><span class="sxs-lookup"><span data-stu-id="3aa3f-140">**glGet** with argument GL\_INDEX\_ARRAY\_COUNT</span></span>

<span data-ttu-id="3aa3f-141">**глжет** с аргументом \_ \_ тип массива индексов GL \_</span><span class="sxs-lookup"><span data-stu-id="3aa3f-141">**glGet** with argument GL\_INDEX\_ARRAY\_TYPE</span></span>

<span data-ttu-id="3aa3f-142">**глжет** с аргументом \_ \_ Размер массива \_ индекса GL</span><span class="sxs-lookup"><span data-stu-id="3aa3f-142">**glGet** with argument GL\_INDEX\_ARRAY\_SIZE</span></span>

<span data-ttu-id="3aa3f-143">[**глжетпоинтерв**](glgetpointerv.md) с аргументом \_ \_ указатель массива \_ индекса GL</span><span class="sxs-lookup"><span data-stu-id="3aa3f-143">[**glGetPointerv**](glgetpointerv.md) with argument GL\_INDEX\_ARRAY\_POINTER</span></span>

## <a name="requirements"></a><span data-ttu-id="3aa3f-144">Требования</span><span class="sxs-lookup"><span data-stu-id="3aa3f-144">Requirements</span></span>



| <span data-ttu-id="3aa3f-145">Требование</span><span class="sxs-lookup"><span data-stu-id="3aa3f-145">Requirement</span></span> | <span data-ttu-id="3aa3f-146">Значение</span><span class="sxs-lookup"><span data-stu-id="3aa3f-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa3f-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3aa3f-147">Minimum supported client</span></span><br/> | <span data-ttu-id="3aa3f-148">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3aa3f-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3aa3f-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3aa3f-149">Minimum supported server</span></span><br/> | <span data-ttu-id="3aa3f-150">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3aa3f-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3aa3f-151">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3aa3f-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aa3f-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3aa3f-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3aa3f-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3aa3f-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="3aa3f-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3aa3f-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3aa3f-155">DLL</span><span class="sxs-lookup"><span data-stu-id="3aa3f-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3aa3f-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3aa3f-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aa3f-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3aa3f-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa3f-158">**гларрайелемент**</span><span class="sxs-lookup"><span data-stu-id="3aa3f-158">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="3aa3f-159">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="3aa3f-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="3aa3f-160">**глдраваррайс**</span><span class="sxs-lookup"><span data-stu-id="3aa3f-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="3aa3f-161">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="3aa3f-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="3aa3f-162">**глжетпоинтерв**</span><span class="sxs-lookup"><span data-stu-id="3aa3f-162">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="3aa3f-163">**глжетстринг**</span><span class="sxs-lookup"><span data-stu-id="3aa3f-163">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="3aa3f-164">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="3aa3f-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="3aa3f-165">**глпушаттриб**</span><span class="sxs-lookup"><span data-stu-id="3aa3f-165">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="3aa3f-166">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="3aa3f-166">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="3aa3f-167">**глвертекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="3aa3f-167">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





