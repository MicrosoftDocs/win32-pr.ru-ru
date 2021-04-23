---
title: Функция Дсресторежетдатабаселокатионс (Нтдсбкли. h)
description: Получает расположения, в которые должны копироваться файлы резервных копий во время операции восстановления.
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсресторежетдатабаселокатионс
topic_type:
- apiref
api_name:
- DsRestoreGetDatabaseLocations
- DsRestoreGetDatabaseLocationsA
- DsRestoreGetDatabaseLocationsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bcebb9f3822332269e1db09f3246c128e4ad1f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892257"
---
# <a name="dsrestoregetdatabaselocations-function"></a><span data-ttu-id="f6c23-104">Функция Дсресторежетдатабаселокатионс</span><span class="sxs-lookup"><span data-stu-id="f6c23-104">DsRestoreGetDatabaseLocations function</span></span>

<span data-ttu-id="f6c23-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="f6c23-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f6c23-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="f6c23-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f6c23-107">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="f6c23-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="f6c23-108">Функция **дсресторежетдатабаселокатионс** получает расположения, в которые должны копироваться файлы резервных копий во время операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="f6c23-108">The **DsRestoreGetDatabaseLocations** function obtains the locations where backup files should be copied during a restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6c23-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6c23-109">Syntax</span></span>


```C++
HRESULT DsRestoreGetDatabaseLocations(
  _In_  HBC     hbc,
  _Out_ LPWSTR  *pszDatabaseLocationList,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="f6c23-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6c23-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6c23-111">*ХБК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6c23-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c23-112">Содержит описатель контекста восстановления, полученный с помощью функции [**дсресторепрепаре**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="f6c23-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f6c23-113">*псздатабаселокатионлист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f6c23-113">*pszDatabaseLocationList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c23-114">Указатель на строку, получающий список расположений базы данных в виде UNC-путей.</span><span class="sxs-lookup"><span data-stu-id="f6c23-114">Pointer to a string pointer that receives the list of database locations as UNC paths.</span></span> <span data-ttu-id="f6c23-115">Этот список получает список из одиночных строк, заканчивающихся нулем, заканчивающийся символом NULL.</span><span class="sxs-lookup"><span data-stu-id="f6c23-115">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="f6c23-116">Этот буфер выделяется функцией **дсресторежетдатабаселокатионс** и должен быть освобожден, если он больше не требуется путем вызова функции [**дсбаккупфри**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="f6c23-116">This buffer is allocated by the **DsRestoreGetDatabaseLocations** function and must be freed when it is no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="f6c23-117">Первый символ каждого из имен файлов содержит одну из [**констант БФТ**](bft-constants.md) , определяющих тип имени.</span><span class="sxs-lookup"><span data-stu-id="f6c23-117">The first character of each of the file names contains one of the [**BFT Constants**](bft-constants.md) that identifies the name type.</span></span> <span data-ttu-id="f6c23-118">Функция **дсресторежетдатабаселокатионс** предоставляет только следующие типы имен.</span><span class="sxs-lookup"><span data-stu-id="f6c23-118">The **DsRestoreGetDatabaseLocations** function only supplies the following name types.</span></span>

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span data-ttu-id="f6c23-119"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_ \_ база данных NTDS БФТ**</span><span class="sxs-lookup"><span data-stu-id="f6c23-119"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>


</dt> <dd>

<span data-ttu-id="f6c23-120">Файл базы данных NTDS должен быть скопирован в этот файл.</span><span class="sxs-lookup"><span data-stu-id="f6c23-120">The NTDS database file should be copied to this file.</span></span> <span data-ttu-id="f6c23-121">Это файл, который был определен как **\_ \_ база данных БФТ NTDS** при выполнении резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="f6c23-121">This is the file that was identified as **BFT\_NTDS\_DATABASE** when the backup was performed.</span></span>

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span data-ttu-id="f6c23-122"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**БФТ \_ log \_ dir**</span><span class="sxs-lookup"><span data-stu-id="f6c23-122"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT\_LOG\_DIR**</span></span>


</dt> <dd>

<span data-ttu-id="f6c23-123">Все файлы журнала копируются в этот каталог.</span><span class="sxs-lookup"><span data-stu-id="f6c23-123">All log files are copied to this directory.</span></span> <span data-ttu-id="f6c23-124">Файлы журнала были идентифицированы как **\_ Журнал БФТ** при выполнении резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="f6c23-124">The log files were identified as **BFT\_LOG** when the backup was performed.</span></span>

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span data-ttu-id="f6c23-125"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**\_dir Checkpoint \_ БФТ**</span><span class="sxs-lookup"><span data-stu-id="f6c23-125"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT\_CHECKPOINT\_DIR**</span></span>


</dt> <dd>

<span data-ttu-id="f6c23-126">Все файлы исправлений копируются в этот каталог.</span><span class="sxs-lookup"><span data-stu-id="f6c23-126">All patch files are copied to this directory.</span></span> <span data-ttu-id="f6c23-127">Файлы исправления были идентифицированы как **\_ \_ файл исправления БФТ** при выполнении резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="f6c23-127">The patch files were identified as **BFT\_PATCH\_FILE** when the backup was performed.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f6c23-128">*пкбсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f6c23-128">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c23-129">Указатель на значение **DWORD** , которое получает размер буфера *псздатабаселокатионлист* в байтах.</span><span class="sxs-lookup"><span data-stu-id="f6c23-129">Pointer to **DWORD** value that receives the size, in bytes, of the *pszDatabaseLocationList* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6c23-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6c23-130">Return value</span></span>

<span data-ttu-id="f6c23-131">Возвращает **значение \_ ОК** , если функция выполнена успешно, или код ошибки Win32 или RPC в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f6c23-131">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="f6c23-132">В следующем списке перечислены возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="f6c23-132">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="f6c23-133">**Ошибка \_ отказа в доступе \_**</span><span class="sxs-lookup"><span data-stu-id="f6c23-133">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="f6c23-134">Вызывающий объект не имеет необходимых прав доступа для вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="f6c23-134">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="f6c23-135">Функцию [**дссетаусидентити**](dssetauthidentity.md) можно использовать для задания учетных данных, используемых для функций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="f6c23-135">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="f6c23-136">**Ошибка \_ недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="f6c23-136">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="f6c23-137">недопустимые *ХБК*, *псздатабаселокатионлист* или *пкбсизе* .</span><span class="sxs-lookup"><span data-stu-id="f6c23-137">*hbc*, *pszDatabaseLocationList*, or *pcbSize* are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="f6c23-138">**Ошибка \_ не \_ хватает \_ памяти**</span><span class="sxs-lookup"><span data-stu-id="f6c23-138">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="f6c23-139">Ошибка при выделении памяти.</span><span class="sxs-lookup"><span data-stu-id="f6c23-139">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6c23-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6c23-140">Remarks</span></span>

<span data-ttu-id="f6c23-141">Функцию **дсресторежетдатабаселокатионс** можно использовать для получения каталогов восстановления без доступа к резервным данным.</span><span class="sxs-lookup"><span data-stu-id="f6c23-141">The **DsRestoreGetDatabaseLocations** function can be used to obtain the restoration directories without access to the backed up data.</span></span> <span data-ttu-id="f6c23-142">Для этого вызовите [**дсресторепрепаре**](dsrestoreprepare.md) с **нулевым значением** для параметра *пвекспиритокен* .</span><span class="sxs-lookup"><span data-stu-id="f6c23-142">To do this, call [**DsRestorePrepare**](dsrestoreprepare.md) with **NULL** for the *pvExpiryToken* parameter.</span></span> <span data-ttu-id="f6c23-143">Это приводит к тому, что **дсресторепрепаре** возвращает ограниченный контекст контекста, который может использоваться только с функцией **дсресторежетдатабаселокатионс** .</span><span class="sxs-lookup"><span data-stu-id="f6c23-143">This causes **DsRestorePrepare** to return a restricted context handle which can only be used with the **DsRestoreGetDatabaseLocations** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6c23-144">Требования</span><span class="sxs-lookup"><span data-stu-id="f6c23-144">Requirements</span></span>



| <span data-ttu-id="f6c23-145">Требование</span><span class="sxs-lookup"><span data-stu-id="f6c23-145">Requirement</span></span> | <span data-ttu-id="f6c23-146">Значение</span><span class="sxs-lookup"><span data-stu-id="f6c23-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c23-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6c23-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c23-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6c23-148">Windows Vista</span></span><br/>                                                                              |
| <span data-ttu-id="f6c23-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6c23-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c23-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6c23-150">Windows Server 2008</span></span><br/>                                                                        |
| <span data-ttu-id="f6c23-151">Header</span><span class="sxs-lookup"><span data-stu-id="f6c23-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6c23-152"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6c23-152"><dt>Ntdsbcli.h</dt></span></span> </dl>                 |
| <span data-ttu-id="f6c23-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f6c23-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="f6c23-154"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6c23-154"><dt>Ntdsbcli.lib</dt></span></span> </dl>               |
| <span data-ttu-id="f6c23-155">DLL</span><span class="sxs-lookup"><span data-stu-id="f6c23-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6c23-156"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6c23-156"><dt>Ntdsbcli.dll</dt></span></span> </dl>               |
| <span data-ttu-id="f6c23-157">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f6c23-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f6c23-158">**Дсресторежетдатабаселокатионсв** (Юникод) и **дсресторежетдатабаселокатионса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f6c23-158">**DsRestoreGetDatabaseLocationsW** (Unicode) and **DsRestoreGetDatabaseLocationsA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6c23-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6c23-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6c23-160">**дсресторепрепаре**</span><span class="sxs-lookup"><span data-stu-id="f6c23-160">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="f6c23-161">**дсбаккупфри**</span><span class="sxs-lookup"><span data-stu-id="f6c23-161">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="f6c23-162">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="f6c23-162">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="f6c23-163">Восстановление Active Directory</span><span class="sxs-lookup"><span data-stu-id="f6c23-163">Restoring Active Directory</span></span>](restoring-an-active-directory-server.md)
</dt> </dl>

 

