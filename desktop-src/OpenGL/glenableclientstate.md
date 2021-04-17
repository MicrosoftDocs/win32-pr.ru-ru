---
title: Функция Гленаблеклиентстате (GL. h)
description: Функции Гленаблеклиентстате и Глдисаблеклиентстате включают и отключают массивы соответственно. | Функция Гленаблеклиентстате (GL. h)
ms.assetid: 02520f81-0b0d-4774-b1e2-713cf226347f
keywords:
- Функция Гленаблеклиентстате OpenGL
topic_type:
- apiref
api_name:
- glEnableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e333a51d4c1fe0a5ff11c717790e03aa6d054a09
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353322"
---
# <a name="glenableclientstate-function"></a><span data-ttu-id="e10f5-105">Функция Гленаблеклиентстате</span><span class="sxs-lookup"><span data-stu-id="e10f5-105">glEnableClientState function</span></span>

<span data-ttu-id="e10f5-106">Функции **гленаблеклиентстате** и [**глдисаблеклиентстате**](gldisableclientstate.md) включают и отключают массивы соответственно.</span><span class="sxs-lookup"><span data-stu-id="e10f5-106">The **glEnableClientState** and [**glDisableClientState**](gldisableclientstate.md) functions enable and disable arrays respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="e10f5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e10f5-107">Syntax</span></span>


```C++
void WINAPI glEnableClientState(
   GLenum array
);
```



## <a name="parameters"></a><span data-ttu-id="e10f5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e10f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e10f5-109">*array*</span><span class="sxs-lookup"><span data-stu-id="e10f5-109">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="e10f5-110">Символьная константа для массива, который необходимо включить или отключить.</span><span class="sxs-lookup"><span data-stu-id="e10f5-110">A symbolic constant for the array you want to enable or disable.</span></span> <span data-ttu-id="e10f5-111">Этот параметр может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e10f5-111">This parameter can assume one of the following values.</span></span>



| <span data-ttu-id="e10f5-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e10f5-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="e10f5-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e10f5-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <span data-ttu-id="e10f5-114"><dt>**\_массив цветов \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e10f5-114"><dt>**GL\_COLOR\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="e10f5-115">Если параметр включен, используйте массивы цветов с вызовами [**гларрайелемент**](glarrayelement.md), [**глдравелементс**](gldrawelements.md)или [**глдраваррайс**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="e10f5-115">If enabled, use color arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="e10f5-116">См. также [**глколорпоинтер**](glcolorpointer.md).</span><span class="sxs-lookup"><span data-stu-id="e10f5-116">See also [**glColorPointer**](glcolorpointer.md).</span></span><br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <span data-ttu-id="e10f5-117"><dt>**\_ \_ массив флагов РЕБРы GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e10f5-117"><dt>**GL\_EDGE\_FLAG\_ARRAY**</dt></span></span> </dl>             | <span data-ttu-id="e10f5-118">Если параметр включен, используйте массивы пограничных флагов с вызовами [**гларрайелемент**](glarrayelement.md), [**глдравелементс**](gldrawelements.md)или [**глдраваррайс**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="e10f5-118">If enabled, use edge flag arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="e10f5-119">См. также [**гледжефлагпоинтер**](gledgeflagpointer.md).</span><span class="sxs-lookup"><span data-stu-id="e10f5-119">See also [**glEdgeFlagPointer**](gledgeflagpointer.md).</span></span><br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <span data-ttu-id="e10f5-120"><dt>**\_массив индексов GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e10f5-120"><dt>**GL\_INDEX\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="e10f5-121">Если параметр включен, используйте индексные массивы с вызовами [**гларрайелемент**](glarrayelement.md), [**глдравелементс**](gldrawelements.md)или [**глдраваррайс**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="e10f5-121">If enabled, use index arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="e10f5-122">См. также [**глиндекспоинтер**](glindexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="e10f5-122">See also [**glIndexPointer**](glindexpointer.md).</span></span><br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <span data-ttu-id="e10f5-123"><dt>**\_стандартный \_ массив GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e10f5-123"><dt>**GL\_NORMAL\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="e10f5-124">Если параметр включен, используйте обычные массивы с вызовами [**гларрайелемент**](glarrayelement.md), [**глдравелементс**](gldrawelements.md)или [**глдраваррайс**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="e10f5-124">If enabled, use normal arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="e10f5-125">См. также [**глнормалпоинтер**](glnormalpointer.md).</span><span class="sxs-lookup"><span data-stu-id="e10f5-125">See also [**glNormalPointer**](glnormalpointer.md).</span></span><br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <span data-ttu-id="e10f5-126"><dt>**\_ \_ массив курд текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e10f5-126"><dt>**GL\_TEXTURE\_COORD\_ARRAY**</dt></span></span> </dl> | <span data-ttu-id="e10f5-127">Если параметр включен, используйте массивы координат текстуры с вызовами [**гларрайелемент**](glarrayelement.md), [**глдравелементс**](gldrawelements.md)или [**глдраваррайс**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="e10f5-127">If enabled, use texture coordinate arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="e10f5-128">См. также [**глтекскурдпоинтер**](gltexcoordpointer.md).</span><span class="sxs-lookup"><span data-stu-id="e10f5-128">See also [**glTexCoordPointer**](gltexcoordpointer.md).</span></span><br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <span data-ttu-id="e10f5-129"><dt>**\_массив ВЕРШИН \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e10f5-129"><dt>**GL\_VERTEX\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="e10f5-130">Если параметр включен, используйте массивы вершин с вызовами [**гларрайелемент**](glarrayelement.md), [**глдравелементс**](gldrawelements.md)или [**глдраваррайс**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="e10f5-130">If enabled, use vertex arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="e10f5-131">См. также [**глвертекспоинтер**](glvertexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="e10f5-131">See also [**glVertexPointer**](glvertexpointer.md).</span></span><br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e10f5-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e10f5-132">Return value</span></span>

<span data-ttu-id="e10f5-133">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e10f5-133">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e10f5-134">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="e10f5-134">Error codes</span></span>

<span data-ttu-id="e10f5-135">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="e10f5-135">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e10f5-136">Имя</span><span class="sxs-lookup"><span data-stu-id="e10f5-136">Name</span></span>                                                                                             | <span data-ttu-id="e10f5-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e10f5-137">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="e10f5-138"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e10f5-138"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="e10f5-139">*массив* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="e10f5-139">*array* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e10f5-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e10f5-140">Remarks</span></span>

<span data-ttu-id="e10f5-141">Функции **гленаблеклиентстате** и **глдисаблеклиентстате** включают и отключают различные отдельные массивы.</span><span class="sxs-lookup"><span data-stu-id="e10f5-141">The **glEnableClientState** and **glDisableClientState** functions enable and disable various individual arrays.</span></span> <span data-ttu-id="e10f5-142">Чтобы определить текущее значение любой возможности, используйте [**глисенаблед**](glisenabled.md) или [**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="e10f5-142">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="e10f5-143">Вызов **гленаблеклиентстате** и **глдисаблеклиентстате** между вызовами [**Глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md) может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="e10f5-143">Calling **glEnableClientState** and **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) can cause an error.</span></span> <span data-ttu-id="e10f5-144">Если ошибка не возникает, поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="e10f5-144">If no error is generated, the behavior is undefined.</span></span>

> [!Note]  
> <span data-ttu-id="e10f5-145">Функции **гленаблеклиентстате** и **глдисаблеклиентстате** доступны только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="e10f5-145">The **glEnableClientState** and **glDisableClientState** functions are only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e10f5-146">Требования</span><span class="sxs-lookup"><span data-stu-id="e10f5-146">Requirements</span></span>



| <span data-ttu-id="e10f5-147">Требование</span><span class="sxs-lookup"><span data-stu-id="e10f5-147">Requirement</span></span> | <span data-ttu-id="e10f5-148">Значение</span><span class="sxs-lookup"><span data-stu-id="e10f5-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e10f5-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e10f5-149">Minimum supported client</span></span><br/> | <span data-ttu-id="e10f5-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e10f5-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e10f5-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e10f5-151">Minimum supported server</span></span><br/> | <span data-ttu-id="e10f5-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e10f5-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e10f5-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e10f5-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="e10f5-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e10f5-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e10f5-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e10f5-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="e10f5-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e10f5-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e10f5-157">DLL</span><span class="sxs-lookup"><span data-stu-id="e10f5-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e10f5-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e10f5-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e10f5-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e10f5-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e10f5-160">**гларрайелемент**</span><span class="sxs-lookup"><span data-stu-id="e10f5-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="e10f5-161">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="e10f5-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e10f5-162">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="e10f5-162">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="e10f5-163">**глдисаблеклиентстате**</span><span class="sxs-lookup"><span data-stu-id="e10f5-163">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="e10f5-164">**глдраваррайс**</span><span class="sxs-lookup"><span data-stu-id="e10f5-164">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="e10f5-165">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="e10f5-165">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="e10f5-166">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="e10f5-166">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="e10f5-167">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="e10f5-167">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="e10f5-168">**гленд**</span><span class="sxs-lookup"><span data-stu-id="e10f5-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e10f5-169">**глжетпоинтерв**</span><span class="sxs-lookup"><span data-stu-id="e10f5-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="e10f5-170">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="e10f5-170">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="e10f5-171">**глинтерлеаведаррайс**</span><span class="sxs-lookup"><span data-stu-id="e10f5-171">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="e10f5-172">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="e10f5-172">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="e10f5-173">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="e10f5-173">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="e10f5-174">**глвертекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="e10f5-174">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





