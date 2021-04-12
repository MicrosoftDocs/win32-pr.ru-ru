---
title: Функция Глделететекстурес (GL. h)
description: Функция Глделететекстурес Удаляет именованные текстуры.
ms.assetid: 300eb99a-9ee5-4495-9489-7e084db9c6c1
keywords:
- Функция Глделететекстурес OpenGL
topic_type:
- apiref
api_name:
- glDeleteTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37893874f143a210bde0099caa7b5ec266f8948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489567"
---
# <a name="gldeletetextures-function"></a><span data-ttu-id="3db3f-104">Функция Глделететекстурес</span><span class="sxs-lookup"><span data-stu-id="3db3f-104">glDeleteTextures function</span></span>

<span data-ttu-id="3db3f-105">Функция **глделететекстурес** Удаляет именованные текстуры.</span><span class="sxs-lookup"><span data-stu-id="3db3f-105">The **glDeleteTextures** function deletes named textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="3db3f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3db3f-106">Syntax</span></span>


```C++
void WINAPI glDeleteTextures(
         GLsizei n,
   const GLuint  *textures
);
```



## <a name="parameters"></a><span data-ttu-id="3db3f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3db3f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3db3f-108">*n*</span><span class="sxs-lookup"><span data-stu-id="3db3f-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="3db3f-109">Число удаляемых текстур.</span><span class="sxs-lookup"><span data-stu-id="3db3f-109">The number of textures to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="3db3f-110">*текстур*</span><span class="sxs-lookup"><span data-stu-id="3db3f-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="3db3f-111">Массив текстур для удаления.</span><span class="sxs-lookup"><span data-stu-id="3db3f-111">An array of textures to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3db3f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3db3f-112">Return value</span></span>

<span data-ttu-id="3db3f-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3db3f-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3db3f-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3db3f-114">Error codes</span></span>

<span data-ttu-id="3db3f-115">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="3db3f-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3db3f-116">Имя</span><span class="sxs-lookup"><span data-stu-id="3db3f-116">Name</span></span>                                                                                                  | <span data-ttu-id="3db3f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3db3f-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3db3f-118"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="3db3f-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="3db3f-119">*n* было отрицательным значением.</span><span class="sxs-lookup"><span data-stu-id="3db3f-119">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="3db3f-120"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="3db3f-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3db3f-121">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3db3f-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3db3f-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3db3f-122">Remarks</span></span>

<span data-ttu-id="3db3f-123">Функция **глделететекстурес** удаляет из *n* текстур, названных элементами *текстур* массива.</span><span class="sxs-lookup"><span data-stu-id="3db3f-123">The **glDeleteTextures** function deletes *n* textures named by the elements of the array *textures*.</span></span> <span data-ttu-id="3db3f-124">После удаления текстуры она не имеет содержимого или размерности, а ее имя может быть свободно для повторного использования (например, с помощью **глжентекстурес**).</span><span class="sxs-lookup"><span data-stu-id="3db3f-124">After a texture is deleted, it has no contents or dimensionality, and its name is free for reuse (for example, by **glGenTextures**).</span></span> <span data-ttu-id="3db3f-125">Функция **глделететекстурес** игнорирует нули и имена, которые не соответствуют существующим текстурам.</span><span class="sxs-lookup"><span data-stu-id="3db3f-125">The **glDeleteTextures** function ignores zeros and names that do not correspond to existing textures.</span></span>

<span data-ttu-id="3db3f-126">Если удаляемая в данный момент текстура удаляется, привязка возвращается к нулю (текстура по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="3db3f-126">If a texture that is currently bound is deleted, the binding reverts to zero (the default texture).</span></span>

<span data-ttu-id="3db3f-127">В списки вывода нельзя включать вызовы **глделететекстурес** .</span><span class="sxs-lookup"><span data-stu-id="3db3f-127">You cannot include calls to **glDeleteTextures** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="3db3f-128">Функция **глделететекстурес** доступна только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="3db3f-128">The **glDeleteTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="3db3f-129">Следующая функция получает сведения, связанные с **глделететекстурес**:</span><span class="sxs-lookup"><span data-stu-id="3db3f-129">The following function retrieves information related to **glDeleteTextures**:</span></span>

-   [<span data-ttu-id="3db3f-130">**глистекстуре**</span><span class="sxs-lookup"><span data-stu-id="3db3f-130">**glIsTexture**</span></span>](glistexture.md)

## <a name="requirements"></a><span data-ttu-id="3db3f-131">Требования</span><span class="sxs-lookup"><span data-stu-id="3db3f-131">Requirements</span></span>



| <span data-ttu-id="3db3f-132">Требование</span><span class="sxs-lookup"><span data-stu-id="3db3f-132">Requirement</span></span> | <span data-ttu-id="3db3f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="3db3f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3db3f-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3db3f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3db3f-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3db3f-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3db3f-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3db3f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3db3f-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3db3f-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3db3f-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3db3f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3db3f-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3db3f-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3db3f-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3db3f-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="3db3f-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3db3f-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3db3f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3db3f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3db3f-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3db3f-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3db3f-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3db3f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3db3f-145">**гларетекстуресресидент**</span><span class="sxs-lookup"><span data-stu-id="3db3f-145">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="3db3f-146">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="3db3f-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3db3f-147">**глбиндтекстуре**</span><span class="sxs-lookup"><span data-stu-id="3db3f-147">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="3db3f-148">**гленд**</span><span class="sxs-lookup"><span data-stu-id="3db3f-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3db3f-149">**глжентекстурес**</span><span class="sxs-lookup"><span data-stu-id="3db3f-149">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="3db3f-150">**глжет**</span><span class="sxs-lookup"><span data-stu-id="3db3f-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="3db3f-151">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="3db3f-151">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="3db3f-152">**глистекстуре**</span><span class="sxs-lookup"><span data-stu-id="3db3f-152">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="3db3f-153">**глприоритизетекстурес**</span><span class="sxs-lookup"><span data-stu-id="3db3f-153">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="3db3f-154">**глтексжен**</span><span class="sxs-lookup"><span data-stu-id="3db3f-154">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="3db3f-155">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="3db3f-155">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="3db3f-156">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="3db3f-156">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="3db3f-157">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="3db3f-157">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





