---
title: Свойство ConnectionOptions. UserName (Всмандисп. h)
description: Задает и возвращает имя пользователя локальной или доменной учетной записи на удаленном компьютере. Это свойство определяет имя пользователя для проверки подлинности.
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows Свойства имени пользователя
- Свойство UserName служба удаленного управления Windows, объект ConnectionOptions
- Служба удаленного управления Windows объекта ConnectionOptions, свойство UserName
topic_type:
- apiref
api_name:
- ConnectionOptions.UserName
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4d6c751dbe579372b863566412e740c2a646a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136502"
---
# <a name="connectionoptionsusername-property"></a><span data-ttu-id="57fd1-107">ConnectionOptions. UserName, свойство</span><span class="sxs-lookup"><span data-stu-id="57fd1-107">ConnectionOptions.UserName property</span></span>

<span data-ttu-id="57fd1-108">Задает и возвращает имя пользователя локальной или доменной учетной записи на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="57fd1-108">Sets and gets the user name of a local or a domain account on the remote computer.</span></span> <span data-ttu-id="57fd1-109">Это свойство определяет имя пользователя для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="57fd1-109">This property determines the user name for authentication.</span></span> <span data-ttu-id="57fd1-110">Дополнительные сведения см. в разделе [Проверка подлинности удаленных подключений](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="57fd1-110">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

<span data-ttu-id="57fd1-111">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="57fd1-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="57fd1-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57fd1-112">Syntax</span></span>


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a><span data-ttu-id="57fd1-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="57fd1-113">Property value</span></span>

<span data-ttu-id="57fd1-114">Строка, содержащая имя локального пользователя или учетной записи домена на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="57fd1-114">String that contains the user name of a local or a domain account on the remote computer.</span></span>

<span data-ttu-id="57fd1-115">Если значение не указано, а флаг **всманфлагкредусернамепассворд** не установлен, используется имя пользователя учетной записи, на которой работает скрипт.</span><span class="sxs-lookup"><span data-stu-id="57fd1-115">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is not set, the user name of the account that is running the script is used.</span></span>

<span data-ttu-id="57fd1-116">Если значение не указано и установлен флаг **всманфлагкредусернамепассворд** , сценарий предлагает пользователю ввести имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="57fd1-116">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is set, the script prompts the user to enter the user name and password.</span></span> <span data-ttu-id="57fd1-117">Если допустимое имя пользователя и пароль не указаны, возвращается ошибка отказа в доступе.</span><span class="sxs-lookup"><span data-stu-id="57fd1-117">If a valid user name and password are not entered, then an access denied error is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="57fd1-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="57fd1-118">Remarks</span></span>

<span data-ttu-id="57fd1-119">Для указания этого свойства используется следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="57fd1-119">The following syntax is used to specify this property.</span></span>


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



<span data-ttu-id="57fd1-120">Вы можете указать **имя пользователя** и [**пароль**](connectionoptions-password.md) для учетной записи домена при использовании проверки подлинности [*Negotiate*](windows-remote-management-glossary.md) или *Kerberos* или для локальной учетной записи с [*обычной*](windows-remote-management-glossary.md) проверкой подлинности.</span><span class="sxs-lookup"><span data-stu-id="57fd1-120">You can supply **UserName** and [**Password**](connectionoptions-password.md) for a domain account when using [*negotiate*](windows-remote-management-glossary.md) or *Kerberos* authentication, or for a local account with [*Basic*](windows-remote-management-glossary.md) authentication.</span></span> <span data-ttu-id="57fd1-121">Для подключения к локальной учетной записи флаги [**WSMan. CreateSession**](wsman-createsession.md) должны содержать сочетание флага **всманфлагусебасик** и флага **всманфлагкредусернамепассворд** .</span><span class="sxs-lookup"><span data-stu-id="57fd1-121">To connect to a local account, the [**WSMan.CreateSession**](wsman-createsession.md) flags must contain the combination of the **WSManFlagUseBasic** flag and the **WsmanFlagCredUserNamePassword** flag.</span></span> <span data-ttu-id="57fd1-122">Для подключения к доменной учетной записи флаги **WSMan. CreateSession** должны содержать сочетание флага **всманфлагусенеготиате** и флага **всманфлагкредусернамепассворд** , а также сочетание флага **всманфлагусекерберос** и флага **всманфлагкредусернамепассворд** .</span><span class="sxs-lookup"><span data-stu-id="57fd1-122">To connect to a domain account, the **WSMan.CreateSession** flags must contain the combination of the **WSManFlagUseNegotiate** flag and the **WsmanFlagCredUserNamePassword** flag, or the combination of the **WSManFlagUseKerberos** flag and the **WsmanFlagCredUserNamePassword** flag.</span></span> <span data-ttu-id="57fd1-123">Для учетной записи домена **имя пользователя** должно быть указано в формате " \\ имя пользователя компьютера", где часть строки может быть либо именем, либо IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="57fd1-123">For a domain account, **UserName** must be specified in the form "computer\\username", where the "computer" part of the string can be either the name or the IP address.</span></span> <span data-ttu-id="57fd1-124">Дополнительные сведения см. в разделе [Проверка подлинности удаленных подключений](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="57fd1-124">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



<span data-ttu-id="57fd1-125">Для подключения к доменной учетной записи флаги [**WSMan. CreateSession**](wsman-createsession.md) должны содержать сочетание флага **всманфлагусенеготиате** и флага **всманфлагкредусернамепассворд** для подключения к учетной записи домена, для которой требуется проверка подлинности Negotiate.</span><span class="sxs-lookup"><span data-stu-id="57fd1-125">For connecting to a domain account, the [**WSMan.CreateSession**](wsman-createsession.md) flags must contain the combination of the **WSManFlagUseNegotiate** flag and the **WsmanFlagCredUserNamePassword** flag for connecting to a domain account, which requires Negotiate authentication.</span></span>


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseNegotiate Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



## <a name="requirements"></a><span data-ttu-id="57fd1-126">Требования</span><span class="sxs-lookup"><span data-stu-id="57fd1-126">Requirements</span></span>



| <span data-ttu-id="57fd1-127">Требование</span><span class="sxs-lookup"><span data-stu-id="57fd1-127">Requirement</span></span> | <span data-ttu-id="57fd1-128">Значение</span><span class="sxs-lookup"><span data-stu-id="57fd1-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="57fd1-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57fd1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="57fd1-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57fd1-130">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="57fd1-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57fd1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="57fd1-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57fd1-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="57fd1-133">Header</span><span class="sxs-lookup"><span data-stu-id="57fd1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="57fd1-134"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="57fd1-134"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="57fd1-135">IDL</span><span class="sxs-lookup"><span data-stu-id="57fd1-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="57fd1-136"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="57fd1-136"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="57fd1-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="57fd1-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="57fd1-138"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="57fd1-138"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="57fd1-139">DLL</span><span class="sxs-lookup"><span data-stu-id="57fd1-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57fd1-140"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57fd1-140"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="57fd1-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57fd1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57fd1-142">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="57fd1-142">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





