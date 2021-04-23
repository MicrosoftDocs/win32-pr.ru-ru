---
description: Проверка доступа определяет, предоставляет ли дескриптор безопасности указанный набор прав доступа клиенту или потоку, определяемым маркером доступа.
ms.assetid: d0259bb1-fd74-4440-ac2a-d6aa84a48d9b
ms.tgt_platform: multiple
title: Выполнение проверок доступа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9af65605b6e96a5ad8b820de876d553f8d19202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702660"
---
# <a name="performing-access-checks"></a><span data-ttu-id="43e03-103">Выполнение проверок доступа</span><span class="sxs-lookup"><span data-stu-id="43e03-103">Performing Access Checks</span></span>

<span data-ttu-id="43e03-104">Проверка доступа определяет, предоставляет ли дескриптор безопасности указанный набор прав доступа клиенту или потоку, определяемым маркером доступа.</span><span class="sxs-lookup"><span data-stu-id="43e03-104">An access check determines whether a security descriptor grants a specified set of access rights to the client or thread identified by an access token.</span></span> <span data-ttu-id="43e03-105">Функцию [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) можно вызвать из клиентских приложений WMI или поставщиков, написанных на C++ или C#.</span><span class="sxs-lookup"><span data-stu-id="43e03-105">You can call the security function [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) from WMI client applications or providers written in C++ or C#.</span></span> <span data-ttu-id="43e03-106">Скрипты и Visual Basic приложения не могут выполнять проверки доступа с помощью описанного здесь метода.</span><span class="sxs-lookup"><span data-stu-id="43e03-106">Scripts and Visual Basic applications cannot perform access checks using the method described here.</span></span>

<span data-ttu-id="43e03-107">Клиентские приложения должны выполнить проверку доступа, чтобы определить удостоверение обратного вызова при возврате результатов в приемник, предоставленный асинхронным вызовом клиента.</span><span class="sxs-lookup"><span data-stu-id="43e03-107">Client applications should do an access check to determine the identity of the callback when returning results to the sink provided by the client asynchronous call.</span></span>

<span data-ttu-id="43e03-108">Если поставщики не могут олицетворять клиентское приложение или сценарий, запрашивающие данные, они должны выполнять проверки доступа в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="43e03-108">When providers cannot impersonate the client application or script that is requesting data, they should perform access checks for the following situations:</span></span>

-   <span data-ttu-id="43e03-109">При доступе к ресурсам, которые не защищены списками управления доступом (ACL).</span><span class="sxs-lookup"><span data-stu-id="43e03-109">When accessing resources that are not protected by access control lists (ACL).</span></span>
-   <span data-ttu-id="43e03-110">Когда клиент подключается на уровне олицетворения с помощью **\_ \_ \_ идентификатора RPC C** .</span><span class="sxs-lookup"><span data-stu-id="43e03-110">When the client has connected at the **RPC\_C\_LEVEL\_IDENTIFY** impersonation level.</span></span>

> [!Note]  
> <span data-ttu-id="43e03-111">Приложения C++ и C# могут контролировать, выполняются ли проверки доступа отдельным процессом.</span><span class="sxs-lookup"><span data-stu-id="43e03-111">C++ and C# applications can control whether access checks are performed by a separate process.</span></span> <span data-ttu-id="43e03-112">Сценарии и Visual Basic приложения могут считывать или изменять раздел реестра, чтобы убедиться, что инструментарий WMI выполняет проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="43e03-112">Scripts and Visual Basic applications can read or change a registry key to ensure that WMI performs access checks.</span></span> <span data-ttu-id="43e03-113">Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="43e03-113">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

 

<span data-ttu-id="43e03-114">В примере кода в этом разделе для правильной компиляции требуются следующие ссылки и \# операторы include.</span><span class="sxs-lookup"><span data-stu-id="43e03-114">The code example in this topic requires the following references and \#include statements to compile correctly.</span></span>


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



<span data-ttu-id="43e03-115">В следующем примере кода показано, как проверить, что маркер безопасности потока клиентского приложения содержит разрешения, соответствующие указанному дескриптору безопасности.</span><span class="sxs-lookup"><span data-stu-id="43e03-115">The following code example shows how to check that the security token of a client application thread contains permissions appropriate to a specified security descriptor.</span></span> <span data-ttu-id="43e03-116">Функция принимает строку " \\ пользователь домена" и возвращает идентификатор безопасности.</span><span class="sxs-lookup"><span data-stu-id="43e03-116">The function takes the string "domain\\user" and returns the SID.</span></span> <span data-ttu-id="43e03-117">Если вызов завершается неудачно, функция возвращает **значение NULL**, в противном случае вызывающий объект должен освободить возвращаемый указатель.</span><span class="sxs-lookup"><span data-stu-id="43e03-117">If the call fails, the function returns **NULL**, otherwise the caller must free the returned pointer.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="43e03-118">См. также</span><span class="sxs-lookup"><span data-stu-id="43e03-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43e03-119">Выбор правильной регистрации</span><span class="sxs-lookup"><span data-stu-id="43e03-119">Choosing Correct Registration</span></span>](choosing-correct-registration.md)
</dt> <dt>

[<span data-ttu-id="43e03-120">Поддержание безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="43e03-120">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="43e03-121">Защита поставщика</span><span class="sxs-lookup"><span data-stu-id="43e03-121">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="43e03-122">Доступ к пространствам имен WMI</span><span class="sxs-lookup"><span data-stu-id="43e03-122">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
