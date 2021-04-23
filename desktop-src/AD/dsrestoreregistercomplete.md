---
title: Функция Дсресторерегистеркомплете (Нтдсбкли. h)
description: Вызывается для разблокировки сервера Active Directory после завершения операции восстановления.
ms.assetid: 781cd2ec-d2e2-4f3a-903d-feda4b871de5
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсресторерегистеркомплете
topic_type:
- apiref
api_name:
- DsRestoreRegisterComplete
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5e5e01b29281860dff59fbcd08a3b48ec66c4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071742"
---
# <a name="dsrestoreregistercomplete-function"></a><span data-ttu-id="f72e4-104">Функция Дсресторерегистеркомплете</span><span class="sxs-lookup"><span data-stu-id="f72e4-104">DsRestoreRegisterComplete function</span></span>

<span data-ttu-id="f72e4-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="f72e4-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f72e4-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="f72e4-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f72e4-107">Вместо этого используйте [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="f72e4-107">Use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="f72e4-108">Функция **дсресторерегистеркомплете** вызывается для разблокировки сервера Active Directory после завершения операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="f72e4-108">The **DsRestoreRegisterComplete** function is called to unlock an Active Directory server after a restore operation is complete.</span></span> <span data-ttu-id="f72e4-109">Эта функция является аналогом функции [**дсресторерегистер**](dsrestoreregister.md) .</span><span class="sxs-lookup"><span data-stu-id="f72e4-109">This function is counterpart to the [**DsRestoreRegister**](dsrestoreregister.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f72e4-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f72e4-110">Syntax</span></span>


```C++
HRESULT DsRestoreRegisterComplete(
  _In_ HBC     hbc,
  _In_ HRESULT hrRestoreState
);
```



## <a name="parameters"></a><span data-ttu-id="f72e4-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f72e4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f72e4-112">*ХБК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f72e4-112">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f72e4-113">Содержит описатель контекста восстановления, полученный с помощью функции [**дсресторепрепаре**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="f72e4-113">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f72e4-114">*хрресторестате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f72e4-114">*hrRestoreState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f72e4-115">Содержит конечное состояние операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="f72e4-115">Contains the final status of the restore operation.</span></span> <span data-ttu-id="f72e4-116">Этот параметр должен содержать **S \_ ОК** , если операция восстановления прошла успешно, или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f72e4-116">This parameter should contain **S\_OK** if the restore operation was successful or an error code otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f72e4-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f72e4-117">Return value</span></span>

<span data-ttu-id="f72e4-118">Возвращает **значение \_ ОК** , если функция выполнена успешно, или код ошибки Win32 или RPC в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f72e4-118">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="f72e4-119">В следующем списке перечислены возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="f72e4-119">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="f72e4-120">**Ошибка \_ отказа в доступе \_**</span><span class="sxs-lookup"><span data-stu-id="f72e4-120">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="f72e4-121">Вызывающий объект не имеет необходимых прав доступа для вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="f72e4-121">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="f72e4-122">Функцию [**дссетаусидентити**](dssetauthidentity.md) можно использовать для задания учетных данных, используемых для функций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="f72e4-122">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f72e4-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f72e4-123">Remarks</span></span>

<span data-ttu-id="f72e4-124">Перед перезагрузкой контроллера домена вызовите эту функцию, чтобы указать состояние операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="f72e4-124">Before you restart the domain controller, call this function to provide the status of the restore operation.</span></span> <span data-ttu-id="f72e4-125">Если состояние не прошло успешно, Служба каталогов не запустится, пока не будет восстановлена допустимая база данных.</span><span class="sxs-lookup"><span data-stu-id="f72e4-125">If the status is not successful, the directory service will not start until a valid database has been restored.</span></span> <span data-ttu-id="f72e4-126">Эта функция завершает операцию восстановления и позволяет запускать службы домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f72e4-126">This function completes the restore operation and allows Active Directory Domain Services to start.</span></span>

## <a name="requirements"></a><span data-ttu-id="f72e4-127">Требования</span><span class="sxs-lookup"><span data-stu-id="f72e4-127">Requirements</span></span>



| <span data-ttu-id="f72e4-128">Требование</span><span class="sxs-lookup"><span data-stu-id="f72e4-128">Requirement</span></span> | <span data-ttu-id="f72e4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="f72e4-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f72e4-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f72e4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f72e4-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f72e4-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f72e4-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f72e4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f72e4-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f72e4-133">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f72e4-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f72e4-134">End of client support</span></span><br/>    | <span data-ttu-id="f72e4-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f72e4-135">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f72e4-136">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f72e4-136">End of server support</span></span><br/>    | <span data-ttu-id="f72e4-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f72e4-137">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f72e4-138">Header</span><span class="sxs-lookup"><span data-stu-id="f72e4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f72e4-139"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="f72e4-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="f72e4-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f72e4-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="f72e4-141"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f72e4-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="f72e4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f72e4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f72e4-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f72e4-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f72e4-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f72e4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f72e4-145">**дсресторерегистер**</span><span class="sxs-lookup"><span data-stu-id="f72e4-145">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="f72e4-146">**дсресторепрепаре**</span><span class="sxs-lookup"><span data-stu-id="f72e4-146">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="f72e4-147">**дссетаусидентити**</span><span class="sxs-lookup"><span data-stu-id="f72e4-147">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="f72e4-148">Восстановление сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="f72e4-148">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="f72e4-149">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="f72e4-149">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

