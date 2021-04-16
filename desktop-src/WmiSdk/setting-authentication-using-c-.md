---
description: 'Одна из основных задач Ивбемлокатор:: Коннектсервер для WMI — возврат указателя на прокси-сервер IWbemServices.'
ms.assetid: bbff43b7-79f8-4c7b-a772-d3d962cf3859
ms.tgt_platform: multiple
title: Настройка проверки подлинности с помощью C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293d317ac521d36bf7ff616a0340f86c364ce885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702557"
---
# <a name="setting-authentication-using-c"></a><span data-ttu-id="b2f91-103">Настройка проверки подлинности с помощью C++</span><span class="sxs-lookup"><span data-stu-id="b2f91-103">Setting Authentication Using C++</span></span>

<span data-ttu-id="b2f91-104">Одна из основных задач [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) для WMI — возврат указателя на прокси-сервер [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="b2f91-104">One of the main tasks of [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) for WMI is returning a pointer to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy.</span></span> <span data-ttu-id="b2f91-105">С помощью прокси-сервера **IWbemServices** можно получить доступ к ВОЗМОЖНОСТЯМ инфраструктуры WMI.</span><span class="sxs-lookup"><span data-stu-id="b2f91-105">Through the **IWbemServices** proxy, you can access the capabilities of the WMI infrastructure.</span></span> <span data-ttu-id="b2f91-106">Однако указатель на прокси-сервер **IWbemServices** имеет идентификатор процесса клиентского приложения, а не удостоверение процесса **IWbemServices** .</span><span class="sxs-lookup"><span data-stu-id="b2f91-106">However, the pointer to the **IWbemServices** proxy has the identity of the client application process and not the identity of the **IWbemServices** process.</span></span> <span data-ttu-id="b2f91-107">Поэтому при попытке доступа к **IWbemServices** с помощью указателя можно получить код, запрещенный для доступа, такой как **E \_ ACCESSDENIED**.</span><span class="sxs-lookup"><span data-stu-id="b2f91-107">Therefore, if you attempt to access **IWbemServices** with the pointer, you can receive an access-denied code such as **E\_ACCESSDENIED**.</span></span> <span data-ttu-id="b2f91-108">Чтобы избежать ошибки отказа в доступе, необходимо задать удостоверение нового указателя с помощью вызова интерфейса [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="b2f91-108">To avoid the access-denied error, you must set the identity of the new pointer with a call to the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) interface.</span></span>

<span data-ttu-id="b2f91-109">Поставщик может установить безопасность для пространства имен таким образом, чтобы никакие данные не возвращались, если только вы не используете конфиденциальность пакетов (**пктприваци**) в подключении к этому пространству имен.</span><span class="sxs-lookup"><span data-stu-id="b2f91-109">A provider can set the security on a namespace so that no data is returned unless you use packet privacy (**PktPrivacy**) in your connection to that namespace.</span></span> <span data-ttu-id="b2f91-110">Это гарантирует, что данные шифруются по мере пересечения сети.</span><span class="sxs-lookup"><span data-stu-id="b2f91-110">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="b2f91-111">При попытке задать более низкий уровень проверки подлинности будет получено сообщение об отказе в доступе.</span><span class="sxs-lookup"><span data-stu-id="b2f91-111">If you try to set a lower authentication level, you will get an access denied message.</span></span> <span data-ttu-id="b2f91-112">Дополнительные сведения см. в разделе [Настройка дескрипторов безопасности намепаце](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="b2f91-112">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

<span data-ttu-id="b2f91-113">Дополнительные сведения о настройке проверки подлинности в скриптах см. в разделе [Задание уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="b2f91-113">For more information about setting authentication in scripting, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

## <a name="setting-security-on-a-remote-iunknown-interface"></a><span data-ttu-id="b2f91-114">Настройка безопасности на удаленном интерфейсе IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2f91-114">Setting Security on a Remote IUnknown Interface</span></span>

<span data-ttu-id="b2f91-115">В некоторых ситуациях требуется больший доступ к серверу, чем просто указатель на прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="b2f91-115">In some situations, more access to a server than just a pointer to a proxy is required.</span></span> <span data-ttu-id="b2f91-116">Иногда может потребоваться получить безопасное подключение к интерфейсу [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) прокси.</span><span class="sxs-lookup"><span data-stu-id="b2f91-116">At times, you may need to gain a secure connection to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the proxy.</span></span> <span data-ttu-id="b2f91-117">С помощью **IUnknown** можно выполнять запросы к удаленной системе для интерфейсов и других необходимых методов.</span><span class="sxs-lookup"><span data-stu-id="b2f91-117">Using **IUnknown**, you can query the remote system for interfaces and other necessary techniques.</span></span>

<span data-ttu-id="b2f91-118">Если прокси-сервер расположен на удаленном компьютере, сервер делегирует все вызовы интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) прокси-сервера интерфейсу **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="b2f91-118">When a proxy is located on a remote computer, the server delegates all calls to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the proxy to the **IUnknown** interface.</span></span> <span data-ttu-id="b2f91-119">Например, при вызове [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на прокси-сервере, а запрошенный интерфейс не был частью прокси-сервера, прокси-сервер отправляет вызов удаленному серверу.</span><span class="sxs-lookup"><span data-stu-id="b2f91-119">For example, if you call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on a proxy and the requested interface was not part of the proxy, the proxy sends the call to the remote server.</span></span> <span data-ttu-id="b2f91-120">Удаленный сервер, в свою очередь, проверяет наличие соответствующей поддержки интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b2f91-120">In turn, the remote server checks for the appropriate interface support.</span></span> <span data-ttu-id="b2f91-121">Если сервер поддерживает интерфейс, COM маршалирует новый прокси обратно клиенту, чтобы приложение может использовать новый интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b2f91-121">If the server does support the interface, COM marshals a new proxy back to the client so that the application can use the new interface.</span></span>

<span data-ttu-id="b2f91-122">Проблемы возникают, если клиент не имеет разрешений на доступ к удаленному серверу, но использует учетные данные пользователя, который выполняет.</span><span class="sxs-lookup"><span data-stu-id="b2f91-122">Problems arise if the client does not have access permissions to the remote server, yet is using the credentials of a user that does.</span></span> <span data-ttu-id="b2f91-123">В этом случае любая попытка доступа к [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на удаленном сервере завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="b2f91-123">In this situation, any attempt to access [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the remote server fails.</span></span> <span data-ttu-id="b2f91-124">В окончательном выпуске прокси-сервера также происходит сбой, так как текущий пользователь не имеет доступа к удаленному серверу.</span><span class="sxs-lookup"><span data-stu-id="b2f91-124">The final release on the proxy fails as well, because the current user does not have access to the remote server.</span></span> <span data-ttu-id="b2f91-125">Симптомом этого является одна или две секунды, прежде чем клиентское приложение завершится сбоем окончательной версии прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="b2f91-125">A symptom of this is a one or two second lag before the client application fails the final proxy release.</span></span> <span data-ttu-id="b2f91-126">Сбой происходит из-за того, что COM пытается получить доступ к удаленному серверу, используя параметры безопасности по умолчанию текущего пользователя, которые не включают измененные учетные данные, которым разрешен доступ к серверу в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="b2f91-126">The failure occurs because COM attempted to access the remote server using the default security settings of the current user, which do not include the modified credentials that allowed access to the server in the first place.</span></span> <span data-ttu-id="b2f91-127">Дополнительные сведения см. в разделе [Настройка параметров безопасности для IWbemServices и других учетных записей-посредников](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="b2f91-127">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="b2f91-128">Чтобы избежать сбоя соединения, используйте метод [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) , чтобы явно задать проверку подлинности в указателе, возвращенном из [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="b2f91-128">To avoid the failed connection, use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to explicitly set the security authentication on the pointer returned from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="b2f91-129">С помощью **CoSetProxyBlanket** можно убедиться, что удаленный сервер получает правильный идентификатор проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b2f91-129">Using **CoSetProxyBlanket**, you can ensure that the remote server receives the correct authentication identity.</span></span>

<span data-ttu-id="b2f91-130">В следующем примере кода показано, как использовать [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) для доступа к удаленному интерфейсу [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b2f91-130">The following code example shows how to use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to access a remote [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>


```C++
SEC_WINNT_AUTH_IDENTITY_W* pAuthIdentity = 
   new SEC_WINNT_AUTH_IDENTITY_W;
ZeroMemory(pAuthIdentity, sizeof(SEC_WINNT_AUTH_IDENTITY_W));

pAuthIdentity->User = new WCHAR[32];
StringCbCopyW(pAuthIdentity->User,sizeof(L"MyUser"),L"MyUser");
pAuthIdentity->UserLength = wcslen(pAuthIdentity->User);

pAuthIdentity->Domain = new WCHAR[32];
StringCbCopyW(pAuthIdentity->Domain,sizeof(L"MyDomain"),L"MyDomain");
pAuthIdentity->DomainLength = wcslen(pAuthIdentity->Domain);

pAuthIdentity->Password = new WCHAR[32];
pAuthIdentity->Password[0] = NULL;
pAuthIdentity->PasswordLength = wcslen( pAuthIdentity->Password);

pAuthIdentity->Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

IWbemServices* pWbemServices = 0;

// Set proxy security
hr = CoSetProxyBlanket(pWbemServices, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pWbemServices->Release();
   return 1;
}

// Set IUnknown security
IUnknown*    pUnk = NULL;
pWbemServices->QueryInterface(IID_IUnknown, (void**) &pUnk);

hr = CoSetProxyBlanket(pUnk, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pUnk->Release();
   pWbemServices->Release();
   delete [] pAuthIdentity->User;
   delete [] pAuthIdentity->Domain;
   delete [] pAuthIdentity->Password;
   delete pAuthIdentity;   
   return 1;
}

// cleanup IUnknown
pUnk->Release();

//
// Perform a bunch of operations
//

// Cleanup
pWbemServices->Release();

delete [] pAuthIdentity->User;
delete [] pAuthIdentity->Domain;
delete [] pAuthIdentity->Password;

delete pAuthIdentity;
```



> [!Note]  
> <span data-ttu-id="b2f91-131">При настройке безопасности для интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) прокси-сервера COM создает копию прокси-сервера, которую невозможно освободить, пока не будет вызван метод [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="b2f91-131">When you set security on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of a proxy, COM creates a copy of the proxy that cannot be released until you call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b2f91-132">См. также</span><span class="sxs-lookup"><span data-stu-id="b2f91-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2f91-133">Настройка проверки подлинности в WMI</span><span class="sxs-lookup"><span data-stu-id="b2f91-133">Setting Authentication in WMI</span></span>](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
