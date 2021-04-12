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
# <a name="composing-spns-for-an-rpcns-service"></a>Составление имен участников-служб для службы Рпкнс

В следующем примере кода солагаются имена субъектов-служб (SPN) для службы RPC, которая имеет запись в контейнере Рпксервицес в каталоге. Служба RPC использует функцию [**рпкнсбиндинжекспорт**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) для создания записи рпксервицес.

Служба RPC использует этот пример кода для создания имени субъекта-службы или SPN, которые обозначают экземпляр службы. Эта подпрограммы используется службой для выполнения следующих задач.

-   Регистрация или Отмена регистрации имен участников-служб в каталоге при установке или удалении службы. Дополнительные сведения и пример кода см. в разделе [Регистрация имен участников-служб для службы](registering-the-spns-for-a-service.md).
-   Регистрация в службе проверки подлинности RPC при запуске службы. Дополнительные сведения см. [в статье взаимная проверка подлинности в приложениях RPC](mutual-authentication-in-rpc-applications.md).

В этом примере кода используется различающееся имя записи Рпксервицес службы для создания имени участника-службы. Перед вызовом этого кода вызовите функцию [**рпкнсбиндинжекспорт**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) , чтобы создать запись рпксервицес службы.

Этот пример кода вызывает функцию [**дсжетспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) для создания имени субъекта-службы. Имя СУБЪЕКТа-службы состоит из имени класса службы и различающегося имени записи службы Рпксервицес.


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



 

 