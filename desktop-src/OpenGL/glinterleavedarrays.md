---
title: Функция Глинтерлеаведаррайс (GL. h)
description: Функция Глинтерлеаведаррайс одновременно указывает и включает несколько чередующихся массивов в более крупном агрегатном массиве.
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- Функция Глинтерлеаведаррайс OpenGL
topic_type:
- apiref
api_name:
- glInterleavedArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41403210e78d1a65dd700561243846d6e45bad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414993"
---
# <a name="glinterleavedarrays-function"></a><span data-ttu-id="83583-104">Функция Глинтерлеаведаррайс</span><span class="sxs-lookup"><span data-stu-id="83583-104">glInterleavedArrays function</span></span>

<span data-ttu-id="83583-105">Функция **глинтерлеаведаррайс** одновременно указывает и включает несколько чередующихся массивов в более крупном агрегатном массиве.</span><span class="sxs-lookup"><span data-stu-id="83583-105">The **glInterleavedArrays** function simultaneously specifies and enables several interleaved arrays in a larger aggregate array.</span></span>

## <a name="syntax"></a><span data-ttu-id="83583-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83583-106">Syntax</span></span>


```C++
void WINAPI glInterleavedArrays(
         GLenum  format,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="83583-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="83583-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83583-108">*format*</span><span class="sxs-lookup"><span data-stu-id="83583-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="83583-109">Тип массива, который необходимо включить.</span><span class="sxs-lookup"><span data-stu-id="83583-109">The type of array to enable.</span></span> <span data-ttu-id="83583-110">Параметр может принимать одно из следующих символьных значений: GL \_ V2F, GL \_ V3F, GL \_ C4UB \_ V2F, GL \_ C4UB \_ V3F, GL \_ C3F \_ V3F, GL \_ N3F \_ V3F, GL \_ C4F N3F V3F \_ \_ , GL \_ T2F \_ V3F, GL T4F V4F \_ \_ , GL \_ T2F \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ C4UB V3F, GL T2F C3F V3F, GL T2F N3F V3F T2F.</span><span class="sxs-lookup"><span data-stu-id="83583-110">The parameter can assume one of the following symbolic values: GL\_V2F, GL\_V3F, GL\_C4UB\_V2F, GL\_C4UB\_V3F, GL\_C3F\_V3F, GL\_N3F\_V3F, GL\_C4F\_N3F\_V3F, GL\_T2F\_V3F, GL\_T4F\_V4F, GL\_T2F\_C4UB\_V3F, GL\_T2F\_C3F\_V3F, GL\_T2F\_N3F\_V3F, GL\_T2F\_C4F\_N3F\_V3F, or GL\_T4F\_C4F\_N3F\_V4F.</span></span>

</dd> <dt>

<span data-ttu-id="83583-111">*шага*</span><span class="sxs-lookup"><span data-stu-id="83583-111">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="83583-112">Смещение в байтах между каждым элементом статистического массива.</span><span class="sxs-lookup"><span data-stu-id="83583-112">The offset in bytes between each aggregate array element.</span></span>

</dd> <dt>

<span data-ttu-id="83583-113">*указатель*</span><span class="sxs-lookup"><span data-stu-id="83583-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="83583-114">Указатель на первый элемент агрегатного массива.</span><span class="sxs-lookup"><span data-stu-id="83583-114">A pointer to the first element of an aggregate array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83583-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83583-115">Return value</span></span>

<span data-ttu-id="83583-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="83583-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="83583-117">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="83583-117">Error codes</span></span>

<span data-ttu-id="83583-118">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="83583-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="83583-119">Имя</span><span class="sxs-lookup"><span data-stu-id="83583-119">Name</span></span>                                                                                                  | <span data-ttu-id="83583-120">Значение</span><span class="sxs-lookup"><span data-stu-id="83583-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83583-121"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="83583-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="83583-122">*Формат* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="83583-122">*format* was not an accepted value.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="83583-123"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="83583-123"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="83583-124">*шаг* был отрицательным значением.</span><span class="sxs-lookup"><span data-stu-id="83583-124">*stride* was a negative value.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="83583-125"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="83583-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="83583-126">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="83583-126">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="83583-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83583-127">Remarks</span></span>

<span data-ttu-id="83583-128">С помощью функции **глинтерлеаведаррайс** можно одновременно указать и включить несколько чередующихся цветов, нормалей, текстур и массивов вершин, элементы которых являются частью более крупного статистического элемента массива.</span><span class="sxs-lookup"><span data-stu-id="83583-128">With the **glInterleavedArrays** function, you can simultaneously specify and enable several interleaved color, normal, texture, and vertex arrays whose elements are part of a larger aggregate array element.</span></span> <span data-ttu-id="83583-129">Для некоторых архитектур памяти это более эффективно, чем указание массивов отдельно.</span><span class="sxs-lookup"><span data-stu-id="83583-129">For some memory architectures, this is more efficient than specifying the arrays separately.</span></span>

<span data-ttu-id="83583-130">Если параметр *stride* равен нулю, то статистические элементы массива хранятся последовательно; в противном случае выполняется *шаг* байтов между статистическими элементами массива.</span><span class="sxs-lookup"><span data-stu-id="83583-130">If the *stride* parameter is zero then the aggregate array elements are stored consecutively; otherwise *stride* bytes occur between aggregate array elements.</span></span>

<span data-ttu-id="83583-131">Параметр *Format* служит ключом, который описывает извлечение отдельных массивов из статистического массива.</span><span class="sxs-lookup"><span data-stu-id="83583-131">The *format* parameter serves as a key that describes how to extract individual arrays from the aggregate array:</span></span>

-   <span data-ttu-id="83583-132">Если *Format* содержит T, то координаты текстуры извлекаются из массива с чередованием.</span><span class="sxs-lookup"><span data-stu-id="83583-132">If *format* contains a T, then texture coordinates are extracted from the interleaved array.</span></span>
-   <span data-ttu-id="83583-133">Если указано значение C, извлекаются значения цвета.</span><span class="sxs-lookup"><span data-stu-id="83583-133">If C is present, color values are extracted.</span></span>
-   <span data-ttu-id="83583-134">Если указано значение N, извлекаются обычные координаты.</span><span class="sxs-lookup"><span data-stu-id="83583-134">If N is present, normal coordinates are extracted.</span></span>
-   <span data-ttu-id="83583-135">Координаты вершин извлекаются всегда.</span><span class="sxs-lookup"><span data-stu-id="83583-135">Vertex coordinates are always extracted.</span></span>
-   <span data-ttu-id="83583-136">Цифры 2, 3 и 4 обозначают количество извлекаемых значений.</span><span class="sxs-lookup"><span data-stu-id="83583-136">The digits 2, 3, and 4 denote how many values are extracted.</span></span>
-   <span data-ttu-id="83583-137">F указывает, что значения извлекаются в виде значений с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="83583-137">F indicates that values are extracted as floating point values.</span></span>
-   <span data-ttu-id="83583-138">Если 4UB соответствует C, цвета также могут извлекаться как 4 неподписанные байты.</span><span class="sxs-lookup"><span data-stu-id="83583-138">If 4UB follows the C, colors may also be extracted as 4 unsigned bytes.</span></span> <span data-ttu-id="83583-139">Если цвет извлекается в виде 4 беззнаковых байт, элемент массива вершин, следующий за ним, находится на первом допустимом адресе с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="83583-139">If a color is extracted as 4 unsigned bytes, the vertex array element that follows is located at the first possible floating-point aligned address.</span></span>

<span data-ttu-id="83583-140">При вызове **глинтерлеаведаррайс** во время компиляции списка отображений он не компилируется в список, но выполняется немедленно.</span><span class="sxs-lookup"><span data-stu-id="83583-140">If you call **glInterleavedArrays** while compiling a display list, it is not compiled into the list but is executed immediately.</span></span>

<span data-ttu-id="83583-141">Невозможно включить вызовы **глинтерлеаведаррайс** в **глдисаблеклиентстате** между вызовами [**Глбегин**](glbegin.md) и соответствующим вызовом **гленд**.</span><span class="sxs-lookup"><span data-stu-id="83583-141">You cannot include calls to **glInterleavedArrays** in **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to **glEnd**.</span></span>

> [!Note]  
> <span data-ttu-id="83583-142">Функция **глинтерлеаведаррайс** доступна только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="83583-142">The **glInterleavedArrays** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="83583-143">Функция **глинтерлеаведаррайс** реализуется на стороне клиента без протокола.</span><span class="sxs-lookup"><span data-stu-id="83583-143">The **glInterleavedArrays** function is implemented on the client side with no protocol.</span></span> <span data-ttu-id="83583-144">Так как параметры массива вершин являются состояниями на стороне клиента, они не сохраняются и не восстанавливаются [**глпушаттриб**](glpushattrib.md) и **глпопаттриб**.</span><span class="sxs-lookup"><span data-stu-id="83583-144">Because the vertex array parameters are client-side state, they are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span> <span data-ttu-id="83583-145">Вместо этого используйте [**глпушклиентаттриб**](glpushclientattrib.md) и **глпопклиентаттриб** .</span><span class="sxs-lookup"><span data-stu-id="83583-145">Use [**glPushClientAttrib**](glpushclientattrib.md) and **glPopClientAttrib** instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="83583-146">Требования</span><span class="sxs-lookup"><span data-stu-id="83583-146">Requirements</span></span>



| <span data-ttu-id="83583-147">Требование</span><span class="sxs-lookup"><span data-stu-id="83583-147">Requirement</span></span> | <span data-ttu-id="83583-148">Значение</span><span class="sxs-lookup"><span data-stu-id="83583-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83583-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83583-149">Minimum supported client</span></span><br/> | <span data-ttu-id="83583-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="83583-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="83583-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83583-151">Minimum supported server</span></span><br/> | <span data-ttu-id="83583-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="83583-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="83583-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="83583-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="83583-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="83583-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="83583-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="83583-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="83583-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83583-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="83583-157">DLL</span><span class="sxs-lookup"><span data-stu-id="83583-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83583-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83583-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83583-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83583-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83583-160">**гларрайелемент**</span><span class="sxs-lookup"><span data-stu-id="83583-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="83583-161">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="83583-161">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="83583-162">**глдраваррайс**</span><span class="sxs-lookup"><span data-stu-id="83583-162">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="83583-163">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="83583-163">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="83583-164">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="83583-164">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="83583-165">**гленаблеклиентстате**</span><span class="sxs-lookup"><span data-stu-id="83583-165">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="83583-166">**глжетпоинтерв**</span><span class="sxs-lookup"><span data-stu-id="83583-166">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="83583-167">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="83583-167">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="83583-168">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="83583-168">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="83583-169">**глпушаттриб**</span><span class="sxs-lookup"><span data-stu-id="83583-169">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="83583-170">**глпушклиентаттриб**</span><span class="sxs-lookup"><span data-stu-id="83583-170">**glPushClientAttrib**</span></span>](glpushclientattrib.md)
</dt> <dt>

[<span data-ttu-id="83583-171">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="83583-171">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="83583-172">**глвертекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="83583-172">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





