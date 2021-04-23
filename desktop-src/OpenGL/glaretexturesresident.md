---
title: Функция Гларетекстуресресидент (GL. h)
description: Функция Гларетекстуресресидент определяет, являются ли указанные объекты текстуры резидентными в памяти текстуры.
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- Функция Гларетекстуресресидент OpenGL
topic_type:
- apiref
api_name:
- glAreTexturesResident
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e7e5965da9604c690384301de6f1879a98994
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672693"
---
# <a name="glaretexturesresident-function"></a><span data-ttu-id="ce121-104">Функция Гларетекстуресресидент</span><span class="sxs-lookup"><span data-stu-id="ce121-104">glAreTexturesResident function</span></span>

<span data-ttu-id="ce121-105">Функция **гларетекстуресресидент** определяет, являются ли указанные объекты текстуры резидентными в памяти текстуры.</span><span class="sxs-lookup"><span data-stu-id="ce121-105">The **glAreTexturesResident** function determines whether specified texture objects are resident in texture memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce121-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce121-106">Syntax</span></span>


```C++
GLboolean WINAPI glAreTexturesResident(
         GLsizei   n,
   const GLuint    *textures,
         GLboolean *residences
);
```



## <a name="parameters"></a><span data-ttu-id="ce121-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce121-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce121-108">*n*</span><span class="sxs-lookup"><span data-stu-id="ce121-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="ce121-109">Число текстур для запроса.</span><span class="sxs-lookup"><span data-stu-id="ce121-109">The number of textures to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="ce121-110">*текстур*</span><span class="sxs-lookup"><span data-stu-id="ce121-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="ce121-111">Адрес массива, содержащего имена текстур для запроса.</span><span class="sxs-lookup"><span data-stu-id="ce121-111">The address of an array containing the names of the textures to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="ce121-112">*места жительства*</span><span class="sxs-lookup"><span data-stu-id="ce121-112">*residences*</span></span> 
</dt> <dd>

<span data-ttu-id="ce121-113">Адрес массива, в котором возвращается состояние проживания текстуры.</span><span class="sxs-lookup"><span data-stu-id="ce121-113">The address of an array in which the texture residence status is returned.</span></span> <span data-ttu-id="ce121-114">Состояние проживания текстуры, названное элементом *текстур* , возвращается в соответствующем *элементе.*</span><span class="sxs-lookup"><span data-stu-id="ce121-114">The residence status of a texture named by an element of *textures* is returned in the corresponding element of *residences*.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="ce121-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="ce121-115">Error codes</span></span>

<span data-ttu-id="ce121-116">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="ce121-116">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ce121-117">Имя</span><span class="sxs-lookup"><span data-stu-id="ce121-117">Name</span></span>                                                                                                  | <span data-ttu-id="ce121-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ce121-118">Meaning</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ce121-119"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ce121-119"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="ce121-120">*n* было отрицательным значением, элемент в *текстурах* равен нулю, или элемент в *текстурах* не содержал идентификатора текстуры.</span><span class="sxs-lookup"><span data-stu-id="ce121-120">*n* was a negative value, an element in *textures* was zero, or an element in *textures* did not contain a texture identifier.</span></span><br/> |
| <dl> <span data-ttu-id="ce121-121"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ce121-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ce121-122">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ce121-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>     |



## <a name="remarks"></a><span data-ttu-id="ce121-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce121-123">Remarks</span></span>

<span data-ttu-id="ce121-124">На компьютерах с ограниченным объемом памяти текстуры OpenGL устанавливает рабочий набор текстур, находящихся в памяти текстуры.</span><span class="sxs-lookup"><span data-stu-id="ce121-124">On machines with a limited amount of texture memory, OpenGL establishes a working set of textures that are resident in texture memory.</span></span> <span data-ttu-id="ce121-125">Эти текстуры могут быть привязаны к цели текстуры гораздо эффективнее, чем нерезидентные текстуры.</span><span class="sxs-lookup"><span data-stu-id="ce121-125">These textures can be bound to a texture target much more efficiently than textures that are not resident.</span></span>

<span data-ttu-id="ce121-126">Функция **гларетекстуресресидент** запрашивает состояние проживания *текстур текстур,* названных элементами *текстур*.</span><span class="sxs-lookup"><span data-stu-id="ce121-126">The **glAreTexturesResident** function queries the texture residence status of the *n* textures named by the elements of *textures*.</span></span> <span data-ttu-id="ce121-127">Если все именованные текстуры находятся в резидентном виде, **гларетекстуресресидент** ВОЗВРАЩАЕТ \_ значение GL true,  а содержимое расположений не затрагивается.</span><span class="sxs-lookup"><span data-stu-id="ce121-127">If all the named textures are resident, **glAreTexturesResident** returns GL\_TRUE, and the contents of *residences* are undisturbed.</span></span> <span data-ttu-id="ce121-128">Если какая-либо из названных текстур не является резидентной, **гларетекстуресресидент** ВОЗВРАЩАЕТ \_ значение ГК false, а подробное состояние возвращается в  *n* элементов.</span><span class="sxs-lookup"><span data-stu-id="ce121-128">If any of the named textures are not resident, **glAreTexturesResident** returns GL\_FALSE, and detailed status is returned in the *n* elements of *residences*.</span></span>

<span data-ttu-id="ce121-129">Если *элемент расположений* имеет \_ значение GL true, то текстура, названная соответствующим элементом *текстур* , накладывается в память текстуры.</span><span class="sxs-lookup"><span data-stu-id="ce121-129">If an element of *residences* is GL\_TRUE, then the texture named by the corresponding element of *textures* is resident in texture memory.</span></span>

<span data-ttu-id="ce121-130">Чтобы запросить состояние проживания для одной ограничивающей текстуры, вызовите [**глжеттекспараметер**](glgettexparameter.md) с *целевым* параметром, для которого задан целевой текстурой, к которой привязан целевой объект, и установите для параметра *pname* значение \_ резидентная текстура GL \_ .</span><span class="sxs-lookup"><span data-stu-id="ce121-130">To query the residence status of a single bound texture, call [**glGetTexParameter**](glgettexparameter.md) with the *target* parameter set to the target texture to which the target is bound and set the *pname* parameter to GL\_TEXTURE\_RESIDENT.</span></span> <span data-ttu-id="ce121-131">Этот метод необходимо использовать для запроса состояния текстуры по умолчанию в резидентном состоянии.</span><span class="sxs-lookup"><span data-stu-id="ce121-131">You must use this method to query the resident status of a default texture.</span></span>

<span data-ttu-id="ce121-132">Невозможно включить **гларетекстуресресидент** в списки вывода.</span><span class="sxs-lookup"><span data-stu-id="ce121-132">You cannot include **glAreTexturesResident** in display lists.</span></span>

<span data-ttu-id="ce121-133">Функция **гларетекстуресресидент** возвращает состояние местонахождение текстур во время вызова.</span><span class="sxs-lookup"><span data-stu-id="ce121-133">The **glAreTexturesResident** function returns the residency status of the textures at the time of invocation.</span></span> <span data-ttu-id="ce121-134">Это не гарантирует, что текстуры будут оставаться резидентными в любое другое время.</span><span class="sxs-lookup"><span data-stu-id="ce121-134">It does not guarantee that the textures will remain resident at any other time.</span></span>

<span data-ttu-id="ce121-135">Если текстуры находятся в виртуальной памяти (нет памяти текстуры), они считаются всегда резидентными.</span><span class="sxs-lookup"><span data-stu-id="ce121-135">If textures reside in virtual memory (there is no texture memory), they are considered always resident.</span></span>

> [!Note]  
> <span data-ttu-id="ce121-136">Функция **гларетекстуресресидент** доступна только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ce121-136">The **glAreTexturesResident** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ce121-137">Требования</span><span class="sxs-lookup"><span data-stu-id="ce121-137">Requirements</span></span>



| <span data-ttu-id="ce121-138">Требование</span><span class="sxs-lookup"><span data-stu-id="ce121-138">Requirement</span></span> | <span data-ttu-id="ce121-139">Значение</span><span class="sxs-lookup"><span data-stu-id="ce121-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce121-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce121-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ce121-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ce121-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ce121-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce121-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ce121-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ce121-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce121-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ce121-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce121-145"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce121-145"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ce121-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ce121-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce121-147"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce121-147"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ce121-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ce121-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce121-149"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce121-149"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce121-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce121-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce121-151">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="ce121-151">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ce121-152">**глбиндтекстуре**</span><span class="sxs-lookup"><span data-stu-id="ce121-152">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="ce121-153">**гленд**</span><span class="sxs-lookup"><span data-stu-id="ce121-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ce121-154">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="ce121-154">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="ce121-155">**глприоритизетекстурес**</span><span class="sxs-lookup"><span data-stu-id="ce121-155">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="ce121-156">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="ce121-156">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="ce121-157">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="ce121-157">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





