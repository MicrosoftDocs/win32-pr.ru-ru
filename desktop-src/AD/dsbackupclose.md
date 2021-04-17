---
title: Функция Дсбаккупклосе (Нтдсбкли. h)
description: Закрывает файл резервной копии, Открытый с помощью функции Дсбаккупопенфиле.
ms.assetid: 5452a222-abe8-4d2d-84ff-6f577073b220
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсбаккупклосе
topic_type:
- apiref
api_name:
- DsBackupClose
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d03c9cd7f125d223d264236a52120714d5198c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490251"
---
# <a name="dsbackupclose-function"></a><span data-ttu-id="fa458-104">Функция Дсбаккупклосе</span><span class="sxs-lookup"><span data-stu-id="fa458-104">DsBackupClose function</span></span>

<span data-ttu-id="fa458-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="fa458-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fa458-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="fa458-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="fa458-107">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="fa458-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="fa458-108">Функция **дсбаккупклосе** закрывает файл резервной копии, Открытый с помощью функции [**дсбаккупопенфиле**](dsbackupopenfile.md) .</span><span class="sxs-lookup"><span data-stu-id="fa458-108">The **DsBackupClose** function closes a backup file opened with the [**DsBackupOpenFile**](dsbackupopenfile.md) function.</span></span> <span data-ttu-id="fa458-109">Для каждого маркера резервного копирования в каждый момент времени может быть открыт только один файл, поэтому эта функция закрывает открытый в данный момент файл.</span><span class="sxs-lookup"><span data-stu-id="fa458-109">For each backup handle, only one file can be opened at a time, so this function closes the currently open file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa458-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa458-110">Syntax</span></span>


```C++
HRESULT DsBackupClose(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="fa458-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa458-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa458-112">*ХБК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa458-112">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa458-113">Содержит описатель контекста резервного копирования, полученный с помощью функции [**дсбаккуппрепаре**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="fa458-113">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa458-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa458-114">Return value</span></span>

<span data-ttu-id="fa458-115">Возвращает **значение \_ ОК** , если функция выполнена успешно, или код ошибки Win32 или RPC в противном случае.</span><span class="sxs-lookup"><span data-stu-id="fa458-115">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="fa458-116">В следующем списке перечислены другие возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="fa458-116">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="fa458-117">**Ошибка \_ недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="fa458-117">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="fa458-118">Недопустимый *ХБК* .</span><span class="sxs-lookup"><span data-stu-id="fa458-118">*hbc* is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="fa458-119">**хринвалидхандле**</span><span class="sxs-lookup"><span data-stu-id="fa458-119">**hrInvalidHandle**</span></span>
</dt> <dd>

<span data-ttu-id="fa458-120">В настоящее время файл не открыт.</span><span class="sxs-lookup"><span data-stu-id="fa458-120">No file is currently open.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa458-121">Требования</span><span class="sxs-lookup"><span data-stu-id="fa458-121">Requirements</span></span>



| <span data-ttu-id="fa458-122">Требование</span><span class="sxs-lookup"><span data-stu-id="fa458-122">Requirement</span></span> | <span data-ttu-id="fa458-123">Значение</span><span class="sxs-lookup"><span data-stu-id="fa458-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa458-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa458-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fa458-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa458-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa458-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa458-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fa458-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa458-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa458-128">Header</span><span class="sxs-lookup"><span data-stu-id="fa458-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa458-129"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa458-129"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa458-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fa458-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa458-131"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa458-131"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="fa458-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fa458-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa458-133"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa458-133"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa458-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa458-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa458-135">**дсбаккупопенфиле**</span><span class="sxs-lookup"><span data-stu-id="fa458-135">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="fa458-136">**дсбаккуппрепаре**</span><span class="sxs-lookup"><span data-stu-id="fa458-136">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="fa458-137">Резервное копирование сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="fa458-137">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="fa458-138">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="fa458-138">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

