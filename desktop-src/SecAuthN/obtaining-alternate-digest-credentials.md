---
description: Чтобы получить учетные данные, отличные от тех, которые связаны с текущим сеансом входа, заполните в секунду \_ \_ структуру удостоверений проверки подлинности WinNT \_ с информацией для альтернативного субъекта безопасности.
ms.assetid: f590ddb5-39a1-4d0c-a787-da938a63c206
title: Получение учетных данных альтернативной дайджеста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260aa1c4cb3bd52395352e2e5dcadcaed7e3fea3cf478367a9e3432c7d2c8d8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921293"
---
# <a name="obtaining-alternate-digest-credentials"></a>Получение учетных данных альтернативной дайджеста

Чтобы получить [*учетные данные*](../secgloss/c-gly.md) , отличные от тех, которые связаны с текущим [*сеансом*](../secgloss/s-gly.md)входа, заполните в [**секунду структуру \_ \_ \_ удостоверений проверки подлинности WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) с информацией для альтернативного [*субъекта безопасности*](../secgloss/s-gly.md). Передайте структуру в функцию [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) с помощью параметра *паусдата* .

В следующей таблице описаны элементы структуры [**\_ \_ \_ удостоверений WinNT auth в секунду**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) .



| Член             | Описание                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **Пользователь**           | Строка, заканчивающаяся нулем, содержащая имя субъекта безопасности, учетные данные которого будут использоваться для установки контекста безопасности. |
| **усерленгс**     | Длина члена **пользователя** в символах. Опустить завершающее значение null.                                                         |
| **Доменная**         | Строка, заканчивающаяся нулем, определяющая домен, содержащий учетную запись субъекта безопасности.                                  |
| **домаинленгс**   | Длина члена **домена** в символах. Опустить завершающее значение null.                                                       |
| **Пароль**       | Строка, заканчивающаяся нулем и содержащая пароль субъекта безопасности.                                                            |
| **пассвордленгс** | Длина элемента **пароля** в символах. Опустить завершающее значение null.                                                     |
| **Флаги**          | Указывает, имеют ли строковые элементы формат ANSI или [*Unicode*](../secgloss/u-gly.md) .  |



 

В следующей таблице перечислены допустимые значения для элемента **flags** структуры.



| Константа                            | Описание                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| с \_ WinNT \_ AUTH \_ удостоверение \_ ANSI    | Строки в этой структуре имеют формат ANSI.                                                                    |
| СЕК \_ . \_ удостоверение проверки подлинности в \_ \_ формате Юникод | Строки в этой структуре имеют формат [*Юникода*](../secgloss/u-gly.md) . |



 

Структура и Константы объявляются в файле заголовков Рпкдце. h, распространяемом с пакетом SDK платформы (Software Development Kit).

В следующем примере демонстрируется вызов на стороне клиента для получения учетных данных дайджеста для конкретной учетной записи пользователя.


```C++
#include <windows.h>

#ifdef UNICODE
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;
#else
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_ANSI;
#endif

void main()
{
    SECURITY_STATUS SecStatus; 
    TimeStamp tsLifetime; 
    CredHandle hCred;
    SEC_WINNT_AUTH_IDENTITY ClientAuthID;
    LPTSTR UserName = TEXT("ASecurityPrinciple");
    LPTSTR DomainName = TEXT("AnAuthenticatingDomain");

    // Initialize the memory.
    ZeroMemory( &ClientAuthID, sizeof(ClientAuthID) );

    // Specify string format for the ClientAuthID structure.


    // Specify an alternate user, domain and password.
      ClientAuthID.User = (unsigned char *) UserName;
      ClientAuthID.UserLength = _tcslen(UserName);

      ClientAuthID.Domain = (unsigned char *) DomainName;
      ClientAuthID.DomainLength = _tcslen(DomainName);

    // Password is an application-defined LPTSTR variable
    // containing the user password.
      ClientAuthID.Password = Password;
      ClientAuthID.PasswordLength = _tcslen(Password);

    // Get the client side credential handle.
    SecStatus = AcquireCredentialsHandle (
      NULL,                  // Default principal.
      WDIGEST_SP_NAME,       // The Digest SSP. 
      SECPKG_CRED_OUTBOUND,  // Client will use the credentials.
      NULL,                  // Do not specify LOGON id.
      &ClientAuthID,         // User information.
      NULL,                  // Not used with Digest SSP.
      NULL,                  // Not used with Digest SSP.
      &hCred,                // Receives the credential handle.
      &tsLifetime            // Receives the credential time limit.
    );
}
```



Функция **\_ ткслен** возвращает длину строки в символах, не включая завершающий символ null.

Если приложение может использовать учетные данные, установленные при входе в систему, см. раздел [Получение учетных данных дайджеста по умолчанию](obtaining-default-digest-credentials.md).

 

 
