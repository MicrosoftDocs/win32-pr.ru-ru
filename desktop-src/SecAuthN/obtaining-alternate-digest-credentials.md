---
description: Чтобы получить учетные данные, отличные от тех, которые связаны с текущим сеансом входа, заполните в секунду \_ \_ структуру удостоверений проверки подлинности WinNT \_ с информацией для альтернативного субъекта безопасности.
ms.assetid: f590ddb5-39a1-4d0c-a787-da938a63c206
title: Получение учетных данных альтернативной дайджеста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed7daa2a3179822929e8c2df8077ee55afaadb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265796"
---
# <a name="obtaining-alternate-digest-credentials"></a><span data-ttu-id="b98a4-103">Получение учетных данных альтернативной дайджеста</span><span class="sxs-lookup"><span data-stu-id="b98a4-103">Obtaining Alternate Digest Credentials</span></span>

<span data-ttu-id="b98a4-104">Чтобы получить [*учетные данные*](../secgloss/c-gly.md) , отличные от тех, которые связаны с текущим [*сеансом*](../secgloss/s-gly.md)входа, заполните в [**секунду структуру \_ \_ \_ удостоверений проверки подлинности WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) с информацией для альтернативного [*субъекта безопасности*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b98a4-104">To obtain [*credentials*](../secgloss/c-gly.md) other than those associated with the current logon [*session*](../secgloss/s-gly.md), populate a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure with information for the alternate [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="b98a4-105">Передайте структуру в функцию [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) с помощью параметра *паусдата* .</span><span class="sxs-lookup"><span data-stu-id="b98a4-105">Pass the structure to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function using the *pAuthData* parameter.</span></span>

<span data-ttu-id="b98a4-106">В следующей таблице описаны элементы структуры [**\_ \_ \_ удостоверений WinNT auth в секунду**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) .</span><span class="sxs-lookup"><span data-stu-id="b98a4-106">The following table describes the members of the [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure.</span></span>



| <span data-ttu-id="b98a4-107">Член</span><span class="sxs-lookup"><span data-stu-id="b98a4-107">Member</span></span>             | <span data-ttu-id="b98a4-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b98a4-108">Description</span></span>                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b98a4-109">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="b98a4-109">**User**</span></span>           | <span data-ttu-id="b98a4-110">Строка, заканчивающаяся нулем, содержащая имя субъекта безопасности, учетные данные которого будут использоваться для установки контекста безопасности.</span><span class="sxs-lookup"><span data-stu-id="b98a4-110">Null-terminated string containing the name of the security principal whose credentials will be used to establish a security context.</span></span> |
| <span data-ttu-id="b98a4-111">**усерленгс**</span><span class="sxs-lookup"><span data-stu-id="b98a4-111">**UserLength**</span></span>     | <span data-ttu-id="b98a4-112">Длина члена **пользователя** в символах.</span><span class="sxs-lookup"><span data-stu-id="b98a4-112">The length of the **User** member, in characters.</span></span> <span data-ttu-id="b98a4-113">Опустить завершающее значение null.</span><span class="sxs-lookup"><span data-stu-id="b98a4-113">Omit the terminating null.</span></span>                                                         |
| <span data-ttu-id="b98a4-114">**Доменная**</span><span class="sxs-lookup"><span data-stu-id="b98a4-114">**Domain**</span></span>         | <span data-ttu-id="b98a4-115">Строка, заканчивающаяся нулем, определяющая домен, содержащий учетную запись субъекта безопасности.</span><span class="sxs-lookup"><span data-stu-id="b98a4-115">Null-terminated string that identifies the domain containing the account of the security principal.</span></span>                                  |
| <span data-ttu-id="b98a4-116">**домаинленгс**</span><span class="sxs-lookup"><span data-stu-id="b98a4-116">**DomainLength**</span></span>   | <span data-ttu-id="b98a4-117">Длина члена **домена** в символах.</span><span class="sxs-lookup"><span data-stu-id="b98a4-117">The length of the **Domain** member, in characters.</span></span> <span data-ttu-id="b98a4-118">Опустить завершающее значение null.</span><span class="sxs-lookup"><span data-stu-id="b98a4-118">Omit the terminating null.</span></span>                                                       |
| <span data-ttu-id="b98a4-119">**Пароль**</span><span class="sxs-lookup"><span data-stu-id="b98a4-119">**Password**</span></span>       | <span data-ttu-id="b98a4-120">Строка, заканчивающаяся нулем и содержащая пароль субъекта безопасности.</span><span class="sxs-lookup"><span data-stu-id="b98a4-120">Null-terminated string containing the password of the security principal.</span></span>                                                            |
| <span data-ttu-id="b98a4-121">**пассвордленгс**</span><span class="sxs-lookup"><span data-stu-id="b98a4-121">**PasswordLength**</span></span> | <span data-ttu-id="b98a4-122">Длина элемента **пароля** в символах.</span><span class="sxs-lookup"><span data-stu-id="b98a4-122">The length of the **Password** member, in characters.</span></span> <span data-ttu-id="b98a4-123">Опустить завершающее значение null.</span><span class="sxs-lookup"><span data-stu-id="b98a4-123">Omit the terminating null.</span></span>                                                     |
| <span data-ttu-id="b98a4-124">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="b98a4-124">**Flags**</span></span>          | <span data-ttu-id="b98a4-125">Указывает, имеют ли строковые элементы формат ANSI или [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b98a4-125">Indicates whether the string members are in ANSI or [*Unicode*](../secgloss/u-gly.md) format.</span></span>  |



 

<span data-ttu-id="b98a4-126">В следующей таблице перечислены допустимые значения для элемента **flags** структуры.</span><span class="sxs-lookup"><span data-stu-id="b98a4-126">The following table lists the valid values for the **Flags** member of the structure.</span></span>



| <span data-ttu-id="b98a4-127">Константа</span><span class="sxs-lookup"><span data-stu-id="b98a4-127">Constant</span></span>                            | <span data-ttu-id="b98a4-128">Описание</span><span class="sxs-lookup"><span data-stu-id="b98a4-128">Description</span></span>                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b98a4-129">с \_ WinNT \_ AUTH \_ удостоверение \_ ANSI</span><span class="sxs-lookup"><span data-stu-id="b98a4-129">SEC\_WINNT\_AUTH\_IDENTITY\_ANSI</span></span>    | <span data-ttu-id="b98a4-130">Строки в этой структуре имеют формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="b98a4-130">Strings in this structure are in ANSI format.</span></span>                                                                    |
| <span data-ttu-id="b98a4-131">СЕК \_ . \_ удостоверение проверки подлинности в \_ \_ формате Юникод</span><span class="sxs-lookup"><span data-stu-id="b98a4-131">SEC\_WINNT\_AUTH\_IDENTITY\_UNICODE</span></span> | <span data-ttu-id="b98a4-132">Строки в этой структуре имеют формат [*Юникода*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b98a4-132">Strings in this structure are in [*Unicode*](../secgloss/u-gly.md) format.</span></span> |



 

<span data-ttu-id="b98a4-133">Структура и Константы объявляются в файле заголовков Рпкдце. h, распространяемом с пакетом SDK платформы (Software Development Kit).</span><span class="sxs-lookup"><span data-stu-id="b98a4-133">The structure and constants are declared in the Rpcdce.h header file distributed with the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="b98a4-134">В следующем примере демонстрируется вызов на стороне клиента для получения учетных данных дайджеста для конкретной учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="b98a4-134">The following example demonstrates a client-side call to obtain Digest credentials for a specific user account.</span></span>


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



<span data-ttu-id="b98a4-135">Функция **\_ ткслен** возвращает длину строки в символах, не включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="b98a4-135">The **\_tcslen** function returns the string length in characters, not including the terminating null character.</span></span>

<span data-ttu-id="b98a4-136">Если приложение может использовать учетные данные, установленные при входе в систему, см. раздел [Получение учетных данных дайджеста по умолчанию](obtaining-default-digest-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="b98a4-136">If your application can use the credentials established at logon, see [Obtaining Default Digest Credentials](obtaining-default-digest-credentials.md).</span></span>

 

 
