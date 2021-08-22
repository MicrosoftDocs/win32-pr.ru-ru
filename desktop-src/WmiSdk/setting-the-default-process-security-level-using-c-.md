---
description: когда клиентское приложение впервые входит в инструментарий управления Windows (WMI) (WMI), оно должно задать уровень безопасности процесса по умолчанию с помощью вызова CoInitializeSecurity.
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: Настройка уровня безопасности процесса по умолчанию с помощью C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcaec4ebbcd39c8cee9ee8aae002621a4a5a1853d1e4cfd4282194115c15ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050292"
---
# <a name="setting-the-default-process-security-level-using-c"></a>Настройка уровня безопасности процесса по умолчанию с помощью C++

когда клиентское приложение впервые входит в инструментарий управления Windows (WMI) (WMI), оно должно задать уровень безопасности процесса по умолчанию с помощью вызова [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). COM использует информацию в вызове, чтобы определить, какой объем безопасности должен иметь другой процесс для доступа к процессу клиентского приложения.

В этом разделе обсуждаются следующие разделы:

-   [Изменение учетных данных проверки подлинности по умолчанию с помощью C++](#changing-the-default-authentication-credentials-using-c)
-   [Изменение уровней олицетворения по умолчанию с помощью C++](#changing-the-default-impersonation-levels-using-c)

Для большинства клиентских приложений аргументы, приведенные в следующем примере, задают параметры безопасности по умолчанию для WMI.


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



Для правильной компиляции кода требуются следующие ссылки и \# операторы include.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



Установка уровня проверки подлинности на **\_ уровне RPC C \_ AUTHN \_ \_ Default** позволяет DCOM согласовать уровень проверки подлинности в соответствии с требованиями безопасности конечного компьютера. дополнительные сведения см. в разделе [изменение учетных данных проверки подлинности по умолчанию с помощью c++](#changing-the-default-authentication-credentials-using-c) и [изменение Параметры олицетворения по умолчанию с помощью c++](#changing-the-default-impersonation-levels-using-c).

## <a name="changing-the-default-authentication-credentials-using-c"></a>Изменение учетных данных проверки подлинности по умолчанию с помощью C++

Учетные данные проверки подлинности по умолчанию работают в большинстве ситуаций, но в разных ситуациях может потребоваться использовать разные учетные данные проверки подлинности. Например, может потребоваться добавить шифрование в процедуры проверки подлинности.

В следующей таблице перечислены и описаны различные уровни проверки подлинности.



| Уровень проверки подлинности                 | Описание                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| \_ \_ \_ по умолчанию на уровне RPC C AUTHN \_        | Проверка подлинности по умолчанию.                                                      |
| \_уровень RPC \_ C \_ AUTHN \_ None           | Без проверки подлинности.                                                                    |
| \_подключение на уровне RPC C \_ AUTHN \_ \_        | Проверка подлинности только в том случае, если клиент создает связь с сервером.           |
| \_ \_ \_ вызов уровня RPC C \_ AUTHN           | Проверка подлинности каждый раз, когда сервер получает RPC.                                  |
| \_PKT на уровне RPC C \_ AUTHN \_ \_            | Проверка подлинности каждый раз, когда сервер получает данные от клиента.                      |
| \_ \_ \_ \_ целостность PKT RPC C AUTHN Level \_ | Проверка подлинности, не изменяющая данные из пакета.                        |
| \_Конфиденциальность RPC C \_ AUTHN \_ Level \_ PKT \_   | Включает все предыдущие уровни проверки подлинности и шифрует значение каждого вызова RPC. |



 

Можно указать учетные данные проверки подлинности по умолчанию для нескольких пользователей, используя **единственную структуру \_ \_ списка проверки подлинности** в параметре *пауслист* параметра [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

В следующем примере кода показано, как изменить учетные данные для проверки подлинности.


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



## <a name="changing-the-default-impersonation-levels-using-c"></a>Изменение уровней олицетворения по умолчанию с помощью C++

COM предоставляет уровни безопасности по умолчанию, считанные из системного реестра. Однако, если не было специально изменено, параметры реестра, установленные на уровне олицетворения, слишком низкие для работы инструментария WMI. Как правило, уровень олицетворения по умолчанию — это **\_ \_ \_ \_ Определение на уровне Imp RPC c**, но для работы с большинством поставщиков инструментарию WMI требуется по крайней мере **\_ уровень RPC c, \_ \_ \_ олицетворение** , и, возможно, возникает ситуация, когда необходимо установить более высокий уровень олицетворения. Дополнительные сведения см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md). В следующей таблице перечислены различные уровни олицетворения.



| Уровень                           | Описание                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ по умолчанию на уровне Imp RPC C \_     | Операционная система выбирает уровень олицетворения.                                                      |
| \_ \_ \_ Анонимный уровень RPC \_ C   | Сервер может олицетворять клиента, но маркер олицетворения не может использоваться ни для чего.               |
| \_Обнаружение на \_ \_ уровне Imp RPC C \_    | Сервер может получить удостоверение клиента и олицетворять клиента для проверки ACL.                 |
| \_ \_ \_ олицетворение на уровне \_ Imp RPC C | Сервер может олицетворять клиента на одной границе компьютера.                                           |
| \_ \_ \_ ДЕЛЕГАТ уровня Imp RPC \_ C    | Сервер может олицетворять клиента через несколько границ и выполнять вызовы от имени клиента. |



 

 

 
