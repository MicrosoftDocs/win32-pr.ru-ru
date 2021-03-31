---
title: Функция Дсиснтдсонлине (Нтдсбкли. h)
description: Определяет, находятся ли службы домен Active Directory на указанном сервере в сети.
ms.assetid: 8f46e4d8-6d05-402c-a5b4-291fd2d6609b
ms.tgt_platform: multiple
keywords:
- Active Directory функции Дсиснтдсонлине
topic_type:
- apiref
api_name:
- DsIsNTDSOnline
- DsIsNTDSOnlineA
- DsIsNTDSOnlineW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f6728f4481eb8820055b48f10cfa0f94c7aaa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135978"
---
# <a name="dsisntdsonline-function"></a><span data-ttu-id="65067-104">Функция Дсиснтдсонлине</span><span class="sxs-lookup"><span data-stu-id="65067-104">DsIsNTDSOnline function</span></span>

<span data-ttu-id="65067-105">\[Эта функция доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="65067-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="65067-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="65067-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="65067-107">Начиная с Windows Vista, вместо нее следует использовать [Служба теневого копирования томов (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="65067-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="65067-108">Функция **дсиснтдсонлине** определяет, подключены ли службы домен Active Directory к сети на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="65067-108">The **DsIsNTDSOnline** function determines if Active Directory Domain Services are online on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="65067-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65067-109">Syntax</span></span>


```C++
HRESULT DsIsNTDSOnline(
  _In_  LPCTSTR szServerName,
  _Out_ BOOL    *pfNTDSOnline
);
```



## <a name="parameters"></a><span data-ttu-id="65067-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="65067-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65067-111">*сзсервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="65067-111">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65067-112">Указатель на строку, завершающуюся нулем, которая содержит имя тестируемого сервера.</span><span class="sxs-lookup"><span data-stu-id="65067-112">Pointer to a null-terminated string that contains the name of the server to test.</span></span> <span data-ttu-id="65067-113">Предыдущие обратные косые черты необязательны.</span><span class="sxs-lookup"><span data-stu-id="65067-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="65067-114">Сервер должен быть тем же компьютером, из которого вызывается эта функция.</span><span class="sxs-lookup"><span data-stu-id="65067-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="65067-115">Имя сервера не может содержать символы подчеркивания ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="65067-115">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="65067-116">Пример имени сервера — \\ \\ Server1.</span><span class="sxs-lookup"><span data-stu-id="65067-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="65067-117">*пфнтдсонлине* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="65067-117">*pfNTDSOnline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65067-118">Указатель на **логическое** значение, получающее результат.</span><span class="sxs-lookup"><span data-stu-id="65067-118">Pointer to **BOOL** value that receives the result.</span></span> <span data-ttu-id="65067-119">Получает **значение true** , если служба каталогов находится в сети, или **значение false** , если служба каталогов находится в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="65067-119">Receives **TRUE** if the directory service is online or **FALSE** if the directory service is offline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65067-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65067-120">Return value</span></span>

<span data-ttu-id="65067-121">Возвращает **значение \_ ОК** , если функция выполнена успешно, или в противном случае — код ошибки.</span><span class="sxs-lookup"><span data-stu-id="65067-121">Returns **S\_OK** if the function is successful or an error code otherwise.</span></span> <span data-ttu-id="65067-122">В следующем списке перечислены возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="65067-122">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="65067-123">**Ошибка \_ отказа в доступе \_**</span><span class="sxs-lookup"><span data-stu-id="65067-123">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="65067-124">Вызывающий объект не имеет необходимых прав доступа для вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="65067-124">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="65067-125">Функцию [**дссетаусидентити**](dssetauthidentity.md) можно использовать для задания учетных данных, используемых для функций резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="65067-125">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="65067-126">**хркаулднотконнект**</span><span class="sxs-lookup"><span data-stu-id="65067-126">**hrCouldNotConnect**</span></span>
</dt> <dd>

<span data-ttu-id="65067-127">Не удается найти сервер в *сзсервернаме* , не является контроллером домена, или *сзсервернаме* имеет неправильный формат.</span><span class="sxs-lookup"><span data-stu-id="65067-127">The server in *szServerName* cannot be found, is not a domain controller, or *szServerName* is not formatted correctly.</span></span> <span data-ttu-id="65067-128">Это значение определено в Нтдсбмсг. h.</span><span class="sxs-lookup"><span data-stu-id="65067-128">This value is defined in Ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="65067-129">**\_ \_ Недопустимая привязка RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="65067-129">**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd>

<span data-ttu-id="65067-130">Функция [**дсиснтдсонлине**](dsisntdsonline.md) вызывается удаленно, или сервер в *сзсервернаме* не является контроллером домена.</span><span class="sxs-lookup"><span data-stu-id="65067-130">The [**DsIsNTDSOnline**](dsisntdsonline.md) function is being called remotely or the server in *szServerName* is not a domain controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65067-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65067-131">Remarks</span></span>

<span data-ttu-id="65067-132">Вызовите эту функцию перед вызовом любой из функций резервного копирования или восстановления каталога.</span><span class="sxs-lookup"><span data-stu-id="65067-132">Call this function before calling any of the directory backup or restore functions.</span></span> <span data-ttu-id="65067-133">Для выполнения резервного копирования каталог должен находиться в оперативном режиме.</span><span class="sxs-lookup"><span data-stu-id="65067-133">The directory must be online in order to perform a backup.</span></span> <span data-ttu-id="65067-134">Для выполнения восстановления каталог должен находиться в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="65067-134">The directory must by offline to perform a restore.</span></span>

<span data-ttu-id="65067-135">Эту функцию можно вызвать только из контроллера домена, который также является целевым сервером, указанным в *сзсервернаме*.</span><span class="sxs-lookup"><span data-stu-id="65067-135">This function can only be called from a domain controller that is also the target server specified in *szServerName*.</span></span> <span data-ttu-id="65067-136">Эта функция не может быть вызвана удаленно.</span><span class="sxs-lookup"><span data-stu-id="65067-136">This function cannot be called remotely.</span></span>

## <a name="requirements"></a><span data-ttu-id="65067-137">Требования</span><span class="sxs-lookup"><span data-stu-id="65067-137">Requirements</span></span>



| <span data-ttu-id="65067-138">Требование</span><span class="sxs-lookup"><span data-stu-id="65067-138">Requirement</span></span> | <span data-ttu-id="65067-139">Значение</span><span class="sxs-lookup"><span data-stu-id="65067-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65067-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65067-140">Minimum supported client</span></span><br/> | <span data-ttu-id="65067-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65067-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65067-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65067-142">Minimum supported server</span></span><br/> | <span data-ttu-id="65067-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65067-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65067-144">Header</span><span class="sxs-lookup"><span data-stu-id="65067-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="65067-145"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="65067-145"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="65067-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="65067-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="65067-147"><dt>Нтдсбкли. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65067-147"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="65067-148">DLL</span><span class="sxs-lookup"><span data-stu-id="65067-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65067-149"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65067-149"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="65067-150">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="65067-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="65067-151">**Дсиснтдсонлинев** (Юникод) и **дсиснтдсонлинеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="65067-151">**DsIsNTDSOnlineW** (Unicode) and **DsIsNTDSOnlineA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="65067-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65067-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65067-153">**дссетаусидентити**</span><span class="sxs-lookup"><span data-stu-id="65067-153">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="65067-154">Функции резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="65067-154">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="65067-155">Резервное копирование и восстановление сервера Active Directory</span><span class="sxs-lookup"><span data-stu-id="65067-155">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> </dl>

 

