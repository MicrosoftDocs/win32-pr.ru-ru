---
title: Составление имен участников-служб для службы Рпкнс
description: В следующем примере кода солагаются имена субъектов-служб (SPN) для службы RPC, которая имеет запись в контейнере Рпксервицес в каталоге. Служба RPC использует функцию Рпкнсбиндинжекспорт для создания записи Рпксервицес.
ms.assetid: 4fd585b3-3f9b-4f7f-bc1b-22879587a590
ms.tgt_platform: multiple
keywords:
- Составление имен участников-служб для службы Рпкнс AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb65b377b5bdd041c5a34b05262f7e62f43801c5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487488"
---
# <a name="composing-spns-for-an-rpcns-service"></a><span data-ttu-id="3e6c0-105">Составление имен участников-служб для службы Рпкнс</span><span class="sxs-lookup"><span data-stu-id="3e6c0-105">Composing SPNs for an RpcNs Service</span></span>

<span data-ttu-id="3e6c0-106">В следующем примере кода солагаются имена субъектов-служб (SPN) для службы RPC, которая имеет запись в контейнере Рпксервицес в каталоге.</span><span class="sxs-lookup"><span data-stu-id="3e6c0-106">The following code example composes the service principal names (SPNs) for an RPC service that has an entry in the RpcServices container in the directory.</span></span> <span data-ttu-id="3e6c0-107">Служба RPC использует функцию [**рпкнсбиндинжекспорт**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) для создания записи рпксервицес.</span><span class="sxs-lookup"><span data-stu-id="3e6c0-107">An RPC service uses the [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) function to create its RpcServices entry.</span></span>

<span data-ttu-id="3e6c0-108">Служба RPC использует этот пример кода для создания имени субъекта-службы или SPN, которые обозначают экземпляр службы.</span><span class="sxs-lookup"><span data-stu-id="3e6c0-108">An RPC service uses this code example to build the SPN or SPNs that identify an instance of the service.</span></span> <span data-ttu-id="3e6c0-109">Эта подпрограммы используется службой для выполнения следующих задач.</span><span class="sxs-lookup"><span data-stu-id="3e6c0-109">The service uses this routine to perform the following tasks:</span></span>

-   <span data-ttu-id="3e6c0-110">Регистрация или Отмена регистрации имен участников-служб в каталоге при установке или удалении службы.</span><span class="sxs-lookup"><span data-stu-id="3e6c0-110">To register or unregister the SPNs in the directory, when the service is installed or removed.</span></span> <span data-ttu-id="3e6c0-111">Дополнительные сведения и пример кода см. в разделе [Регистрация имен участников-служб для службы](registering-the-spns-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="3e6c0-111">For more information and a code example, see [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span>
-   <span data-ttu-id="3e6c0-112">Регистрация в службе проверки подлинности RPC при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="3e6c0-112">Register itself with the RPC authentication service when the service starts.</span></span> <span data-ttu-id="3e6c0-113">Дополнительные сведения см. [в статье взаимная проверка подлинности в приложениях RPC](mutual-authentication-in-rpc-applications.md).</span><span class="sxs-lookup"><span data-stu-id="3e6c0-113">For more information, see [Mutual Authentication in RPC Applications](mutual-authentication-in-rpc-applications.md).</span></span>

<span data-ttu-id="3e6c0-114">В этом примере кода используется различающееся имя записи Рпксервицес службы для создания имени участника-службы.</span><span class="sxs-lookup"><span data-stu-id="3e6c0-114">This code example uses the distinguished name of the service's RpcServices entry to compose the SPN.</span></span> <span data-ttu-id="3e6c0-115">Перед вызовом этого кода вызовите функцию [**рпкнсбиндинжекспорт**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) , чтобы создать запись рпксервицес службы.</span><span class="sxs-lookup"><span data-stu-id="3e6c0-115">Before calling this code, call the [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) function to create the service's RpcServices entry.</span></span>

<span data-ttu-id="3e6c0-116">Этот пример кода вызывает функцию [**дсжетспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) для создания имени субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="3e6c0-116">This code example calls the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to build an SPN.</span></span> <span data-ttu-id="3e6c0-117">Имя СУБЪЕКТа-службы состоит из имени класса службы и различающегося имени записи службы Рпксервицес.</span><span class="sxs-lookup"><span data-stu-id="3e6c0-117">The SPN is composed from service class name and the distinguished name of the service RpcServices entry.</span></span>


```C++
/**********

    SpnCompose()

    Composes a service principal name from a service name and class.

    Parameters:

    pszServiceName - Contains a null-terminated string that contains 
    the name of the service.

    pszServiceClass - Contains a null-terminated string that contains 
    the name of the service class.

    pspn - Pointer to an LPTSTR array that receives the array of 
    SPNs. This array must freed with the DsFreeSpnArray function when 
    it is no longer required.

    pulSpn - Pointer to a unsigned long that receives the number of 
    elements in the pspn array.

***********/

HRESULT SpnCompose(LPTSTR pszServiceName, 
                   LPTSTR pszServiceClass, 
                   LPTSTR **pspn, 
                   unsigned long *pulSpn) 
{
    HRESULT hr;
    CComPtr<IADs> spRoot;

    // Get the defaultNamingContext for the local domain.
    hr = ADsGetObject(L"LDAP://RootDSE",
                      IID_IADs,
                      (void**)&spRoot);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the distinguished name of the current domain.
    CComVariant svarDSRoot;
    hr = spRoot->Get(CComBSTR("defaultNamingContext"), &svarDSRoot);
     
    /*
    Compose the DN of the service's entry in the RpcServices 
    container, created by a call to RpcNsBindingExport. The entry 
    for an RPC service is in the System/RpcServices container in the 
    defaultNamingContext of the local domain.
    */
    
    CComBSTR sbstrDsEntryName = "CN=";
    sbstrDsEntryName += pszServiceName;
    sbstrDsEntryName += ",CN=RpcServices,CN=System,";
    sbstrDsEntryName += svarDSRoot.bstrVal;

    USES_CONVERSION;  // Required for the W2T() macro.
    DWORD status;

    /*
    Build the SPN for this service using the DN and the service 
    class.
    */
    status = DsGetSpn(
        DS_SPN_SERVICE, // Type of SPN to create.
        pszServiceClass, // Service class - a name in this case.
        W2T(sbstrDsEntryName), // DN of the RpcServices for 
                               // this RPC service.
        0, // Use the default instance port.
        0, // Number of additional instance names.
        NULL, // No additional instance names.
        NULL, // No additional instance ports.
        pulSpn, // Size of SPN array.
        pspn // Returned SPN(s).
        );
     
    return HRESULT_FROM_WIN32(status);
}
```



 

 