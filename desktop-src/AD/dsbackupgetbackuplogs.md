---
title: Функция Дсбаккупжетбаккуплогс (Нтдсбкли. h)
description: Получает список файлов журнала, для которых необходимо создать резервную копию для данного контекста резервного копирования.
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсбаккупжетбаккуплогс
topic_type:
- apiref
api_name:
- DsBackupGetBackupLogs
- DsBackupGetBackupLogsA
- DsBackupGetBackupLogsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a02c5c7234810623a95dea030f0c623cca92293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988775"
---
# <a name="dsbackupgetbackuplogs-function"></a><span data-ttu-id="79c72-104">Функция Дсбаккупжетбаккуплогс</span><span class="sxs-lookup"><span data-stu-id="79c72-104">DsBackupGetBackupLogs function</span></span>

<span data-ttu-id="79c72-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="79c72-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="79c72-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="79c72-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="79c72-107">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="79c72-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="79c72-108">Функция **дсбаккупжетбаккуплогс** получает список файлов журнала, для которых необходимо создать резервную копию для данного контекста резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="79c72-108">The **DsBackupGetBackupLogs** function obtains the list of log files that must be backed up for the given backup context.</span></span>

## <a name="syntax"></a><span data-ttu-id="79c72-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79c72-109">Syntax</span></span>


```C++
HRESULT DsBackupGetBackupLogs(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszBackupLogFiles,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="79c72-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="79c72-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79c72-111">*ХБК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="79c72-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79c72-112">Содержит описатель контекста резервного копирования, полученный с помощью функции [**дсбаккуппрепаре**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="79c72-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="79c72-113">*псзбаккуплогфилес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="79c72-113">*pszBackupLogFiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79c72-114">Указатель на строку, получающий список имен файлов журналов в виде UNC-путей.</span><span class="sxs-lookup"><span data-stu-id="79c72-114">Pointer to a string pointer that receives the list of log file names as UNC paths.</span></span> <span data-ttu-id="79c72-115">Перед вызовом **дсбаккупжетбаккуплогс** инициализируйте это значение значением **null** .</span><span class="sxs-lookup"><span data-stu-id="79c72-115">Initialize this value to **NULL** before calling **DsBackupGetBackupLogs**.</span></span>

<span data-ttu-id="79c72-116">Этот список получает список из одиночных строк, заканчивающихся нулем, заканчивающийся символом NULL.</span><span class="sxs-lookup"><span data-stu-id="79c72-116">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="79c72-117">Этот буфер выделяется функцией **дсбаккупжетбаккуплогс** и должен быть освобожден, если он больше не требуется путем вызова функции [**дсбаккупфри**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="79c72-117">This buffer is allocated by the **DsBackupGetBackupLogs** function and must be freed when no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="79c72-118">Первый символ каждого из имен файлов содержит одну из [**констант БФТ**](bft-constants.md) , определяющих тип имени.</span><span class="sxs-lookup"><span data-stu-id="79c72-118">The first character of each of the file names contains one of the [**BFT Constants**](bft-constants.md) that identifies the type of name.</span></span>

</dd> <dt>

<span data-ttu-id="79c72-119">*пкбсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="79c72-119">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79c72-120">Указатель на значение **DWORD** , которое получает размер буфера *псзбаккуплогфилес* в байтах.</span><span class="sxs-lookup"><span data-stu-id="79c72-120">Pointer to **DWORD** value that receives the size, in bytes, of the *pszBackupLogFiles* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79c72-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79c72-121">Return value</span></span>

<span data-ttu-id="79c72-122">Возвращает **значение \_ ОК** , если функция выполнена успешно, или код ошибки Win32 или RPC в противном случае.</span><span class="sxs-lookup"><span data-stu-id="79c72-122">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="79c72-123">В следующем списке перечислены другие возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="79c72-123">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="79c72-124">**Ошибка \_ отказа в доступе \_**</span><span class="sxs-lookup"><span data-stu-id="79c72-124">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="79c72-125">Вызывающий объект не имеет необходимых прав доступа для вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="79c72-125">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="79c72-126">Функцию [**дссетаусидентити**](dssetauthidentity.md) можно использовать для задания учетных данных, используемых для функций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="79c72-126">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="79c72-127">**Ошибка \_ недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="79c72-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="79c72-128">Недопустимый *ХБК*, *псзбаккуплогфилес* или *пкбсизе* .</span><span class="sxs-lookup"><span data-stu-id="79c72-128">*hbc*, *pszBackupLogFiles*, or *pcbSize* is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="79c72-129">**Ошибка \_ не \_ хватает \_ памяти**</span><span class="sxs-lookup"><span data-stu-id="79c72-129">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="79c72-130">Ошибка при выделении памяти.</span><span class="sxs-lookup"><span data-stu-id="79c72-130">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79c72-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79c72-131">Remarks</span></span>

<span data-ttu-id="79c72-132">Функция **дсбаккупжетбаккуплогс** предоставляет список файлов журналов, необходимых для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="79c72-132">The **DsBackupGetBackupLogs** function provides a list of the log files necessary for a backup.</span></span> <span data-ttu-id="79c72-133">Полная резервная копия состоит из файлов базы данных, предоставляемых функцией [**дсбаккупжетдатабасенамес**](dsbackupgetdatabasenames.md) и файлами журнала.</span><span class="sxs-lookup"><span data-stu-id="79c72-133">A full backup consists of the database files provided by the [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) function and the log files.</span></span> <span data-ttu-id="79c72-134">Добавочное резервное копирование Active Directory серверов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="79c72-134">Incremental backups of Active Directory servers are not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="79c72-135">Требования</span><span class="sxs-lookup"><span data-stu-id="79c72-135">Requirements</span></span>



| <span data-ttu-id="79c72-136">Требование</span><span class="sxs-lookup"><span data-stu-id="79c72-136">Requirement</span></span> | <span data-ttu-id="79c72-137">Значение</span><span class="sxs-lookup"><span data-stu-id="79c72-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79c72-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79c72-138">Minimum supported client</span></span><br/> | <span data-ttu-id="79c72-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79c72-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79c72-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79c72-140">Minimum supported server</span></span><br/> | <span data-ttu-id="79c72-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79c72-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79c72-142">Header</span><span class="sxs-lookup"><span data-stu-id="79c72-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="79c72-143"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="79c72-143"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="79c72-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="79c72-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="79c72-145"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79c72-145"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="79c72-146">DLL</span><span class="sxs-lookup"><span data-stu-id="79c72-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79c72-147"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79c72-147"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="79c72-148">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="79c72-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="79c72-149">**Дсбаккупжетбаккуплогсв** (Юникод) и **дсбаккупжетбаккуплогса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="79c72-149">**DsBackupGetBackupLogsW** (Unicode) and **DsBackupGetBackupLogsA** (ANSI)</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="79c72-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79c72-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79c72-151">**дсбаккупфри**</span><span class="sxs-lookup"><span data-stu-id="79c72-151">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="79c72-152">**дсбаккупжетдатабасенамес**</span><span class="sxs-lookup"><span data-stu-id="79c72-152">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
</dt> <dt>

[<span data-ttu-id="79c72-153">**Константы БФТ**</span><span class="sxs-lookup"><span data-stu-id="79c72-153">**BFT Constants**</span></span>](bft-constants.md)
</dt> <dt>

[<span data-ttu-id="79c72-154">Резервное копирование сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="79c72-154">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="79c72-155">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="79c72-155">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

