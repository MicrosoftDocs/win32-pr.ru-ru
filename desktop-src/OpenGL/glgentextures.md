---
title: Функция Глжентекстурес (GL. h)
description: Функция Глжентекстурес создает имена текстур.
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
keywords:
- Функция Глжентекстурес OpenGL
topic_type:
- apiref
api_name:
- glGenTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204a5d4fb736a88cf615577f4c740cde15d75829
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989267"
---
# <a name="glgentextures-function"></a><span data-ttu-id="379ec-104">Функция Глжентекстурес</span><span class="sxs-lookup"><span data-stu-id="379ec-104">glGenTextures function</span></span>

<span data-ttu-id="379ec-105">Функция **глжентекстурес** создает имена текстур.</span><span class="sxs-lookup"><span data-stu-id="379ec-105">The **glGenTextures** function generates texture names.</span></span>

## <a name="syntax"></a><span data-ttu-id="379ec-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="379ec-106">Syntax</span></span>


```C++
void WINAPI glGenTextures(
   GLsizei n,
   GLuint  *textures
);
```



## <a name="parameters"></a><span data-ttu-id="379ec-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="379ec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="379ec-108">*n*</span><span class="sxs-lookup"><span data-stu-id="379ec-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="379ec-109">Число создаваемых текстурных названий.</span><span class="sxs-lookup"><span data-stu-id="379ec-109">The number of texture names to be generated.</span></span>

</dd> <dt>

<span data-ttu-id="379ec-110">*текстур*</span><span class="sxs-lookup"><span data-stu-id="379ec-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="379ec-111">Указатель на первый элемент массива, в котором хранятся созданные имена текстур.</span><span class="sxs-lookup"><span data-stu-id="379ec-111">A pointer to the first element of an array in which the generated texture names are stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="379ec-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="379ec-112">Return value</span></span>

<span data-ttu-id="379ec-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="379ec-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="379ec-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="379ec-114">Error codes</span></span>

<span data-ttu-id="379ec-115">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="379ec-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="379ec-116">Имя</span><span class="sxs-lookup"><span data-stu-id="379ec-116">Name</span></span>                                                                                                  | <span data-ttu-id="379ec-117">Значение</span><span class="sxs-lookup"><span data-stu-id="379ec-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="379ec-118"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="379ec-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="379ec-119">*n* было отрицательным значением.</span><span class="sxs-lookup"><span data-stu-id="379ec-119">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="379ec-120"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="379ec-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="379ec-121">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="379ec-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="379ec-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="379ec-122">Remarks</span></span>

<span data-ttu-id="379ec-123">Функция **глжентекстурес** возвращает *n* названий текстур в параметре *текстуры* .</span><span class="sxs-lookup"><span data-stu-id="379ec-123">The **glGenTextures** function returns *n* texture names in the *textures* parameter.</span></span> <span data-ttu-id="379ec-124">Названия текстур не обязательно являются непрерывным набором целых чисел, однако ни одно из возвращаемых имен не может быть использовано непосредственно перед вызовом функции **глжентекстурес** .</span><span class="sxs-lookup"><span data-stu-id="379ec-124">The texture names are not necessarily a contiguous set of integers, however, none of the returned names can have been in use immediately prior to calling the **glGenTextures** function.</span></span> <span data-ttu-id="379ec-125">Созданные текстуры предполагают размерность цели текстуры, к которой они сначала привязаны с помощью функции [**глбиндтекстуре**](glbindtexture.md) .</span><span class="sxs-lookup"><span data-stu-id="379ec-125">The generated textures assume the dimensionality of the texture target to which they are first bound with the [**glBindTexture**](glbindtexture.md) function.</span></span> <span data-ttu-id="379ec-126">Имена текстур, возвращаемые функцией **глжентекстурес** , не возвращаются при последующих вызовах **глжентекстурес** , если они не были сначала удалены путем вызова [**глделететекстурес**](gldeletetextures.md).</span><span class="sxs-lookup"><span data-stu-id="379ec-126">Texture names returned by **glGenTextures** are not returned by subsequent calls to **glGenTextures** unless they are first deleted by calling [**glDeleteTextures**](gldeletetextures.md).</span></span>

<span data-ttu-id="379ec-127">Невозможно включить **глжентекстурес** в списки вывода.</span><span class="sxs-lookup"><span data-stu-id="379ec-127">You cannot include **glGenTextures** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="379ec-128">Функция **глжентекстурес** доступна только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="379ec-128">The **glGenTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="379ec-129">Следующая функция получает сведения, связанные с **глжентекстурес**:</span><span class="sxs-lookup"><span data-stu-id="379ec-129">The following function retrieves information related to **glGenTextures**:</span></span>

-   [<span data-ttu-id="379ec-130">**глистекстуре**</span><span class="sxs-lookup"><span data-stu-id="379ec-130">**glIsTexture**</span></span>](glistexture.md)

## <a name="requirements"></a><span data-ttu-id="379ec-131">Требования</span><span class="sxs-lookup"><span data-stu-id="379ec-131">Requirements</span></span>



| <span data-ttu-id="379ec-132">Требование</span><span class="sxs-lookup"><span data-stu-id="379ec-132">Requirement</span></span> | <span data-ttu-id="379ec-133">Значение</span><span class="sxs-lookup"><span data-stu-id="379ec-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="379ec-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="379ec-134">Minimum supported client</span></span><br/> | <span data-ttu-id="379ec-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="379ec-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="379ec-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="379ec-136">Minimum supported server</span></span><br/> | <span data-ttu-id="379ec-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="379ec-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="379ec-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="379ec-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="379ec-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="379ec-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="379ec-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="379ec-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="379ec-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="379ec-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="379ec-142">DLL</span><span class="sxs-lookup"><span data-stu-id="379ec-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="379ec-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="379ec-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="379ec-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="379ec-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="379ec-145">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="379ec-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="379ec-146">**глбиндтекстуре**</span><span class="sxs-lookup"><span data-stu-id="379ec-146">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="379ec-147">**глделететекстурес**</span><span class="sxs-lookup"><span data-stu-id="379ec-147">**glDeleteTextures**</span></span>](gldeletetextures.md)
</dt> <dt>

[<span data-ttu-id="379ec-148">**гленд**</span><span class="sxs-lookup"><span data-stu-id="379ec-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="379ec-149">**глжет**</span><span class="sxs-lookup"><span data-stu-id="379ec-149">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="379ec-150">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="379ec-150">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="379ec-151">**глистекстуре**</span><span class="sxs-lookup"><span data-stu-id="379ec-151">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="379ec-152">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="379ec-152">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="379ec-153">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="379ec-153">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="379ec-154">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="379ec-154">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





