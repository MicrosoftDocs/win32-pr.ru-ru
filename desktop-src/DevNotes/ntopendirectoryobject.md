---
description: Открывает существующий объект каталога.
ms.assetid: 7313fb32-976b-4c73-b9ba-09fb8ad7faf1
title: Функция Нтопендиректорйобжект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ceea03c36e0617e2f48887275e7867e3589c87ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648019"
---
# <a name="ntopendirectoryobject-function"></a><span data-ttu-id="02db6-103">Функция Нтопендиректорйобжект</span><span class="sxs-lookup"><span data-stu-id="02db6-103">NtOpenDirectoryObject function</span></span>

<span data-ttu-id="02db6-104">\[Эта функция может быть изменена или недоступна в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="02db6-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="02db6-105">Открывает существующий объект каталога.</span><span class="sxs-lookup"><span data-stu-id="02db6-105">Opens an existing directory object.</span></span>

## <a name="syntax"></a><span data-ttu-id="02db6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02db6-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtOpenDirectoryObject(
  _Out_ PHANDLE            DirectoryHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="02db6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="02db6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02db6-108">*Директорихандле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="02db6-108">*DirectoryHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02db6-109">Маркер для вновь открытого объекта каталога.</span><span class="sxs-lookup"><span data-stu-id="02db6-109">A handle to the newly opened directory object.</span></span>

</dd> <dt>

<span data-ttu-id="02db6-110">*Десиредакцесс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="02db6-110">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02db6-111">[**\_ Маска доступа**](../secauthz/access-mask.md) , указывающая запрошенный доступ к объекту каталога.</span><span class="sxs-lookup"><span data-stu-id="02db6-111">An [**ACCESS\_MASK**](../secauthz/access-mask.md) that specifies the requested access to the directory object.</span></span> <span data-ttu-id="02db6-112">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="02db6-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="02db6-113">Значение</span><span class="sxs-lookup"><span data-stu-id="02db6-113">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="02db6-114">Значение</span><span class="sxs-lookup"><span data-stu-id="02db6-114">Meaning</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="DIRECTORY_QUERY"></span><span id="directory_query"></span><dl> <span data-ttu-id="02db6-115"><dt>**Каталог \_**</dt> <dt>0x0001</dt> запросов</span><span class="sxs-lookup"><span data-stu-id="02db6-115"><dt>**DIRECTORY\_QUERY**</dt> <dt>0x0001</dt></span></span> </dl>                                            | <span data-ttu-id="02db6-116">Запрос доступа к объекту каталога.</span><span class="sxs-lookup"><span data-stu-id="02db6-116">Query access to the directory object.</span></span><br/>                            |
| <span id="DIRECTORY_TRAVERSE"></span><span id="directory_traverse"></span><dl> <span data-ttu-id="02db6-117"><dt>**Каталог \_ ОБХОД**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="02db6-117"><dt>**DIRECTORY\_TRAVERSE**</dt> <dt>0x0002</dt></span></span> </dl>                                   | <span data-ttu-id="02db6-118">Имя — Поиск доступа к объекту каталога.</span><span class="sxs-lookup"><span data-stu-id="02db6-118">Name-lookup access to the directory object.</span></span><br/>                      |
| <span id="DIRECTORY_CREATE_OBJECT"></span><span id="directory_create_object"></span><dl> <span data-ttu-id="02db6-119"><dt>**Каталог \_ СОЗДАТЬ \_ объект**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="02db6-119"><dt>**DIRECTORY\_CREATE\_OBJECT**</dt> <dt>0x0004</dt></span></span> </dl>                   | <span data-ttu-id="02db6-120">Имя — создание доступа к объекту каталога.</span><span class="sxs-lookup"><span data-stu-id="02db6-120">Name-creation access to the directory object.</span></span><br/>                    |
| <span id="DIRECTORY_CREATE_SUBDIRECTORY"></span><span id="directory_create_subdirectory"></span><dl> <span data-ttu-id="02db6-121"><dt>**Каталог \_ СОЗДАТЬ \_ подкаталог**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="02db6-121"><dt>**DIRECTORY\_CREATE\_SUBDIRECTORY**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="02db6-122">Подкаталог — доступ на создание объекта каталога.</span><span class="sxs-lookup"><span data-stu-id="02db6-122">Subdirectory-creation access to the directory object.</span></span><br/>            |
| <span id="DIRECTORY_ALL_ACCESS"></span><span id="directory_all_access"></span><dl> <span data-ttu-id="02db6-123"><dt>**Каталог \_ \_**</dt> <dt> \_ Требуются права доступа Standard \_ \| 0xF</dt></span><span class="sxs-lookup"><span data-stu-id="02db6-123"><dt>**DIRECTORY\_ALL\_ACCESS**</dt> <dt>STANDARD\_RIGHTS\_REQUIRED \| 0xF</dt></span></span> </dl> | <span data-ttu-id="02db6-124">Все предыдущие права, а также **стандартные \_ права, \_ необходимы**.</span><span class="sxs-lookup"><span data-stu-id="02db6-124">All of the preceding rights plus **STANDARD\_RIGHTS\_REQUIRED**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="02db6-125">*Обжектаттрибутес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="02db6-125">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02db6-126">Атрибуты для объекта каталога.</span><span class="sxs-lookup"><span data-stu-id="02db6-126">The attributes for the directory object.</span></span> <span data-ttu-id="02db6-127">Чтобы инициализировать структуру **\_ атрибутов объекта** , используйте макрос **инитиализеобжектаттрибутес** .</span><span class="sxs-lookup"><span data-stu-id="02db6-127">To initialize the **OBJECT\_ATTRIBUTES** structure, use the **InitializeObjectAttributes** macro.</span></span> <span data-ttu-id="02db6-128">Дополнительные сведения см. в документации по этим элементам в документации по WDK.</span><span class="sxs-lookup"><span data-stu-id="02db6-128">For more information, see the documentation for these items in the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02db6-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02db6-129">Return value</span></span>

<span data-ttu-id="02db6-130">Функция возвращает состояние \_ Success или Error.</span><span class="sxs-lookup"><span data-stu-id="02db6-130">The function returns STATUS\_SUCCESS or an error status.</span></span> <span data-ttu-id="02db6-131">Возможные коды состояния включают следующее.</span><span class="sxs-lookup"><span data-stu-id="02db6-131">The possible status codes include the following.</span></span>



| <span data-ttu-id="02db6-132">Код возврата</span><span class="sxs-lookup"><span data-stu-id="02db6-132">Return code</span></span>                                                                                                       | <span data-ttu-id="02db6-133">Описание</span><span class="sxs-lookup"><span data-stu-id="02db6-133">Description</span></span>                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="02db6-134"><dt>**СОСТОЯНИЕ " \_ недостаточно \_ ресурсов"**</dt></span><span class="sxs-lookup"><span data-stu-id="02db6-134"><dt>**STATUS\_INSUFFICIENT\_RESOURCES**</dt></span></span> </dl>    | <span data-ttu-id="02db6-135">Не удалось выделить временный буфер, необходимый для этой функции.</span><span class="sxs-lookup"><span data-stu-id="02db6-135">A temporary buffer required by this function could not be allocated.</span></span><br/>                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="02db6-136"><dt>**\_Недопустимый \_ параметр Status**</dt></span><span class="sxs-lookup"><span data-stu-id="02db6-136"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>         | <span data-ttu-id="02db6-137">Указанный параметр Обжектаттрибутес был **пустым** указателем, не является допустимым указателем на **структуру \_ атрибутов объекта** или некоторые из элементов, указанных в структуре **\_ атрибутов объекта** , недопустимы.</span><span class="sxs-lookup"><span data-stu-id="02db6-137">The specified ObjectAttributes parameter was a **NULL** pointer, not a valid pointer to an **OBJECT\_ATTRIBUTES** structure, or some of the members specified in the **OBJECT\_ATTRIBUTES** structure were not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="02db6-138"><dt>**\_ \_ недопустимое имя объекта состояния \_**</dt></span><span class="sxs-lookup"><span data-stu-id="02db6-138"><dt>**STATUS\_OBJECT\_NAME\_INVALID**</dt></span></span> </dl>      | <span data-ttu-id="02db6-139">Параметр *обжектаттрибутес* содержал элемент **objectname** в структуре **\_ атрибутов объекта** , который является недопустимым, поскольку после символа **\_ \_ \_ разделителя пути к имени объекта** обнаружена пустая строка.</span><span class="sxs-lookup"><span data-stu-id="02db6-139">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure that was not valid because an empty string was found after the **OBJECT\_NAME\_PATH\_SEPARATOR** character.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="02db6-140"><dt>**\_ \_ \_ не \_ найдено имя объекта состояния**</dt></span><span class="sxs-lookup"><span data-stu-id="02db6-140"><dt>**STATUS\_OBJECT\_NAME\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="02db6-141">Параметр *обжектаттрибутес* содержал элемент **objectname** в структуре **\_ атрибутов объекта** , который не удалось найти.</span><span class="sxs-lookup"><span data-stu-id="02db6-141">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure that could not be found.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="02db6-142"><dt>**\_ \_ путь к объекту состояния \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="02db6-142"><dt>**STATUS\_OBJECT\_PATH\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="02db6-143">Параметр *обжектаттрибутес* содержал элемент **objectname** в структуре **\_ атрибутов объекта** с путем к объекту, который не удалось найти.</span><span class="sxs-lookup"><span data-stu-id="02db6-143">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure with an object path that could not be found.</span></span> <br/>                                                                                                                                      |
| <dl> <span data-ttu-id="02db6-144"><dt>**Состояние \_ \_ \_ \_ неправильный синтаксис пути к объекту**</dt></span><span class="sxs-lookup"><span data-stu-id="02db6-144"><dt>**STATUS\_OBJECT\_PATH\_SYNTAX\_BAD** </dt></span></span> </dl> | <span data-ttu-id="02db6-145">Параметр *обжектаттрибутес* не содержит элемент **RootDirectory** , но элемент **objectname** в структуре **\_ атрибутов объекта** был пустой строкой или не содержит символ **\_ \_ \_ разделителя пути к имени объекта** .</span><span class="sxs-lookup"><span data-stu-id="02db6-145">The *ObjectAttributes* parameter did not contain a **RootDirectory** member, but the **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure was an empty string or did not contain an **OBJECT\_NAME\_PATH\_SEPARATOR** character.</span></span> <span data-ttu-id="02db6-146">Указывает неверный синтаксис пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="02db6-146">This indicates incorrect syntax for the object path.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="02db6-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02db6-147">Remarks</span></span>

<span data-ttu-id="02db6-148">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="02db6-148">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="02db6-149">Требования</span><span class="sxs-lookup"><span data-stu-id="02db6-149">Requirements</span></span>



| <span data-ttu-id="02db6-150">Требование</span><span class="sxs-lookup"><span data-stu-id="02db6-150">Requirement</span></span> | <span data-ttu-id="02db6-151">Значение</span><span class="sxs-lookup"><span data-stu-id="02db6-151">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="02db6-152">DLL</span><span class="sxs-lookup"><span data-stu-id="02db6-152">DLL</span></span><br/> | <dl> <span data-ttu-id="02db6-153"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02db6-153"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02db6-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02db6-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02db6-155">**нткуеридиректорйобжект**</span><span class="sxs-lookup"><span data-stu-id="02db6-155">**NtQueryDirectoryObject**</span></span>](ntquerydirectoryobject.md)
</dt> </dl>

 

 
