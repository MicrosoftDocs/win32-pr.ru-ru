---
title: Функция Глжетстринг (GL. h)
description: Функция Глжетстринг возвращает строку, описывающую текущее подключение OpenGL.
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- Функция Глжетстринг OpenGL
topic_type:
- apiref
api_name:
- glGetString
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e263e35802af752fa262c898d036fccaa37aff87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989266"
---
# <a name="glgetstring-function"></a><span data-ttu-id="2c51e-104">Функция Глжетстринг</span><span class="sxs-lookup"><span data-stu-id="2c51e-104">glGetString function</span></span>

<span data-ttu-id="2c51e-105">Функция **глжетстринг** возвращает строку, описывающую текущее подключение OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2c51e-105">The **glGetString** function returns a string describing the current OpenGL connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c51e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c51e-106">Syntax</span></span>


```C++
const GLubyte* WINAPI glGetString(
   GLenum name
);
```



## <a name="parameters"></a><span data-ttu-id="2c51e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c51e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c51e-108">*name*</span><span class="sxs-lookup"><span data-stu-id="2c51e-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="2c51e-109">Одна из следующих символьных констант.</span><span class="sxs-lookup"><span data-stu-id="2c51e-109">One of the following symbolic constants.</span></span>



| <span data-ttu-id="2c51e-110">Значение</span><span class="sxs-lookup"><span data-stu-id="2c51e-110">Value</span></span>                                                                                                                                                         | <span data-ttu-id="2c51e-111">Значение</span><span class="sxs-lookup"><span data-stu-id="2c51e-111">Meaning</span></span>                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <span data-ttu-id="2c51e-112"><dt>**\_поставщик GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2c51e-112"><dt>**GL\_VENDOR**</dt></span></span> </dl>             | <span data-ttu-id="2c51e-113">Возвращает компанию, ответственную за эту реализацию OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2c51e-113">Returns the company responsible for this OpenGL implementation.</span></span> <span data-ttu-id="2c51e-114">Это имя не меняется с выпуска на выпуск.</span><span class="sxs-lookup"><span data-stu-id="2c51e-114">This name does not change from release to release.</span></span><br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <span data-ttu-id="2c51e-115"><dt>**модуль \_ подготовки отчетов GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2c51e-115"><dt>**GL\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="2c51e-116">Возвращает имя модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="2c51e-116">Returns the name of the renderer.</span></span> <span data-ttu-id="2c51e-117">Это имя обычно характерно для конкретной конфигурации аппаратной платформы.</span><span class="sxs-lookup"><span data-stu-id="2c51e-117">This name is typically specific to a particular configuration of a hardware platform.</span></span> <span data-ttu-id="2c51e-118">Он не меняется с выпуска на выпуск.</span><span class="sxs-lookup"><span data-stu-id="2c51e-118">It does not change from release to release.</span></span><br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <span data-ttu-id="2c51e-119"><dt>**\_версия GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2c51e-119"><dt>**GL\_VERSION**</dt></span></span> </dl>          | <span data-ttu-id="2c51e-120">Возвращает версию или номер выпуска.</span><span class="sxs-lookup"><span data-stu-id="2c51e-120">Returns a version or release number.</span></span><br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <span data-ttu-id="2c51e-121"><dt>**\_расширения GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2c51e-121"><dt>**GL\_EXTENSIONS**</dt></span></span> </dl> | <span data-ttu-id="2c51e-122">Возвращает список поддерживаемых расширений OpenGL с разделителями-пробелами.</span><span class="sxs-lookup"><span data-stu-id="2c51e-122">Returns a space-separated list of supported extensions to OpenGL.</span></span><br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="2c51e-123">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="2c51e-123">Error codes</span></span>

<span data-ttu-id="2c51e-124">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="2c51e-124">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2c51e-125">Имя</span><span class="sxs-lookup"><span data-stu-id="2c51e-125">Name</span></span>                                                                                                  | <span data-ttu-id="2c51e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2c51e-126">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c51e-127"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2c51e-127"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2c51e-128">*имя* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="2c51e-128">*name* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="2c51e-129"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2c51e-129"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2c51e-130">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2c51e-130">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2c51e-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c51e-131">Remarks</span></span>

<span data-ttu-id="2c51e-132">Функция **глжетстринг** возвращает указатель на статическую строку, описывающую некоторые аспекты текущего подключения OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2c51e-132">The **glGetString** function returns a pointer to a static string describing some aspect of the current OpenGL connection.</span></span>

<span data-ttu-id="2c51e-133">Поскольку OpenGL не включает запросы для характеристик производительности реализации, предполагается, что некоторые приложения будут написаны для распознавания известных платформ и изменят использование OpenGL на основе известных характеристик производительности этих платформ.</span><span class="sxs-lookup"><span data-stu-id="2c51e-133">Because OpenGL does not include queries for the performance characteristics of an implementation, it is expected that some applications will be written to recognize known platforms and will modify their OpenGL usage based on known performance characteristics of these platforms.</span></span> <span data-ttu-id="2c51e-134">Строки "поставщик GL" \_ и " \_ Подготовка к выпуску GL" вместе уникальным образом определяют платформу и не будут изменяться с выпуска на выпуск.</span><span class="sxs-lookup"><span data-stu-id="2c51e-134">The strings GL\_VENDOR and GL\_RENDERER together uniquely specify a platform, and will not change from release to release.</span></span> <span data-ttu-id="2c51e-135">Они должны использоваться алгоритмами распознавания платформ.</span><span class="sxs-lookup"><span data-stu-id="2c51e-135">They should be used as such by platform recognition algorithms.</span></span>

<span data-ttu-id="2c51e-136">Формат и содержимое строки, возвращаемой **глжетстринг** , зависят от реализации, за исключением того, что:</span><span class="sxs-lookup"><span data-stu-id="2c51e-136">The format and contents of the string that **glGetString** returns depend on the implementation, except that:</span></span>

-   <span data-ttu-id="2c51e-137">Имена расширений не будут содержать пробелы и будут разделены символами пробела в \_ строке РАСШИРЕНИЙ GL.</span><span class="sxs-lookup"><span data-stu-id="2c51e-137">Extension names will not include space characters and will be separated by space characters in the GL\_EXTENSIONS string.</span></span>
-   <span data-ttu-id="2c51e-138">\_Строка версии GL начинается с номера версии.</span><span class="sxs-lookup"><span data-stu-id="2c51e-138">The GL\_VERSION string begins with a version number.</span></span> <span data-ttu-id="2c51e-139">Номер версии использует одну из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="2c51e-139">The version number uses one of these forms:</span></span>

    <span data-ttu-id="2c51e-140">*основной \_ номер*. *дополнительный \_ номер*</span><span class="sxs-lookup"><span data-stu-id="2c51e-140">*major\_number*.*minor\_number*</span></span>

    <span data-ttu-id="2c51e-141">*основной \_ номер*. *дополнительный \_ номер*. *\_ номер выпуска*</span><span class="sxs-lookup"><span data-stu-id="2c51e-141">*major\_number*.*minor\_number*.*release\_number*</span></span>

-   <span data-ttu-id="2c51e-142">Сведения, относящиеся к поставщику, могут соответствовать номеру версии.</span><span class="sxs-lookup"><span data-stu-id="2c51e-142">Vendor-specific information may follow the version number.</span></span> <span data-ttu-id="2c51e-143">Его формат зависит от реализации, но пробел всегда отделяет номер версии и сведения, относящиеся к поставщику.</span><span class="sxs-lookup"><span data-stu-id="2c51e-143">Its format depends on the implementation, but a space always separates the version number and the vendor-specific information.</span></span>
-   <span data-ttu-id="2c51e-144">Все строки завершаются нулем.</span><span class="sxs-lookup"><span data-stu-id="2c51e-144">All strings are null-terminated.</span></span>

<span data-ttu-id="2c51e-145">Если возникает ошибка, **глжетстринг** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="2c51e-145">If an error is generated, **glGetString** returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c51e-146">Требования</span><span class="sxs-lookup"><span data-stu-id="2c51e-146">Requirements</span></span>



| <span data-ttu-id="2c51e-147">Требование</span><span class="sxs-lookup"><span data-stu-id="2c51e-147">Requirement</span></span> | <span data-ttu-id="2c51e-148">Значение</span><span class="sxs-lookup"><span data-stu-id="2c51e-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c51e-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c51e-149">Minimum supported client</span></span><br/> | <span data-ttu-id="2c51e-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c51e-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2c51e-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c51e-151">Minimum supported server</span></span><br/> | <span data-ttu-id="2c51e-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2c51e-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2c51e-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2c51e-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c51e-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c51e-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2c51e-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2c51e-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="2c51e-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c51e-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2c51e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="2c51e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c51e-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c51e-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c51e-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c51e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c51e-160">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="2c51e-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2c51e-161">**гленд**</span><span class="sxs-lookup"><span data-stu-id="2c51e-161">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





