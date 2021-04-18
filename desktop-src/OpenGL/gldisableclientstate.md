---
title: Функция Глдисаблеклиентстате (GL. h)
description: Функции Гленаблеклиентстате и Глдисаблеклиентстате включают и отключают массивы соответственно. | Функция Глдисаблеклиентстате (GL. h)
ms.assetid: b3316519-00ed-45f8-9c4b-2e04c483751e
keywords:
- Функция Глдисаблеклиентстате OpenGL
topic_type:
- apiref
api_name:
- glDisableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 163a7c3b679c979e5c800d2aa41ba2abb00e11f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664939"
---
# <a name="gldisableclientstate-function"></a><span data-ttu-id="032ee-105">Функция Глдисаблеклиентстате</span><span class="sxs-lookup"><span data-stu-id="032ee-105">glDisableClientState function</span></span>

<span data-ttu-id="032ee-106">Функции [**гленаблеклиентстате**](glenableclientstate.md) и **глдисаблеклиентстате** включают и отключают массивы соответственно.</span><span class="sxs-lookup"><span data-stu-id="032ee-106">The [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** functions enable and disable arrays respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="032ee-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="032ee-107">Syntax</span></span>


```C++
void WINAPI glDisableClientState(
   GLenum array
);
```



## <a name="parameters"></a><span data-ttu-id="032ee-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="032ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="032ee-109">*array*</span><span class="sxs-lookup"><span data-stu-id="032ee-109">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="032ee-110">Символьная константа для массива, который необходимо включить или отключить.</span><span class="sxs-lookup"><span data-stu-id="032ee-110">A symbolic constant for the array you want to enable or disable.</span></span> <span data-ttu-id="032ee-111">Этот параметр может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="032ee-111">This parameter can assume one of the following values.</span></span>



| <span data-ttu-id="032ee-112">Значение</span><span class="sxs-lookup"><span data-stu-id="032ee-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="032ee-113">Значение</span><span class="sxs-lookup"><span data-stu-id="032ee-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <span data-ttu-id="032ee-114"><dt>**\_массив цветов \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="032ee-114"><dt>**GL\_COLOR\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="032ee-115">Если параметр включен, используйте массивы цветов с вызовами [**гларрайелемент**](glarrayelement.md), [**глдравелементс**](gldrawelements.md)или [**глдраваррайс**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="032ee-115">If enabled, use color arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="032ee-116">См. также [**глколорпоинтер**](glcolorpointer.md).</span><span class="sxs-lookup"><span data-stu-id="032ee-116">See also [**glColorPointer**](glcolorpointer.md).</span></span><br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <span data-ttu-id="032ee-117"><dt>**\_ \_ массив флагов РЕБРы GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="032ee-117"><dt>**GL\_EDGE\_FLAG\_ARRAY**</dt></span></span> </dl>             | <span data-ttu-id="032ee-118">Если параметр включен, используйте массивы пограничных флагов с вызовами [**гларрайелемент**](glarrayelement.md), [**глдравелементс**](gldrawelements.md)или [**глдраваррайс**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="032ee-118">If enabled, use edge flag arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="032ee-119">См. также [**гледжефлагпоинтер**](gledgeflagpointer.md).</span><span class="sxs-lookup"><span data-stu-id="032ee-119">See also [**glEdgeFlagPointer**](gledgeflagpointer.md).</span></span><br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <span data-ttu-id="032ee-120"><dt>**\_массив индексов GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="032ee-120"><dt>**GL\_INDEX\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="032ee-121">Если параметр включен, используйте индексные массивы с вызовами [**гларрайелемент**](glarrayelement.md), [**глдравелементс**](gldrawelements.md)или [**глдраваррайс**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="032ee-121">If enabled, use index arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="032ee-122">См. также [**глиндекспоинтер**](glindexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="032ee-122">See also [**glIndexPointer**](glindexpointer.md).</span></span><br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <span data-ttu-id="032ee-123"><dt>**\_стандартный \_ массив GL**</dt></span><span class="sxs-lookup"><span data-stu-id="032ee-123"><dt>**GL\_NORMAL\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="032ee-124">Если параметр включен, используйте обычные массивы с вызовами [**гларрайелемент**](glarrayelement.md), [**глдравелементс**](gldrawelements.md)или [**глдраваррайс**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="032ee-124">If enabled, use normal arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="032ee-125">См. также [**глнормалпоинтер**](glnormalpointer.md).</span><span class="sxs-lookup"><span data-stu-id="032ee-125">See also [**glNormalPointer**](glnormalpointer.md).</span></span><br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <span data-ttu-id="032ee-126"><dt>**\_ \_ массив курд текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="032ee-126"><dt>**GL\_TEXTURE\_COORD\_ARRAY**</dt></span></span> </dl> | <span data-ttu-id="032ee-127">Если параметр включен, используйте массивы координат текстуры с вызовами [**гларрайелемент**](glarrayelement.md), [**глдравелементс**](gldrawelements.md)или [**глдраваррайс**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="032ee-127">If enabled, use texture coordinate arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="032ee-128">См. также [**глтекскурдпоинтер**](gltexcoordpointer.md).</span><span class="sxs-lookup"><span data-stu-id="032ee-128">See also [**glTexCoordPointer**](gltexcoordpointer.md).</span></span><br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <span data-ttu-id="032ee-129"><dt>**\_массив ВЕРШИН \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="032ee-129"><dt>**GL\_VERTEX\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="032ee-130">Если параметр включен, используйте массивы вершин с вызовами [**гларрайелемент**](glarrayelement.md), [**глдравелементс**](gldrawelements.md)или [**глдраваррайс**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="032ee-130">If enabled, use vertex arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="032ee-131">См. также [**глвертекспоинтер**](glvertexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="032ee-131">See also [**glVertexPointer**](glvertexpointer.md).</span></span><br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="032ee-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="032ee-132">Return value</span></span>

<span data-ttu-id="032ee-133">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="032ee-133">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="032ee-134">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="032ee-134">Error codes</span></span>

<span data-ttu-id="032ee-135">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="032ee-135">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="032ee-136">Имя</span><span class="sxs-lookup"><span data-stu-id="032ee-136">Name</span></span>                                                                                             | <span data-ttu-id="032ee-137">Значение</span><span class="sxs-lookup"><span data-stu-id="032ee-137">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="032ee-138"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="032ee-138"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="032ee-139">*массив* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="032ee-139">*array* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="032ee-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="032ee-140">Remarks</span></span>

<span data-ttu-id="032ee-141">Функции [**гленаблеклиентстате**](glenableclientstate.md) и **глдисаблеклиентстате** включают и отключают различные отдельные массивы.</span><span class="sxs-lookup"><span data-stu-id="032ee-141">The [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** functions enable and disable various individual arrays.</span></span> <span data-ttu-id="032ee-142">Чтобы определить текущее значение любой возможности, используйте [**глисенаблед**](glisenabled.md) или [**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="032ee-142">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="032ee-143">Вызов [**гленаблеклиентстате**](glenableclientstate.md) и **глдисаблеклиентстате** между вызовами [**Глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md) может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="032ee-143">Calling [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) can cause an error.</span></span> <span data-ttu-id="032ee-144">Если ошибка не возникает, поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="032ee-144">If no error is generated, the behavior is undefined.</span></span>

> [!Note]  
> <span data-ttu-id="032ee-145">Функции [**гленаблеклиентстате**](glenableclientstate.md) и **глдисаблеклиентстате** доступны только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="032ee-145">The [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** functions are only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="032ee-146">Требования</span><span class="sxs-lookup"><span data-stu-id="032ee-146">Requirements</span></span>



| <span data-ttu-id="032ee-147">Требование</span><span class="sxs-lookup"><span data-stu-id="032ee-147">Requirement</span></span> | <span data-ttu-id="032ee-148">Значение</span><span class="sxs-lookup"><span data-stu-id="032ee-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="032ee-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="032ee-149">Minimum supported client</span></span><br/> | <span data-ttu-id="032ee-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="032ee-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="032ee-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="032ee-151">Minimum supported server</span></span><br/> | <span data-ttu-id="032ee-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="032ee-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="032ee-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="032ee-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="032ee-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="032ee-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="032ee-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="032ee-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="032ee-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="032ee-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="032ee-157">DLL</span><span class="sxs-lookup"><span data-stu-id="032ee-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="032ee-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="032ee-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="032ee-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="032ee-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="032ee-160">**гларрайелемент**</span><span class="sxs-lookup"><span data-stu-id="032ee-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="032ee-161">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="032ee-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="032ee-162">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="032ee-162">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="032ee-163">**глдраваррайс**</span><span class="sxs-lookup"><span data-stu-id="032ee-163">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="032ee-164">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="032ee-164">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="032ee-165">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="032ee-165">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="032ee-166">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="032ee-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="032ee-167">**гленаблеклиентстате**</span><span class="sxs-lookup"><span data-stu-id="032ee-167">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="032ee-168">**гленд**</span><span class="sxs-lookup"><span data-stu-id="032ee-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="032ee-169">**глжетпоинтерв**</span><span class="sxs-lookup"><span data-stu-id="032ee-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="032ee-170">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="032ee-170">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="032ee-171">**глинтерлеаведаррайс**</span><span class="sxs-lookup"><span data-stu-id="032ee-171">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="032ee-172">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="032ee-172">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="032ee-173">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="032ee-173">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="032ee-174">**глвертекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="032ee-174">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





