---
title: Функция Дсбаккупенд (Нтдсбкли. h)
description: Вызывается для завершения операции резервного копирования.
ms.assetid: 872645bc-3dbe-4b12-af4f-778d54feb18f
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсбаккупенд
topic_type:
- apiref
api_name:
- DsBackupEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9663eedec7bc298ef594990baababcf2083546e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891802"
---
# <a name="dsbackupend-function"></a><span data-ttu-id="866f3-104">Функция Дсбаккупенд</span><span class="sxs-lookup"><span data-stu-id="866f3-104">DsBackupEnd function</span></span>

<span data-ttu-id="866f3-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="866f3-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="866f3-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="866f3-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="866f3-107">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="866f3-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="866f3-108">Для завершения операции резервного копирования вызывается функция **дсбаккупенд** .</span><span class="sxs-lookup"><span data-stu-id="866f3-108">The **DsBackupEnd** function is called to terminate a backup operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="866f3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="866f3-109">Syntax</span></span>


```C++
HRESULT DsBackupEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="866f3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="866f3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="866f3-111">*ХБК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="866f3-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="866f3-112">Содержит описатель контекста резервного копирования, полученный с помощью функции [**дсбаккуппрепаре**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="866f3-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="866f3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="866f3-113">Return value</span></span>

<span data-ttu-id="866f3-114">Возвращает **значение \_ ОК** , если функция выполнена успешно, или код ошибки Win32 или RPC в противном случае.</span><span class="sxs-lookup"><span data-stu-id="866f3-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="866f3-115">В следующем списке перечислены другие возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="866f3-115">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="866f3-116">**Ошибка \_ недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="866f3-116">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="866f3-117">Недопустимый *ХБК* .</span><span class="sxs-lookup"><span data-stu-id="866f3-117">*hbc* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="866f3-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="866f3-118">Remarks</span></span>

<span data-ttu-id="866f3-119">Функция **дсбаккупенд** закрывает необработанные дескрипторы привязки и выполняет очистку после успешной или неудачной попытки резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="866f3-119">The **DsBackupEnd** function closes outstanding binding handles and performs a cleanup after a successful or unsuccessful backup attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="866f3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="866f3-120">Requirements</span></span>



| <span data-ttu-id="866f3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="866f3-121">Requirement</span></span> | <span data-ttu-id="866f3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="866f3-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="866f3-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="866f3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="866f3-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="866f3-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="866f3-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="866f3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="866f3-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="866f3-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="866f3-127">Header</span><span class="sxs-lookup"><span data-stu-id="866f3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="866f3-128"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="866f3-128"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="866f3-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="866f3-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="866f3-130"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="866f3-130"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="866f3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="866f3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="866f3-132"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="866f3-132"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="866f3-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="866f3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="866f3-134">**дссетаусидентити**</span><span class="sxs-lookup"><span data-stu-id="866f3-134">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="866f3-135">Резервное копирование сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="866f3-135">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="866f3-136">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="866f3-136">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

