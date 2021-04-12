---
title: Функция Дсресторепрепаре (Нтдсбкли. h)
description: Подключается к указанному серверу каталогов и готовит его к операции восстановления.
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсресторепрепаре
topic_type:
- apiref
api_name:
- DsRestorePrepare
- DsRestorePrepareA
- DsRestorePrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb040a315b6cc94f2d296b032a954b00473a4ca2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135734"
---
# <a name="dsrestoreprepare-function"></a><span data-ttu-id="f7b7b-104">Функция Дсресторепрепаре</span><span class="sxs-lookup"><span data-stu-id="f7b7b-104">DsRestorePrepare function</span></span>

<span data-ttu-id="f7b7b-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f7b7b-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f7b7b-107">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="f7b7b-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="f7b7b-108">Функция **дсресторепрепаре** подключается к указанному серверу каталогов и подготавливает ее для операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-108">The **DsRestorePrepare** function connects to the specified directory server and prepares it for the restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b7b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7b7b-109">Syntax</span></span>


```C++
HRESULT DsRestorePrepare(
  _In_  LPCWSTR szServerName,
  _In_  ULONG   rtFlag,
  _In_  PVOID   pvExpiryToken,
  _In_  DWORD   cbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a><span data-ttu-id="f7b7b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7b7b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7b7b-111">*сзсервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7b7b-111">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b7b-112">Указатель на строку, завершающуюся нулем, которая содержит имя восстанавливаемого сервера.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-112">Pointer to a null-terminated string that contains the name of the server to restore.</span></span> <span data-ttu-id="f7b7b-113">Предыдущие обратные косые черты необязательны.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="f7b7b-114">Сервер должен быть тем же компьютером, из которого вызывается эта функция.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="f7b7b-115">Имя сервера не может содержать символы подчеркивания ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="f7b7b-115">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="f7b7b-116">Пример имени сервера — \\ \\ Server1.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="f7b7b-117">*ртфлаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7b7b-117">*rtFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b7b-118">Указывает тип выполняемого восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-118">Specifies the type of restoration to perform.</span></span> <span data-ttu-id="f7b7b-119">Это может быть ноль или одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-119">This can be zero or one of the following values.</span></span>

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span data-ttu-id="f7b7b-120"><span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**\_CATCHUP типа \_ восстановления**</span><span class="sxs-lookup"><span data-stu-id="f7b7b-120"><span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**RESTORE\_TYPE\_CATCHUP**</span></span>


</dt> <dd>

<span data-ttu-id="f7b7b-121">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-121">Default.</span></span> <span data-ttu-id="f7b7b-122">Восстановленная версия выверена с помощью стандартной логики сверки, поэтому восстановленный DIT может синхронизироваться с другими компьютерами Enterprise Server.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-122">The restored version is reconciled through the standard reconciliation logic so that the restored DIT can synchronize with other enterprise server computers.</span></span>

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span data-ttu-id="f7b7b-123"><span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**\_аусоратативе типа \_ восстановления**</span><span class="sxs-lookup"><span data-stu-id="f7b7b-123"><span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**RESTORE\_TYPE\_AUTHORATATIVE**</span></span>


</dt> <dd>

<span data-ttu-id="f7b7b-124">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-124">Not Supported.</span></span>

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span data-ttu-id="f7b7b-125"><span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**тип восстановления в \_ \_ сети**</span><span class="sxs-lookup"><span data-stu-id="f7b7b-125"><span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**RESTORE\_TYPE\_ONLINE**</span></span>


</dt> <dd>

<span data-ttu-id="f7b7b-126">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-126">Not Supported.</span></span> <span data-ttu-id="f7b7b-127">Восстановление выполняется, когда NTDS находится в сети.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-127">Restoration is performed when NTDS is online.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f7b7b-128">*пвекспиритокен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7b7b-128">*pvExpiryToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b7b-129">Указатель на маркер срока действия, связанный с восстанавливаемой резервной копией.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-129">Pointer to the expiry token associated with the backup being restored.</span></span> <span data-ttu-id="f7b7b-130">Этот маркер был получен из функции [**дсбаккуппрепаре**](dsbackupprepare.md) при резервном копировании каталога.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-130">This token was obtained from the [**DsBackupPrepare**](dsbackupprepare.md) function when the directory was backed up.</span></span>

<span data-ttu-id="f7b7b-131">Если этот параметр имеет **значение NULL**, то маркер, возвращаемый в *ФБК* , можно использовать только для получения каталогов восстановления с помощью функции [**дсресторежетдатабаселокатионс**](dsrestoregetdatabaselocations.md) .</span><span class="sxs-lookup"><span data-stu-id="f7b7b-131">If this parameter is **NULL**, the handle returned in *phbc* can only be used to obtain the restoration directories with the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function.</span></span> <span data-ttu-id="f7b7b-132">Этот обработчик нельзя использовать для других функций восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-132">The handle cannot be used for any other restoration functions.</span></span>

</dd> <dt>

<span data-ttu-id="f7b7b-133">*кбекспиритокенсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7b7b-133">*cbExpiryTokenSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b7b-134">Содержит размер (в байтах) токена срока действия в *пвекспиритокен*.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-134">Contains the size, in bytes, of the expiry token in *pvExpiryToken*.</span></span>

</dd> <dt>

<span data-ttu-id="f7b7b-135">*ФБК* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f7b7b-135">*phbc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b7b-136">Указатель на значение **ХБК** , которое получает маркер для восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-136">Pointer to an **HBC** value that receives the handle for the restore.</span></span> <span data-ttu-id="f7b7b-137">Этот маркер используется при вызове других функций восстановления службы каталогов, таких как [**дсбаккупопенфиле**](dsbackupopenfile.md) и [**дсресторинд**](dsrestoreend.md).</span><span class="sxs-lookup"><span data-stu-id="f7b7b-137">This handle is used when calling other Directory Service restore functions, such as [**DsBackupOpenFile**](dsbackupopenfile.md) and [**DsRestoreEnd**](dsrestoreend.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7b7b-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7b7b-138">Return value</span></span>

<span data-ttu-id="f7b7b-139">В случае успеха возвращает стандартные коды **HRESULT** ; в противном случае возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-139">If successful, returns a standard **HRESULT** codes; otherwise, a failure code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b7b-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7b7b-140">Remarks</span></span>

<span data-ttu-id="f7b7b-141">Функция **дсресторепрепаре** требует, чтобы вызывающая сторона была членом группы администраторов на сервере.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-141">The **DsRestorePrepare** function requires that the caller is a member of the Administrators group on the server.</span></span>

<span data-ttu-id="f7b7b-142">**Дсресторепрепаре** можно использовать с указанным токеном или без него.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-142">**DsRestorePrepare** may be used with or without a token provided.</span></span> <span data-ttu-id="f7b7b-143">Если указан маркер, он проверяется на срок действия, и все операции разрешаются в возвращаемом контексте.</span><span class="sxs-lookup"><span data-stu-id="f7b7b-143">If the token is provided, it is checked for expiration, and all operations are allowed on the context returned.</span></span> <span data-ttu-id="f7b7b-144">Если токен не указан, возвращаемый контекст ограничен и может использоваться только для функции [**дсресторежетдатабаселокатионс**](dsrestoregetdatabaselocations.md) .</span><span class="sxs-lookup"><span data-stu-id="f7b7b-144">If the token is not provided, the context returned is restricted, and may be used only for the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function.</span></span> <span data-ttu-id="f7b7b-145">Он не может использоваться для функции [**дсресторерегистер**](dsrestoreregister.md) .</span><span class="sxs-lookup"><span data-stu-id="f7b7b-145">It may not be used for the [**DsRestoreRegister**](dsrestoreregister.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b7b-146">Требования</span><span class="sxs-lookup"><span data-stu-id="f7b7b-146">Requirements</span></span>



| <span data-ttu-id="f7b7b-147">Требование</span><span class="sxs-lookup"><span data-stu-id="f7b7b-147">Requirement</span></span> | <span data-ttu-id="f7b7b-148">Значение</span><span class="sxs-lookup"><span data-stu-id="f7b7b-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b7b-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7b7b-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b7b-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7b7b-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f7b7b-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7b7b-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b7b-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7b7b-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f7b7b-153">Header</span><span class="sxs-lookup"><span data-stu-id="f7b7b-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7b7b-154"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7b7b-154"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7b7b-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f7b7b-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="f7b7b-156"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7b7b-156"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="f7b7b-157">DLL</span><span class="sxs-lookup"><span data-stu-id="f7b7b-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7b7b-158"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7b7b-158"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="f7b7b-159">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f7b7b-159">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f7b7b-160">**Дсресторепрепарев** (Юникод) и **дсресторепрепареа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f7b7b-160">**DsRestorePrepareW** (Unicode) and **DsRestorePrepareA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f7b7b-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7b7b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b7b-162">Восстановление сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="f7b7b-162">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="f7b7b-163">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="f7b7b-163">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="f7b7b-164">**дсресторежетдатабаселокатионс**</span><span class="sxs-lookup"><span data-stu-id="f7b7b-164">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="f7b7b-165">**дсресторерегистер**</span><span class="sxs-lookup"><span data-stu-id="f7b7b-165">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="f7b7b-166">**дсресторерегистеркомплете**</span><span class="sxs-lookup"><span data-stu-id="f7b7b-166">**DsRestoreRegisterComplete**</span></span>](dsrestoreregistercomplete.md)
</dt> <dt>

[<span data-ttu-id="f7b7b-167">**дсресторинд**</span><span class="sxs-lookup"><span data-stu-id="f7b7b-167">**DsRestoreEnd**</span></span>](dsrestoreend.md)
</dt> </dl>

 

