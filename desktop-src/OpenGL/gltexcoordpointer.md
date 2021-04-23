---
title: Функция Глтекскурдпоинтер (GL. h)
description: Функция Глтекскурдпоинтер определяет массив координат текстуры.
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- Функция Глтекскурдпоинтер OpenGL
topic_type:
- apiref
api_name:
- glTexCoordPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: febc9c79bdbc4a1ed1c14380af47f36309f12662
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682154"
---
# <a name="gltexcoordpointer-function"></a><span data-ttu-id="0fb02-104">Функция Глтекскурдпоинтер</span><span class="sxs-lookup"><span data-stu-id="0fb02-104">glTexCoordPointer function</span></span>

<span data-ttu-id="0fb02-105">Функция **глтекскурдпоинтер** определяет массив координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="0fb02-105">The **glTexCoordPointer** function defines an array of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fb02-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0fb02-106">Syntax</span></span>


```C++
void WINAPI glTexCoordPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="0fb02-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fb02-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fb02-108">*size*</span><span class="sxs-lookup"><span data-stu-id="0fb02-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="0fb02-109">Количество координат на элемент массива.</span><span class="sxs-lookup"><span data-stu-id="0fb02-109">The number of coordinates per array element.</span></span> <span data-ttu-id="0fb02-110">Значение *size* должно быть равно 1, 2, 3 или 4.</span><span class="sxs-lookup"><span data-stu-id="0fb02-110">The value of *size* must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="0fb02-111">*type*</span><span class="sxs-lookup"><span data-stu-id="0fb02-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="0fb02-112">Тип данных каждой координаты текстуры в массиве, используя следующие символьные константы: **GL \_ Short**, **GL \_ int**, **GL с \_ плавающей запятой** и значение **ГК типа \_ Double**.</span><span class="sxs-lookup"><span data-stu-id="0fb02-112">The data type of each texture coordinate in the array using the following symbolic constants: **GL\_SHORT**, **GL\_INT**, **GL\_FLOAT**, and **GL\_DOUBLE**.</span></span>

</dd> <dt>

<span data-ttu-id="0fb02-113">*шага*</span><span class="sxs-lookup"><span data-stu-id="0fb02-113">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="0fb02-114">Смещение в байтах между последовательными элементами массива.</span><span class="sxs-lookup"><span data-stu-id="0fb02-114">The byte offset between consecutive array elements.</span></span> <span data-ttu-id="0fb02-115">Если *шаг* равен нулю, элементы массива тесно упакованы в массив.</span><span class="sxs-lookup"><span data-stu-id="0fb02-115">When *stride* is zero, the array elements are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="0fb02-116">*указатель*</span><span class="sxs-lookup"><span data-stu-id="0fb02-116">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="0fb02-117">Указатель на первую координату первого элемента в массиве.</span><span class="sxs-lookup"><span data-stu-id="0fb02-117">A pointer to the first coordinate of the first element in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fb02-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0fb02-118">Return value</span></span>

<span data-ttu-id="0fb02-119">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0fb02-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0fb02-120">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="0fb02-120">Error codes</span></span>

<span data-ttu-id="0fb02-121">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="0fb02-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0fb02-122">Имя</span><span class="sxs-lookup"><span data-stu-id="0fb02-122">Name</span></span>                                                                                              | <span data-ttu-id="0fb02-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0fb02-123">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0fb02-124"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="0fb02-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="0fb02-125">*тип* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="0fb02-125">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="0fb02-126"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="0fb02-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="0fb02-127">*Размер* не был равен 1, 2, 3 или 4.</span><span class="sxs-lookup"><span data-stu-id="0fb02-127">*size* was not 1, 2, 3, or 4.</span></span><br/>     |
| <dl> <span data-ttu-id="0fb02-128"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="0fb02-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="0fb02-129">*шаг* был отрицательным.</span><span class="sxs-lookup"><span data-stu-id="0fb02-129">*stride* was negative.</span></span><br/>            |



## <a name="remarks"></a><span data-ttu-id="0fb02-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0fb02-130">Remarks</span></span>

<span data-ttu-id="0fb02-131">Функция **глтекскурдпоинтер** задает расположение и данные массива координат текстуры для использования при подготовке к просмотру. Параметр *size* задает количество координат, используемых для каждого элемента массива. Параметр *типа* задает тип данных для каждой координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="0fb02-131">The **glTexCoordPointer** function specifies the location and data of an array of texture coordinates to use when rendering.The *size* parameter specifies the number of coordinates used for each element of the array.The *type* parameter specifies the data type of each texture coordinate.</span></span> <span data-ttu-id="0fb02-132">Параметр *stride* определяет смещение в байтах от одного элемента массива к другому, позволяя упаковать вершин и атрибуты в одном массиве или хранилище в отдельных массивах.</span><span class="sxs-lookup"><span data-stu-id="0fb02-132">The *stride* parameter determines the byte offset from one array element to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="0fb02-133">В некоторых реализациях хранение вершин и атрибутов в одном массиве может быть более эффективным, чем использование отдельных массивов.</span><span class="sxs-lookup"><span data-stu-id="0fb02-133">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span> <span data-ttu-id="0fb02-134">Дополнительные сведения см. в разделе [**глинтерлеаведаррайс**](glinterleavedarrays.md).</span><span class="sxs-lookup"><span data-stu-id="0fb02-134">For more information, see [**glInterleavedArrays**](glinterleavedarrays.md).</span></span> <span data-ttu-id="0fb02-135">Если задан массив координат текстуры, то размер, тип, шаг и указатель сохраняются в состоянии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="0fb02-135">When a texture coordinate array is specified, size, type, stride, and pointer are saved client-side state.</span></span>

<span data-ttu-id="0fb02-136">Массив координат текстуры включается при указании константы **\_ \_ курд \_ Array текстуры GL** с [**гленаблеклиентстате**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="0fb02-136">A texture coordinate array is enabled when you specify the **GL\_TEXTURE\_COORD\_ARRAY** constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="0fb02-137">Если этот параметр включен, [**глдраваррайс**](gldrawarrays.md), [**глдравелементс**](gldrawelements.md)и [**гларрайелемент**](glarrayelement.md) используют массив координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="0fb02-137">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md), and [**glArrayElement**](glarrayelement.md) use the texture coordinate array.</span></span> <span data-ttu-id="0fb02-138">По умолчанию массив координат текстуры отключен.</span><span class="sxs-lookup"><span data-stu-id="0fb02-138">By default the texture coordinate array is disabled.</span></span>

<span data-ttu-id="0fb02-139">Невозможно включить **глтекскурдпоинтер** в списки вывода.</span><span class="sxs-lookup"><span data-stu-id="0fb02-139">You cannot include **glTexCoordPointer** in display lists.</span></span>

<span data-ttu-id="0fb02-140">При указании массива координат текстуры с помощью **глтекскурдпоинтер** значения всех параметров массива координат текстуры сохраняются в состоянии на стороне клиента, а статические элементы массива могут быть кэшированы.</span><span class="sxs-lookup"><span data-stu-id="0fb02-140">When you specify a texture coordinate array using **glTexCoordPointer**, the values of all the function's texture coordinate array parameters are saved in a client-side state, and static array elements can be cached.</span></span> <span data-ttu-id="0fb02-141">Так как параметры массива координат текстуры являются состояниями на стороне клиента, их значения не сохраняются и не восстанавливаются [**глпушаттриб**](glpushattrib.md) и [**глпопаттриб**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="0fb02-141">Because the texture coordinate array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

<span data-ttu-id="0fb02-142">Несмотря на то что ошибка не возникает при вызове **глтекскурдпоинтер** в парах [**глбегин**](glbegin.md) и [**гленд**](glend.md) , результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="0fb02-142">Although no error is generated when you call **glTexCoordPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="0fb02-143">Следующие функции извлекают сведения, относящиеся к **глтекскурдпоинтер**:</span><span class="sxs-lookup"><span data-stu-id="0fb02-143">The following functions retrieve information related to **glTexCoordPointer**:</span></span>

<span data-ttu-id="0fb02-144">[**глисенаблед**](glisenabled.md) с аргументом **GL \_ текстура \_ курд \_ массив**</span><span class="sxs-lookup"><span data-stu-id="0fb02-144">[**glIsEnabled**](glisenabled.md) with argument **GL\_TEXTURE\_COORD\_ARRAY**</span></span>

<span data-ttu-id="0fb02-145">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом **GL \_ текстура \_ курд \_ \_ Размер массива**</span><span class="sxs-lookup"><span data-stu-id="0fb02-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument **GL\_TEXTURE\_COORD\_ARRAY\_SIZE**</span></span>

<span data-ttu-id="0fb02-146">**глжет** с аргументом **GL \_ текстура \_ курд \_ Индекс \_ stride**</span><span class="sxs-lookup"><span data-stu-id="0fb02-146">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_STRIDE**</span></span>

<span data-ttu-id="0fb02-147">**глжет** с аргументом **GL \_ текстура \_ курд \_ \_ число массивов**</span><span class="sxs-lookup"><span data-stu-id="0fb02-147">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_COUNT**</span></span>

<span data-ttu-id="0fb02-148">**глжет** с аргументом **GL \_ текстура \_ курд \_ \_ тип массива**</span><span class="sxs-lookup"><span data-stu-id="0fb02-148">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_TYPE**</span></span>

<span data-ttu-id="0fb02-149">[**глжетпоинтерв**](glgetpointerv.md) с аргументом **GL \_ текстура \_ курд \_ \_ указатель массива**</span><span class="sxs-lookup"><span data-stu-id="0fb02-149">[**glGetPointerv**](glgetpointerv.md) with argument **GL\_TEXTURE\_COORD\_ARRAY\_POINTER**</span></span>

## <a name="requirements"></a><span data-ttu-id="0fb02-150">Требования</span><span class="sxs-lookup"><span data-stu-id="0fb02-150">Requirements</span></span>



| <span data-ttu-id="0fb02-151">Требование</span><span class="sxs-lookup"><span data-stu-id="0fb02-151">Requirement</span></span> | <span data-ttu-id="0fb02-152">Значение</span><span class="sxs-lookup"><span data-stu-id="0fb02-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fb02-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0fb02-153">Minimum supported client</span></span><br/> | <span data-ttu-id="0fb02-154">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0fb02-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0fb02-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0fb02-155">Minimum supported server</span></span><br/> | <span data-ttu-id="0fb02-156">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0fb02-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0fb02-157">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0fb02-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fb02-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fb02-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0fb02-159">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0fb02-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="0fb02-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fb02-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0fb02-161">DLL</span><span class="sxs-lookup"><span data-stu-id="0fb02-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fb02-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fb02-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fb02-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0fb02-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fb02-164">**гларрайелемент**</span><span class="sxs-lookup"><span data-stu-id="0fb02-164">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="0fb02-165">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="0fb02-165">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="0fb02-166">**глдраваррайс**</span><span class="sxs-lookup"><span data-stu-id="0fb02-166">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="0fb02-167">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="0fb02-167">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="0fb02-168">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="0fb02-168">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="0fb02-169">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="0fb02-169">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="0fb02-170">**глжетпоинтерв**</span><span class="sxs-lookup"><span data-stu-id="0fb02-170">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="0fb02-171">**глжетстринг**</span><span class="sxs-lookup"><span data-stu-id="0fb02-171">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="0fb02-172">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="0fb02-172">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="0fb02-173">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="0fb02-173">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="0fb02-174">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="0fb02-174">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="0fb02-175">**глпопклиентаттриб**</span><span class="sxs-lookup"><span data-stu-id="0fb02-175">**glPopClientAttrib**</span></span>](glpopclientattrib.md)
</dt> <dt>

[<span data-ttu-id="0fb02-176">**глпушклиентаттриб**</span><span class="sxs-lookup"><span data-stu-id="0fb02-176">**glPushClientAttrib**</span></span>](glpushclientattrib.md)
</dt> <dt>

[<span data-ttu-id="0fb02-177">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="0fb02-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="0fb02-178">**глвертекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="0fb02-178">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





