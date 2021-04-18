---
title: Объект ConnectionOptions (Всмандисп. h)
description: Объект ConnectionOptions передается методу CreateSession для предоставления имени пользователя и пароля, связанных с локальной учетной записью на удаленном компьютере.
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows объекта ConnectionOptions
- Служба удаленного управления Windows объекта ConnectionOptions, описание
topic_type:
- apiref
api_name:
- ConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 164eb886ce98266cab3109e773b731e002d1abac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701063"
---
# <a name="connectionoptions-object"></a><span data-ttu-id="a5063-105">Объект ConnectionOptions</span><span class="sxs-lookup"><span data-stu-id="a5063-105">ConnectionOptions object</span></span>

<span data-ttu-id="a5063-106">Объект **ConnectionOptions** передается методу [**CreateSession**](wsman-createsession.md) для предоставления имени пользователя и пароля, связанных с локальной учетной записью на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a5063-106">The **ConnectionOptions** object is passed to the [**CreateSession**](wsman-createsession.md) method to provide the user name and password associated with the local account on the remote computer.</span></span> <span data-ttu-id="a5063-107">Если параметры не указаны, то для учетных данных, в которых выполняется скрипт, задаются значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a5063-107">If no parameters are supplied, then the credentials of the account running the script are set to the default values.</span></span>

## <a name="members"></a><span data-ttu-id="a5063-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="a5063-108">Members</span></span>

<span data-ttu-id="a5063-109">Объект **ConnectionOptions** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a5063-109">The **ConnectionOptions** object has these types of members:</span></span>

-   [<span data-ttu-id="a5063-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5063-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5063-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5063-111">Properties</span></span>

<span data-ttu-id="a5063-112">Объект **ConnectionOptions** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a5063-112">The **ConnectionOptions** object has these properties.</span></span>



| <span data-ttu-id="a5063-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="a5063-113">Property</span></span>                                                  | <span data-ttu-id="a5063-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="a5063-114">Access type</span></span>           | <span data-ttu-id="a5063-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a5063-115">Description</span></span>                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5063-116">**Пароль**</span><span class="sxs-lookup"><span data-stu-id="a5063-116">**Password**</span></span>](connectionoptions-password.md)<br/> | <span data-ttu-id="a5063-117">Только на запись</span><span class="sxs-lookup"><span data-stu-id="a5063-117">Write-only</span></span><br/> | <span data-ttu-id="a5063-118">Задает пароль локальной или доменной учетной записи на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a5063-118">Sets the password of a local or domain account on the remote computer.</span></span><br/>           |
| [<span data-ttu-id="a5063-119">**Имен**</span><span class="sxs-lookup"><span data-stu-id="a5063-119">**UserName**</span></span>](connectionoptions-username.md)<br/> | <span data-ttu-id="a5063-120">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="a5063-120">Read/write</span></span><br/> | <span data-ttu-id="a5063-121">Задает и возвращает имя пользователя локальной или доменной учетной записи на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a5063-121">Sets and gets the user name of a local or domain account on the remote computer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a5063-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5063-122">Remarks</span></span>

<span data-ttu-id="a5063-123">Объект **ConnectionOptions** соответствует интерфейсу [**ивсманконнектионоптионс**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) .</span><span class="sxs-lookup"><span data-stu-id="a5063-123">The **ConnectionOptions** object corresponds to the [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) interface.</span></span>

<span data-ttu-id="a5063-124">Если клиентское приложение служба удаленного управления Windows выполняется под олицетворением, то при установке свойства [**Password**](connectionoptions-password.md) происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="a5063-124">If a Windows Remote Management client application is running under impersonation, then a failure occurs if you set the [**Password**](connectionoptions-password.md) property.</span></span> <span data-ttu-id="a5063-125">Клиентское приложение — это сценарий или другая программа, которая отправляет запрос в службу WinRM на локальном или удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a5063-125">A client application is a script or other program that sends a request to WinRM on the local or a remote computer.</span></span> <span data-ttu-id="a5063-126">Клиентское приложение может работать под олицетворением, так как оно называется функцией, например [**имперсонатеклиент**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5063-126">The client application may be running under impersonation because it called a function like [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)).</span></span> <span data-ttu-id="a5063-127">Страница Active Server (ASP) или служба не может запрашивать имя пользователя и пароль, если процесс ASP выполняется с учетной записью, выполняющей олицетворение клиента.</span><span class="sxs-lookup"><span data-stu-id="a5063-127">An Active Server Page (ASP) or service cannot request a user name and password if the ASP process runs under an account that impersonates a client.</span></span>

<span data-ttu-id="a5063-128">Флаг **всманфлагкредусернамепассворд** должен быть установлен для вызова [**WSman. CreateSession**](wsman-createsession.md) при использовании [**имени пользователя**](connectionoptions-username.md) и [**пароля**](connectionoptions-password.md) для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a5063-128">The **WSManFlagCredUserNamePassword** flag should be set on the [**WSman.CreateSession**](wsman-createsession.md) call when using the [**UserName**](connectionoptions-username.md) and [**Password**](connectionoptions-password.md) for authentication.</span></span>

## <a name="examples"></a><span data-ttu-id="a5063-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="a5063-129">Examples</span></span>

<span data-ttu-id="a5063-130">В следующем примере кода VBScript показано, как создать объект **ConnectionOptions** , задать свойства учетной записи на удаленном компьютере и использовать его при создании объекта [**Session**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="a5063-130">The following VBScript code example shows how to create a **ConnectionOptions** object, set the properties for the account on the remote computer, and use it in creating a [**Session**](session.md) object.</span></span>


```VB
Set objWsman = CreateObject( "Wsman.Automation" )
'Create ConnectionOptions object.
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "johns "
objConnectionOptions.Password = "Dtf#4542?98"
iFlags = objWsman.SessionFlagUseBasic Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession _
  ("https://172.30.168.2", iFlags, objConnectionOptions)
strResource = objSession.Get("winrm/config")
```



## <a name="requirements"></a><span data-ttu-id="a5063-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a5063-131">Requirements</span></span>



| <span data-ttu-id="a5063-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a5063-132">Requirement</span></span> | <span data-ttu-id="a5063-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a5063-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5063-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5063-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a5063-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5063-135">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a5063-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5063-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a5063-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5063-137">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a5063-138">Header</span><span class="sxs-lookup"><span data-stu-id="a5063-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5063-139"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5063-139"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5063-140">IDL</span><span class="sxs-lookup"><span data-stu-id="a5063-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a5063-141"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a5063-141"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="a5063-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a5063-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5063-143"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a5063-143"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a5063-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a5063-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5063-145"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5063-145"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a5063-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5063-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5063-147">Проверка подлинности для удаленных подключений</span><span class="sxs-lookup"><span data-stu-id="a5063-147">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> <dt>

[<span data-ttu-id="a5063-148">API сценариев WinRM</span><span class="sxs-lookup"><span data-stu-id="a5063-148">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="a5063-149">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="a5063-149">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="a5063-150">Использование служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="a5063-150">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="a5063-151">Создание сценариев в служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="a5063-151">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="a5063-152">Получение данных с локального компьютера</span><span class="sxs-lookup"><span data-stu-id="a5063-152">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="a5063-153">Получение данных с удаленного компьютера</span><span class="sxs-lookup"><span data-stu-id="a5063-153">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

