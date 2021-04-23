---
title: Пример кода для поиска сервера узла раздела каталога приложений
description: Этот раздел содержит пример кода, который находит сервер узла раздела каталога приложений.
ms.assetid: c161323b-13ce-4986-8b24-b459009ff53c
ms.tgt_platform: multiple
keywords:
- Пример кода для поиска сервера узла раздела каталога приложений
- Раздел каталога приложений Active Directory, пример кода для поиска сервера узла раздела каталога приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa82c91573e0ce00017fe93b8e8713f50ab7b26c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328491"
---
# <a name="example-code-for-locating-an-application-directory-partition-host-server"></a><span data-ttu-id="bc33f-105">Пример кода для поиска сервера узла раздела каталога приложений</span><span class="sxs-lookup"><span data-stu-id="bc33f-105">Example Code for Locating an Application Directory Partition Host Server</span></span>

<span data-ttu-id="bc33f-106">Этот раздел содержит пример кода, который находит сервер узла раздела каталога приложений.</span><span class="sxs-lookup"><span data-stu-id="bc33f-106">This topic includes a code example that locates an application directory partition host server.</span></span>

<span data-ttu-id="bc33f-107">В следующем примере кода C/C++ показано, как использовать функцию [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) для нахождение контроллера домена, на котором размещена реплика раздела каталога приложений.</span><span class="sxs-lookup"><span data-stu-id="bc33f-107">The following C/C++ code example shows how to use the [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) function to locate a domain controller that hosts a replica of an application directory partition.</span></span> <span data-ttu-id="bc33f-108">В этом примере кода также показано, как с помощью функции [**DsCrackNames**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dscracknamesa) преобразовать различающееся имя раздела каталога приложения в DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="bc33f-108">This code example also shows how to use the [**DsCrackNames**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dscracknamesa) function to convert the distinguished name of an application directory partition to a DNS name.</span></span>


```C++
/***************************************************************************

    AppPartitionDNToDNS()

    Converts the distinguished name of an application directory partition to 
    a DNS name for the partition.

    The caller must free the memory allocated to ppszDNS by calling 
    FreeADsMem when it is no longer required.

***************************************************************************/

DWORD AppPartitionDNToDNS(LPCTSTR pszDN, LPTSTR *ppszDNS)
{   
    DWORD dwRet;
    LPCTSTR rgpszNames[] = {pszDN};
    PDS_NAME_RESULT pResults;

    /*
    Convert the distinguished name to a DNS name using only syntactic 
    mapping. The DS_NAME_FLAG_SYNTACTICAL_ONLY flag allows DsCrackNames to 
    be called without binding.
    */
    dwRet = DsCrackNames(NULL, 
        DS_NAME_FLAG_SYNTACTICAL_ONLY,
        DS_FQDN_1779_NAME,
        DS_CANONICAL_NAME,
        1,
        rgpszNames,
        &pResults);

    if(NO_ERROR == dwRet)
    {
        /*
        Allocate the memory and copy the DNS name of the partition.
        */
        DWORD dwBytes = (lstrlen(pResults->rItems[0].pDomain) + 1) * sizeof(TCHAR);
        *ppszDNS = (LPTSTR)AllocADsMem(dwBytes);
        if(*ppszDNS)
        {
            wcsncpy_s(*ppszDNS, pResults->rItems[0].pDomain, dwBytes);

            dwRet = NO_ERROR;
        }
        else
        {
            dwRet = ERROR_NOT_ENOUGH_MEMORY;
        }
        
        // Free the result set.
        DsFreeNameResult(pResults);
    }
    
    return dwRet;
}

/***************************************************************************

    PrintDCFromAppPartition()

    Given the distinguished name of an application directory partition, 
    prints to the console the DNS name of a domain controller that hosts a 
    replica of the application directory partition.

***************************************************************************/

DWORD PrintDCFromAppPartition(LPCTSTR pszAppPartitionDN)
{
    DWORD dwRet;

    /*
    Convert the distinguished name of the partition to a DNS name so that 
    the DNS name can be passed to DsGetDcName.
    */
    LPTSTR pszDNS;
    dwRet = AppPartitionDNToDNS(pszAppPartitionDN, &pszDNS);
    if(NO_ERROR == dwRet)
    {
        PDOMAIN_CONTROLLER_INFO pdci;

        /*
        Get the name of a domain controller that hosts a replica of the 
        application directory partition.
        */
        dwRet = DsGetDcName(NULL, 
            pszDNS, 
            NULL, 
            NULL, 
            DS_ONLY_LDAP_NEEDED, 
            &pdci);

        if(NO_ERROR == dwRet)
        {
            // Print the DNS name of the domain controller.
            _tprintf(pdci->DomainControllerName);
            
            NetApiBufferFree(pdci);
        }

        FreeADsMem(pszDNS);
    }

    return dwRet;
}
```



 

 




