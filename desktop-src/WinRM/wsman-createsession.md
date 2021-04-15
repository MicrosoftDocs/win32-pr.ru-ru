---
title: Метод WSMan. CreateSession (Всмандисп. h)
description: Создает объект сеанса, который затем может использоваться для последующих сетевых операций.
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода CreateSession
- Служба удаленного управления Windows метода CreateSession, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод CreateSession
topic_type:
- apiref
api_name:
- WSMan.CreateSession
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 966fd1f43db7114d3a4c0cf4cddaa4428fcb41c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534529"
---
# <a name="wsmancreatesession-method"></a><span data-ttu-id="e5197-106">Метод WSMan. CreateSession</span><span class="sxs-lookup"><span data-stu-id="e5197-106">WSMan.CreateSession method</span></span>

<span data-ttu-id="e5197-107">Создает объект [**сеанса**](session.md) , который затем может использоваться для последующих сетевых операций.</span><span class="sxs-lookup"><span data-stu-id="e5197-107">Creates a [**Session**](session.md) object that can then be used for subsequent network operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5197-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5197-108">Syntax</span></span>


```VB
WSMan.CreateSession( _
  [ ByVal connection ], _
  [ ByVal flags ], _
  [ ByVal connectionOptions ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e5197-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5197-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5197-110">*Подключение к* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e5197-110">*connection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e5197-111">Протокол и служба для подключения, включая IPv4 или IPv6.</span><span class="sxs-lookup"><span data-stu-id="e5197-111">The protocol and service to connect to, including either IPv4 or IPv6.</span></span> <span data-ttu-id="e5197-112">Формат сведений о соединении выглядит следующим образом: < ><  >< *суффикса* адреса транспорта>.</span><span class="sxs-lookup"><span data-stu-id="e5197-112">The format of the connection information is as follows: <*Transport*><*Address*><*Suffix*>.</span></span> <span data-ttu-id="e5197-113">Примеры см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="e5197-113">For examples, see Remarks.</span></span> <span data-ttu-id="e5197-114">Если сведения о соединении не указаны, используется локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="e5197-114">If no connection information is provided, the local computer is used.</span></span>

</dd> <dt>

<span data-ttu-id="e5197-115">*Флаги* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e5197-115">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e5197-116">Флаги сеанса, указывающие метод проверки подлинности, например [*Negotiate*](windows-remote-management-glossary.md) или [*дайджест-аутентификация*](windows-remote-management-glossary.md), для подключения к удаленному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="e5197-116">The session flags that specify the authentication method, such as [*Negotiate authentication*](windows-remote-management-glossary.md) or [*Digest authentication*](windows-remote-management-glossary.md), for connecting to a remote computer.</span></span> <span data-ttu-id="e5197-117">Эти флаги также указывают другие сведения о подключении сеанса, такие как кодирование или шифрование.</span><span class="sxs-lookup"><span data-stu-id="e5197-117">These flags also specify other session connection information, such as encoding or encryption.</span></span> <span data-ttu-id="e5197-118">Этот параметр должен содержать один или несколько флагов в **\_ \_ всмансессионфлагс** для удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="e5197-118">This parameter must contain one or more of the flags in **\_\_WSManSessionFlags** for a remote connection.</span></span> <span data-ttu-id="e5197-119">Дополнительные сведения см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e5197-119">For more information, see [Session Constants](session-constants.md).</span></span> <span data-ttu-id="e5197-120">Для подключения к WinRM на локальном компьютере параметры флага не требуются.</span><span class="sxs-lookup"><span data-stu-id="e5197-120">No flag settings are required for a connection to WinRM on the local computer.</span></span> <span data-ttu-id="e5197-121">Значение по умолчанию — **всманфлагусенеготиате**.</span><span class="sxs-lookup"><span data-stu-id="e5197-121">The default is **WSManFlagUseNegotiate**.</span></span>

<span data-ttu-id="e5197-122">Дополнительные сведения см. в разделе [Проверка подлинности удаленных подключений](authentication-for-remote-connections.md) и параметр *connectionOptions* .</span><span class="sxs-lookup"><span data-stu-id="e5197-122">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md) and the *connectionOptions* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e5197-123">*connectionOptions* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e5197-123">*connectionOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e5197-124">Указатель на объект [**ConnectionOptions**](connectionoptions.md) , содержащий имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="e5197-124">A pointer to a [**ConnectionOptions**](connectionoptions.md) object that contains a user name and password.</span></span> <span data-ttu-id="e5197-125">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="e5197-125">The default is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5197-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5197-126">Return value</span></span>

<span data-ttu-id="e5197-127">Объект [**сеанса**](session.md) , который затем можно использовать для выполнения локальных или удаленных операций WinRM.</span><span class="sxs-lookup"><span data-stu-id="e5197-127">A [**Session**](session.md) object that can then be used to perform local or remote WinRM operations.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5197-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5197-128">Remarks</span></span>

<span data-ttu-id="e5197-129">Метод **CreateSession** Инициализирует объект [**Session**](session.md) , собирая параметры, такие как флаги, учетные данные и строку подключения для параметра *соединения* .</span><span class="sxs-lookup"><span data-stu-id="e5197-129">The **CreateSession** method initializes the [**Session**](session.md) object by gathering parameters, such as flags, credentials, and a connection string for the *connection* parameter.</span></span> <span data-ttu-id="e5197-130">**CreateSession** на самом деле не подключается к локальному или удаленному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="e5197-130">**CreateSession** does not actually connect to the local or remote computer.</span></span> <span data-ttu-id="e5197-131">Если соединение не может быть установлено, происходит сбой при выполнении первой операции **сеанса** , такой как [**Get**](session-get.md) или [**reenumerate**](session-enumerate.md), после вызова **CreateSession**.</span><span class="sxs-lookup"><span data-stu-id="e5197-131">If the connection cannot be established, a failure occurs on the first **Session** operation, such as a [**Get**](session-get.md) or [**Enumerate**](session-enumerate.md), after the call to **CreateSession**.</span></span> <span data-ttu-id="e5197-132">Это поведение отличается от [*WMI*](windows-remote-management-glossary.md) -соединения с [*пространством имен*](windows-remote-management-glossary.md) на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e5197-132">This behavior differs from a [*WMI*](windows-remote-management-glossary.md) connection to a [*namespace*](windows-remote-management-glossary.md) on a remote computer.</span></span> <span data-ttu-id="e5197-133">Дополнительные сведения см. в разделе [Служба удаленного управления Windows и инструментарий WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="e5197-133">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="e5197-134">Для вызова этого метода используется следующий пример кода VBScript.</span><span class="sxs-lookup"><span data-stu-id="e5197-134">The following VBScript code example is used to call this method.</span></span>


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



<span data-ttu-id="e5197-135">В следующих примерах показаны различные форматы, используемые для указания сведений о соединении в параметре *подключения* (при создании сеанса HTTPS поле <*адрес*> должно совпадать с именем сертификата компьютера сервера, в противном случае произойдет сбой):</span><span class="sxs-lookup"><span data-stu-id="e5197-135">The following examples show the different formats used to specify connection information in the *connection* parameter (when creating an HTTPS session, the <*Address*> field must match the server computer certificate name, otherwise a failure occurs):</span></span>

-   <span data-ttu-id="e5197-136">"https://service"</span><span class="sxs-lookup"><span data-stu-id="e5197-136">"https://service"</span></span>

    <span data-ttu-id="e5197-137">Использует протокол HTTPS для подключения к расположению веб-службы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5197-137">Uses HTTPS to connect to the default web service location.</span></span>

-   <span data-ttu-id="e5197-138">"https://service.corp.com/websvcs/wsman"</span><span class="sxs-lookup"><span data-stu-id="e5197-138">"https://service.corp.com/websvcs/wsman"</span></span>

    <span data-ttu-id="e5197-139">Использует протокол HTTPS для подключения к определенному расположению веб-службы.</span><span class="sxs-lookup"><span data-stu-id="e5197-139">Uses HTTPS to connect to the specific web service location.</span></span>

-   <span data-ttu-id="e5197-140">"https:// \[ E3D7:0000:0000:0000:51F4:9BC8: c0a8:6420 \] "</span><span class="sxs-lookup"><span data-stu-id="e5197-140">"https://\[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420\]"</span></span>

    <span data-ttu-id="e5197-141">Использует HTTPS и IPv6 с портом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5197-141">Uses HTTPS and IPv6 with the default port.</span></span>

-   <span data-ttu-id="e5197-142">"https:// \[ E3D7:0000:0000:0000:51F4:9BC8: c0a8:6420 \] : 9999/WSMAN"</span><span class="sxs-lookup"><span data-stu-id="e5197-142">"https://\[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420\]:9999/wsman"</span></span>

    <span data-ttu-id="e5197-143">Использует HTTPS и IPv6 с заданным портом.</span><span class="sxs-lookup"><span data-stu-id="e5197-143">Uses HTTPS and IPv6 with the given port.</span></span>

## <a name="examples"></a><span data-ttu-id="e5197-144">Примеры</span><span class="sxs-lookup"><span data-stu-id="e5197-144">Examples</span></span>

<span data-ttu-id="e5197-145">Следующий пример кода VBScript создает сеанс на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e5197-145">The following VBScript code example creates a session on the local computer.</span></span>


```VB
 Set NewSession = Wsman.CreateSession   
   
```



<span data-ttu-id="e5197-146">В следующем примере кода VBScript создается сеанс на удаленном компьютере, который идентифицируется по IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="e5197-146">The following VBScript code example creates a session on a remote computer that is identified by an IP address.</span></span> <span data-ttu-id="e5197-147">Сценарий предоставляет имя пользователя и пароль для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e5197-147">The script supplies a user name and password for an account.</span></span> <span data-ttu-id="e5197-148">Флаги **всманфлагкредусернамепассворд** и **всманфлагусебасик** объединяются, чтобы указать, что учетная запись является локальной учетной записью на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e5197-148">The flags **WSManFlagCredUserNamePassword** and **WSManFlagUseBasic** are combined to indicate that the account is a local account on the remote computer.</span></span> <span data-ttu-id="e5197-149">В случае сбоя создания сеанса сценарий завершается.</span><span class="sxs-lookup"><span data-stu-id="e5197-149">If the creation of the session fails, the script terminates.</span></span> <span data-ttu-id="e5197-150">Скрипт использует методы, возвращающие константу, например [**WSMan. сессионфлагусебасик**](wsman-sessionflagusebasic.md).</span><span class="sxs-lookup"><span data-stu-id="e5197-150">The script uses the methods that return the constant, such as [**WSMan.SessionFlagUseBasic**](wsman-sessionflagusebasic.md).</span></span>

<span data-ttu-id="e5197-151">Чтобы выполнить этот сценарий, необходимо настроить параметры конфигурации по умолчанию как для клиента, так и для сервера, чтобы разрешить незашифрованный трафик и обычную проверку подлинности (для **алловуненкриптед** задано значение **true** , а для параметра Basic — значение **true**).</span><span class="sxs-lookup"><span data-stu-id="e5197-151">To run this script, be aware that you must configure the default configuration settings for both client and server to allow unencrypted traffic and Basic authentication (**AllowUnencrypted** set to **True** and Basic set to **True**).</span></span> <span data-ttu-id="e5197-152">Дополнительные сведения см. в разделе [Установка и настройка для служба удаленного управления Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="e5197-152">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



<span data-ttu-id="e5197-153">В следующем примере кода VBScript учетная запись является учетной записью домена и используется проверка подлинности Negotiate.</span><span class="sxs-lookup"><span data-stu-id="e5197-153">In the following VBScript code example, the account is a domain account and Negotiate authentication is used.</span></span> <span data-ttu-id="e5197-154">При использовании проверки подлинности Negotiate необходимо указать имя пользователя как `computername\username` или `ipaddress\username` .</span><span class="sxs-lookup"><span data-stu-id="e5197-154">With Negotiate authentication, you must specify the user name as `computername\username` or `ipaddress\username`.</span></span>


```VB
iFlags = WSMan.SessionFlagUseNegotiate Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyComputer\MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



## <a name="requirements"></a><span data-ttu-id="e5197-155">Требования</span><span class="sxs-lookup"><span data-stu-id="e5197-155">Requirements</span></span>



| <span data-ttu-id="e5197-156">Требование</span><span class="sxs-lookup"><span data-stu-id="e5197-156">Requirement</span></span> | <span data-ttu-id="e5197-157">Значение</span><span class="sxs-lookup"><span data-stu-id="e5197-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5197-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5197-158">Minimum supported client</span></span><br/> | <span data-ttu-id="e5197-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5197-159">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e5197-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5197-160">Minimum supported server</span></span><br/> | <span data-ttu-id="e5197-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5197-161">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e5197-162">Header</span><span class="sxs-lookup"><span data-stu-id="e5197-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5197-163"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5197-163"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5197-164">IDL</span><span class="sxs-lookup"><span data-stu-id="e5197-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e5197-165"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e5197-165"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="e5197-166">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5197-166">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5197-167"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e5197-167"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e5197-168">DLL</span><span class="sxs-lookup"><span data-stu-id="e5197-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5197-169"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5197-169"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e5197-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5197-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5197-171">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="e5197-171">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="e5197-172">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="e5197-172">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> <dt>

[<span data-ttu-id="e5197-173">**Session**</span><span class="sxs-lookup"><span data-stu-id="e5197-173">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="e5197-174">Проверка подлинности для удаленных подключений</span><span class="sxs-lookup"><span data-stu-id="e5197-174">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> <dt>

[<span data-ttu-id="e5197-175">Установка и настройка для служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="e5197-175">Installation and Configuration for Windows Remote Management</span></span>](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





