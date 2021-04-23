---
title: Изменение Дефаултсекуритидескриптор для класса Object
description: В следующем примере кода извлекается дескриптор безопасности по умолчанию для класса объекта, добавляется ACE в список DACL, а затем задается измененный дескриптор безопасности для класса объекта.
ms.assetid: 38b4d129-f98f-43da-9bd9-1ae23c090657
ms.tgt_platform: multiple
keywords:
- Описатель безопасности AD, изменение Дефаултсекуритидескриптор для класса объекта
- объекты AD, изменение Дефаултсекуритидескриптор для класса Object
- класс AD, изменение Дефаултсекуритидескриптор для класса Object
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc3bd441cb19c43ee36550520d18ee38726b05e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986141"
---
# <a name="modifying-the-defaultsecuritydescriptor-for-an-object-class"></a><span data-ttu-id="d2f62-106">Изменение Дефаултсекуритидескриптор для класса Object</span><span class="sxs-lookup"><span data-stu-id="d2f62-106">Modifying the defaultSecurityDescriptor for an Object Class</span></span>

<span data-ttu-id="d2f62-107">В следующем примере кода извлекается дескриптор безопасности по умолчанию для класса объекта, добавляется ACE в список DACL, а затем задается измененный дескриптор безопасности для класса объекта.</span><span class="sxs-lookup"><span data-stu-id="d2f62-107">The following code example retrieves the default security descriptor for an object class, adds an ACE to the DACL, and then sets the modified security descriptor on the object class.</span></span>

<span data-ttu-id="d2f62-108">Имейте в виду, что изменение схемы по умолчанию отключено на всех контроллерах домена Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d2f62-108">Be aware that schema modification is disabled, by default, on all Windows 2000 domain controllers.</span></span> <span data-ttu-id="d2f62-109">Чтобы включить изменение схемы на определенном контроллере домена, установите \_ значение reg DWORD с именем "обновление схемы разрешено" в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="d2f62-109">To enable schema modification at a particular DC, set a REG\_DWORD value named "Schema Update Allowed" under the following registry key:</span></span>

<span data-ttu-id="d2f62-110">**HKey \_ \_** \\ Параметры NTDS локальных **системных систем** \\ **CurrentControlSet** \\ **Services** \\  \\ </span><span class="sxs-lookup"><span data-stu-id="d2f62-110">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**NTDS**\\**Parameters**</span></span>

<span data-ttu-id="d2f62-111">Добавьте это значение, если оно еще не существует.</span><span class="sxs-lookup"><span data-stu-id="d2f62-111">Add this value if it does not already exist.</span></span> <span data-ttu-id="d2f62-112">Задайте для этого параметра значение 1, чтобы включить изменение схемы.</span><span class="sxs-lookup"><span data-stu-id="d2f62-112">Set this value to 1 to enable schema modification.</span></span> <span data-ttu-id="d2f62-113">Если это значение равно нулю, изменение схемы отключено.</span><span class="sxs-lookup"><span data-stu-id="d2f62-113">If this value is zero, schema modification is disabled.</span></span> <span data-ttu-id="d2f62-114">Оснастка MMC "Диспетчер схемы" предоставляет флажок, который позволяет выбрать или очистить этот раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="d2f62-114">The Schema Manager MMC snap-in provides a check box that selects or clears this registry key.</span></span>


```C++
//  Add msvcrt.dll to your project
//  Add activeds.lib to your project
//  Add adsiid.lib to your project

#include "stdafx.h"
#include <wchar.h>
#include <objbase.h>
#include <activeds.h>
#include <ACLAPI.h>
#include <winnt.h>
#include <Sddl.h>
#include "atlbase.h"
#include "stdio.h"
#include "iads.h"
 
#define _WIN32_WINNT 0x0500
 
HRESULT ModifyDefaultSecurityDescriptor( IADs *pObject );

//  Entry point for the application.
int main(int argc, char *argv[])
{
LPOLESTR szPath = new OLECHAR[MAX_PATH];
LPOLESTR pszBuffer  = new WCHAR[MAX_PATH];
HRESULT hr = S_OK;
IADs *pObject = NULL;
VARIANT var;
 
wprintf(L"This program modifies the default security descriptor of an object class\n");
wprintf(L"Specify the object class:");
#ifdef _MBCS
_getws_s(pszBuffer);
if (!pszBuffer)
    return TRUE;
wcscpy_s(szPath,L"LDAP://cn=");
wcscat_s(szPath,pszBuffer);
wcscat_s(szPath,L",");
#endif _MBCS
 
//  Initialize COM.
CoInitialize(NULL);
 
//  Get rootDSE and the schema container DN. Bind to the
//  current user's domain using current user's security context.
 
hr = ADsOpenObject(L"LDAP://rootDSE",
            NULL,
            NULL,
            ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
            IID_IADs,
            (void**)&pObject);
 
if (SUCCEEDED(hr)) {
    hr = pObject->Get(CComBSTR("schemaNamingContext"), &var);
    if (SUCCEEDED(hr)) {
        #ifdef _MBCS
        wcscat_s(szPath,var.bstrVal);
        #endif _MBCS
        VariantClear(&var);
        if (pObject) {
            pObject->Release();
            pObject = NULL;
    }
    hr = ADsOpenObject(szPath,
               NULL,
               NULL,
               ADS_SECURE_AUTHENTICATION, //  Use Secure Authentication.
               IID_IADs,
               (void**)&pObject);
    if (SUCCEEDED(hr)) {
        wprintf(L"Modify the default SD for the %s class\n", pszBuffer);
        hr = ModifyDefaultSecurityDescriptor( pObject );
    }
  }
}
 
if (FAILED(hr))
    wprintf(L"Failed with the following HRESULT: 0x%x\n", hr);
 
if (pObject)
    pObject->Release();
 
//  Uninitialize COM.
 
CoUninitialize();
return TRUE;
}    
 
 
HRESULT ModifyDefaultSecurityDescriptor(
                          IADs *pObject
                          )
{
HRESULT hr = E_FAIL;
VARIANT var;
PSECURITY_DESCRIPTOR pSDCNV = NULL;
SECURITY_DESCRIPTOR SD = {0};
DWORD dwSDSize = sizeof(SECURITY_DESCRIPTOR);
PSID pOwnerSID = NULL;
DWORD dwOwnerSIDSize = 0;
PSID pGroupSID = NULL;
DWORD dwGroupSIDSize = 0;
PACL pDACL = NULL;
DWORD dwDACLSize = 0;
PACL pSACL = NULL;
DWORD dwSACLSize = 0;
BOOL bDaclPresent = FALSE;
BOOL bDaclDefaulted = FALSE;
PACL pOldDACL, pNewDACL;
ULONG ulLen;
EXPLICIT_ACCESS ea;
DWORD dwRes;
 
//  Get the default security descriptor. Type should be VT_BSTR.
 
hr = pObject->Get(CComBSTR("defaultSecurityDescriptor"), &var);
if (FAILED(hr) || var.vt!=VT_BSTR ) {
    wprintf(L"Error getting default SD: 0x%x\n", hr );
    goto Cleanup;
}
 
wprintf(L"Old Default SD: %s\n", var.bstrVal);
 
//  Convert the security descriptor string to a security descriptor.
 
if ( ! ConvertStringSecurityDescriptorToSecurityDescriptor (
           var.bstrVal, SDDL_REVISION_1, &pSDCNV, NULL )) {
    wprintf(L"Error converting string security descriptor: %d\n", 
           GetLastError() );
    goto Cleanup;
}
 
//  Convert self-relative security descriptor to absolute.
//  First, get the required buffer sizes.
 
if (! MakeAbsoluteSD(pSDCNV, &SD, &dwSDSize, 
           pDACL, &dwDACLSize, 
           pSACL, &dwSACLSize, 
           pOwnerSID, &dwOwnerSIDSize, 
           pGroupSID, &dwGroupSIDSize) ) {
 
  //  Allocate the buffers.
 
  pDACL = (PACL) GlobalAlloc(GPTR, dwDACLSize);
  pSACL = (PACL) GlobalAlloc(GPTR, dwSACLSize);
  pOwnerSID = (PACL) GlobalAlloc(GPTR, dwOwnerSIDSize);
  pGroupSID = (PACL) GlobalAlloc(GPTR, dwGroupSIDSize);
  if (! (pDACL && pSACL && pOwnerSID && pGroupSID) ) {
    wprintf(L"GlobalAlloc failed: %d\n", GetLastError() );
    goto Cleanup;
  }
 
  //  Perform the conversion.
 
  if (! MakeAbsoluteSD(pSDCNV, &SD, &dwSDSize, pDACL, &dwDACLSize, 
           pSACL, &dwSACLSize, pOwnerSID, &dwOwnerSIDSize, 
           pGroupSID, &dwGroupSIDSize) ) {
    wprintf(L"MakeAbsoluteSD: %d\n", GetLastError() );
    goto Cleanup;
  }
}
 
//  Get the DACL from the security descriptor.
 
if (! GetSecurityDescriptorDacl(&SD, &bDaclPresent, 
                  &pOldDACL, &bDaclDefaulted) ) {
    wprintf(L"GetSecurityDescriptorDacl failed: %d\n", GetLastError() );
    goto Cleanup;
} 
 
//  Initialize an EXPLICIT_ACCESS structure for the new ACE.
//  The ACE grants Everyone the right to read properties.
 
ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
ea.grfAccessPermissions = ADS_RIGHT_DS_READ_PROP;
ea.grfAccessMode = GRANT_ACCESS;
ea.grfInheritance= 0;
ea.Trustee.TrusteeForm = TRUSTEE_IS_NAME;
ea.Trustee.ptstrName = TEXT("Everyone");
 
//  Create a new ACL that merges the new ACE into the existing DACL.
 
dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
if (ERROR_SUCCESS != dwRes)  {
    wprintf(L"SetEntriesInAcl Error %u\n", dwRes );
    goto Cleanup;
}
 
//  Put the modified DACL into the security descriptor.
 
if (! SetSecurityDescriptorDacl(&SD, TRUE, pNewDACL, FALSE) ) {
    wprintf(L"SetSecurityDescriptorOwner failed: %d\n", 
            GetLastError() );
    goto Cleanup;
} 
 
//  Convert the security descriptor back to string format.
 
VariantClear(&var);
if ( ! ConvertSecurityDescriptorToStringSecurityDescriptor (
        &SD, SDDL_REVISION_1, 
        GROUP_SECURITY_INFORMATION | OWNER_SECURITY_INFORMATION |
        DACL_SECURITY_INFORMATION | SACL_SECURITY_INFORMATION, 
        &var.bstrVal, &ulLen )) {
    wprintf(L"Error converting security descriptor to string: %d\n", 
        GetLastError() );
    goto Cleanup;
}
 
wprintf(L"New default SD: %s\n", var.bstrVal);
V_VT(&var) = VT_BSTR;
 
//  Use Put and SetInfo to set the modified security descriptor.
 
hr = pObject->Put(CComBSTR("defaultSecurityDescriptor"), var);
if (FAILED(hr)) {
    wprintf(L"Error putting default SD: 0x%x\n", hr );
    goto Cleanup;
}
 
hr = pObject->SetInfo();
if (FAILED(hr)) {
    wprintf(L"Error setting default SD: 0x%x\n", hr );
    goto Cleanup;
}
 
Cleanup:
 
VariantClear(&var);
if (pSDCNV) 
    LocalFree(pSDCNV);
if (pDACL) 
    GlobalFree(pDACL);
if (pSACL) 
    GlobalFree(pSACL);
if (pOwnerSID) 
    GlobalFree(pOwnerSID);
if (pGroupSID) 
    GlobalFree(pGroupSID);
if (pNewDACL) 
    LocalFree(pNewDACL);
 
return hr;
}
```



 

 




