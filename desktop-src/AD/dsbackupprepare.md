---
title: Функция Дсбаккуппрепаре (Нтдсбкли. h)
description: Подготавливает каталог на указанном сервере для оперативной архивации и возвращает описатель контекста резервного копирования, используемый при последующих вызовах других функций резервного копирования.
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсбаккуппрепаре
topic_type:
- apiref
api_name:
- DsBackupPrepare
- DsBackupPrepareA
- DsBackupPrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa561a7e41164ece68fb18fd882a8b05d6357cec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491025"
---
# <a name="dsbackupprepare-function"></a><span data-ttu-id="719b3-104">Функция Дсбаккуппрепаре</span><span class="sxs-lookup"><span data-stu-id="719b3-104">DsBackupPrepare function</span></span>

<span data-ttu-id="719b3-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="719b3-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="719b3-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="719b3-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="719b3-107">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="719b3-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="719b3-108">Функция **дсбаккуппрепаре** подготавливает каталог на указанном сервере для оперативной архивации и возвращает описатель контекста резервного копирования, используемый в последующих вызовах других функций резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="719b3-108">The **DsBackupPrepare** function prepares the directory on the specified server for the online backup and returns a backup context handle used in subsequent calls to other backup functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="719b3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="719b3-109">Syntax</span></span>


```C++
HRESULT DsBackupPrepare(
  _In_  LPCTSTR szBackupServer,
  _In_  ULONG   grbit,
  _In_  ULONG   btBackupType,
  _Out_ PVOID   *ppvExpiryToken,
  _Out_ LPDWORD pcbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a><span data-ttu-id="719b3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="719b3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="719b3-111">*сзбаккупсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="719b3-111">*szBackupServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="719b3-112">Указатель на строку, завершающуюся нулем, которая содержит имя сервера для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="719b3-112">Pointer to a null-terminated string that contains the name of the server to backup.</span></span> <span data-ttu-id="719b3-113">Предыдущие обратные косые черты необязательны.</span><span class="sxs-lookup"><span data-stu-id="719b3-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="719b3-114">Сервер должен быть тем же компьютером, из которого вызывается эта функция.</span><span class="sxs-lookup"><span data-stu-id="719b3-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="719b3-115">Имя сервера не может содержать символ подчеркивания ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="719b3-115">The server name cannot contain an underscore (\_) character.</span></span> <span data-ttu-id="719b3-116">Пример имени сервера — \\ \\ Server1.</span><span class="sxs-lookup"><span data-stu-id="719b3-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="719b3-117">*грбит* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="719b3-117">*grbit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="719b3-118">Определяет, будут ли создаваться резервные копии файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="719b3-118">Determines if the log files will be backed up.</span></span> <span data-ttu-id="719b3-119">Это значение всегда должно быть равно 0, так как добавочные резервные копии не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="719b3-119">This value should always be 0 because incremental backups are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="719b3-120">*бтбаккуптипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="719b3-120">*btBackupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="719b3-121">Указывает тип резервной копии.</span><span class="sxs-lookup"><span data-stu-id="719b3-121">Specifies the type of backup.</span></span> <span data-ttu-id="719b3-122">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="719b3-122">This can be one of the following values.</span></span>

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span data-ttu-id="719b3-123"><span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**Тип РЕЗЕРВной копии \_ \_ полон**</span><span class="sxs-lookup"><span data-stu-id="719b3-123"><span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**BACKUP\_TYPE\_FULL**</span></span>


</dt> <dd>

<span data-ttu-id="719b3-124">Указывает полное резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="719b3-124">Specifies a full backup.</span></span> <span data-ttu-id="719b3-125">Выполняется резервное копирование всего каталога (DIT, файлов журнала и файлов обновления).</span><span class="sxs-lookup"><span data-stu-id="719b3-125">The complete directory (DIT, log files, and update files) are backed up.</span></span> <span data-ttu-id="719b3-126">Все данные архивируются, а файлы журнала транзакций усекаются.</span><span class="sxs-lookup"><span data-stu-id="719b3-126">All data is backed up and transaction log files are truncated.</span></span> <span data-ttu-id="719b3-127">Поддерживаются только полные резервные копии.</span><span class="sxs-lookup"><span data-stu-id="719b3-127">Only full backups are supported.</span></span>

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span data-ttu-id="719b3-128"><span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**\_ \_ только журналы типа резервного копирования \_**</span><span class="sxs-lookup"><span data-stu-id="719b3-128"><span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**BACKUP\_TYPE\_LOGS\_ONLY**</span></span>


</dt> <dd>

<span data-ttu-id="719b3-129">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="719b3-129">This value is not supported.</span></span> <span data-ttu-id="719b3-130">Указывает, что будет создана резервная копия только журналов базы данных, а не самой базы данных.</span><span class="sxs-lookup"><span data-stu-id="719b3-130">Specifies that only the database logs, and not the database itself, will be backed up.</span></span> <span data-ttu-id="719b3-131">Обычно это используется при выполнении разностного или добавочного резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="719b3-131">This is normally used when performing a differential or incremental backup.</span></span>

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span data-ttu-id="719b3-132"><span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**\_добавочный тип резервного копирования \_**</span><span class="sxs-lookup"><span data-stu-id="719b3-132"><span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**BACKUP\_TYPE\_INCREMENTAL**</span></span>


</dt> <dd>

<span data-ttu-id="719b3-133">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="719b3-133">This value is not supported.</span></span> <span data-ttu-id="719b3-134">**Дсбаккуппрепаре** возвращает **ошибку " \_ Недопустимый \_ параметр**".</span><span class="sxs-lookup"><span data-stu-id="719b3-134">**DsBackupPrepare** returns **ERROR\_INVALID\_PARAMETER**.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="719b3-135">*ппвекспиритокен* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="719b3-135">*ppvExpiryToken* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="719b3-136">Указатель на значение **PVOID** , которое получает указатель на маркер окончания срока действия, связанный с этой резервной копией.</span><span class="sxs-lookup"><span data-stu-id="719b3-136">Pointer to a **PVOID** value that receives a pointer to an expiry token associated with this backup.</span></span> <span data-ttu-id="719b3-137">*пкбекспиритокенсизе* получает размер этих данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="719b3-137">*pcbExpiryTokenSize* receives the size, in bytes, of this data.</span></span> <span data-ttu-id="719b3-138">Вызывающий объект должен сохранить содержимое этого маркера с резервной копией, так как при попытке восстановить данные маркер должен быть передан в [**дсресторепрепаре**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="719b3-138">The caller must save the contents of this token with the backup because the token must be passed to [**DsRestorePrepare**](dsrestoreprepare.md) when attempting to restore data.</span></span> <span data-ttu-id="719b3-139">После того как токен сохранен и больше не требуется, вызывающий объект должен освободить выделенную память с помощью [**дсбаккупфри**](dsbackupfree.md).</span><span class="sxs-lookup"><span data-stu-id="719b3-139">After the token has been stored and is no longer required, the caller should free the allocated memory using [**DsBackupFree**](dsbackupfree.md).</span></span>

</dd> <dt>

<span data-ttu-id="719b3-140">*пкбекспиритокенсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="719b3-140">*pcbExpiryTokenSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="719b3-141">Указатель на значение **DWORD** , которое получает размер маркера (в байтах) в *ппвекспиритокен*.</span><span class="sxs-lookup"><span data-stu-id="719b3-141">Pointer to a **DWORD** value that receives the size, in bytes, of the token in *ppvExpiryToken*.</span></span>

</dd> <dt>

<span data-ttu-id="719b3-142">*ФБК* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="719b3-142">*phbc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="719b3-143">Указатель на значение **ХБК** , которое получает маркер для резервной копии.</span><span class="sxs-lookup"><span data-stu-id="719b3-143">Pointer to an **HBC** value that receives the handle for the backup.</span></span> <span data-ttu-id="719b3-144">Этот маркер используется при вызове других функций резервного копирования службы каталогов, таких как [**дсбаккупопенфиле**](dsbackupopenfile.md) и [**дсбаккупенд**](dsbackupend.md).</span><span class="sxs-lookup"><span data-stu-id="719b3-144">This handle is used when calling other Directory Service backup functions, such as [**DsBackupOpenFile**](dsbackupopenfile.md) and [**DsBackupEnd**](dsbackupend.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="719b3-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="719b3-145">Return value</span></span>

<span data-ttu-id="719b3-146">Возвращает **значение \_ ОК** , если функция выполнена успешно, или в противном случае — код ошибки.</span><span class="sxs-lookup"><span data-stu-id="719b3-146">Returns **S\_OK** if the function is successful or an error code otherwise.</span></span> <span data-ttu-id="719b3-147">В следующем списке перечислены другие возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="719b3-147">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="719b3-148">**Ошибка \_ отказа в доступе \_**</span><span class="sxs-lookup"><span data-stu-id="719b3-148">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="719b3-149">Вызывающий объект не имеет необходимых прав доступа для вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="719b3-149">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="719b3-150">Функцию [**дссетаусидентити**](dssetauthidentity.md) можно использовать для задания учетных данных, используемых для функций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="719b3-150">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="719b3-151">**Ошибка \_ недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="719b3-151">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="719b3-152">недопустимые *сзбаккупсервер* или *фбкбаккупконтекст* .</span><span class="sxs-lookup"><span data-stu-id="719b3-152">*szBackupServer* or *phbcBackupContext* are not valid.</span></span>

</dd> <dt>

<span data-ttu-id="719b3-153">**Ошибка \_ не \_ хватает \_ памяти**</span><span class="sxs-lookup"><span data-stu-id="719b3-153">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="719b3-154">Ошибка при выделении памяти.</span><span class="sxs-lookup"><span data-stu-id="719b3-154">A memory allocation failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="719b3-155">**хркаулднотконнект**</span><span class="sxs-lookup"><span data-stu-id="719b3-155">**hrCouldNotConnect**</span></span>
</dt> <dd>

<span data-ttu-id="719b3-156">Не удалось найти сервер в *сзбаккупсервер* , не является контроллером домена, или *сзбаккупсервер* имеет неправильный формат.</span><span class="sxs-lookup"><span data-stu-id="719b3-156">The server in *szBackupServer* could not be found, is not a domain controller or *szBackupServer* is not formatted correctly.</span></span> <span data-ttu-id="719b3-157">Это значение определено в нтдсбмсг. h.</span><span class="sxs-lookup"><span data-stu-id="719b3-157">This value is defined in ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="719b3-158">**хринвалидпарам**</span><span class="sxs-lookup"><span data-stu-id="719b3-158">**hrInvalidParam**</span></span>
</dt> <dd>

<span data-ttu-id="719b3-159">*ппвекспиритокен* и (или) *пкбекспиритокенсизе* являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="719b3-159">*ppvExpiryToken* and/or *pcbExpiryTokenSize* are invalid.</span></span> <span data-ttu-id="719b3-160">Это значение определено в Нтдсбмсг. h.</span><span class="sxs-lookup"><span data-stu-id="719b3-160">This value is defined in Ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="719b3-161">**\_ \_ Недопустимая привязка RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="719b3-161">**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd>

<span data-ttu-id="719b3-162">Функция вызывается удаленно, или сервер в *сзсервернаме* не является контроллером домена.</span><span class="sxs-lookup"><span data-stu-id="719b3-162">The function is called remotely or the server in *szServerName* is not a domain controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="719b3-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="719b3-163">Remarks</span></span>

<span data-ttu-id="719b3-164">Эта функция требует наличия у вызывающего пользователя привилегий **SE \_ BACKUP \_ Name** .</span><span class="sxs-lookup"><span data-stu-id="719b3-164">This function requires that the caller has the **SE\_BACKUP\_NAME** privilege.</span></span> <span data-ttu-id="719b3-165">Функцию [**дссетаусидентити**](dssetauthidentity.md) можно использовать для изменения контекста безопасности, в котором вызывается эта функция.</span><span class="sxs-lookup"><span data-stu-id="719b3-165">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to change the security context under which this function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="719b3-166">Требования</span><span class="sxs-lookup"><span data-stu-id="719b3-166">Requirements</span></span>



| <span data-ttu-id="719b3-167">Требование</span><span class="sxs-lookup"><span data-stu-id="719b3-167">Requirement</span></span> | <span data-ttu-id="719b3-168">Значение</span><span class="sxs-lookup"><span data-stu-id="719b3-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="719b3-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="719b3-169">Minimum supported client</span></span><br/> | <span data-ttu-id="719b3-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="719b3-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="719b3-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="719b3-171">Minimum supported server</span></span><br/> | <span data-ttu-id="719b3-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="719b3-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="719b3-173">Header</span><span class="sxs-lookup"><span data-stu-id="719b3-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="719b3-174"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="719b3-174"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="719b3-175">Библиотека</span><span class="sxs-lookup"><span data-stu-id="719b3-175">Library</span></span><br/>                  | <dl> <span data-ttu-id="719b3-176"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="719b3-176"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="719b3-177">DLL</span><span class="sxs-lookup"><span data-stu-id="719b3-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="719b3-178"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="719b3-178"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="719b3-179">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="719b3-179">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="719b3-180">**Дсбаккуппрепарев** (Юникод) и **дсбаккуппрепареа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="719b3-180">**DsBackupPrepareW** (Unicode) and **DsBackupPrepareA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="719b3-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="719b3-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="719b3-182">**дсресторепрепаре**</span><span class="sxs-lookup"><span data-stu-id="719b3-182">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="719b3-183">**дсбаккупфри**</span><span class="sxs-lookup"><span data-stu-id="719b3-183">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="719b3-184">**дсбаккупопенфиле**</span><span class="sxs-lookup"><span data-stu-id="719b3-184">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="719b3-185">**дсбаккупенд**</span><span class="sxs-lookup"><span data-stu-id="719b3-185">**DsBackupEnd**</span></span>](dsbackupend.md)
</dt> <dt>

[<span data-ttu-id="719b3-186">**дссетаусидентити**</span><span class="sxs-lookup"><span data-stu-id="719b3-186">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="719b3-187">Резервное копирование сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="719b3-187">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="719b3-188">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="719b3-188">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

