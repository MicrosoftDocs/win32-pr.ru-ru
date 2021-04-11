---
description: В следующем примере добавляется запись управления доступом (ACE) в список управления доступом на уровне пользователей (DACL) объекта.
ms.assetid: 0c168bb7-996f-42a8-96cd-2ba7870a3333
title: Изменение списков управления доступом объекта в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21195b1164ce949d1305f0c1748d24b0dbb7525b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999296"
---
# <a name="modifying-the-acls-of-an-object-in-c"></a>Изменение списков управления доступом объекта в C++

В следующем примере добавляется [*запись управления доступом*](/windows/desktop/SecGloss/a-gly) (ACE) в [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) объекта.

Параметр *AccessMode* определяет тип нового элемента управления доступом и то, как новый элемент управления доступом объединяется с любым существующим элементом ACE для указанного доверенного лица. Используйте \_ Флаги предоставления доступа, задания \_ доступа, запрета доступа \_ или отмены доступа \_ в параметре *AccessMode* . Дополнительные сведения об этих флагах см. в разделе [**\_ режим доступа**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Аналогичный код можно использовать для работы с [*системным списком управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL). Укажите \_ \_ сведения о безопасности SACL в функциях [**жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) и [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , чтобы получить и задать список SACL для объекта. Используйте \_ \_ Флаги Set Audit Success, Set \_ Audit \_ Failure и REVOKE \_ Access в параметре *AccessMode* . Дополнительные сведения об этих флагах см. в разделе [**\_ режим доступа**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Используйте этот код, чтобы добавить [запись ACE для конкретного объекта](object-specific-aces.md) в список DACL объекта службы каталогов. Чтобы указать идентификаторы GUID в записи ACE конкретного объекта, установите для параметра *трустиформ* значение доверенное \_ лицо \_ — \_ объекты \_ , имя или доверенное лицо \_ — \_ объекты \_ и \_ идентификатор безопасности, а параметр *псзтрусти* — как указатель на [**объекты \_ , \_ имя**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) или [**объекты и структуру \_ \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) .

В этом примере используется функция [**жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) для получения существующего списка DACL. Затем она заполняет [**явную структуру \_ доступа**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) сведениями о записи ACE и использует функцию [**сетентриесинакл**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) для слияния нового элемента ACE с любым существующим элементом ACE в списке DACL. Наконец, в примере вызывается функция [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) для присоединения нового списка DACL к [*дескриптору безопасности*](/windows/desktop/SecGloss/s-gly) объекта.


```C++
#include <windows.h>
#include <stdio.h>

DWORD AddAceToObjectsSecurityDescriptor (
    LPTSTR pszObjName,          // name of object
    SE_OBJECT_TYPE ObjectType,  // type of object
    LPTSTR pszTrustee,          // trustee for new ACE
    TRUSTEE_FORM TrusteeForm,   // format of trustee structure
    DWORD dwAccessRights,       // access mask for new ACE
    ACCESS_MODE AccessMode,     // type of ACE
    DWORD dwInheritance         // inheritance flags for new ACE
) 
{
    DWORD dwRes = 0;
    PACL pOldDACL = NULL, pNewDACL = NULL;
    PSECURITY_DESCRIPTOR pSD = NULL;
    EXPLICIT_ACCESS ea;

    if (NULL == pszObjName) 
        return ERROR_INVALID_PARAMETER;

    // Get a pointer to the existing DACL.

    dwRes = GetNamedSecurityInfo(pszObjName, ObjectType, 
          DACL_SECURITY_INFORMATION,
          NULL, NULL, &pOldDACL, NULL, &pSD);
    if (ERROR_SUCCESS != dwRes) {
        printf( "GetNamedSecurityInfo Error %u\n", dwRes );
        goto Cleanup; 
    }  

    // Initialize an EXPLICIT_ACCESS structure for the new ACE. 

    ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
    ea.grfAccessPermissions = dwAccessRights;
    ea.grfAccessMode = AccessMode;
    ea.grfInheritance= dwInheritance;
    ea.Trustee.TrusteeForm = TrusteeForm;
    ea.Trustee.ptstrName = pszTrustee;

    // Create a new ACL that merges the new ACE
    // into the existing DACL.

    dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
    if (ERROR_SUCCESS != dwRes)  {
        printf( "SetEntriesInAcl Error %u\n", dwRes );
        goto Cleanup; 
    }  

    // Attach the new ACL as the object's DACL.

    dwRes = SetNamedSecurityInfo(pszObjName, ObjectType, 
          DACL_SECURITY_INFORMATION,
          NULL, NULL, pNewDACL, NULL);
    if (ERROR_SUCCESS != dwRes)  {
        printf( "SetNamedSecurityInfo Error %u\n", dwRes );
        goto Cleanup; 
    }  

    Cleanup:

        if(pSD != NULL) 
            LocalFree((HLOCAL) pSD); 
        if(pNewDACL != NULL) 
            LocalFree((HLOCAL) pNewDACL); 

        return dwRes;
}

```



 

 
