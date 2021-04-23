---
title: Функция Дсбаккуптрункателогс (Нтдсбкли. h)
description: Усекает ранее прочитанные журналы резервного копирования.
ms.assetid: fae2e19f-08b8-410f-a735-dd4d41fc71a6
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсбаккуптрункателогс
topic_type:
- apiref
api_name:
- DsBackupTruncateLogs
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051ced828656c6b6e5af156e2d1a69c3b741cdce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534052"
---
# <a name="dsbackuptruncatelogs-function"></a><span data-ttu-id="f42d7-104">Функция Дсбаккуптрункателогс</span><span class="sxs-lookup"><span data-stu-id="f42d7-104">DsBackupTruncateLogs function</span></span>

<span data-ttu-id="f42d7-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="f42d7-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f42d7-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="f42d7-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f42d7-107">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="f42d7-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="f42d7-108">Функция **дсбаккуптрункателогс** усекает ранее прочитанные журналы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="f42d7-108">The **DsBackupTruncateLogs** function truncates the previously read backup logs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f42d7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f42d7-109">Syntax</span></span>


```C++
HRESULT DsBackupTruncateLogs(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="f42d7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f42d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f42d7-111">*ХБК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f42d7-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f42d7-112">Содержит описатель контекста резервного копирования, полученный с помощью функции [**дсбаккуппрепаре**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="f42d7-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f42d7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f42d7-113">Return value</span></span>

<span data-ttu-id="f42d7-114">Возвращает **значение \_ ОК** , если функция выполнена успешно, или код ошибки Win32 или RPC в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f42d7-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="f42d7-115">В следующем списке перечислены другие возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="f42d7-115">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="f42d7-116">**Ошибка \_ отказа в доступе \_**</span><span class="sxs-lookup"><span data-stu-id="f42d7-116">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="f42d7-117">Вызывающий объект не имеет необходимых прав доступа для вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="f42d7-117">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="f42d7-118">Функцию [**дссетаусидентити**](dssetauthidentity.md) можно использовать для задания учетных данных, используемых для функций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="f42d7-118">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="f42d7-119">**Ошибка \_ недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="f42d7-119">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="f42d7-120">Недопустимый *ХБК* .</span><span class="sxs-lookup"><span data-stu-id="f42d7-120">*hbc* is invalid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f42d7-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f42d7-121">Remarks</span></span>

<span data-ttu-id="f42d7-122">При успешном завершении полной или добавочной архивации используйте функцию **дсбаккуптрункателогс** .</span><span class="sxs-lookup"><span data-stu-id="f42d7-122">Use the **DsBackupTruncateLogs** function when a full or incremental backup has completed successfully.</span></span>

> [!Caution]  
> <span data-ttu-id="f42d7-123">Если эта функция вызывается после разностной резервной копии, все добавочные резервные копии будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="f42d7-123">If this function is called after a differential backup, all of the incremental backup information will be lost.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f42d7-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f42d7-124">Requirements</span></span>



| <span data-ttu-id="f42d7-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f42d7-125">Requirement</span></span> | <span data-ttu-id="f42d7-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f42d7-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f42d7-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f42d7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f42d7-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f42d7-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f42d7-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f42d7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f42d7-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f42d7-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f42d7-131">Header</span><span class="sxs-lookup"><span data-stu-id="f42d7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f42d7-132"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="f42d7-132"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="f42d7-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f42d7-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="f42d7-134"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f42d7-134"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="f42d7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f42d7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f42d7-136"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f42d7-136"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f42d7-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f42d7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f42d7-138">**дсбаккуппрепаре**</span><span class="sxs-lookup"><span data-stu-id="f42d7-138">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="f42d7-139">**дсбаккупжетбаккуплогс**</span><span class="sxs-lookup"><span data-stu-id="f42d7-139">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="f42d7-140">**дссеткуррентбаккуплог**</span><span class="sxs-lookup"><span data-stu-id="f42d7-140">**DsSetCurrentBackupLog**</span></span>](dssetcurrentbackuplog.md)
</dt> <dt>

[<span data-ttu-id="f42d7-141">Резервное копирование сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="f42d7-141">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="f42d7-142">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="f42d7-142">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

