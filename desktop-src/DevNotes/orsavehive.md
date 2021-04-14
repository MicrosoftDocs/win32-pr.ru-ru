---
description: Записывает указанный автономный куст реестра в файл.
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: Функция Орсавехиве (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSaveHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 59df5b191a9bc0cfe98e1681665c5814935aa2c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647979"
---
# <a name="orsavehive-function"></a><span data-ttu-id="7c3e7-103">Функция Орсавехиве</span><span class="sxs-lookup"><span data-stu-id="7c3e7-103">ORSaveHive function</span></span>

<span data-ttu-id="7c3e7-104">Записывает указанный автономный куст реестра в файл.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-104">Writes the specified offline registry hive to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c3e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c3e7-105">Syntax</span></span>


```C++
DWORD ORSaveHive(
  _In_ ORHKEY Handle,
  _In_ PCWSTR lpHivePath,
  _In_ DWORD  dwOsMajorVersion,
  _In_ DWORD  dwOsMinorVersion
);
```



## <a name="parameters"></a><span data-ttu-id="7c3e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c3e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c3e7-107">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c3e7-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c3e7-108">Описатель автономного куста реестра для сохранения.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-108">A handle to the offline registry hive to save.</span></span>

</dd> <dt>

<span data-ttu-id="7c3e7-109">*лфивепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c3e7-109">*lpHivePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c3e7-110">Указатель на строку в Юникоде, указывающую имя файла куста реестра.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-110">A pointer to a Unicode string that specifies the name of the registry hive file.</span></span> <span data-ttu-id="7c3e7-111">Это имя не может совпадать с именем существующего файла.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-111">This cannot be the name of an existing file.</span></span>

</dd> <dt>

<span data-ttu-id="7c3e7-112">*двосмажорверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c3e7-112">*dwOsMajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c3e7-113">Основной номер версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-113">The major version number of the operating system.</span></span> <span data-ttu-id="7c3e7-114">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-114">This member can be one of the following values.</span></span>



| <span data-ttu-id="7c3e7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7c3e7-115">Value</span></span>                                                                        | <span data-ttu-id="7c3e7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7c3e7-116">Meaning</span></span>                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c3e7-117"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7c3e7-117"><dt>5</dt></span></span> </dl> | <span data-ttu-id="7c3e7-118">Если *двосминорверсион* имеет значение 1, то операционной системой является Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-118">If *dwOsMinorVersion* is 1, the operating system is Windows XP.</span></span><br/> <span data-ttu-id="7c3e7-119">Если *двосминорверсион* имеет значение 2, то используется операционная система windows Server 2003 R2, windows Server 2003 или Windows XP Professional x64 Edition.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-119">If *dwOsMinorVersion* is 2, the operating system is Windows Server 2003 R2, Windows Server 2003, or Windows XP Professional x64 Edition.</span></span><br/> |
| <dl> <span data-ttu-id="7c3e7-120"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7c3e7-120"><dt>6</dt></span></span> </dl> | <span data-ttu-id="7c3e7-121">Если *двосминорверсион* имеет значение 0, то операционной системой является windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-121">If *dwOsMinorVersion* is 0, the operating system is Windows Server 2008 or Windows Vista.</span></span><br/> <span data-ttu-id="7c3e7-122">Если *двосминорверсион* имеет значение 1, то операционной системой является windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-122">If *dwOsMinorVersion* is 1, the operating system is Windows Server 2008 R2 or Windows 7.</span></span><br/>                       |



 

</dd> <dt>

<span data-ttu-id="7c3e7-123">*двосминорверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c3e7-123">*dwOsMinorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c3e7-124">Дополнительный номер версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-124">The minor version number of the operating system.</span></span> <span data-ttu-id="7c3e7-125">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-125">This member can be one of the following values.</span></span>



| <span data-ttu-id="7c3e7-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7c3e7-126">Value</span></span>                                                                        | <span data-ttu-id="7c3e7-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7c3e7-127">Meaning</span></span>                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c3e7-128"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7c3e7-128"><dt>0</dt></span></span> </dl> | <span data-ttu-id="7c3e7-129">Если *двосмажорверсион* имеет значение 6, то операционной системой является windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-129">If *dwOsMajorVersion* is 6, the operating system is Windows Server 2008 or Windows Vista.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="7c3e7-130"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7c3e7-130"><dt>1</dt></span></span> </dl> | <span data-ttu-id="7c3e7-131">Если *двосмажорверсион* имеет значение 5, то операционной системой является Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-131">If *dwOsMajorVersion* is 5, the operating system is Windows XP.</span></span><br/> <span data-ttu-id="7c3e7-132">Если *двосмажорверсион* имеет значение 6, то операционной системой является windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-132">If *dwOsMajorVersion* is 6, the operating system is Windows Server 2008 R2 or Windows 7.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="7c3e7-133"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7c3e7-133"><dt>2</dt></span></span> </dl> | <span data-ttu-id="7c3e7-134">Если *двосмажорверсион* имеет значение 5, то операционной системой является windows Server 2003 R2, windows Server 2003 или Windows XP Professional x64 Edition.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-134">If *dwOsMajorVersion* is 5, the operating system is Windows Server 2003 R2, Windows Server 2003, or Windows XP Professional x64 Edition.</span></span> <br/> <span data-ttu-id="7c3e7-135">Если *двосмажорверсион* имеет значение 6, параметр *двосминорверсион* должен иметь значение 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-135">If *dwOsMajorVersion* is 6, the *dwOsMinorVersion* parameter must be 0 or 1.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c3e7-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c3e7-136">Return value</span></span>

<span data-ttu-id="7c3e7-137">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-137">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="7c3e7-138">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-138">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="7c3e7-139">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-139">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="7c3e7-140">Ниже перечислены возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-140">Possible error codes include the following:</span></span>

-   <span data-ttu-id="7c3e7-141">Если вызывающий объект не имеет необходимых прав доступа для записи файла, функция возвращает сообщение об ошибке \_ отказа в доступе \_ .</span><span class="sxs-lookup"><span data-stu-id="7c3e7-141">If the caller does not have the necessary access rights to write the file, the function returns ERROR\_ACCESS\_DENIED.</span></span>
-   <span data-ttu-id="7c3e7-142">Если указанный файл уже существует, функция возвращает ошибку \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7c3e7-142">If the specified file already exists, the function returns ERROR\_ALREADY\_EXISTS.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c3e7-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c3e7-143">Remarks</span></span>

<span data-ttu-id="7c3e7-144">Для сохранения изменений, внесенных в автономный куст реестра, необходимо использовать функцию **орсавехиве** .</span><span class="sxs-lookup"><span data-stu-id="7c3e7-144">The **ORSaveHive** function must be used to save changes made to an offline registry hive.</span></span> <span data-ttu-id="7c3e7-145">Изменения не сохраняются до тех пор, пока не будет вызван **орсавехиве** для сохранения Hive в файле.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-145">Changes are not preserved until **ORSaveHive** is called to save the hive to a file.</span></span>

<span data-ttu-id="7c3e7-146">Параметры *двосмажорверсион* и *двосминорверсион* вместе указывают формат целевого файла куста реестра.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-146">The *dwOsMajorVersion* and *dwOsMinorVersion* parameters together specify the target format of the registry hive file.</span></span> <span data-ttu-id="7c3e7-147">В следующей таблице перечислены последние номера версий операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-147">The following table summarizes the most recent operating system version numbers.</span></span>



| <span data-ttu-id="7c3e7-148">Операционная система</span><span class="sxs-lookup"><span data-stu-id="7c3e7-148">Operating system</span></span>                    | <span data-ttu-id="7c3e7-149">Номер версии</span><span class="sxs-lookup"><span data-stu-id="7c3e7-149">Version number</span></span> |
|-------------------------------------|----------------|
| <span data-ttu-id="7c3e7-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c3e7-150">Windows Server 2008 R2</span></span>              | <span data-ttu-id="7c3e7-151">6.1</span><span class="sxs-lookup"><span data-stu-id="7c3e7-151">6.1</span></span>            |
| <span data-ttu-id="7c3e7-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7c3e7-152">Windows 7</span></span>                           | <span data-ttu-id="7c3e7-153">6.1</span><span class="sxs-lookup"><span data-stu-id="7c3e7-153">6.1</span></span>            |
| <span data-ttu-id="7c3e7-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c3e7-154">Windows Server 2008</span></span>                 | <span data-ttu-id="7c3e7-155">6.0</span><span class="sxs-lookup"><span data-stu-id="7c3e7-155">6.0</span></span>            |
| <span data-ttu-id="7c3e7-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c3e7-156">Windows Vista</span></span>                       | <span data-ttu-id="7c3e7-157">6.0</span><span class="sxs-lookup"><span data-stu-id="7c3e7-157">6.0</span></span>            |
| <span data-ttu-id="7c3e7-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7c3e7-158">Windows Server 2003 R2</span></span>              | <span data-ttu-id="7c3e7-159">5,2</span><span class="sxs-lookup"><span data-stu-id="7c3e7-159">5.2</span></span>            |
| <span data-ttu-id="7c3e7-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7c3e7-160">Windows Server 2003</span></span>                 | <span data-ttu-id="7c3e7-161">5,2</span><span class="sxs-lookup"><span data-stu-id="7c3e7-161">5.2</span></span>            |
| <span data-ttu-id="7c3e7-162">Windows XP Professional x64 Edition</span><span class="sxs-lookup"><span data-stu-id="7c3e7-162">Windows XP Professional x64 Edition</span></span> | <span data-ttu-id="7c3e7-163">5,2</span><span class="sxs-lookup"><span data-stu-id="7c3e7-163">5.2</span></span>            |
| <span data-ttu-id="7c3e7-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7c3e7-164">Windows XP</span></span>                          | <span data-ttu-id="7c3e7-165">5.1</span><span class="sxs-lookup"><span data-stu-id="7c3e7-165">5.1</span></span>            |



 

<span data-ttu-id="7c3e7-166">Используйте функцию [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) для получения сведений о текущей операционной системе.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-166">Use the [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) function to retrieve information about the current operating system.</span></span>

<span data-ttu-id="7c3e7-167">Функция **орсавехиве** блокирует куст реестра при записи Hive в файл, а затем закрывает файл и снимает блокировку.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-167">The **ORSaveHive** function locks the registry hive while it is writing the hive to the file, then closes the file and releases the lock.</span></span> <span data-ttu-id="7c3e7-168">Куст реестра остается в памяти до тех пор, пока он не будет закрыт путем вызова функции [**орклосехиве**](orclosehive.md) .</span><span class="sxs-lookup"><span data-stu-id="7c3e7-168">The registry hive remains in memory until it is closed by calling the [**ORCloseHive**](orclosehive.md) function.</span></span> <span data-ttu-id="7c3e7-169">Можно внести дальнейшие изменения в куст реестра, когда он открыт. Однако, чтобы сохранить эти изменения, необходимо сохранить куст Hive в новый файл, так как функция **орсавехиве** не перезапишет существующий файл.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-169">It is possible to make further changes to the registry hive while it is open; however, to preserve these changes the hive must be saved to a new file, because the **ORSaveHive** function will not overwrite an existing file.</span></span>

<span data-ttu-id="7c3e7-170">Функцию **орсавехиве** можно использовать для сохранения части автономного куста реестра.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-170">The **ORSaveHive** function can be used to save part of the offline registry hive.</span></span> <span data-ttu-id="7c3e7-171">Ключ, указанный в параметре *Handle* , преобразуется в корневой ключ Hive, состоящий из указанного ключа и всех его подразделов.</span><span class="sxs-lookup"><span data-stu-id="7c3e7-171">The key specified in the *Handle* parameter becomes the root key of a hive that consists of the specified key and all of its subkeys.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c3e7-172">Требования</span><span class="sxs-lookup"><span data-stu-id="7c3e7-172">Requirements</span></span>



| <span data-ttu-id="7c3e7-173">Требование</span><span class="sxs-lookup"><span data-stu-id="7c3e7-173">Requirement</span></span> | <span data-ttu-id="7c3e7-174">Значение</span><span class="sxs-lookup"><span data-stu-id="7c3e7-174">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c3e7-175">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7c3e7-175">Redistributable</span></span><br/> | <span data-ttu-id="7c3e7-176">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="7c3e7-176">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="7c3e7-177">Header</span><span class="sxs-lookup"><span data-stu-id="7c3e7-177">Header</span></span><br/>          | <dl> <span data-ttu-id="7c3e7-178"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c3e7-178"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c3e7-179">DLL</span><span class="sxs-lookup"><span data-stu-id="7c3e7-179">DLL</span></span><br/>             | <dl> <span data-ttu-id="7c3e7-180"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c3e7-180"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c3e7-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c3e7-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c3e7-182">GetVersionEx</span><span class="sxs-lookup"><span data-stu-id="7c3e7-182">GetVersionEx</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[<span data-ttu-id="7c3e7-183">**орклосехиве**</span><span class="sxs-lookup"><span data-stu-id="7c3e7-183">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="7c3e7-184">**оропенхиве**</span><span class="sxs-lookup"><span data-stu-id="7c3e7-184">**OROpenHive**</span></span>](oropenhive.md)
</dt> </dl>

 

 
