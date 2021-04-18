---
title: Функция Глвертекспоинтер (GL. h)
description: Функция Глвертекспоинтер определяет массив данных вершин.
ms.assetid: e5f97fdc-9448-4389-8533-3855a3213feb
keywords:
- Функция Глвертекспоинтер OpenGL
topic_type:
- apiref
api_name:
- glVertexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422dd1a7938cc5adb183ff7e17c59a8f52eb4909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492120"
---
# <a name="glvertexpointer-function"></a><span data-ttu-id="decfc-104">Функция Глвертекспоинтер</span><span class="sxs-lookup"><span data-stu-id="decfc-104">glVertexPointer function</span></span>

<span data-ttu-id="decfc-105">Функция **глвертекспоинтер** определяет массив данных вершин.</span><span class="sxs-lookup"><span data-stu-id="decfc-105">The **glVertexPointer** function defines an array of vertex data.</span></span>

## <a name="syntax"></a><span data-ttu-id="decfc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="decfc-106">Syntax</span></span>


```C++
void WINAPI glVertexPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="decfc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="decfc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="decfc-108">*size*</span><span class="sxs-lookup"><span data-stu-id="decfc-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="decfc-109">Число координат на вершину.</span><span class="sxs-lookup"><span data-stu-id="decfc-109">The number of coordinates per vertex.</span></span> <span data-ttu-id="decfc-110">Значение параметра *size* должно быть равно 2, 3 или 4.</span><span class="sxs-lookup"><span data-stu-id="decfc-110">The value of *size* must be 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="decfc-111">*type*</span><span class="sxs-lookup"><span data-stu-id="decfc-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="decfc-112">Тип данных каждой координаты в массиве, используя следующие символьные константы: GL \_ Short, GL \_ int, GL \_ float и GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="decfc-112">The data type of each coordinate in the array using the following symbolic constants: GL\_SHORT, GL\_INT, GL\_FLOAT, and GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="decfc-113">*шага*</span><span class="sxs-lookup"><span data-stu-id="decfc-113">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="decfc-114">Смещение в байтах между последовательными вершинами.</span><span class="sxs-lookup"><span data-stu-id="decfc-114">The byte offset between consecutive vertices.</span></span> <span data-ttu-id="decfc-115">Если *шаг* равен нулю, вершины плотно упаковываются в массив.</span><span class="sxs-lookup"><span data-stu-id="decfc-115">When *stride* is zero, the vertices are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="decfc-116">*указатель*</span><span class="sxs-lookup"><span data-stu-id="decfc-116">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="decfc-117">Указатель на первую координату первой вершины в массиве.</span><span class="sxs-lookup"><span data-stu-id="decfc-117">A pointer to the first coordinate of the first vertex in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="decfc-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="decfc-118">Return value</span></span>

<span data-ttu-id="decfc-119">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="decfc-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="decfc-120">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="decfc-120">Error codes</span></span>

<span data-ttu-id="decfc-121">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="decfc-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="decfc-122">Имя</span><span class="sxs-lookup"><span data-stu-id="decfc-122">Name</span></span>                                                                                              | <span data-ttu-id="decfc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="decfc-123">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="decfc-124"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="decfc-124"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="decfc-125">*Размер* не был 2, 3 или 4.</span><span class="sxs-lookup"><span data-stu-id="decfc-125">*size* was not 2, 3, or 4.</span></span> <br/>        |
| <dl> <span data-ttu-id="decfc-126"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="decfc-126"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="decfc-127">*тип* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="decfc-127">*type* was not an accepted value.</span></span><br/>  |
| <dl> <span data-ttu-id="decfc-128"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="decfc-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="decfc-129">*шаг* или *число* были отрицательными.</span><span class="sxs-lookup"><span data-stu-id="decfc-129">*stride* or *count* was negative.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="decfc-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="decfc-130">Remarks</span></span>

<span data-ttu-id="decfc-131">Функция **глвертекспоинтер** задает расположение и данные массива координат вершин, используемых при подготовке к просмотру.</span><span class="sxs-lookup"><span data-stu-id="decfc-131">The **glVertexPointer** function specifies the location and data of an array of vertex coordinates to use when rendering.</span></span> <span data-ttu-id="decfc-132">Параметр *size* задает количество координат на вершину.</span><span class="sxs-lookup"><span data-stu-id="decfc-132">The *size* parameter specifies the number of coordinates per vertex.</span></span> <span data-ttu-id="decfc-133">Параметр *типа* задает тип данных для каждой координаты вершины.</span><span class="sxs-lookup"><span data-stu-id="decfc-133">The *type* parameter specifies the data type of each vertex coordinate.</span></span> <span data-ttu-id="decfc-134">Параметр *stride* определяет смещение в байтах от одной вершины к следующей, позволяя упаковать вершин и атрибуты в одном массиве или хранилище в отдельных массивах.</span><span class="sxs-lookup"><span data-stu-id="decfc-134">The *stride* parameter determines the byte offset from one vertex to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="decfc-135">В некоторых реализациях хранение вершин и атрибутов в одном массиве может оказаться более эффективным, чем использование отдельных массивов (см. [**глинтерлеаведаррайс**](glinterleavedarrays.md)).</span><span class="sxs-lookup"><span data-stu-id="decfc-135">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays (see [**glInterleavedArrays**](glinterleavedarrays.md)).</span></span>

<span data-ttu-id="decfc-136">Массив вершин включается при указании \_ \_ константы массива вершин GL с [**гленаблеклиентстате**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="decfc-136">A vertex array is enabled when you specify the GL\_VERTEX\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="decfc-137">Если этот параметр включен, [**глдраваррайс**](gldrawarrays.md), [**глдравелементс**](gldrawelements.md)и [**гларрайелемент**](glarrayelement.md) используют массив вершин.</span><span class="sxs-lookup"><span data-stu-id="decfc-137">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md), and [**glArrayElement**](glarrayelement.md) use the vertex array.</span></span> <span data-ttu-id="decfc-138">По умолчанию массив вершин отключен.</span><span class="sxs-lookup"><span data-stu-id="decfc-138">By default, the vertex array is disabled.</span></span>

<span data-ttu-id="decfc-139">Невозможно включить **глвертекспоинтер** в списки вывода.</span><span class="sxs-lookup"><span data-stu-id="decfc-139">You cannot include **glVertexPointer** in display lists.</span></span>

<span data-ttu-id="decfc-140">При указании массива вершин с помощью **глвертекспоинтер** значения всех параметров массива вершин сохраняются в состоянии на стороне клиента, а статические элементы массива могут быть кэшированы.</span><span class="sxs-lookup"><span data-stu-id="decfc-140">When you specify a vertex array using **glVertexPointer**, the values of all the function's vertex array parameters are saved in a client-side state, and static array elements can be cached.</span></span> <span data-ttu-id="decfc-141">Так как параметры массива вершин являются состояниями на стороне клиента, их значения не сохраняются и не восстанавливаются [**глпушаттриб**](glpushattrib.md) и **глпопаттриб**.</span><span class="sxs-lookup"><span data-stu-id="decfc-141">Because the vertex array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span>

<span data-ttu-id="decfc-142">Несмотря на то что ошибка не возникает при вызове **глвертекспоинтер** в парах [**глбегин**](glbegin.md) и [**гленд**](glend.md) , результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="decfc-142">Although no error is generated if you call **glVertexPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="decfc-143">Следующие функции извлекают сведения, относящиеся к **глвертекспоинтер**:</span><span class="sxs-lookup"><span data-stu-id="decfc-143">The following functions retrieve information related to **glVertexPointer**:</span></span>

<span data-ttu-id="decfc-144">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ \_ Размер массива \_ вершин GL</span><span class="sxs-lookup"><span data-stu-id="decfc-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_VERTEX\_ARRAY\_SIZE</span></span>

<span data-ttu-id="decfc-145">**глжет** с аргументом "шаг" для \_ массива вершин GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="decfc-145">**glGet** with argument GL\_VERTEX\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="decfc-146">**глжет** с аргументом \_ \_ число массивов вершин GL \_</span><span class="sxs-lookup"><span data-stu-id="decfc-146">**glGet** with argument GL\_VERTEX\_ARRAY\_COUNT</span></span>

<span data-ttu-id="decfc-147">**глжет** с аргументом \_ \_ тип массива \_ вершин GL</span><span class="sxs-lookup"><span data-stu-id="decfc-147">**glGet** with argument GL\_VERTEX\_ARRAY\_TYPE</span></span>

<span data-ttu-id="decfc-148">[**глжетпоинтерв**](glgetpointerv.md) с аргументом в качестве \_ указателя на массив вершин GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="decfc-148">[**glGetPointerv**](glgetpointerv.md) with argument GL\_VERTEX\_ARRAY\_POINTER</span></span>

<span data-ttu-id="decfc-149">[**глисенаблед**](glisenabled.md) с аргументом " \_ массив вершин GL" \_</span><span class="sxs-lookup"><span data-stu-id="decfc-149">[**glIsEnabled**](glisenabled.md) with argument GL\_VERTEX\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="decfc-150">Требования</span><span class="sxs-lookup"><span data-stu-id="decfc-150">Requirements</span></span>



| <span data-ttu-id="decfc-151">Требование</span><span class="sxs-lookup"><span data-stu-id="decfc-151">Requirement</span></span> | <span data-ttu-id="decfc-152">Значение</span><span class="sxs-lookup"><span data-stu-id="decfc-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="decfc-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="decfc-153">Minimum supported client</span></span><br/> | <span data-ttu-id="decfc-154">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="decfc-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="decfc-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="decfc-155">Minimum supported server</span></span><br/> | <span data-ttu-id="decfc-156">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="decfc-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="decfc-157">Заголовок</span><span class="sxs-lookup"><span data-stu-id="decfc-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="decfc-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="decfc-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="decfc-159">Библиотека</span><span class="sxs-lookup"><span data-stu-id="decfc-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="decfc-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="decfc-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="decfc-161">DLL</span><span class="sxs-lookup"><span data-stu-id="decfc-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="decfc-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="decfc-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="decfc-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="decfc-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="decfc-164">**гларрайелемент**</span><span class="sxs-lookup"><span data-stu-id="decfc-164">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="decfc-165">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="decfc-165">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="decfc-166">**глдраваррайс**</span><span class="sxs-lookup"><span data-stu-id="decfc-166">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="decfc-167">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="decfc-167">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="decfc-168">**гленаблеклиентстате**</span><span class="sxs-lookup"><span data-stu-id="decfc-168">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="decfc-169">**глжетпоинтерв**</span><span class="sxs-lookup"><span data-stu-id="decfc-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="decfc-170">**глжетстринг**</span><span class="sxs-lookup"><span data-stu-id="decfc-170">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="decfc-171">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="decfc-171">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="decfc-172">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="decfc-172">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="decfc-173">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="decfc-173">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="decfc-174">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="decfc-174">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> </dl>

 

 





