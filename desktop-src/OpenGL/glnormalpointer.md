---
title: Функция Глнормалпоинтер (GL. h)
description: Функция Глнормалпоинтер определяет массив нормалей.
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- Функция Глнормалпоинтер OpenGL
topic_type:
- apiref
api_name:
- glNormalPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f3abbfbd989351af647557ec64f8ee3172dc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989394"
---
# <a name="glnormalpointer-function"></a><span data-ttu-id="8ec3c-104">Функция Глнормалпоинтер</span><span class="sxs-lookup"><span data-stu-id="8ec3c-104">glNormalPointer function</span></span>

<span data-ttu-id="8ec3c-105">Функция **глнормалпоинтер** определяет массив нормалей.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-105">The **glNormalPointer** function defines an array of normals.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ec3c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ec3c-106">Syntax</span></span>


```C++
void WINAPI glNormalPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="8ec3c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ec3c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ec3c-108">*type*</span><span class="sxs-lookup"><span data-stu-id="8ec3c-108">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="8ec3c-109">Тип данных каждой координаты в массиве с использованием следующих символьных констант: GL, Short, GL, GL \_ \_ и GL, с \_ \_ плавающей запятой \_ .</span><span class="sxs-lookup"><span data-stu-id="8ec3c-109">The data type of each coordinate in the array using the following symbolic constants: GL\_BYTE, GL\_SHORT, GL\_INT, GL\_FLOAT, and GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="8ec3c-110">*шага*</span><span class="sxs-lookup"><span data-stu-id="8ec3c-110">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="8ec3c-111">Смещение в байтах между последовательными нормальными значениями.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-111">The byte offset between consecutive normals.</span></span> <span data-ttu-id="8ec3c-112">Если *шаг* равен нулю, нормали тесно упакованы в массив.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-112">When *stride* is zero, the normals are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="8ec3c-113">*указатель*</span><span class="sxs-lookup"><span data-stu-id="8ec3c-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="8ec3c-114">Указатель на первое значение нормали в массиве.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-114">A pointer to the first normal in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ec3c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ec3c-115">Return value</span></span>

<span data-ttu-id="8ec3c-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8ec3c-117">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="8ec3c-117">Error codes</span></span>

<span data-ttu-id="8ec3c-118">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8ec3c-119">Имя</span><span class="sxs-lookup"><span data-stu-id="8ec3c-119">Name</span></span>                                                                                                  | <span data-ttu-id="8ec3c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8ec3c-120">Meaning</span></span>                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8ec3c-121"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec3c-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8ec3c-122">*тип* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-122">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="8ec3c-123"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec3c-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8ec3c-124">*шаг* или *число* были отрицательными.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-124">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8ec3c-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ec3c-125">Remarks</span></span>

<span data-ttu-id="8ec3c-126">Функция **глнормалпоинтер** задает расположение и данные массива нормалей для использования при подготовке к просмотру.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-126">The **glNormalPointer** function specifies the location and data of an array of normals to use when rendering.</span></span> <span data-ttu-id="8ec3c-127">Параметр *типа* задает тип данных каждой стандартной координаты.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-127">The *type* parameter specifies the data type of each normal coordinate.</span></span> <span data-ttu-id="8ec3c-128">Параметр *stride* определяет смещение в байтах от одного обычного до следующего, включая упаковку вершин и атрибуты в одном массиве или хранилище в отдельных массивах.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-128">The *stride* parameter determines the byte offset from one normal to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="8ec3c-129">В некоторых реализациях хранение вершин и атрибутов в одном массиве может быть более эффективным, чем использование отдельных массивов. Дополнительные сведения см. в разделе [**глинтерлеаведаррайс**](glinterleavedarrays.md) .</span><span class="sxs-lookup"><span data-stu-id="8ec3c-129">In some implementations storing the vertices and attributes in a single array can be more efficient than using separate arrays; see [**glInterleavedArrays**](glinterleavedarrays.md) for details.</span></span>

<span data-ttu-id="8ec3c-130">Стандартный массив включается при указании \_ обычной \_ константы массива GL с помощью [**гленаблеклиентстате**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="8ec3c-130">A normal array is enabled when you specify the GL\_NORMAL\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="8ec3c-131">Если параметр включен, [**глдраваррайс**](gldrawarrays.md), [**глдравелементс**](gldrawelements.md) и [**гларрайелемент**](glarrayelement.md) используют стандартный массив.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-131">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md) and [**glArrayElement**](glarrayelement.md) use the normal array.</span></span> <span data-ttu-id="8ec3c-132">По умолчанию стандартный массив отключен.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-132">By default the normal array is disabled.</span></span>

<span data-ttu-id="8ec3c-133">Невозможно включить **глнормалпоинтер** в списки вывода.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-133">You cannot include **glNormalPointer** in display lists.</span></span>

<span data-ttu-id="8ec3c-134">При указании обычного массива с помощью **глнормалпоинтер** значения всех обычных параметров массива функции сохраняются в состоянии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-134">When you specify a normal array using **glNormalPointer**, the values of all the function's normal array parameters are saved in a client-side state.</span></span> <span data-ttu-id="8ec3c-135">Поскольку обычные параметры массива сохраняются в состоянии на стороне клиента, их значения не сохраняются и не восстанавливаются [**глпушаттриб**](glpushattrib.md) и [**глпопаттриб**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="8ec3c-135">Because the normal array parameters are saved in a client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

<span data-ttu-id="8ec3c-136">Несмотря на то что ошибка не возникает при вызове **глнормалпоинтер** в парах [**глбегин**](glbegin.md) и [**гленд**](glend.md) , результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="8ec3c-136">Although no error is generated when you call **glNormalPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="8ec3c-137">С **глнормалпоинтер** связаны следующие функции:</span><span class="sxs-lookup"><span data-stu-id="8ec3c-137">The following functions are associated with **glNormalPointer**:</span></span>

<span data-ttu-id="8ec3c-138">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ обычного \_ массива \_ stride</span><span class="sxs-lookup"><span data-stu-id="8ec3c-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NORMAL\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="8ec3c-139">**глжет** с аргументом \_ стандартное \_ число массивов GL \_</span><span class="sxs-lookup"><span data-stu-id="8ec3c-139">**glGet** with argument GL\_NORMAL\_ARRAY\_COUNT</span></span>

<span data-ttu-id="8ec3c-140">**глжет** с аргументом \_ обычного \_ типа массива GL \_</span><span class="sxs-lookup"><span data-stu-id="8ec3c-140">**glGet** with argument GL\_NORMAL\_ARRAY\_TYPE</span></span>

<span data-ttu-id="8ec3c-141">**глжетпоинтерв** с аргументом \_ обычного \_ указателя массива GL \_</span><span class="sxs-lookup"><span data-stu-id="8ec3c-141">**glGetPointerv** with argument GL\_NORMAL\_ARRAY\_POINTER</span></span>

<span data-ttu-id="8ec3c-142">[**глисенаблед**](glisenabled.md) с аргументом \_ обычного \_ массива GL</span><span class="sxs-lookup"><span data-stu-id="8ec3c-142">[**glIsEnabled**](glisenabled.md) with argument GL\_NORMAL\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="8ec3c-143">Требования</span><span class="sxs-lookup"><span data-stu-id="8ec3c-143">Requirements</span></span>



| <span data-ttu-id="8ec3c-144">Требование</span><span class="sxs-lookup"><span data-stu-id="8ec3c-144">Requirement</span></span> | <span data-ttu-id="8ec3c-145">Значение</span><span class="sxs-lookup"><span data-stu-id="8ec3c-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec3c-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ec3c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8ec3c-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8ec3c-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8ec3c-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ec3c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8ec3c-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8ec3c-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8ec3c-150">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8ec3c-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ec3c-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ec3c-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8ec3c-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8ec3c-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="8ec3c-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ec3c-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8ec3c-154">DLL</span><span class="sxs-lookup"><span data-stu-id="8ec3c-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ec3c-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ec3c-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ec3c-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ec3c-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec3c-157">**гларрайелемент**</span><span class="sxs-lookup"><span data-stu-id="8ec3c-157">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="8ec3c-158">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="8ec3c-158">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="8ec3c-159">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="8ec3c-159">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="8ec3c-160">**глдраваррайс**</span><span class="sxs-lookup"><span data-stu-id="8ec3c-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="8ec3c-161">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="8ec3c-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="8ec3c-162">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="8ec3c-162">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="8ec3c-163">**глжетпоинтерв**</span><span class="sxs-lookup"><span data-stu-id="8ec3c-163">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="8ec3c-164">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="8ec3c-164">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="8ec3c-165">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="8ec3c-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="8ec3c-166">**глинтерлеаведаррайс**</span><span class="sxs-lookup"><span data-stu-id="8ec3c-166">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="8ec3c-167">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="8ec3c-167">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="8ec3c-168">**глвертекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="8ec3c-168">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> <dt>

[<span data-ttu-id="8ec3c-169">**глжетстринг**</span><span class="sxs-lookup"><span data-stu-id="8ec3c-169">**glGetString**</span></span>](glgetstring.md)
</dt> </dl>

 

 





