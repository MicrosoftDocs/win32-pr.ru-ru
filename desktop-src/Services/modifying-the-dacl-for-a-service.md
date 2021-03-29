---
description: Программа управления службами может создать или изменить список DACL, связанный со службой, для управления доступом.
ms.assetid: 24bfb2b5-34be-4d38-a690-90d29f5d4f9c
title: Изменение списка DACL для службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d814f6bc81b6d6a207bebf0e9b88c0bb672cdfbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912227"
---
# <a name="modifying-the-dacl-for-a-service"></a>Изменение списка DACL для службы

[Программа управления службами](service-control-programs.md) может создать или изменить список DACL, связанный со службой, для управления доступом. Чтобы получить список DACL, связанный с объектом службы, используйте функцию [**куерисервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) . Чтобы задать список DACL, используйте функцию [**сетсервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) . Любые изменения, внесенные [**в \_ дескриптор безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , связанные с объектом службы, сохраняются до тех пор, пока служба не будет удалена из системы.

В следующем примере создается и задается новый список DACL для службы. Код выполняет слияние одной записи управления доступом (ACE) с существующим списком DACL для службы. Новый элемент управления доступом предоставляет гостевой учетной записи запуск, завершение, удаление и \_ Управление доступом к указанной службе. Доступ к службе можно изменить с помощью параметра *AccessPermissions* , передаваемого функции [**буилдексплиЦитакцессвиснаме**](/windows/desktop/api/aclapi/nf-aclapi-buildexplicitaccesswithnamea) .

Переменная Сзсвкнаме представляет собой глобальную переменную, которая содержит имя службы. Полный пример, задающий эту переменную, см. в разделе [свкконтрол. cpp](svccontrol-cpp.md).


```C++
//
// Purpose: 
//   Updates the service DACL to grant start, stop, delete, and read
//   control access to the Guest account.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoUpdateSvcDacl()
{
    EXPLICIT_ACCESS      ea;
    SECURITY_DESCRIPTOR  sd;
    PSECURITY_DESCRIPTOR psd            = NULL;
    PACL                 pacl           = NULL;
    PACL                 pNewAcl        = NULL;
    BOOL                 bDaclPresent   = FALSE;
    BOOL                 bDaclDefaulted = FALSE;
    DWORD                dwError        = 0;
    DWORD                dwSize         = 0;
    DWORD                dwBytesNeeded  = 0;

    // Get a handle to the SCM database. 
 
    schSCManager = OpenSCManager( 
        NULL,                    // local computer
        NULL,                    // ServicesActive database 
        SC_MANAGER_ALL_ACCESS);  // full access rights 
 
    if (NULL == schSCManager) 
    {
        printf("OpenSCManager failed (%d)\n", GetLastError());
        return;
    }

    // Get a handle to the service

    schService = OpenService( 
        schSCManager,              // SCManager database 
        szSvcName,                 // name of service 
        READ_CONTROL | WRITE_DAC); // access
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Get the current security descriptor.

    if (!QueryServiceObjectSecurity(schService,
        DACL_SECURITY_INFORMATION, 
        &psd,           // using NULL does not work on all versions
        0, 
        &dwBytesNeeded))
    {
        if (GetLastError() == ERROR_INSUFFICIENT_BUFFER)
        {
            dwSize = dwBytesNeeded;
            psd = (PSECURITY_DESCRIPTOR)HeapAlloc(GetProcessHeap(),
                    HEAP_ZERO_MEMORY, dwSize);
            if (psd == NULL)
            {
                // Note: HeapAlloc does not support GetLastError.
                printf("HeapAlloc failed\n");
                goto dacl_cleanup;
            }
  
            if (!QueryServiceObjectSecurity(schService,
                DACL_SECURITY_INFORMATION, psd, dwSize, &dwBytesNeeded))
            {
                printf("QueryServiceObjectSecurity failed (%d)\n", GetLastError());
                goto dacl_cleanup;
            }
        }
        else 
        {
            printf("QueryServiceObjectSecurity failed (%d)\n", GetLastError());
            goto dacl_cleanup;
        }
    }

    // Get the DACL.

    if (!GetSecurityDescriptorDacl(psd, &bDaclPresent, &pacl,
                                   &bDaclDefaulted))
    {
        printf("GetSecurityDescriptorDacl failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }

    // Build the ACE.

    BuildExplicitAccessWithName(&ea, TEXT("GUEST"),
        SERVICE_START | SERVICE_STOP | READ_CONTROL | DELETE,
        SET_ACCESS, NO_INHERITANCE);

    dwError = SetEntriesInAcl(1, &ea, pacl, &pNewAcl);
    if (dwError != ERROR_SUCCESS)
    {
        printf("SetEntriesInAcl failed(%d)\n", dwError);
        goto dacl_cleanup;
    }

    // Initialize a new security descriptor.

    if (!InitializeSecurityDescriptor(&sd, 
        SECURITY_DESCRIPTOR_REVISION))
    {
        printf("InitializeSecurityDescriptor failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }

    // Set the new DACL in the security descriptor.

    if (!SetSecurityDescriptorDacl(&sd, TRUE, pNewAcl, FALSE))
    {
        printf("SetSecurityDescriptorDacl failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }

    // Set the new DACL for the service object.

    if (!SetServiceObjectSecurity(schService, 
        DACL_SECURITY_INFORMATION, &sd))
    {
        printf("SetServiceObjectSecurity failed(%d)\n", GetLastError());
        goto dacl_cleanup;
    }
    else printf("Service DACL updated successfully\n");

dacl_cleanup:
    CloseServiceHandle(schSCManager);
    CloseServiceHandle(schService);

    if(NULL != pNewAcl)
        LocalFree((HLOCAL)pNewAcl);
    if(NULL != psd)
        HeapFree(GetProcessHeap(), 0, (LPVOID)psd);
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Полный пример службы](the-complete-service-sample.md)
</dt> </dl>

 

 
