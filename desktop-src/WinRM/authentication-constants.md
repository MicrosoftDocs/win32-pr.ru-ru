---
title: Константы проверки подлинности (Всмандисп. h)
description: Укажите метод проверки подлинности и способ обработки серверов сертификатов для транспорта запросов по протоколу HTTPS.
ms.assetid: adfefbc9-c386-48db-a0c2-145aa4f91bfa
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagCredUsernamePassword
- WSManFlagSkipCACheck
- WSManFlagSkipCNCheck
- WSManFlagUseNoAuthentication
- WSManFlagUseDigest
- WSManFlagUseNegotiate
- WSManFlagUseBasic
- WSManFlagUseKerberos
- WSManFlagNoEncryption
- WSManFlagUseClientCertificate
- WSManFlagUseCredSsp
- WSManFlagSkipRevocationCheck
- WSManFlagAllowNegotiateImplicitCredentials
- WSManFlagUseSsl
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce45d1474cf6c925149c05ae348231333c3356e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535159"
---
# <a name="authentication-constants"></a><span data-ttu-id="d6f06-103">Константы проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="d6f06-103">Authentication Constants</span></span>

<span data-ttu-id="d6f06-104">Константы проверки подлинности — это константы в перечислении **\_ \_ всмансессионфлагс** , которые указывают метод проверки подлинности и способ обработки серверов сертификатов для транспорта запросов по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d6f06-104">Authentication constants are constants in the **\_\_WSManSessionFlags** enumeration that specify the authentication method and how to handle certificate servers for HTTPS transport of requests.</span></span>

<span data-ttu-id="d6f06-105">Одна или несколько констант, перечисленных в следующем списке, являются обязательными в параметре *flags* в вызовах [**WSMan. CreateSession**](wsman-createsession.md) или в вызовах [**ивсман:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) , подключающихся к удаленному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="d6f06-105">One or more of the constants listed in the following list are required in the *flags* parameter in calls to [**WSMan.CreateSession**](wsman-createsession.md) or in [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) calls that connect to a remote computer.</span></span>

<dl> <dt>

<span data-ttu-id="d6f06-106"><span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**всманфлагкредусернамепассворд**</span><span class="sxs-lookup"><span data-stu-id="d6f06-106"><span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f06-107">4096 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="d6f06-107">4096 (0x1000)</span></span>
</dt> <dt>



<span data-ttu-id="d6f06-108">Используйте имя пользователя и пароль в качестве учетных данных.</span><span class="sxs-lookup"><span data-stu-id="d6f06-108">Use the user name and password as the credentials.</span></span> <span data-ttu-id="d6f06-109">Установите этот флаг при создании объекта [**ConnectionOptions**](connectionoptions.md) и укажите [**имя пользователя**](connectionoptions-username.md) и [**пароль**](connectionoptions-password.md).</span><span class="sxs-lookup"><span data-stu-id="d6f06-109">Set this flag when you create a [**ConnectionOptions**](connectionoptions.md) object and supply [**Username**](connectionoptions-username.md) and [**Password**](connectionoptions-password.md).</span></span> <span data-ttu-id="d6f06-110">Учетные данные могут быть учетной записью домена или учетной записью на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d6f06-110">The credentials can be a domain account or an account on the local computer.</span></span> <span data-ttu-id="d6f06-111">По умолчанию учетная запись должна быть членом локальной группы администраторов на локальном или удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d6f06-111">By default, the account must be a member of the local Administrators group on the local or remote computer.</span></span> <span data-ttu-id="d6f06-112">Однако службу WinRM можно настроить для предоставления другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="d6f06-112">However, the WinRM service can be configured to allow other users.</span></span> <span data-ttu-id="d6f06-113">Дополнительные сведения см. в разделе [Установка и настройка для служба удаленного управления Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="d6f06-113">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span> <span data-ttu-id="d6f06-114">Этот флаг можно установить при указании учетных данных для проверки подлинности согласования (также известной как [*Встроенная проверка подлинности Windows*](windows-remote-management-glossary.md)) или [*обычной проверки подлинности*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="d6f06-114">You can set this flag when you specify credentials for Negotiate authentication (also known as [*Windows Integrated Authentication*](windows-remote-management-glossary.md)) or for [*Basic authentication*](windows-remote-management-glossary.md).</span></span>

<span data-ttu-id="d6f06-115">Связанный метод создания скриптов — это [**WSMan. сессионфлагкредусернамепассворд**](wsman-sessionflagcredusernamepassword.md), а метод C++ — [**ивсманекс. сессионфлагкредусернамепассворд**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).</span><span class="sxs-lookup"><span data-stu-id="d6f06-115">The associated scripting method is [**WSMan.SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md), and the C++ method is [**IWSManEx.SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6f06-116"><span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**всманфлагскипкачекк**</span><span class="sxs-lookup"><span data-stu-id="d6f06-116"><span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f06-117">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="d6f06-117">8192 (0x2000)</span></span>
</dt> <dt>



<span data-ttu-id="d6f06-118">При подключении по протоколу HTTPS клиент не проверяет, подписан ли сертификат сервера доверенным центром сертификации (ЦС).</span><span class="sxs-lookup"><span data-stu-id="d6f06-118">When connecting over HTTPS, the client does not validate that the server certificate is signed by a trusted certification authority (CA).</span></span> <span data-ttu-id="d6f06-119">Используйте это значение только в том случае, если удаленный компьютер является доверенным другим средством, например, если удаленный компьютер является частью сети, физически защищенной и изолированной, либо удаленный компьютер указан как доверенный узел в конфигурации WinRM.</span><span class="sxs-lookup"><span data-stu-id="d6f06-119">Use this value only when the remote computer is trusted by other means, for example, if the remote computer is part of a network that is physically secure and isolated or the remote computer is listed as a trusted host in the WinRM configuration.</span></span>

<span data-ttu-id="d6f06-120">Связанный метод создания скриптов — это [**WSMan. сессионфлагскипкачекк**](wsman-sessionflagskipcacheck.md), а метод C++ — [**ивсманекс. сессионфлагскипкачекк**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).</span><span class="sxs-lookup"><span data-stu-id="d6f06-120">The associated scripting method is [**WSMan.SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md), and the C++ method is [**IWSManEx.SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6f06-121"><span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**всманфлагскипкнчекк**</span><span class="sxs-lookup"><span data-stu-id="d6f06-121"><span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f06-122">16384 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="d6f06-122">16384 (0x4000)</span></span>
</dt> <dt>



<span data-ttu-id="d6f06-123">При подключении по протоколу HTTPS клиент не будет проверять, соответствует ли общее имя (CN) в сертификате сервера имени компьютера в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="d6f06-123">When connecting over HTTPS, the client will not validate that the common name (CN) in the server certificate matches the computer name in the connection string.</span></span> <span data-ttu-id="d6f06-124">Используйте только в том случае, если удаленный компьютер является доверенным другим средством, например, если удаленный компьютер является частью сети, физически защищенной и изолированной, либо удаленный компьютер указан как доверенный узел в конфигурации WinRM.</span><span class="sxs-lookup"><span data-stu-id="d6f06-124">Use only when the remote computer is trusted by other means, for example, if the remote computer is part of a network that is physically secure and isolated or the remote computer is listed as a trusted host in the WinRM configuration.</span></span>

<span data-ttu-id="d6f06-125">Связанный метод создания скриптов — это [**WSMan. сессионфлагскипкнчекк**](wsman-sessionflagskipcncheck.md), а метод C++ — [**ивсманекс. сессионфлагскипкнчекк**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).</span><span class="sxs-lookup"><span data-stu-id="d6f06-125">The associated scripting method is [**WSMan.SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md), and the C++ method is [**IWSManEx.SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6f06-126"><span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**всманфлагусеноаусентикатион**</span><span class="sxs-lookup"><span data-stu-id="d6f06-126"><span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f06-127">32768 (0x8000)</span><span class="sxs-lookup"><span data-stu-id="d6f06-127">32768 (0x8000)</span></span>
</dt> <dt>



<span data-ttu-id="d6f06-128">Не использовать проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="d6f06-128">Use no authentication.</span></span> <span data-ttu-id="d6f06-129">Укажите эту константу при проверке подключения к удаленному компьютеру, чтобы определить, настроен ли для службы, реализующей Протокол WS-Management, прослушивание запросов данных.</span><span class="sxs-lookup"><span data-stu-id="d6f06-129">Specify this constant when testing a connection to a remote computer to determine if a service that implements the WS-Management protocol is configured to listen for data requests.</span></span> <span data-ttu-id="d6f06-130">**Всманфлагусеноаусентикатион** нельзя сочетать с другими константами [**сеанса**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="d6f06-130">**WSManFlagUseNoAuthentication** cannot be combined with any other [**Session**](session.md) constant.</span></span> <span data-ttu-id="d6f06-131">Связанный метод создания скриптов — это [**WSMan. сессионфлагусеноаусентикатион**](wsman-sessionflagusenoauthentication.md), а метод C++ — [**всманекс. сессионфлагусеноаусентикатион**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).</span><span class="sxs-lookup"><span data-stu-id="d6f06-131">The associated scripting method is [**WSMan.SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md), and the C++ method is [**WSManEx.SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6f06-132"><span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**всманфлагуседижест**</span><span class="sxs-lookup"><span data-stu-id="d6f06-132"><span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f06-133">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="d6f06-133">65536 (0x10000)</span></span>
</dt> <dt>



<span data-ttu-id="d6f06-134">Использовать дайджест-проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="d6f06-134">Use Digest authentication.</span></span> <span data-ttu-id="d6f06-135">Инициировать запрос дайджест-проверки подлинности может только клиентский компьютер.</span><span class="sxs-lookup"><span data-stu-id="d6f06-135">Only the client computer can initiate a Digest authentication request.</span></span> <span data-ttu-id="d6f06-136">Клиент отправляет запрос на сервер для проверки подлинности и получения строки токена с сервера.</span><span class="sxs-lookup"><span data-stu-id="d6f06-136">The client sends a request to the server to authenticate and receives a token string from the server.</span></span> <span data-ttu-id="d6f06-137">Затем клиент отправляет запрос ресурса, включая имя пользователя и криптографический хэш пароля, в сочетании со строкой токена.</span><span class="sxs-lookup"><span data-stu-id="d6f06-137">The client then sends the resource request, including the user name and a cryptographic hash of the password combined with the token string.</span></span> <span data-ttu-id="d6f06-138">Дайджест-проверка подлинности поддерживается для HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d6f06-138">Digest authentication is supported for HTTP and HTTPS.</span></span> <span data-ttu-id="d6f06-139">Клиентские скрипты и приложения WinRM могут указывать дайджест-проверку подлинности, но не службу.</span><span class="sxs-lookup"><span data-stu-id="d6f06-139">WinRM client scripts and applications can specify Digest authentication, but not the service.</span></span>

<span data-ttu-id="d6f06-140">Связанный метод создания скриптов — это [**WSMan. сессионфлагуседижест**](wsman-sessionflagusedigest.md), а метод C++ — [**ивсманекс. сессионфлагуседижест**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).</span><span class="sxs-lookup"><span data-stu-id="d6f06-140">The associated scripting method is [**WSMan.SessionFlagUseDigest**](wsman-sessionflagusedigest.md), and the C++ method is [**IWSManEx.SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6f06-141"><span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**всманфлагусенеготиате**</span><span class="sxs-lookup"><span data-stu-id="d6f06-141"><span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f06-142">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="d6f06-142">131072 (0x20000)</span></span>
</dt> <dt>



<span data-ttu-id="d6f06-143">Использовать проверку подлинности Negotiate.</span><span class="sxs-lookup"><span data-stu-id="d6f06-143">Use Negotiate authentication.</span></span> <span data-ttu-id="d6f06-144">Клиент отправляет запрос на сервер для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="d6f06-144">The client sends a request to the server to authenticate.</span></span> <span data-ttu-id="d6f06-145">Сервер определяет, следует ли использовать Kerberos или NTLM.</span><span class="sxs-lookup"><span data-stu-id="d6f06-145">The server determines whether to use Kerberos or NTLM.</span></span> <span data-ttu-id="d6f06-146">Выбран протокол Kerberos для проверки подлинности учетной записи домена, и для учетных записей локального компьютера выбран протокол NTLM.</span><span class="sxs-lookup"><span data-stu-id="d6f06-146">Kerberos is selected to authenticate a domain account and NTLM is selected for local computer accounts.</span></span> <span data-ttu-id="d6f06-147">Имя пользователя должно быть указано в формате домен \\ имя_пользователя для пользователя домена или имени пользователя ServerName \\ для локального пользователя на компьютере сервера.</span><span class="sxs-lookup"><span data-stu-id="d6f06-147">The user name should be specified in the form domain\\username for a domain user or servername\\username for a local user on a server computer.</span></span>

<span data-ttu-id="d6f06-148">[Управление учетными записями пользователей (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) влияет на доступ к службе WinRM.</span><span class="sxs-lookup"><span data-stu-id="d6f06-148">[User Account Control (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) affects access to the WinRM service.</span></span> <span data-ttu-id="d6f06-149">Если в Рабочей группе или домене используется проверка подлинности Negotiate, доступ к службе может получить только встроенная учетная запись администратора.</span><span class="sxs-lookup"><span data-stu-id="d6f06-149">When Negotiate authentication is used in a workgroup or domain, only the built-in Administrator account can access the service.</span></span> <span data-ttu-id="d6f06-150">Чтобы разрешить всем учетным записям в группе "Администраторы" доступ к службе, присвойте следующему разделу реестра значение 1: **hKey \_ Local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ политики \\ System \\ LocalAccountTokenFilterPolicy**.</span><span class="sxs-lookup"><span data-stu-id="d6f06-150">To allow all accounts in the Administrators group to access the service, set the following registry key to 1: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\system\\LocalAccountTokenFilterPolicy**.</span></span>

<span data-ttu-id="d6f06-151">Связанный метод создания скриптов — это [**WSMan. сессионфлагусенеготиате**](wsman-sessionflagusenegotiate.md), а метод C++ — [**ивсманекс. сессионфлагусенеготиате**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).</span><span class="sxs-lookup"><span data-stu-id="d6f06-151">The associated scripting method is [**WSMan.SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md), and the C++ method is [**IWSManEx.SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6f06-152"><span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**всманфлагусебасик**</span><span class="sxs-lookup"><span data-stu-id="d6f06-152"><span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f06-153">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="d6f06-153">262144 (0x40000)</span></span>
</dt> <dt>



<span data-ttu-id="d6f06-154">Используйте обычную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="d6f06-154">Use Basic authentication.</span></span> <span data-ttu-id="d6f06-155">Клиент предоставляет учетные данные в виде имени пользователя и пароля, которые передаются непосредственно в сообщении запроса.</span><span class="sxs-lookup"><span data-stu-id="d6f06-155">The client presents credentials in the form of a user name and password, directly transmitted in the request message.</span></span> <span data-ttu-id="d6f06-156">Можно указать только учетные данные, которые определяют учетную запись локального администратора на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d6f06-156">You can specify only credentials that identify a local administrator account on the remote computer.</span></span>

<span data-ttu-id="d6f06-157">Связанный метод создания скриптов — это [**WSMan. сессионфлагусебасик**](wsman-sessionflagusebasic.md), а метод C++ — [**ивсманекс. сессионфлагусебасик**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).</span><span class="sxs-lookup"><span data-stu-id="d6f06-157">The associated scripting method is [**WSMan.SessionFlagUseBasic**](wsman-sessionflagusebasic.md), and the C++ method is [**IWSManEx.SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6f06-158"><span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**всманфлагусекерберос**</span><span class="sxs-lookup"><span data-stu-id="d6f06-158"><span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f06-159">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="d6f06-159">524288 (0x80000)</span></span>
</dt> <dt>



<span data-ttu-id="d6f06-160">Используйте проверку подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="d6f06-160">Use Kerberos authentication.</span></span> <span data-ttu-id="d6f06-161">Клиент и сервер выполняют взаимную проверку подлинности с помощью билетов Kerberos.</span><span class="sxs-lookup"><span data-stu-id="d6f06-161">The client and server mutually authenticate using Kerberos tickets.</span></span>

<span data-ttu-id="d6f06-162">Связанный метод создания скриптов — это [**WSMan. сессионфлагусекерберос**](wsman-sessionflagusekerberos.md), а метод C++ — [**ивсманекс. WSMan. сессионфлагусекерберос**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).</span><span class="sxs-lookup"><span data-stu-id="d6f06-162">The associated scripting method is [**WSMan.SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md), and the C++ method is [**IWSManEx.WSMan.SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6f06-163"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**всманфлагноенкриптион**</span><span class="sxs-lookup"><span data-stu-id="d6f06-163"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f06-164">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="d6f06-164">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="d6f06-165">Не использовать шифрование.</span><span class="sxs-lookup"><span data-stu-id="d6f06-165">Use no encryption.</span></span> <span data-ttu-id="d6f06-166">По умолчанию незашифрованный трафик не разрешен и должен быть включен как на клиенте, так и на сервере.</span><span class="sxs-lookup"><span data-stu-id="d6f06-166">Unencrypted traffic is not allowed by default and must be enabled on both the client and server.</span></span>

<span data-ttu-id="d6f06-167">Связанный метод создания скриптов — это [**WSMan. сессионфлагноенкриптион**](wsman-sessionflagnoencryption.md), а метод C++ — [**ивсманекс. сессионфлагноенкриптион**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span><span class="sxs-lookup"><span data-stu-id="d6f06-167">The associated scripting method is [**WSMan.SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md), and the C++ method is [**IWSManEx.SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6f06-168"><span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**всманфлагусеклиентцертификате**</span><span class="sxs-lookup"><span data-stu-id="d6f06-168"><span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f06-169">2097152 (0x200000)</span><span class="sxs-lookup"><span data-stu-id="d6f06-169">2097152 (0x200000)</span></span>
</dt> <dt>



<span data-ttu-id="d6f06-170">Использовать проверку подлинности на основе сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="d6f06-170">Use client certificate-based authentication.</span></span>

<span data-ttu-id="d6f06-171">Связанный метод создания скриптов — это [**WSMan. сессионфлагусеклиентцертификате**](wsman-sessionflaguseclientcert.md), а метод C++ — [**IWSManEx2. сессионфлагусеклиентцертификате**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).</span><span class="sxs-lookup"><span data-stu-id="d6f06-171">The associated scripting method is [**WSMan.SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md), and the C++ method is [**IWSManEx2.SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6f06-172"><span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**всманфлагусекредссп**</span><span class="sxs-lookup"><span data-stu-id="d6f06-172"><span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f06-173">16777216 (0x1000000)</span><span class="sxs-lookup"><span data-stu-id="d6f06-173">16777216 (0x1000000)</span></span>
</dt> <dt>



<span data-ttu-id="d6f06-174">Используйте проверку подлинности с помощью поставщика поддержки безопасности учетных данных (CredSSP).</span><span class="sxs-lookup"><span data-stu-id="d6f06-174">Use Credential Security Support Provider (CredSSP) authentication.</span></span>

<span data-ttu-id="d6f06-175">Связанный метод создания скриптов — это [**WSMan. сессионфлагусекредссп**](wsman-sessionflagusecredssp.md), а метод C++ — [**IWSManEx3. сессионфлагусекредссп**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).</span><span class="sxs-lookup"><span data-stu-id="d6f06-175">The associated scripting method is [**WSMan.SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md), and the C++ method is [**IWSManEx3.SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6f06-176"><span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**всманфлагскипревокатиончекк**</span><span class="sxs-lookup"><span data-stu-id="d6f06-176"><span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f06-177">0x2000000</span><span class="sxs-lookup"><span data-stu-id="d6f06-177">0x2000000</span></span>
</dt> <dt>



<span data-ttu-id="d6f06-178">Не проверять отзыв сертификата во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="d6f06-178">Do not check for certificate revocation during authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6f06-179"><span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**всманфлагалловнеготиатеимплиЦиткредентиалс**</span><span class="sxs-lookup"><span data-stu-id="d6f06-179"><span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f06-180">0x4000000</span><span class="sxs-lookup"><span data-stu-id="d6f06-180">0x4000000</span></span>
</dt> <dt>



<span data-ttu-id="d6f06-181">Разрешить неявные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="d6f06-181">Allow implicit credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6f06-182"><span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**всманфлагусессл**</span><span class="sxs-lookup"><span data-stu-id="d6f06-182"><span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6f06-183">0x8000000</span><span class="sxs-lookup"><span data-stu-id="d6f06-183">0x8000000</span></span>
</dt> <dt>



<span data-ttu-id="d6f06-184">Используйте защищенный уровень сокетов, включает протокол HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d6f06-184">Use Secure Socket Layer, enables HTTPS.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6f06-185">Требования</span><span class="sxs-lookup"><span data-stu-id="d6f06-185">Requirements</span></span>



| <span data-ttu-id="d6f06-186">Требование</span><span class="sxs-lookup"><span data-stu-id="d6f06-186">Requirement</span></span> | <span data-ttu-id="d6f06-187">Значение</span><span class="sxs-lookup"><span data-stu-id="d6f06-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f06-188">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6f06-188">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f06-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6f06-189">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="d6f06-190">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6f06-190">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f06-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6f06-191">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d6f06-192">Header</span><span class="sxs-lookup"><span data-stu-id="d6f06-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6f06-193"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6f06-193"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6f06-194">IDL</span><span class="sxs-lookup"><span data-stu-id="d6f06-194">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d6f06-195"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6f06-195"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6f06-196">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6f06-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f06-197">Константы сеанса</span><span class="sxs-lookup"><span data-stu-id="d6f06-197">Session Constants</span></span>](session-constants.md)
</dt> </dl>

 

 





