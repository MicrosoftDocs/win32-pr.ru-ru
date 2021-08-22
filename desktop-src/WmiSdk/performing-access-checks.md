---
description: Проверка доступа определяет, предоставляет ли дескриптор безопасности указанный набор прав доступа клиенту или потоку, определяемым маркером доступа.
ms.assetid: d0259bb1-fd74-4440-ac2a-d6aa84a48d9b
ms.tgt_platform: multiple
title: Выполнение проверок доступа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e06f2bccab886b38b53ecc3592371555b8c93a0ed12cdad0a4f039b62d62752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050512"
---
# <a name="performing-access-checks"></a>Выполнение проверок доступа

Проверка доступа определяет, предоставляет ли дескриптор безопасности указанный набор прав доступа клиенту или потоку, определяемым маркером доступа. Функцию [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) можно вызвать из клиентских приложений WMI или поставщиков, написанных на C++ или C#. скрипты и Visual Basic приложения не могут выполнять проверки доступа с помощью описанного здесь метода.

Клиентские приложения должны выполнить проверку доступа, чтобы определить удостоверение обратного вызова при возврате результатов в приемник, предоставленный асинхронным вызовом клиента.

Если поставщики не могут олицетворять клиентское приложение или сценарий, запрашивающие данные, они должны выполнять проверки доступа в следующих ситуациях:

-   При доступе к ресурсам, которые не защищены списками управления доступом (ACL).
-   Когда клиент подключается на уровне олицетворения с помощью **\_ \_ \_ идентификатора RPC C** .

> [!Note]  
> Приложения C++ и C# могут контролировать, выполняются ли проверки доступа отдельным процессом. сценарии и Visual Basic приложения могут считывать или изменять раздел реестра, чтобы убедиться, что инструментарий WMI выполняет проверки доступа. Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).

 

В примере кода в этом разделе для правильной компиляции требуются следующие ссылки и \# операторы include.


```C++
#include <lmcons.h>
#define _WIN32_DCOM
#define SECURITY_WIN32
#include <wbemidl.h>
#include <security.h>
#include <safestr.h>
#pragma comment(lib, "wbemuuid.lib")
#pragma comment(lib, "Secur32.lib")
```



В следующем примере кода показано, как проверить, что маркер безопасности потока клиентского приложения содержит разрешения, соответствующие указанному дескриптору безопасности. Функция принимает строку " \\ пользователь домена" и возвращает идентификатор безопасности. Если вызов завершается неудачно, функция возвращает **значение NULL**, в противном случае вызывающий объект должен освободить возвращаемый указатель.


```C++
BYTE * GetSid(LPWSTR pwcUserName)
{
    DWORD dwSidSize = 0, dwDomainSize = 0;
    SID_NAME_USE use;

    // first call is to get the size
    BOOL bRet = LookupAccountNameW(

      NULL,            // system name
      pwcUserName,     // account name
      NULL,            // security identifier
      &dwSidSize,      // size of security identifier
      NULL,            // domain name
      &dwDomainSize,   // size of domain name
      &use             // SID-type indicator
      );    

    if(bRet == FALSE && ERROR_INSUFFICIENT_BUFFER 
        != GetLastError())\
        return NULL;

    BYTE * buff = new BYTE[dwSidSize];

    if(buff == NULL)
        return NULL;

    WCHAR * pwcDomain = new WCHAR[dwDomainSize];

    if(pwcDomain == NULL)

    {
        delete [] buff;
        return FALSE;
    }

    // Call to LookupAccountNameW actually gets the SID
    bRet = LookupAccountNameW(

      NULL,           // system name
      pwcUserName,    // account name
      buff,           // security identifier
      &dwSidSize,     // size of security identifier
      pwcDomain,      // domain name
      &dwDomainSize,  // size of domain name
      &use            // SID-type indicator
      );    

    delete [] pwcDomain;

    if(bRet == FALSE)
    {
        delete [] buff;
        return NULL;
    }

    return buff;
}

// This returns true if the caller is coming 
//   from the expected computer in the expected domain.

BOOL IsAllowed(LPWSTR pwsExpectedDomain, 
   LPWSTR pwsExpectedMachine)
{

    WCHAR wCallerName[UNLEN + 1];
    DWORD nSize = UNLEN + 1;

// Impersonate the caller and get its name

    HRESULT hr = CoImpersonateClient();
    if(FAILED(hr))

        return FALSE;

    BOOL bRet = GetUserNameExW(NameSamCompatible, 
       wCallerName, &nSize);

    CoRevertToSelf();

    if(bRet == FALSE)

        return FALSE;


    // take the expected domain and lan manager 
    //   style name and create a SID.  In actual
    // production code, it would be more efficient 
    //   to do this only when necessary

    WCHAR wExpectedName[UNLEN + 1];

    HRESULT hrCopyCat;
    hrCopyCat = StringCchCopy(wExpectedName,
        sizeof(pwsExpectedDomain)*sizeof(WCHAR)+1, 
        pwsExpectedDomain);
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = 
        StringCchCat(wExpectedName,sizeof(wExpectedName)
        + 2*sizeof(WCHAR)+1, L"\\");
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = StringCchCat(wExpectedName,sizeof(wExpectedName)
        + sizeof(pwsExpectedMachine)*sizeof(WCHAR)+1, 
        pwsExpectedMachine);
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = StringCchCat(wExpectedName,sizeof(wExpectedName)
        + sizeof(WCHAR)+1, L"$");
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
  

    // convert the two names to SIDs and compare.  
    // Note that SIDs are used since 
    //   the format of the names might vary.  

    BYTE * pCaller = GetSid(wCallerName);

    if(pCaller == NULL)

        return FALSE;

    BYTE * pExpected = GetSid(wExpectedName);

    if(pExpected == NULL)
    {
        delete [] pCaller;

        return FALSE;
    }

    bRet = EqualSid((PSID)pCaller, (PSID)pExpected);

    delete [] pCaller;
    delete [] pExpected;

    return bRet;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Выбор правильной регистрации](choosing-correct-registration.md)
</dt> <dt>

[Поддержание безопасности WMI](maintaining-wmi-security.md)
</dt> <dt>

[Защита поставщика](securing-your-provider.md)
</dt> <dt>

[Доступ к пространствам имен WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
