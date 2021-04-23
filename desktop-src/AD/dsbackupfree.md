---
title: Функция Дсбаккупфри (Нтдсбкли. h)
description: Освобождает память, выделенную функциями резервного копирования и восстановления домен Active Directory Services.
ms.assetid: cde2a530-60e6-440c-9d4e-a90d55846973
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсбаккупфри
topic_type:
- apiref
api_name:
- DsBackupFree
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27855eeb3417eede371357528457248857c3e626
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891801"
---
# <a name="dsbackupfree-function"></a><span data-ttu-id="0deec-104">Функция Дсбаккупфри</span><span class="sxs-lookup"><span data-stu-id="0deec-104">DsBackupFree function</span></span>

<span data-ttu-id="0deec-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="0deec-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0deec-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="0deec-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="0deec-107">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="0deec-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="0deec-108">Функция **дсбаккупфри** освобождает память, выделенную функциями резервного копирования и восстановления домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="0deec-108">The **DsBackupFree** function releases memory allocated by the Active Directory Domain Services backup and restore functions.</span></span> <span data-ttu-id="0deec-109">Следующие функции выделяют память, которая должна быть освобождена с помощью функции **дсбаккупфри** .</span><span class="sxs-lookup"><span data-stu-id="0deec-109">The following functions allocate memory that must be released with the **DsBackupFree** function.</span></span>

-   [<span data-ttu-id="0deec-110">**дсбаккупжетбаккуплогс**</span><span class="sxs-lookup"><span data-stu-id="0deec-110">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
-   [<span data-ttu-id="0deec-111">**дсбаккупжетдатабасенамес**</span><span class="sxs-lookup"><span data-stu-id="0deec-111">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
-   [<span data-ttu-id="0deec-112">**дсбаккуппрепаре**</span><span class="sxs-lookup"><span data-stu-id="0deec-112">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
-   [<span data-ttu-id="0deec-113">**дсресторежетдатабаселокатионс**</span><span class="sxs-lookup"><span data-stu-id="0deec-113">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)

## <a name="syntax"></a><span data-ttu-id="0deec-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0deec-114">Syntax</span></span>


```C++
VOID NTDSBCLI_API DsBackupFree(
  _In_ PVOID pvBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="0deec-115">Параметры</span><span class="sxs-lookup"><span data-stu-id="0deec-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0deec-116">*пвбуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0deec-116">*pvBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0deec-117">Указатель на буфер памяти, который необходимо освободить.</span><span class="sxs-lookup"><span data-stu-id="0deec-117">Pointer to the memory buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0deec-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0deec-118">Return value</span></span>

<span data-ttu-id="0deec-119">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0deec-119">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0deec-120">Требования</span><span class="sxs-lookup"><span data-stu-id="0deec-120">Requirements</span></span>



| <span data-ttu-id="0deec-121">Требование</span><span class="sxs-lookup"><span data-stu-id="0deec-121">Requirement</span></span> | <span data-ttu-id="0deec-122">Значение</span><span class="sxs-lookup"><span data-stu-id="0deec-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0deec-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0deec-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0deec-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0deec-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0deec-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0deec-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0deec-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0deec-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0deec-127">Header</span><span class="sxs-lookup"><span data-stu-id="0deec-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0deec-128"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="0deec-128"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="0deec-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0deec-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="0deec-130"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0deec-130"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="0deec-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0deec-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0deec-132"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0deec-132"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0deec-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0deec-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0deec-134">**дсбаккупжетбаккуплогс**</span><span class="sxs-lookup"><span data-stu-id="0deec-134">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="0deec-135">**дсбаккупжетдатабасенамес**</span><span class="sxs-lookup"><span data-stu-id="0deec-135">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
</dt> <dt>

[<span data-ttu-id="0deec-136">**дсбаккуппрепаре**</span><span class="sxs-lookup"><span data-stu-id="0deec-136">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="0deec-137">**дсресторежетдатабаселокатионс**</span><span class="sxs-lookup"><span data-stu-id="0deec-137">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="0deec-138">Резервное копирование сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="0deec-138">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="0deec-139">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="0deec-139">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

