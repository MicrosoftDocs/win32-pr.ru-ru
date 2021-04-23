---
description: Когда клиентское приложение впервые входит в инструментарий управления Windows (WMI) (WMI), оно должно задать уровень безопасности процесса по умолчанию с помощью вызова CoInitializeSecurity.
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: Настройка уровня безопасности процесса по умолчанию с помощью C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bb51deb2c228f0958209c774e7526b4eeed958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546871"
---
# <a name="setting-the-default-process-security-level-using-c"></a><span data-ttu-id="08681-103">Настройка уровня безопасности процесса по умолчанию с помощью C++</span><span class="sxs-lookup"><span data-stu-id="08681-103">Setting the Default Process Security Level Using C++</span></span>

<span data-ttu-id="08681-104">Когда клиентское приложение впервые входит в инструментарий управления Windows (WMI) (WMI), оно должно задать уровень безопасности процесса по умолчанию с помощью вызова [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="08681-104">When a client application logs on to Windows Management Instrumentation (WMI) for the first time, it must set the default process security level with a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="08681-105">COM использует информацию в вызове, чтобы определить, какой объем безопасности должен иметь другой процесс для доступа к процессу клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="08681-105">COM uses the information in the call to determine how much security another process must have to access the client application process.</span></span>

<span data-ttu-id="08681-106">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="08681-106">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="08681-107">Изменение учетных данных проверки подлинности по умолчанию с помощью C++</span><span class="sxs-lookup"><span data-stu-id="08681-107">Changing the Default Authentication Credentials Using C++</span></span>](#changing-the-default-authentication-credentials-using-c)
-   [<span data-ttu-id="08681-108">Изменение уровней олицетворения по умолчанию с помощью C++</span><span class="sxs-lookup"><span data-stu-id="08681-108">Changing the Default Impersonation Levels Using C++</span></span>](#changing-the-default-impersonation-levels-using-c)

<span data-ttu-id="08681-109">Для большинства клиентских приложений аргументы, приведенные в следующем примере, задают параметры безопасности по умолчанию для WMI.</span><span class="sxs-lookup"><span data-stu-id="08681-109">For most client applications the arguments shown in the following example set the default security for WMI.</span></span>


```C++
HRESULT hr = NULL;
hr = CoInitializeSecurity(
        NULL,                       // security descriptor
       -1,                          // use this simple setting
       NULL,                        // use this simple setting
       NULL,                        // reserved
       RPC_C_AUTHN_LEVEL_DEFAULT,   // authentication level  
       RPC_C_IMP_LEVEL_IMPERSONATE, // impersonation level
       NULL,                        // use this simple setting
       EOAC_NONE,                   // no special capabilities
       NULL);                          // reserved

if (FAILED(hr))
{
  CoUninitialize();
  cout << "Failed to initialize security. Error code = 0x"
       << hex << hr << endl;
  return;
}
```



<span data-ttu-id="08681-110">Для правильной компиляции кода требуются следующие ссылки и \# операторы include.</span><span class="sxs-lookup"><span data-stu-id="08681-110">The code requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="08681-111">Установка уровня проверки подлинности на **\_ уровне RPC C \_ AUTHN \_ \_ Default** позволяет DCOM согласовать уровень проверки подлинности в соответствии с требованиями безопасности конечного компьютера.</span><span class="sxs-lookup"><span data-stu-id="08681-111">Setting the authentication level to **RPC\_C\_AUTHN\_LEVEL\_DEFAULT** allows DCOM to negotiate the authentication level to match the security demands of the target computer.</span></span> <span data-ttu-id="08681-112">Дополнительные сведения см. в разделе [изменение учетных данных проверки подлинности по умолчанию с помощью c++](#changing-the-default-authentication-credentials-using-c) и [изменение параметров олицетворения по умолчанию с помощью c++](#changing-the-default-impersonation-levels-using-c).</span><span class="sxs-lookup"><span data-stu-id="08681-112">For more information, see [Changing the Default Authentication Credentials Using C++](#changing-the-default-authentication-credentials-using-c) and [Changing the Default Impersonation Settings Using C++](#changing-the-default-impersonation-levels-using-c).</span></span>

## <a name="changing-the-default-authentication-credentials-using-c"></a><span data-ttu-id="08681-113">Изменение учетных данных проверки подлинности по умолчанию с помощью C++</span><span class="sxs-lookup"><span data-stu-id="08681-113">Changing the Default Authentication Credentials Using C++</span></span>

<span data-ttu-id="08681-114">Учетные данные проверки подлинности по умолчанию работают в большинстве ситуаций, но в разных ситуациях может потребоваться использовать разные учетные данные проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="08681-114">The default authentication credentials work for most situations, but you might need to use different authentication credentials in different situations.</span></span> <span data-ttu-id="08681-115">Например, может потребоваться добавить шифрование в процедуры проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="08681-115">For example, you might want to add encryption to the authentication procedures.</span></span>

<span data-ttu-id="08681-116">В следующей таблице перечислены и описаны различные уровни проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="08681-116">The following table lists and describes the different levels of authentication.</span></span>



| <span data-ttu-id="08681-117">Уровень проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="08681-117">Authentication level</span></span>                 | <span data-ttu-id="08681-118">Описание</span><span class="sxs-lookup"><span data-stu-id="08681-118">Description</span></span>                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08681-119">\_ \_ \_ по умолчанию на уровне RPC C AUTHN \_</span><span class="sxs-lookup"><span data-stu-id="08681-119">RPC\_C\_AUTHN\_LEVEL\_DEFAULT</span></span>        | <span data-ttu-id="08681-120">Проверка подлинности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="08681-120">Default security authentication.</span></span>                                                      |
| <span data-ttu-id="08681-121">\_уровень RPC \_ C \_ AUTHN \_ None</span><span class="sxs-lookup"><span data-stu-id="08681-121">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           | <span data-ttu-id="08681-122">Без проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="08681-122">No authentication.</span></span>                                                                    |
| <span data-ttu-id="08681-123">\_подключение на уровне RPC C \_ AUTHN \_ \_</span><span class="sxs-lookup"><span data-stu-id="08681-123">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        | <span data-ttu-id="08681-124">Проверка подлинности только в том случае, если клиент создает связь с сервером.</span><span class="sxs-lookup"><span data-stu-id="08681-124">Authentication only when the client creates a relationship with the server.</span></span>           |
| <span data-ttu-id="08681-125">\_ \_ \_ вызов уровня RPC C \_ AUTHN</span><span class="sxs-lookup"><span data-stu-id="08681-125">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           | <span data-ttu-id="08681-126">Проверка подлинности каждый раз, когда сервер получает RPC.</span><span class="sxs-lookup"><span data-stu-id="08681-126">Authentication each time the server receives an RPC.</span></span>                                  |
| <span data-ttu-id="08681-127">\_PKT на уровне RPC C \_ AUTHN \_ \_</span><span class="sxs-lookup"><span data-stu-id="08681-127">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            | <span data-ttu-id="08681-128">Проверка подлинности каждый раз, когда сервер получает данные от клиента.</span><span class="sxs-lookup"><span data-stu-id="08681-128">Authentication each time the server receives data from a client.</span></span>                      |
| <span data-ttu-id="08681-129">\_ \_ \_ \_ целостность PKT RPC C AUTHN Level \_</span><span class="sxs-lookup"><span data-stu-id="08681-129">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> | <span data-ttu-id="08681-130">Проверка подлинности, не изменяющая данные из пакета.</span><span class="sxs-lookup"><span data-stu-id="08681-130">Authentication that no data from the packet has been modified.</span></span>                        |
| <span data-ttu-id="08681-131">\_Конфиденциальность RPC C \_ AUTHN \_ Level \_ PKT \_</span><span class="sxs-lookup"><span data-stu-id="08681-131">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   | <span data-ttu-id="08681-132">Включает все предыдущие уровни проверки подлинности и шифрует значение каждого вызова RPC.</span><span class="sxs-lookup"><span data-stu-id="08681-132">Includes all previous authentication levels, and encrypts the value of each RPC call.</span></span> |



 

<span data-ttu-id="08681-133">Можно указать учетные данные проверки подлинности по умолчанию для нескольких пользователей, используя **единственную структуру \_ \_ списка проверки подлинности** в параметре *пауслист* параметра [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="08681-133">You can specify the default authentication credentials for multiple users by using a **SOLE\_AUTHENTICATION\_LIST** structure in the *pAuthList* parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

<span data-ttu-id="08681-134">В следующем примере кода показано, как изменить учетные данные для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="08681-134">The following code example shows how to change the authentication credentials.</span></span>


```C++
// Auth Identity structure
SEC_WINNT_AUTH_IDENTITY_W        authidentity;
SecureZeroMemory( &authidentity, sizeof(authidentity) );

authidentity.User = L"MyUser";
authidentity.UserLength = wcslen( authidentity.User );
authidentity.Domain = L"MyDomain ";
authidentity.DomainLength = wcslen( authidentity.Domain );
authidentity.Password = L"";
authidentity.PasswordLength = wcslen( authidentity.Password );
authidentity.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

SecureZeroMemory( authninfo, sizeof(SOLE_AUTHENTICATION_INFO)*2 );

// NTLM Settings
authninfo[0].dwAuthnSvc = RPC_C_AUTHN_WINNT;
authninfo[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[0].pAuthInfo = &authidentity;

// Kerberos Settings
authninfo[1].dwAuthnSvc = RPC_C_AUTHN_GSS_KERBEROS ;
authninfo[1].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[1].pAuthInfo = &authidentity;

SOLE_AUTHENTICATION_LIST    authentlist;

authentlist.cAuthInfo = 2;
authentlist.aAuthInfo = authninfo;

CoInitializeSecurity( 
  NULL, 
  -1, 
  NULL, 
  NULL, 
  RPC_C_AUTHN_LEVEL_CALL, 
  RPC_C_IMP_LEVEL_IMPERSONATE,
  &authentlist, 
  EOAC_NONE,
  NULL);
```



## <a name="changing-the-default-impersonation-levels-using-c"></a><span data-ttu-id="08681-135">Изменение уровней олицетворения по умолчанию с помощью C++</span><span class="sxs-lookup"><span data-stu-id="08681-135">Changing the Default Impersonation Levels Using C++</span></span>

<span data-ttu-id="08681-136">COM предоставляет уровни безопасности по умолчанию, считанные из системного реестра.</span><span class="sxs-lookup"><span data-stu-id="08681-136">COM provides default security levels read from the system registry.</span></span> <span data-ttu-id="08681-137">Однако, если не было специально изменено, параметры реестра, установленные на уровне олицетворения, слишком низкие для работы инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="08681-137">However, unless specifically modified, the registry settings set the impersonation level too low for WMI to function.</span></span> <span data-ttu-id="08681-138">Как правило, уровень олицетворения по умолчанию — это **\_ \_ \_ \_ Определение на уровне Imp RPC c**, но для работы с большинством поставщиков инструментарию WMI требуется по крайней мере **\_ уровень RPC c, \_ \_ \_ олицетворение** , и, возможно, возникает ситуация, когда необходимо установить более высокий уровень олицетворения.</span><span class="sxs-lookup"><span data-stu-id="08681-138">Typically, the default impersonation level is **RPC\_C\_IMP\_LEVEL\_IDENTIFY**, but WMI needs at least **RPC\_C\_IMP\_LEVEL\_IMPERSONATE** to function with most providers, and you might encounter a situation where you need to set a higher level of impersonation.</span></span> <span data-ttu-id="08681-139">Дополнительные сведения см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="08681-139">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="08681-140">В следующей таблице перечислены различные уровни олицетворения.</span><span class="sxs-lookup"><span data-stu-id="08681-140">The following table lists the different levels of impersonation.</span></span>



| <span data-ttu-id="08681-141">Level</span><span class="sxs-lookup"><span data-stu-id="08681-141">Level</span></span>                           | <span data-ttu-id="08681-142">Описание</span><span class="sxs-lookup"><span data-stu-id="08681-142">Description</span></span>                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08681-143">\_ \_ \_ по умолчанию на уровне Imp RPC C \_</span><span class="sxs-lookup"><span data-stu-id="08681-143">RPC\_C\_IMP\_LEVEL\_DEFAULT</span></span>     | <span data-ttu-id="08681-144">Операционная система выбирает уровень олицетворения.</span><span class="sxs-lookup"><span data-stu-id="08681-144">The operating system chooses the level of impersonation.</span></span>                                                      |
| <span data-ttu-id="08681-145">\_ \_ \_ Анонимный уровень RPC \_ C</span><span class="sxs-lookup"><span data-stu-id="08681-145">RPC\_C\_IMP\_LEVEL\_ANONYMOUS</span></span>   | <span data-ttu-id="08681-146">Сервер может олицетворять клиента, но маркер олицетворения не может использоваться ни для чего.</span><span class="sxs-lookup"><span data-stu-id="08681-146">The server can impersonate the client, but the impersonation token cannot be used for anything.</span></span>               |
| <span data-ttu-id="08681-147">\_Обнаружение на \_ \_ уровне Imp RPC C \_</span><span class="sxs-lookup"><span data-stu-id="08681-147">RPC\_C\_IMP\_LEVEL\_IDENTIFY</span></span>    | <span data-ttu-id="08681-148">Сервер может получить удостоверение клиента и олицетворять клиента для проверки ACL.</span><span class="sxs-lookup"><span data-stu-id="08681-148">The server can obtain the identity of the client and impersonate the client for ACL checking.</span></span>                 |
| <span data-ttu-id="08681-149">\_ \_ \_ олицетворение на уровне \_ Imp RPC C</span><span class="sxs-lookup"><span data-stu-id="08681-149">RPC\_C\_IMP\_LEVEL\_IMPERSONATE</span></span> | <span data-ttu-id="08681-150">Сервер может олицетворять клиента на одной границе компьютера.</span><span class="sxs-lookup"><span data-stu-id="08681-150">The server can impersonate the client across one computer boundary.</span></span>                                           |
| <span data-ttu-id="08681-151">\_ \_ \_ ДЕЛЕГАТ уровня Imp RPC \_ C</span><span class="sxs-lookup"><span data-stu-id="08681-151">RPC\_C\_IMP\_LEVEL\_DELEGATE</span></span>    | <span data-ttu-id="08681-152">Сервер может олицетворять клиента через несколько границ и выполнять вызовы от имени клиента.</span><span class="sxs-lookup"><span data-stu-id="08681-152">The server can impersonate the client across multiple boundaries, and can make calls on behalf of the client.</span></span> |



 

 

 
