---
title: Функция Дссеткуррентбаккуплог (Нтдсбкли. h)
description: Задает текущий номер журнала резервного копирования после успешного восстановления.
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дссеткуррентбаккуплог
topic_type:
- apiref
api_name:
- DsSetCurrentBackupLog
- DsSetCurrentBackupLogA
- DsSetCurrentBackupLogW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f50fc41317ae22ae89c47f63bb19f981563e5c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892181"
---
# <a name="dssetcurrentbackuplog-function"></a><span data-ttu-id="22c86-104">Функция Дссеткуррентбаккуплог</span><span class="sxs-lookup"><span data-stu-id="22c86-104">DsSetCurrentBackupLog function</span></span>

<span data-ttu-id="22c86-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="22c86-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="22c86-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="22c86-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="22c86-107">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="22c86-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="22c86-108">Функция **дссеткуррентбаккуплог** задает текущий номер журнала резервного копирования после успешного восстановления.</span><span class="sxs-lookup"><span data-stu-id="22c86-108">The **DsSetCurrentBackupLog** function sets the current backup log number after a successful restore.</span></span> <span data-ttu-id="22c86-109">Так как службы домен Active Directory поддерживают только циклическое ведение журнала, эта функция обычно не используется.</span><span class="sxs-lookup"><span data-stu-id="22c86-109">Because Active Directory Domain Services only support circular logging, this function is not normally used.</span></span>

## <a name="syntax"></a><span data-ttu-id="22c86-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22c86-110">Syntax</span></span>


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a><span data-ttu-id="22c86-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="22c86-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22c86-112">*сзсервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22c86-112">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c86-113">Указатель на строку, завершающуюся нулем, которая содержит имя сервера, для которого задается номер журнала резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="22c86-113">Pointer to a null-terminated string that contains the name of the server to set the backup log number for.</span></span> <span data-ttu-id="22c86-114">Предыдущие обратные косые черты необязательны.</span><span class="sxs-lookup"><span data-stu-id="22c86-114">Preceding backslashes are optional.</span></span> <span data-ttu-id="22c86-115">Сервер должен быть тем же компьютером, из которого вызывается эта функция.</span><span class="sxs-lookup"><span data-stu-id="22c86-115">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="22c86-116">Имя сервера не может содержать символы подчеркивания ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="22c86-116">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="22c86-117">Пример имени сервера — \\ \\ Server1.</span><span class="sxs-lookup"><span data-stu-id="22c86-117">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="22c86-118">*двкуррентлог* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22c86-118">*dwCurrentLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c86-119">Содержит номер журнала резервного копирования, который необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="22c86-119">Contains the backup log number to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22c86-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22c86-120">Return value</span></span>

<span data-ttu-id="22c86-121">Возвращает **значение \_ ОК** , если функция выполнена успешно, или код ошибки Win32 или RPC в противном случае.</span><span class="sxs-lookup"><span data-stu-id="22c86-121">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="22c86-122">В следующем списке перечислены возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="22c86-122">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="22c86-123">**Ошибка \_ недопустимого \_ параметра**</span><span class="sxs-lookup"><span data-stu-id="22c86-123">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="22c86-124">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="22c86-124">One or more parameters are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="22c86-125">**Ошибка \_ не \_ хватает \_ памяти**</span><span class="sxs-lookup"><span data-stu-id="22c86-125">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="22c86-126">Ошибка при выделении памяти.</span><span class="sxs-lookup"><span data-stu-id="22c86-126">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22c86-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22c86-127">Remarks</span></span>

<span data-ttu-id="22c86-128">Обычно не требуется вызывать функцию **дссеткуррентбаккуплог** .</span><span class="sxs-lookup"><span data-stu-id="22c86-128">It is not normally required to call the **DsSetCurrentBackupLog** function.</span></span> <span data-ttu-id="22c86-129">Функции резервного копирования автоматически определяют и устанавливают последний номер журнала, резервная копия которого была создана.</span><span class="sxs-lookup"><span data-stu-id="22c86-129">The backup functions automatically determine and set the last log number backed up.</span></span> <span data-ttu-id="22c86-130">Используйте **дссеткуррентбаккуплог** , чтобы предотвратить выполнение другого добавочного резервного копирования до выполнения полного резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="22c86-130">Use **DsSetCurrentBackupLog** to prevent another incremental backup from succeeding until a full backup is performed.</span></span>

## <a name="requirements"></a><span data-ttu-id="22c86-131">Требования</span><span class="sxs-lookup"><span data-stu-id="22c86-131">Requirements</span></span>



| <span data-ttu-id="22c86-132">Требование</span><span class="sxs-lookup"><span data-stu-id="22c86-132">Requirement</span></span> | <span data-ttu-id="22c86-133">Значение</span><span class="sxs-lookup"><span data-stu-id="22c86-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22c86-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22c86-134">Minimum supported client</span></span><br/> | <span data-ttu-id="22c86-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22c86-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="22c86-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22c86-136">Minimum supported server</span></span><br/> | <span data-ttu-id="22c86-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22c86-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22c86-138">Header</span><span class="sxs-lookup"><span data-stu-id="22c86-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="22c86-139"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="22c86-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="22c86-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="22c86-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="22c86-141"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22c86-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="22c86-142">DLL</span><span class="sxs-lookup"><span data-stu-id="22c86-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22c86-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22c86-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="22c86-144">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="22c86-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="22c86-145">**Дссеткуррентбаккуплогв** (Юникод) и **дссеткуррентбаккуплога** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="22c86-145">**DsSetCurrentBackupLogW** (Unicode) and **DsSetCurrentBackupLogA** (ANSI)</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="22c86-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22c86-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22c86-147">Резервное копирование и восстановление сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="22c86-147">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="22c86-148">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="22c86-148">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

