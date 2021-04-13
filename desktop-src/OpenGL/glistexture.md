---
title: Функция Глистекстуре (GL. h)
description: Функция Глистекстуре определяет, соответствует ли имя текстуре.
ms.assetid: 89d06642-ff28-4a67-ac7f-ca58150f301e
keywords:
- Функция Глистекстуре OpenGL
topic_type:
- apiref
api_name:
- glIsTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8897cc0eb004da701f28b410f2ca28b6194c9d26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492603"
---
# <a name="glistexture-function"></a><span data-ttu-id="56d93-104">Функция Глистекстуре</span><span class="sxs-lookup"><span data-stu-id="56d93-104">glIsTexture function</span></span>

<span data-ttu-id="56d93-105">Функция **глистекстуре** определяет, соответствует ли имя текстуре.</span><span class="sxs-lookup"><span data-stu-id="56d93-105">The **glIsTexture** function determines if a name corresponds to a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="56d93-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56d93-106">Syntax</span></span>


```C++
GLboolean WINAPI glIsTexture(
   GLuint texture
);
```



## <a name="parameters"></a><span data-ttu-id="56d93-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="56d93-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56d93-108">*поддержки*</span><span class="sxs-lookup"><span data-stu-id="56d93-108">*texture*</span></span> 
</dt> <dd>

<span data-ttu-id="56d93-109">Значение типа, которое является именем текстуры.</span><span class="sxs-lookup"><span data-stu-id="56d93-109">A value that is the name of a texture.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="56d93-110">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="56d93-110">Error codes</span></span>

<span data-ttu-id="56d93-111">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="56d93-111">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="56d93-112">Имя</span><span class="sxs-lookup"><span data-stu-id="56d93-112">Name</span></span>                                                                                                  | <span data-ttu-id="56d93-113">Значение</span><span class="sxs-lookup"><span data-stu-id="56d93-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="56d93-114"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="56d93-114"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="56d93-115">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="56d93-115">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="56d93-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56d93-116">Remarks</span></span>

<span data-ttu-id="56d93-117">Если параметр *текстуры* в настоящее время является именем текстуры, функция **глистекстуре** возвращает \_ значение true.</span><span class="sxs-lookup"><span data-stu-id="56d93-117">If the *texture* parameter is currently the name of a texture, the **glIsTexture** function returns GL\_TRUE.</span></span> <span data-ttu-id="56d93-118">Функция **глистекстуре** возвращает \_ значение false, если *текстура* равна нулю.</span><span class="sxs-lookup"><span data-stu-id="56d93-118">The **glIsTexture** function returns GL\_FALSE if *texture* is zero.</span></span> <span data-ttu-id="56d93-119">Он также возвращает значение GL \_ false, если это ненулевое значение, которое в настоящее время не является именем текстуры, или если возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="56d93-119">It also returns GL\_FALSE if it is a non-zero value that is not currently the name of a texture, or if an error occurs.</span></span>

<span data-ttu-id="56d93-120">В списки вывода нельзя включать вызовы **глистекстуре** .</span><span class="sxs-lookup"><span data-stu-id="56d93-120">You cannot include calls to **glIsTexture** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="56d93-121">Функция **глистекстуре** доступна только в OpenGL версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="56d93-121">The **glIsTexture** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="56d93-122">Требования</span><span class="sxs-lookup"><span data-stu-id="56d93-122">Requirements</span></span>



| <span data-ttu-id="56d93-123">Требование</span><span class="sxs-lookup"><span data-stu-id="56d93-123">Requirement</span></span> | <span data-ttu-id="56d93-124">Значение</span><span class="sxs-lookup"><span data-stu-id="56d93-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56d93-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56d93-125">Minimum supported client</span></span><br/> | <span data-ttu-id="56d93-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="56d93-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="56d93-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56d93-127">Minimum supported server</span></span><br/> | <span data-ttu-id="56d93-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="56d93-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="56d93-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="56d93-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="56d93-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="56d93-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="56d93-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="56d93-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="56d93-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56d93-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="56d93-133">DLL</span><span class="sxs-lookup"><span data-stu-id="56d93-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56d93-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56d93-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56d93-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56d93-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56d93-136">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="56d93-136">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="56d93-137">**глбиндтекстуре**</span><span class="sxs-lookup"><span data-stu-id="56d93-137">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="56d93-138">**гленд**</span><span class="sxs-lookup"><span data-stu-id="56d93-138">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="56d93-139">**глжентекстурес**</span><span class="sxs-lookup"><span data-stu-id="56d93-139">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="56d93-140">**глжет**</span><span class="sxs-lookup"><span data-stu-id="56d93-140">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="56d93-141">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="56d93-141">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="56d93-142">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="56d93-142">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="56d93-143">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="56d93-143">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="56d93-144">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="56d93-144">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





