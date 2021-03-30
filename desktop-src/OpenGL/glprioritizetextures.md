---
title: Функция Глприоритизетекстурес (GL. h)
description: Функция Глприоритизетекстурес задает приоритет проживания для текстур.
ms.assetid: 09018c86-c667-4e43-a95a-51a8077aed33
keywords:
- Функция Глприоритизетекстурес OpenGL
topic_type:
- apiref
api_name:
- glPrioritizeTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38ab4b1bd6b5f9682b4d8753e7e84f1f2b58a09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801636"
---
# <a name="glprioritizetextures-function"></a><span data-ttu-id="02212-104">Функция Глприоритизетекстурес</span><span class="sxs-lookup"><span data-stu-id="02212-104">glPrioritizeTextures function</span></span>

<span data-ttu-id="02212-105">Функция **глприоритизетекстурес** задает приоритет проживания для текстур.</span><span class="sxs-lookup"><span data-stu-id="02212-105">The **glPrioritizeTextures** function sets the residence priority of textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="02212-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02212-106">Syntax</span></span>


```C++
void WINAPI glPrioritizeTextures(
         GLsizei  n,
   const GLuint   *textures,
   const GLclampf *priorities
);
```



## <a name="parameters"></a><span data-ttu-id="02212-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="02212-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02212-108">*n*</span><span class="sxs-lookup"><span data-stu-id="02212-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="02212-109">Число текстур для определения приоритетов.</span><span class="sxs-lookup"><span data-stu-id="02212-109">The number of textures to be prioritized.</span></span>

</dd> <dt>

<span data-ttu-id="02212-110">*текстур*</span><span class="sxs-lookup"><span data-stu-id="02212-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="02212-111">Указатель на первый элемент массива, содержащий имена текстур, для которых необходимо задать приоритеты.</span><span class="sxs-lookup"><span data-stu-id="02212-111">A pointer to the first element of an array containing the names of the textures to be prioritized.</span></span>

</dd> <dt>

<span data-ttu-id="02212-112">*приоритеты*</span><span class="sxs-lookup"><span data-stu-id="02212-112">*priorities*</span></span> 
</dt> <dd>

<span data-ttu-id="02212-113">Указатель на первый элемент массива, содержащий приоритеты текстуры.</span><span class="sxs-lookup"><span data-stu-id="02212-113">A pointer to the first element of an array containing the texture priorities.</span></span> <span data-ttu-id="02212-114">Приоритет, заданный в *элементе параметра prioritys, применяется* к текстуре, названной соответствующим элементом параметра *текстуры* .</span><span class="sxs-lookup"><span data-stu-id="02212-114">A priority given in an element of the *priorities* parameter applies to the texture named by the corresponding element of the *textures* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02212-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02212-115">Return value</span></span>

<span data-ttu-id="02212-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="02212-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="02212-117">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="02212-117">Error codes</span></span>

<span data-ttu-id="02212-118">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="02212-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="02212-119">Имя</span><span class="sxs-lookup"><span data-stu-id="02212-119">Name</span></span>                                                                                                  | <span data-ttu-id="02212-120">Значение</span><span class="sxs-lookup"><span data-stu-id="02212-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="02212-121"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="02212-121"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="02212-122">*n* было отрицательным значением.</span><span class="sxs-lookup"><span data-stu-id="02212-122">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="02212-123"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="02212-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="02212-124">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="02212-124">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="02212-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02212-125">Remarks</span></span>

<span data-ttu-id="02212-126">Функция **глприоритизетекстурес** назначает приоритеты текстуры *n* , указанные в параметре *приоритеты* , с текстурами *n* , названными в параметре *текстуры* .</span><span class="sxs-lookup"><span data-stu-id="02212-126">The **glPrioritizeTextures** function assigns the *n* texture priorities specified in the *priorities* parameter to the *n* textures named in the *textures* parameter.</span></span> <span data-ttu-id="02212-127">На компьютерах с ограниченным объемом памяти текстуры OpenGL устанавливает "Рабочий набор" текстур, которые находятся в памяти текстуры.</span><span class="sxs-lookup"><span data-stu-id="02212-127">On computers with a limited amount of texture memory, OpenGL establishes a "working set" of textures that are resident in texture memory.</span></span> <span data-ttu-id="02212-128">Эти текстуры могут быть привязаны к цели текстуры гораздо эффективнее, чем нерезидентные текстуры.</span><span class="sxs-lookup"><span data-stu-id="02212-128">These textures can be bound to a texture target much more efficiently than textures that are not resident.</span></span>

<span data-ttu-id="02212-129">При указании приоритета для каждой текстуры функция **глприоритизетекстурес** позволяет определить, какие текстуры должны быть резидентными.</span><span class="sxs-lookup"><span data-stu-id="02212-129">By specifying a priority for each texture, the **glPrioritizeTextures** function enables you to determine which textures should be resident.</span></span>

<span data-ttu-id="02212-130">*Приоритеты текстур задаются* в диапазоне \[ 0,0, 1,0 \] перед присвоением.</span><span class="sxs-lookup"><span data-stu-id="02212-130">The texture priorities elements in *priorities* are clamped to the range \[0.0, 1.0\] before being assigned.</span></span> <span data-ttu-id="02212-131">Ноль указывает на самый низкий приоритет; таким, текстуры с нулевым приоритетом, скорее всего, будут резидентными.</span><span class="sxs-lookup"><span data-stu-id="02212-131">Zero indicates the lowest priority; thus textures with priority zero are least likely to be resident.</span></span> <span data-ttu-id="02212-132">Значение 1,0 указывает на самый высокий приоритет; таким, текстуры с приоритетом 1,0, скорее всего, будут резидентными.</span><span class="sxs-lookup"><span data-stu-id="02212-132">The value 1.0 indicates the highest priority; thus textures with priority 1.0 are most likely to be resident.</span></span> <span data-ttu-id="02212-133">Однако текстуры не гарантируют резидентные, пока они не будут привязаны.</span><span class="sxs-lookup"><span data-stu-id="02212-133">However, textures are not guaranteed to be resident until they are bound.</span></span>

<span data-ttu-id="02212-134">Функция **глприоритизетекстурес** игнорирует попытки определения приоритета текстуры 0 или любого названия текстуры, которое не соответствует существующей текстуре.</span><span class="sxs-lookup"><span data-stu-id="02212-134">The **glPrioritizeTextures** function ignores attempts to prioritize texture 0, or any texture name that does not correspond to an existing texture.</span></span> <span data-ttu-id="02212-135">Ни одна из функций, названных с помощью параметра *текстуры* , не должна быть привязана к цели текстуры.</span><span class="sxs-lookup"><span data-stu-id="02212-135">None of the functions named by the *textures* parameter need to be bound to a texture target.</span></span>

<span data-ttu-id="02212-136">Если в настоящее время привязана текстура, можно также использовать функцию [**глтекспараметер**](gltexparameter-functions.md) для установки ее приоритета.</span><span class="sxs-lookup"><span data-stu-id="02212-136">If a texture is currently bound, you can also use the [**glTexParameter**](gltexparameter-functions.md) function to set its priority.</span></span> <span data-ttu-id="02212-137">Это единственный способ задать приоритет текстуры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="02212-137">This is the only way to set the priority of a default texture.</span></span>

<span data-ttu-id="02212-138">**Глприоритизетекстурес** можно включить в списки вывода.</span><span class="sxs-lookup"><span data-stu-id="02212-138">You can include **glPrioritizeTextures** in display lists.</span></span>

<span data-ttu-id="02212-139">Следующая функция получает приоритет текстуры, привязанной к текущему моменту, связанной с **глприоритизетекстурес**:</span><span class="sxs-lookup"><span data-stu-id="02212-139">The following function retrieves the priority of a currently-bound texture related to **glPrioritizeTextures**:</span></span>

-   <span data-ttu-id="02212-140">[**глжеттекспараметер**](glgettexparameter.md) с именем параметра \_ приоритет текстуры \_ GL</span><span class="sxs-lookup"><span data-stu-id="02212-140">[**glGetTexParameter**](glgettexparameter.md) with parameter name GL\_TEXTURE\_PRIORITY</span></span>

> [!Note]  
> <span data-ttu-id="02212-141">Функция **глприоритизетекстурес** доступна только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="02212-141">The **glPrioritizeTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="02212-142">Требования</span><span class="sxs-lookup"><span data-stu-id="02212-142">Requirements</span></span>



| <span data-ttu-id="02212-143">Требование</span><span class="sxs-lookup"><span data-stu-id="02212-143">Requirement</span></span> | <span data-ttu-id="02212-144">Значение</span><span class="sxs-lookup"><span data-stu-id="02212-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02212-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02212-145">Minimum supported client</span></span><br/> | <span data-ttu-id="02212-146">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="02212-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="02212-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02212-147">Minimum supported server</span></span><br/> | <span data-ttu-id="02212-148">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="02212-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02212-149">Заголовок</span><span class="sxs-lookup"><span data-stu-id="02212-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="02212-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="02212-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="02212-151">Библиотека</span><span class="sxs-lookup"><span data-stu-id="02212-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="02212-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02212-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="02212-153">DLL</span><span class="sxs-lookup"><span data-stu-id="02212-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02212-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02212-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02212-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02212-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02212-156">**гларетекстуресресидент**</span><span class="sxs-lookup"><span data-stu-id="02212-156">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="02212-157">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="02212-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="02212-158">**гленд**</span><span class="sxs-lookup"><span data-stu-id="02212-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="02212-159">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="02212-159">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="02212-160">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="02212-160">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="02212-161">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="02212-161">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="02212-162">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="02212-162">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





