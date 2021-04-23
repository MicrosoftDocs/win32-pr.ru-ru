---
title: Функция Глбиндтекстуре (GL. h)
description: Функция Глбиндтекстуре позволяет создать именованную текстуру, привязанную к цели текстуры.
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- Функция Глбиндтекстуре OpenGL
topic_type:
- apiref
api_name:
- glBindTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76009a486e3903ad8230891af8b7593ab8aaa47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415704"
---
# <a name="glbindtexture-function"></a><span data-ttu-id="3d25d-104">Функция Глбиндтекстуре</span><span class="sxs-lookup"><span data-stu-id="3d25d-104">glBindTexture function</span></span>

<span data-ttu-id="3d25d-105">Функция **глбиндтекстуре** позволяет создать именованную текстуру, привязанную к цели текстуры.</span><span class="sxs-lookup"><span data-stu-id="3d25d-105">The **glBindTexture** function enables the creation of a named texture that is bound to a texture target.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d25d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d25d-106">Syntax</span></span>


```C++
void WINAPI glBindTexture(
   GLenum target,
   GLuint texture
);
```



## <a name="parameters"></a><span data-ttu-id="3d25d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d25d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d25d-108">*target*</span><span class="sxs-lookup"><span data-stu-id="3d25d-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="3d25d-109">Целевой объект, к которому привязана текстура.</span><span class="sxs-lookup"><span data-stu-id="3d25d-109">The target to which the texture is bound.</span></span> <span data-ttu-id="3d25d-110">Должно иметь значение GL \_ текстуры \_ 1d или \_ 2D текстура GL \_ .</span><span class="sxs-lookup"><span data-stu-id="3d25d-110">Must have the value GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="3d25d-111">*поддержки*</span><span class="sxs-lookup"><span data-stu-id="3d25d-111">*texture*</span></span> 
</dt> <dd>

<span data-ttu-id="3d25d-112">Имя текстуры; Имя текстуры в настоящее время не может использоваться.</span><span class="sxs-lookup"><span data-stu-id="3d25d-112">The name of a texture; the texture name cannot currently be in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d25d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d25d-113">Return value</span></span>

<span data-ttu-id="3d25d-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3d25d-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3d25d-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3d25d-115">Error codes</span></span>

<span data-ttu-id="3d25d-116">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="3d25d-116">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3d25d-117">Имя</span><span class="sxs-lookup"><span data-stu-id="3d25d-117">Name</span></span>                                                                                                  | <span data-ttu-id="3d25d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3d25d-118">Meaning</span></span>                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3d25d-119"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="3d25d-119"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="3d25d-120">*Целевой объект* параметра не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="3d25d-120">The parameter *target* was not an accepted value.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="3d25d-121"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="3d25d-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3d25d-122">*Текстура* параметра не имеет такой же размерности, что и *целевой объект*, или функция была вызвана между вызовом [**Глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3d25d-122">The parameter *texture* did not have the same dimensionality as *target*, or the function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3d25d-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d25d-123">Remarks</span></span>

<span data-ttu-id="3d25d-124">Функция **глбиндтекстуре** позволяет создать именованную текстуру.</span><span class="sxs-lookup"><span data-stu-id="3d25d-124">The **glBindTexture** function enables you to create a named texture.</span></span> <span data-ttu-id="3d25d-125">При вызове **глбиндтекстуре** с *ЦЕЛЕВЫМ объектом* \_ текстуры GL \_ 1d или \_ 2D текстуры GL \_ , а для параметра *текстура* — имя новой текстуры, которая была создана, привязывает название текстуры к соответствующей цели текстуры.</span><span class="sxs-lookup"><span data-stu-id="3d25d-125">Calling **glBindTexture** with *target* set to GL\_TEXTURE\_1D or GL\_TEXTURE\_2D, and *texture* set to the name of the new texture you have created binds the texture name to the appropriate texture target.</span></span> <span data-ttu-id="3d25d-126">Если текстура привязана к целевому объекту, то предыдущая привязка для этого целевого объекта больше не действует.</span><span class="sxs-lookup"><span data-stu-id="3d25d-126">When a texture is bound to a target, the previous binding for that target is no longer in effect.</span></span>

<span data-ttu-id="3d25d-127">Названия текстур — это целые числа без знака с нулевым зарезервированным значением, представляющие текстуру по умолчанию для каждой цели текстуры.</span><span class="sxs-lookup"><span data-stu-id="3d25d-127">Texture names are unsigned integers with the value zero reserved to represent the default texture for each texture target.</span></span> <span data-ttu-id="3d25d-128">Названия текстур и соответствующие содержимое текстур являются локальными для общего пространства отображения, отображаемого в текущем контексте визуализации OpenGL. два контекста отрисовки используют только названия текстур, если они также совместно используют списки отображения.</span><span class="sxs-lookup"><span data-stu-id="3d25d-128">Texture names and the corresponding texture contents are local to the shared display-list space of the current OpenGL rendering context; two rendering contexts share texture names only if they also share display lists.</span></span> <span data-ttu-id="3d25d-129">С помощью [**глжентекстурес**](glgentextures.md)можно создать набор новых текстурных имен.</span><span class="sxs-lookup"><span data-stu-id="3d25d-129">You can generate a set of new texture names using [**glGenTextures**](glgentextures.md).</span></span>

<span data-ttu-id="3d25d-130">При первой привязке текстуры предполагается размер целевого объекта текстуры. Текстура, привязанная к \_ текстуре \_ 1d, преобразуется в одномерный, а текстура, привязанная к \_ ДВУХМЕРНОЙ текстуре GL, \_ преобразуется в двухмерный.</span><span class="sxs-lookup"><span data-stu-id="3d25d-130">When a texture is first bound, it assumes the dimensionality of its texture target; a texture bound to GL\_TEXTURE\_1D becomes one-dimensional and a texture bound to GL\_TEXTURE\_2D becomes two-dimensional.</span></span> <span data-ttu-id="3d25d-131">Операции, выполняемые на целевом объекте текстуры, также влияют на текстуру, привязанную к целевому объекту.</span><span class="sxs-lookup"><span data-stu-id="3d25d-131">Operations you perform on a texture target also affect a texture bound to the target.</span></span> <span data-ttu-id="3d25d-132">При запросе к цели текстуры возвращаемое значение является состоянием текстуры, привязанной к ней.</span><span class="sxs-lookup"><span data-stu-id="3d25d-132">When you query a texture target, the return value is the state of the texture bound to it.</span></span> <span data-ttu-id="3d25d-133">Цели текстуры становятся псевдонимами для текстур, которые в настоящее время привязаны к ним.</span><span class="sxs-lookup"><span data-stu-id="3d25d-133">Texture targets become aliases for textures currently bound to them.</span></span>

<span data-ttu-id="3d25d-134">При привязке текстуры с помощью **глбиндтекстуре** привязка остается активной до тех пор, пока другая текстура не будет привязана к тому же целевому объекту или вы не удалите связанную текстуру с помощью функции [**глделететекстурес**](gldeletetextures.md) .</span><span class="sxs-lookup"><span data-stu-id="3d25d-134">When you bind a texture with **glBindTexture**, the binding remains active until a different texture is bound to the same target or you delete the bound texture with the [**glDeleteTextures**](gldeletetextures.md) function.</span></span> <span data-ttu-id="3d25d-135">После создания именованной текстуры ее можно привязать к цели текстуры с такой же размерностью, как и при необходимости.</span><span class="sxs-lookup"><span data-stu-id="3d25d-135">Once you create a named texture you can bind it to a texture target that has the same dimensionality as often as needed.</span></span>

<span data-ttu-id="3d25d-136">Обычно гораздо быстрее использовать **глбиндтекстуре** для привязки существующей именованной текстуры к одному из целей текстуры, чем перезагружать изображение текстуры с помощью [**glTexImage1D**](glteximage1d.md) или [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="3d25d-136">It is usually much faster to use **glBindTexture** to bind an existing named texture to one of the texture targets than it is to reload the texture image using [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span> <span data-ttu-id="3d25d-137">Для дополнительного управления производительностью текстур используйте [**глприоритизетекстурес**](glprioritizetextures.md).</span><span class="sxs-lookup"><span data-stu-id="3d25d-137">For additional control of texturing performance, use [**glPrioritizeTextures**](glprioritizetextures.md).</span></span>

<span data-ttu-id="3d25d-138">В списки вывода можно включить вызовы **глбиндтекстуре** .</span><span class="sxs-lookup"><span data-stu-id="3d25d-138">You can include calls to **glBindTexture** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="3d25d-139">Функция **глбиндтекстуре** доступна только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="3d25d-139">The **glBindTexture** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="3d25d-140">Следующие функции извлекают сведения, относящиеся к **глбиндтекстуре**:</span><span class="sxs-lookup"><span data-stu-id="3d25d-140">The following functions retrieve information related to **glBindTexture**:</span></span>

-   <span data-ttu-id="3d25d-141">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ текстура \_ 1d \_ привязывание</span><span class="sxs-lookup"><span data-stu-id="3d25d-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_1D\_BINDING</span></span>

<span data-ttu-id="3d25d-142">**глжет** с аргументом \_ \_ двухмерной \_ привязки текстуры GL</span><span class="sxs-lookup"><span data-stu-id="3d25d-142">**glGet** with argument GL\_TEXTURE\_2D\_BINDING</span></span>

## <a name="requirements"></a><span data-ttu-id="3d25d-143">Требования</span><span class="sxs-lookup"><span data-stu-id="3d25d-143">Requirements</span></span>



| <span data-ttu-id="3d25d-144">Требование</span><span class="sxs-lookup"><span data-stu-id="3d25d-144">Requirement</span></span> | <span data-ttu-id="3d25d-145">Значение</span><span class="sxs-lookup"><span data-stu-id="3d25d-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d25d-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d25d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3d25d-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3d25d-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3d25d-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d25d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3d25d-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3d25d-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3d25d-150">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3d25d-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d25d-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d25d-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3d25d-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3d25d-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="3d25d-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d25d-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3d25d-154">DLL</span><span class="sxs-lookup"><span data-stu-id="3d25d-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d25d-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d25d-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d25d-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d25d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d25d-157">**гларетекстуресресидент**</span><span class="sxs-lookup"><span data-stu-id="3d25d-157">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="3d25d-158">**глделететекстурес**</span><span class="sxs-lookup"><span data-stu-id="3d25d-158">**glDeleteTextures**</span></span>](gldeletetextures.md)
</dt> <dt>

[<span data-ttu-id="3d25d-159">**глжентекстурес**</span><span class="sxs-lookup"><span data-stu-id="3d25d-159">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="3d25d-160">**глжет**</span><span class="sxs-lookup"><span data-stu-id="3d25d-160">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="3d25d-161">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="3d25d-161">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="3d25d-162">**глистекстуре**</span><span class="sxs-lookup"><span data-stu-id="3d25d-162">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="3d25d-163">**глприоритизетекстурес**</span><span class="sxs-lookup"><span data-stu-id="3d25d-163">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="3d25d-164">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="3d25d-164">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="3d25d-165">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="3d25d-165">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="3d25d-166">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="3d25d-166">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





