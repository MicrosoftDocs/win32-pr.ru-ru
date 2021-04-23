---
title: Функция Дсресторерегистер (Нтдсбкли. h)
description: Регистрирует операцию восстановления.
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсресторерегистер
topic_type:
- apiref
api_name:
- DsRestoreRegister
- DsRestoreRegisterA
- DsRestoreRegisterW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 610d49c73ade9bab47c95e90af73bac606f4bd23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071743"
---
# <a name="dsrestoreregister-function"></a><span data-ttu-id="19c7d-104">Функция Дсресторерегистер</span><span class="sxs-lookup"><span data-stu-id="19c7d-104">DsRestoreRegister function</span></span>

<span data-ttu-id="19c7d-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="19c7d-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="19c7d-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="19c7d-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="19c7d-107">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="19c7d-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="19c7d-108">Функция **дсресторерегистер** регистрирует операцию восстановления. Эта функция блокирует все последующие операции восстановления и предотвращает запуск целевого объекта восстановления до тех пор, пока не будет вызвана функция [**дсресторерегистеркомплете**](dsrestoreregistercomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="19c7d-108">The **DsRestoreRegister** function registers a restore operation.This function interlocks all subsequent restore operations and prevents the restore target from starting until the [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) function is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="19c7d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19c7d-109">Syntax</span></span>


```C++
HRESULT DsRestoreRegister(
  _In_ HBC        hbc,
  _In_ LPCTSTR    szCheckPointFilePath,
  _In_ LPCTSTR    szLogPath,
  _In_ EDB_RSTMAP rgrstmap[],
  _In_ LONG       crstmap,
  _In_ LPCTSTR    szBackupLogPath,
  _In_ ULONG      genLow,
  _In_ ULONG      genHigh
);
```



## <a name="parameters"></a><span data-ttu-id="19c7d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="19c7d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19c7d-111">*ХБК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19c7d-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c7d-112">Содержит описатель контекста восстановления, полученный с помощью функции [**дсресторепрепаре**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="19c7d-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="19c7d-113">*сзчеккпоинтфилепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19c7d-113">*szCheckPointFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c7d-114">Указатель на строку, завершающуюся нулем, которая содержит путь к файлу контрольных точек.</span><span class="sxs-lookup"><span data-stu-id="19c7d-114">Pointer to a null-terminated string that contains the path to the checkpoint file.</span></span> <span data-ttu-id="19c7d-115">Этот путь предоставляется функцией [**дсресторежетдатабаселокатионс**](dsrestoregetdatabaselocations.md) и имеет значение **БФТ** в **БФТ \_ Checkpoint \_ dir**.</span><span class="sxs-lookup"><span data-stu-id="19c7d-115">This path is provided by the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function and has a **BFT** value of **BFT\_CHECKPOINT\_DIR**.</span></span> <span data-ttu-id="19c7d-116">Обычно это то же самое, что и путь к системной базе данных.</span><span class="sxs-lookup"><span data-stu-id="19c7d-116">Typically this is the same as the system database path.</span></span> <span data-ttu-id="19c7d-117">Этот путь необходим для правильной функции Backup Restore.</span><span class="sxs-lookup"><span data-stu-id="19c7d-117">This path is required for proper backup restore function.</span></span> <span data-ttu-id="19c7d-118">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="19c7d-118">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="19c7d-119">Передача **значения NULL** в этом параметре приведет к ошибке в процессе восстановления.</span><span class="sxs-lookup"><span data-stu-id="19c7d-119">Passing **NULL** in this parameter will cause an error during the restore process.</span></span>

</dd> <dt>

<span data-ttu-id="19c7d-120">*сзлогпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19c7d-120">*szLogPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c7d-121">Указатель на строку, завершающуюся нулем, которая содержит путь, по которому будут восстановлены файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="19c7d-121">Pointer to a null-terminated string that contains the path where the log files will be restored.</span></span> <span data-ttu-id="19c7d-122">Этот путь предоставляется функцией [**дсресторежетдатабаселокатионс**](dsrestoregetdatabaselocations.md) и имеет значение **БФТ** в **БФТ \_ log \_ dir**.</span><span class="sxs-lookup"><span data-stu-id="19c7d-122">This path is provided by the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function and has a **BFT** value of **BFT\_LOG\_DIR**.</span></span> <span data-ttu-id="19c7d-123">Если путь указывает на пустой каталог, в нем создаются новые файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="19c7d-123">If the path points to an empty directory, new log files are created there.</span></span> <span data-ttu-id="19c7d-124">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="19c7d-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19c7d-125">*ргрстмап* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19c7d-125">*rgrstmap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c7d-126">Массив структур [**EDB \_ рстмап**](edb-rstmap.md) , который содержит старый и новый пути для каждой базы данных.</span><span class="sxs-lookup"><span data-stu-id="19c7d-126">An array of [**EDB\_RSTMAP**](edb-rstmap.md) structures that contains the old and new paths for each database.</span></span> <span data-ttu-id="19c7d-127">Для каждой базы данных существует одна структура.</span><span class="sxs-lookup"><span data-stu-id="19c7d-127">There is one structure for each database.</span></span> <span data-ttu-id="19c7d-128">Для каталога существует структура системной базы данных и другая структура для базы данных каталога.</span><span class="sxs-lookup"><span data-stu-id="19c7d-128">For the directory, there is a structure for the system database and another structure for the directory database.</span></span> <span data-ttu-id="19c7d-129">Порядок элементов в массиве не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="19c7d-129">The order of the elements in the array does not matter.</span></span> <span data-ttu-id="19c7d-130">Параметр *крстмап* содержит количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="19c7d-130">The *crstmap* parameter contains the number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="19c7d-131">*крстмап* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19c7d-131">*crstmap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c7d-132">Содержит количество элементов в массиве *ргрстмап* .</span><span class="sxs-lookup"><span data-stu-id="19c7d-132">Contains the number of elements in the *rgrstmap* array.</span></span>

</dd> <dt>

<span data-ttu-id="19c7d-133">*сзбаккуплогпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19c7d-133">*szBackupLogPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c7d-134">Указатель на строку, завершающуюся нулем, которая содержит путь, по которому в данный момент хранятся резервные копии файлов журналов.</span><span class="sxs-lookup"><span data-stu-id="19c7d-134">Pointer to a null-terminated string that contains the path where the backed up log files currently reside.</span></span> <span data-ttu-id="19c7d-135">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="19c7d-135">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19c7d-136">*женлов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19c7d-136">*genLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c7d-137">Содержит минимальный номер журнала для восстановления в этом сеансе восстановления.</span><span class="sxs-lookup"><span data-stu-id="19c7d-137">Contains the lowest log number to restore in this restore session.</span></span> <span data-ttu-id="19c7d-138">Это шестнадцатеричное число в диапазоне от 0x00000 до 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="19c7d-138">This is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="19c7d-139">*женхигх* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19c7d-139">*genHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19c7d-140">Содержит максимальный номер журнала для восстановления в этом сеансе восстановления.</span><span class="sxs-lookup"><span data-stu-id="19c7d-140">Contains the highest log number to restore in this restore session.</span></span> <span data-ttu-id="19c7d-141">Это шестнадцатеричное число в диапазоне от 0x00000 до 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="19c7d-141">This is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19c7d-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19c7d-142">Return value</span></span>

<span data-ttu-id="19c7d-143">Возвращает **значение \_ ОК** , если функция выполнена успешно, или код ошибки Win32 или RPC в противном случае.</span><span class="sxs-lookup"><span data-stu-id="19c7d-143">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="19c7d-144">В следующем списке перечислены возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="19c7d-144">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="19c7d-145">**Ошибка \_ отказа в доступе \_**</span><span class="sxs-lookup"><span data-stu-id="19c7d-145">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="19c7d-146">Вызывающий объект не имеет необходимых прав доступа для вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="19c7d-146">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="19c7d-147">Функцию [**дссетаусидентити**](dssetauthidentity.md) можно использовать для задания учетных данных, используемых для функций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="19c7d-147">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="19c7d-148">**Ошибка \_ недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="19c7d-148">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="19c7d-149">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="19c7d-149">One or more parameters are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="19c7d-150">**хрмиссинжекспиритокен**</span><span class="sxs-lookup"><span data-stu-id="19c7d-150">**hrMissingExpiryToken**</span></span>
</dt> <dd>

<span data-ttu-id="19c7d-151">Недопустимый токен срока действия, переданный в [**дсресторепрепаре**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="19c7d-151">The expiry token supplied to [**DsRestorePrepare**](dsrestoreprepare.md) was invalid.</span></span> <span data-ttu-id="19c7d-152">Это значение определено в Нтдсбмсг. h.</span><span class="sxs-lookup"><span data-stu-id="19c7d-152">This value is defined in Ntdsbmsg.h.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19c7d-153">Требования</span><span class="sxs-lookup"><span data-stu-id="19c7d-153">Requirements</span></span>



| <span data-ttu-id="19c7d-154">Требование</span><span class="sxs-lookup"><span data-stu-id="19c7d-154">Requirement</span></span> | <span data-ttu-id="19c7d-155">Значение</span><span class="sxs-lookup"><span data-stu-id="19c7d-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19c7d-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19c7d-156">Minimum supported client</span></span><br/> | <span data-ttu-id="19c7d-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19c7d-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19c7d-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19c7d-158">Minimum supported server</span></span><br/> | <span data-ttu-id="19c7d-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19c7d-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19c7d-160">Header</span><span class="sxs-lookup"><span data-stu-id="19c7d-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="19c7d-161"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="19c7d-161"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="19c7d-162">Библиотека</span><span class="sxs-lookup"><span data-stu-id="19c7d-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="19c7d-163"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19c7d-163"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="19c7d-164">DLL</span><span class="sxs-lookup"><span data-stu-id="19c7d-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19c7d-165"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19c7d-165"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="19c7d-166">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="19c7d-166">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="19c7d-167">**Дсресторерегистерв** (Юникод) и **дсресторерегистера** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="19c7d-167">**DsRestoreRegisterW** (Unicode) and **DsRestoreRegisterA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="19c7d-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19c7d-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19c7d-169">**дсресторерегистеркомплете**</span><span class="sxs-lookup"><span data-stu-id="19c7d-169">**DsRestoreRegisterComplete**</span></span>](dsrestoreregistercomplete.md)
</dt> <dt>

[<span data-ttu-id="19c7d-170">**дсресторепрепаре**</span><span class="sxs-lookup"><span data-stu-id="19c7d-170">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="19c7d-171">**дсресторежетдатабаселокатионс**</span><span class="sxs-lookup"><span data-stu-id="19c7d-171">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="19c7d-172">**дсресторинд**</span><span class="sxs-lookup"><span data-stu-id="19c7d-172">**DsRestoreEnd**</span></span>](dsrestoreend.md)
</dt> <dt>

[<span data-ttu-id="19c7d-173">**\_РСТМАП EDB**</span><span class="sxs-lookup"><span data-stu-id="19c7d-173">**EDB\_RSTMAP**</span></span>](edb-rstmap.md)
</dt> <dt>

[<span data-ttu-id="19c7d-174">Восстановление Active Directory</span><span class="sxs-lookup"><span data-stu-id="19c7d-174">Restoring Active Directory</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="19c7d-175">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="19c7d-175">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

