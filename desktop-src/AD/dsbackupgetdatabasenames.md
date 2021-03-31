---
title: Функция Дсбаккупжетдатабасенамес (Нтдсбкли. h)
description: Получает список файлов базы данных для резервного копирования в данном контексте резервного копирования.
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсбаккупжетдатабасенамес
topic_type:
- apiref
api_name:
- DsBackupGetDatabaseNames
- DsBackupGetDatabaseNamesA
- DsBackupGetDatabaseNamesW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6643b17a85727f6e0df4e8deea9609f73afd1e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491028"
---
# <a name="dsbackupgetdatabasenames-function"></a><span data-ttu-id="8e58d-104">Функция Дсбаккупжетдатабасенамес</span><span class="sxs-lookup"><span data-stu-id="8e58d-104">DsBackupGetDatabaseNames function</span></span>

<span data-ttu-id="8e58d-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="8e58d-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8e58d-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="8e58d-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8e58d-107">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="8e58d-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="8e58d-108">Функция **дсбаккупжетдатабасенамес** получает список файлов базы данных для резервного копирования в данном контексте резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="8e58d-108">The **DsBackupGetDatabaseNames** function obtains the list of database files to be backed up for the given backup context.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e58d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e58d-109">Syntax</span></span>


```C++
HRESULT DsBackupGetDatabaseNames(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszAttachmentInfo,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="8e58d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e58d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e58d-111">*ХБК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e58d-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e58d-112">Содержит описатель контекста резервного копирования, полученный с помощью функции [**дсбаккуппрепаре**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="8e58d-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8e58d-113">*псзаттачментинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8e58d-113">*pszAttachmentInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e58d-114">Указатель на строку, которая получает список имен файлов базы данных в виде UNC-путей.</span><span class="sxs-lookup"><span data-stu-id="8e58d-114">Pointer to a string pointer that receives the list of database file names as UNC paths.</span></span> <span data-ttu-id="8e58d-115">Перед вызовом **дсбаккупжетдатабасенамес** это значение должно быть инициализировано **значением NULL** .</span><span class="sxs-lookup"><span data-stu-id="8e58d-115">This value must be initialized to **NULL** prior to calling **DsBackupGetDatabaseNames**.</span></span>

<span data-ttu-id="8e58d-116">Этот список получает список из одиночных строк, заканчивающихся нулем, заканчивающийся символом NULL.</span><span class="sxs-lookup"><span data-stu-id="8e58d-116">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="8e58d-117">Этот буфер выделяется функцией **дсбаккупжетдатабасенамес** и должен быть освобожден, если он больше не требуется путем вызова функции [**дсбаккупфри**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="8e58d-117">This buffer is allocated by the **DsBackupGetDatabaseNames** function and must be freed when it is no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="8e58d-118">Первый символ каждого имени файла содержит одну из [**констант БФТ**](bft-constants.md) , определяющих тип имени.</span><span class="sxs-lookup"><span data-stu-id="8e58d-118">The first character of each file name contains one of the [**BFT Constants**](bft-constants.md) that identifies the type of name.</span></span> <span data-ttu-id="8e58d-119">Функция [**дсресторежетдатабаселокатионс**](dsrestoregetdatabaselocations.md) предоставляет только следующие типы имен.</span><span class="sxs-lookup"><span data-stu-id="8e58d-119">The [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function only supplies the following types of names.</span></span>

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span data-ttu-id="8e58d-120"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_ \_ база данных NTDS БФТ**</span><span class="sxs-lookup"><span data-stu-id="8e58d-120"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>


</dt> <dd>

<span data-ttu-id="8e58d-121">Файл является файлом базы данных NTDS.</span><span class="sxs-lookup"><span data-stu-id="8e58d-121">The file is an NTDS database file.</span></span> <span data-ttu-id="8e58d-122">Этот файл должен быть скопирован в файл, определенный как **\_ \_ база данных БФТ NTDS** , при восстановлении данных.</span><span class="sxs-lookup"><span data-stu-id="8e58d-122">This file should be copied to the file identified as **BFT\_NTDS\_DATABASE** when the data is restored.</span></span>

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span data-ttu-id="8e58d-123"><span id="BFT_LOG"></span><span id="bft_log"></span>**\_Журнал БФТ**</span><span class="sxs-lookup"><span data-stu-id="8e58d-123"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT\_LOG**</span></span>


</dt> <dd>

<span data-ttu-id="8e58d-124">Файл является файлом журнала.</span><span class="sxs-lookup"><span data-stu-id="8e58d-124">The file is a log file.</span></span> <span data-ttu-id="8e58d-125">При восстановлении данных все файлы журнала копируются в каталог, определенный как **БФТ \_ log \_ dir** .</span><span class="sxs-lookup"><span data-stu-id="8e58d-125">All log files are copied to the directory identified as **BFT\_LOG\_DIR** when the data is restored.</span></span>

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span data-ttu-id="8e58d-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_файл исправления \_ БФТ**</span><span class="sxs-lookup"><span data-stu-id="8e58d-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT\_PATCH\_FILE**</span></span>


</dt> <dd>

<span data-ttu-id="8e58d-127">Файл является файлом исправления.</span><span class="sxs-lookup"><span data-stu-id="8e58d-127">The file is a patch file.</span></span> <span data-ttu-id="8e58d-128">Все файлы исправлений копируются в каталог, определенный как **БФТ \_ Checkpoint \_ dir** , при восстановлении данных.</span><span class="sxs-lookup"><span data-stu-id="8e58d-128">All patch files are copied to the directory identified as **BFT\_CHECKPOINT\_DIR** when the data is restored.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8e58d-129">*пкбсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8e58d-129">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e58d-130">Указатель на значение **DWORD** , которое получает размер буфера *псзаттачментинфо* в байтах.</span><span class="sxs-lookup"><span data-stu-id="8e58d-130">Pointer to **DWORD** value that receives the size, in bytes, of the *pszAttachmentInfo* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e58d-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e58d-131">Return value</span></span>

<span data-ttu-id="8e58d-132">Возвращает **значение \_ ОК** , если функция выполнена успешно, или код ошибки Win32 или RPC в противном случае.</span><span class="sxs-lookup"><span data-stu-id="8e58d-132">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="8e58d-133">В следующем списке перечислены другие возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="8e58d-133">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="8e58d-134">**Ошибка \_ отказа в доступе \_**</span><span class="sxs-lookup"><span data-stu-id="8e58d-134">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="8e58d-135">Вызывающий объект не имеет необходимых прав доступа для вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="8e58d-135">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="8e58d-136">Функцию [**дссетаусидентити**](dssetauthidentity.md) можно использовать для задания учетных данных, используемых для функций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="8e58d-136">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="8e58d-137">**Ошибка \_ недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="8e58d-137">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="8e58d-138">недопустимые *ХБК*, *псзаттачментинфо* или *пкбсизе* .</span><span class="sxs-lookup"><span data-stu-id="8e58d-138">*hbc*, *pszAttachmentInfo*, or *pcbSize* are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="8e58d-139">**Ошибка \_ не \_ хватает \_ памяти**</span><span class="sxs-lookup"><span data-stu-id="8e58d-139">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="8e58d-140">Ошибка при выделении памяти.</span><span class="sxs-lookup"><span data-stu-id="8e58d-140">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e58d-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e58d-141">Remarks</span></span>

<span data-ttu-id="8e58d-142">Функция **дсбаккупжетдатабасенамес** предоставляет список файлов базы данных, необходимых для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="8e58d-142">The **DsBackupGetDatabaseNames** function provides a list of the database files necessary for a backup.</span></span> <span data-ttu-id="8e58d-143">Полная резервная копия состоит из файлов базы данных и файлов журналов, предоставляемых функцией [**дсбаккупжетбаккуплогс**](dsbackupgetbackuplogs.md) .</span><span class="sxs-lookup"><span data-stu-id="8e58d-143">A full backup consists of the database files and the log files provided by the [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) function.</span></span> <span data-ttu-id="8e58d-144">Добавочное резервное копирование Active Directory серверов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8e58d-144">Incremental backups of Active Directory servers are not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e58d-145">Требования</span><span class="sxs-lookup"><span data-stu-id="8e58d-145">Requirements</span></span>



| <span data-ttu-id="8e58d-146">Требование</span><span class="sxs-lookup"><span data-stu-id="8e58d-146">Requirement</span></span> | <span data-ttu-id="8e58d-147">Значение</span><span class="sxs-lookup"><span data-stu-id="8e58d-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e58d-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e58d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="8e58d-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e58d-149">Windows Vista</span></span><br/>                                                                    |
| <span data-ttu-id="8e58d-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e58d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="8e58d-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e58d-151">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="8e58d-152">Header</span><span class="sxs-lookup"><span data-stu-id="8e58d-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e58d-153"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e58d-153"><dt>Ntdsbcli.h</dt></span></span> </dl>       |
| <span data-ttu-id="8e58d-154">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8e58d-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="8e58d-155"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e58d-155"><dt>Ntdsbcli.lib</dt></span></span> </dl>     |
| <span data-ttu-id="8e58d-156">DLL</span><span class="sxs-lookup"><span data-stu-id="8e58d-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e58d-157"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e58d-157"><dt>Ntdsbcli.dll</dt></span></span> </dl>     |
| <span data-ttu-id="8e58d-158">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="8e58d-158">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8e58d-159">**Дсбаккупжетдатабасенамесв** (Юникод) и **дсбаккупжетдатабасенамеса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8e58d-159">**DsBackupGetDatabaseNamesW** (Unicode) and **DsBackupGetDatabaseNamesA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e58d-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e58d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e58d-161">**дсбаккуппрепаре**</span><span class="sxs-lookup"><span data-stu-id="8e58d-161">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="8e58d-162">**дсбаккупфри**</span><span class="sxs-lookup"><span data-stu-id="8e58d-162">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="8e58d-163">**дсбаккупжетбаккуплогс**</span><span class="sxs-lookup"><span data-stu-id="8e58d-163">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="8e58d-164">**Константы БФТ**</span><span class="sxs-lookup"><span data-stu-id="8e58d-164">**BFT Constants**</span></span>](bft-constants.md)
</dt> <dt>

[<span data-ttu-id="8e58d-165">Резервное копирование сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="8e58d-165">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="8e58d-166">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="8e58d-166">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

