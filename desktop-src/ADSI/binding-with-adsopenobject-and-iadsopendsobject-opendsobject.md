---
title: Привязка с помощью ADsOpenObject и Иадсопендсобжект Опендсобжект
description: Функция ADsOpenObject и метод Иадсопендсобжект Опендсобжект используются для привязки к объектам службы каталогов, когда необходимо указать альтернативные учетные данные и требуется шифрование данных.
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- Привязка с помощью ADsOpenObject и Иадсопендсобжект Опендсобжект ADSI
- ADSI ADSI, использование, привязка с помощью ADsOpenObject и Иадсопендсобжект Опендсобжект
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a249aa3d51520d0d345b5a098f84480e5b5016
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070614"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a><span data-ttu-id="a5ead-105">Привязка с ADsOpenObject и Иадсопендсобжект:: Опендсобжект</span><span class="sxs-lookup"><span data-stu-id="a5ead-105">Binding With ADsOpenObject and IADsOpenDSObject::OpenDSObject</span></span>

<span data-ttu-id="a5ead-106">Функция [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) и метод [**Иадсопендсобжект:: опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) используются для привязки к объектам службы каталогов, если необходимо указать альтернативные учетные данные и требуется шифрование данных.</span><span class="sxs-lookup"><span data-stu-id="a5ead-106">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method are used to bind to directory service objects when alternate credentials must be specified and when data encryption is required.</span></span>

<span data-ttu-id="a5ead-107">По возможности следует использовать учетные данные вызывающего потока.</span><span class="sxs-lookup"><span data-stu-id="a5ead-107">The credentials of the calling thread should be used when possible.</span></span> <span data-ttu-id="a5ead-108">Однако, если необходимо использовать альтернативные учетные данные, необходимо использовать функцию [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) или метод [**Иадсопендсобжект:: опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .</span><span class="sxs-lookup"><span data-stu-id="a5ead-108">However, if alternate credentials must be used, the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function or the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method must be used.</span></span> <span data-ttu-id="a5ead-109">Если используются альтернативные учетные данные, важно не кэшировать пароль.</span><span class="sxs-lookup"><span data-stu-id="a5ead-109">If alternate credentials are used, it is important to not cache the password.</span></span> <span data-ttu-id="a5ead-110">Можно выполнить несколько операций привязки, указав имя пользователя и пароль для первой операции привязки, а затем указав только имя пользователя в последующих привязках.</span><span class="sxs-lookup"><span data-stu-id="a5ead-110">Multiple bind operations can be performed by specifying the user name and password for the first bind operation and then specifying only the user name in subsequent binds.</span></span> <span data-ttu-id="a5ead-111">Система настраивает сеанс при первом вызове и использует тот же сеанс при последующих вызовах привязки при условии, что выполняются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="a5ead-111">The system sets up a session on the first call and uses the same session on subsequent bind calls as long as the following conditions are met:</span></span>

-   <span data-ttu-id="a5ead-112">Одно и то же имя пользователя в каждой операции привязки.</span><span class="sxs-lookup"><span data-stu-id="a5ead-112">The same user name in each bind operation.</span></span>
-   <span data-ttu-id="a5ead-113">Реализуйте бессерверную привязку или привяжите к одному и тому же серверу в каждой операции привязки.</span><span class="sxs-lookup"><span data-stu-id="a5ead-113">Implement serverless binding or bind to the same server in each bind operation.</span></span>
-   <span data-ttu-id="a5ead-114">Сохраните открытый сеанс, нажимая на ссылку на объект в одной из операций привязки.</span><span class="sxs-lookup"><span data-stu-id="a5ead-114">Maintain an open session by holding on to an object reference from one of the bind operations.</span></span> <span data-ttu-id="a5ead-115">Сеанс закрывается при освобождении последней ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="a5ead-115">The session is closed when the last object reference is released.</span></span>

<span data-ttu-id="a5ead-116">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) и [**Иадсопендсобжект:: Опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) используют [интерфейсы поставщика поддержки безопасности Windows NT (SSPI)](/windows/desktop/SecAuthN/sspi) для обеспечения гибкости при использовании параметров проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a5ead-116">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) use the Windows NT [Security Support Provider Interfaces (SSPI)](/windows/desktop/SecAuthN/sspi) to allow flexibility in authentication options.</span></span> <span data-ttu-id="a5ead-117">Основным преимуществом использования этих интерфейсов является предоставление различных типов проверки подлинности для Active Directory клиентов и шифрования сеанса.</span><span class="sxs-lookup"><span data-stu-id="a5ead-117">The major advantage of using these interfaces is to provide different types of authentication to Active Directory clients and to encrypt the session.</span></span> <span data-ttu-id="a5ead-118">В настоящее время ADSI не разрешает передачу сертификатов.</span><span class="sxs-lookup"><span data-stu-id="a5ead-118">Currently, ADSI does not allow certificates to be passed in.</span></span> <span data-ttu-id="a5ead-119">Таким образом, можно использовать SSL для шифрования, а затем Kerberos, NTLM или простую проверку подлинности в зависимости от того, как установлены флаги в параметре *двресервед* .</span><span class="sxs-lookup"><span data-stu-id="a5ead-119">Therefore, you can use SSL for encryption and then Kerberos, NTLM, or simple authentication, depending on how the flags are set on the *dwReserved* parameter.</span></span>

<span data-ttu-id="a5ead-120">В ADSI нельзя запрашивать конкретный поставщик SSPI, хотя всегда получается самый высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="a5ead-120">You cannot request a specific SSPI provider in ADSI, although you always get the highest preference protocol.</span></span> <span data-ttu-id="a5ead-121">В случае привязки клиента Windows к компьютеру под управлением Windows используется протокол Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a5ead-121">In the case of a Windows client binding to a computer running Windows, the protocol is Kerberos.</span></span> <span data-ttu-id="a5ead-122">Не разрешайте проверку подлинности сертификата в случае веб-страницы, так как проверка подлинности выполняется перед запуском веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="a5ead-122">Not allowing a certificate for authentication is acceptable in the case of a webpage because authentication occurs prior to running the webpage.</span></span>

<span data-ttu-id="a5ead-123">Хотя открытые операции позволяют указать пользователя и пароль, делать это не следует.</span><span class="sxs-lookup"><span data-stu-id="a5ead-123">Although Open operations allow you to specify a user and password, you should not do so.</span></span> <span data-ttu-id="a5ead-124">Вместо этого не указывайте учетные данные и неявно используйте учетные данные контекста безопасности вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="a5ead-124">Instead, do not specify any credentials and implicitly use the credentials of the caller's security context.</span></span> <span data-ttu-id="a5ead-125">Чтобы выполнить привязку к объекту каталога с помощью учетных данных вызывающего объекта с [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) или [**Иадсопендсобжект:: Опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), укажите **значение NULL** как для имени пользователя, так и для пароля.</span><span class="sxs-lookup"><span data-stu-id="a5ead-125">To bind to a directory object using the caller's credentials with [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) or [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), specify **NULL** for both user name and password.</span></span>

<span data-ttu-id="a5ead-126">Наконец, чтобы выполнить привязку без проверки подлинности, используйте флаг **\_ без \_ проверки подлинности ADS** .</span><span class="sxs-lookup"><span data-stu-id="a5ead-126">Finally, to bind with no authentication, use the **ADS\_NO\_AUTHENTICATION** flag.</span></span> <span data-ttu-id="a5ead-127">Без проверки подлинности указывает, что ADSI пытается выполнить привязку в качестве анонимного пользователя к целевому объекту и не выполняет проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="a5ead-127">No authentication indicates that ADSI attempts to bind as an anonymous user to the target object and performs no authentication.</span></span> <span data-ttu-id="a5ead-128">Это эквивалентно запросу анонимной привязки в протоколе LDAP и показывает, что все пользователи включены в контекст безопасности.</span><span class="sxs-lookup"><span data-stu-id="a5ead-128">This is equivalent to requesting anonymous binding in LDAP and indicates that all users are included in the security context.</span></span>

<span data-ttu-id="a5ead-129">Если флаги проверки подлинности имеют значение 0, ADSI выполняет простую привязку, отправку в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="a5ead-129">If the authentication flags are set to zero, ADSI performs a simple bind, sent as plaintext.</span></span>

> [!Caution]  
> <span data-ttu-id="a5ead-130">Если имя пользователя и пароль указаны без указания флагов проверки подлинности, имя пользователя и пароль передаются по сети в виде открытого текста, что является угрозой безопасности.</span><span class="sxs-lookup"><span data-stu-id="a5ead-130">If a user name and password are specified without specifying authentication flags, the user name and password are transmitted over the network in plaintext, which is a security risk.</span></span> <span data-ttu-id="a5ead-131">Не указывайте имя пользователя и пароль, не указывая флаги проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a5ead-131">Do not specify a user name and password without specifying authentication flags.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a5ead-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="a5ead-132">Examples</span></span>

<span data-ttu-id="a5ead-133">В следующем Visual Basic примере кода показано, как использовать метод [**иадсопендсобжект:: опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .</span><span class="sxs-lookup"><span data-stu-id="a5ead-133">The following Visual Basic code example shows how to use the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method.</span></span>


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



<span data-ttu-id="a5ead-134">В следующем примере кода C++ показано, как использовать функцию [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="a5ead-134">The following C++ code example shows how to use the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>


```C++
IADs *pObject;
HRESULT hr;

hr = ADsOpenObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,
    (void**)&pObject);
if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}
```



<span data-ttu-id="a5ead-135">Интерфейс [**иадсопендсобжект**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) также можно использовать в C++, но дублирует функцию [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="a5ead-135">The [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) interface can also be used in C++, but it duplicates the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>

<span data-ttu-id="a5ead-136">В следующем примере кода C++ показано, как использовать интерфейс [**иадсопендсобжект**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) для выполнения той же операции привязки, что и в приведенном выше примере кода.</span><span class="sxs-lookup"><span data-stu-id="a5ead-136">The following C++ code example shows how to use the [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) interface to perform the same bind operation as in the code example above.</span></span>


```C++
IADsOpenDSObject *pDSO;
HRESULT hr;
 
hr = ADsGetObject(L"LDAP:", IID_IADsOpenDSObject, (void**)&pDSO);
if(SUCCEEDED(hr))
{
    IDispatch *pDisp;

    hr = pDSO->OpenDSObject(CComBSTR("LDAP://CN=jeffsmith,DC=fabrikam,DC=com"),
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION, 
        &pDisp);
    if(SUCCEEDED(hr))
    {
        IADs *pObject;

        hr = pDisp->QueryInterface(IID_IADs, (void**) &pObject);
        if(SUCCEEDED(hr))
        {
            // Use the object.

            // Release the object.
            pObject->Release();
        }

        pDisp->Release();
    }
    
    pDSO->Release();
}
```



 

 