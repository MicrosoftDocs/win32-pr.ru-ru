---
title: Создание точки подключения службы
description: В следующем примере кода показано, как создать и инициализировать точку подключения службы.
ms.assetid: 6ab1e72f-22e8-499a-916e-c2ba8e2c2aff
ms.tgt_platform: multiple
keywords:
- Создание точки подключения службы AD
- Точка подключения службы, создание AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a1ec4e9097414ea8131b3dd1cbd832e73b388e5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069801"
---
# <a name="creating-a-service-connection-point"></a><span data-ttu-id="3e0ff-105">Создание точки подключения службы</span><span class="sxs-lookup"><span data-stu-id="3e0ff-105">Creating a Service Connection Point</span></span>

<span data-ttu-id="3e0ff-106">В следующем примере кода показано, как создать и инициализировать точку подключения службы.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-106">The following code example shows how to create and initialize a service connection point.</span></span> <span data-ttu-id="3e0ff-107">В примере кода выполняются дополнительные действия, позволяющие службе обновлять значения SCP во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-107">The code example performs additional steps that enable the service to update the SCP values at run time.</span></span> <span data-ttu-id="3e0ff-108">Как правило, установщик службы выполняет эти действия в процессе установки экземпляра службы на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-108">Typically, a service installer performs these steps as part of installing a service instance on a host computer.</span></span>

<span data-ttu-id="3e0ff-109">Этот пример кода создает объект SCP в качестве дочернего объекта для объекта локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-109">This code example creates the SCP object as a child object for the object of the local computer.</span></span> <span data-ttu-id="3e0ff-110">Для получения DN объекта локального компьютера используется функция [**жеткомпутеробжектнаме**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) .</span><span class="sxs-lookup"><span data-stu-id="3e0ff-110">It uses the [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) function to get the DN of the local computer object.</span></span> <span data-ttu-id="3e0ff-111">Затем он использует DN для привязки к указателю [**идиректорйобжект**](/windows/desktop/api/iads/nn-iads-idirectoryobject) для объекта Computer.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-111">It then uses the DN to bind to an [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) pointer for the computer object.</span></span> <span data-ttu-id="3e0ff-112">Метод [**идиректорйобжект:: креатедсобжект**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) создает SCP и задает начальные значения для важных атрибутов SCP.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-112">The [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method creates the SCP and specifies initial values for the important SCP attributes.</span></span>

<span data-ttu-id="3e0ff-113">[**Креатедсобжект**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) возвращает указатель на новую SCP, которую пример кода использует для получения указателя [**iAds**](/windows/desktop/api/iads/nn-iads-iads) для SCP.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-113">[**CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) returns a pointer to the new SCP, which the code example uses to retrieve an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) pointer for the SCP.</span></span> <span data-ttu-id="3e0ff-114">В примере кода методы **iAds** используются для получения атрибутов **objectGUID** и **distinguishedName** точки подключения службы.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-114">The code example uses **IADs** methods to retrieve the **objectGUID** and **distinguishedName** attributes of the SCP.</span></span> <span data-ttu-id="3e0ff-115">В примере кода **атрибут objectGUID** используется для составления строки, используемой для привязки к SCP, а затем кэширует строку привязки GUID в локальном реестре, где она может быть извлечена службой во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-115">The code example uses the **objectGUID** to compose a string used to bind to the SCP, and then caches the GUID binding string in the local registry where it can be retrieved by the service at run time.</span></span> <span data-ttu-id="3e0ff-116">**DistinguishedName** возвращается в вызывающую функцию для использования при составлении имени участника-службы (SPN) для экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-116">The **distinguishedName** is returned to the function caller for use in composing a service principal name (SPN) for the service instance.</span></span>

<span data-ttu-id="3e0ff-117">В следующем примере кода эта функция вызывается в рамках основных шагов по установке службы с поддержкой каталогов.</span><span class="sxs-lookup"><span data-stu-id="3e0ff-117">The following code example calls this function as part of the basic steps of installing a directory-enabled service.</span></span> <span data-ttu-id="3e0ff-118">Дополнительные сведения см. в разделе [Установка службы на главном компьютере](installing-a-service-on-a-host-computer.md).</span><span class="sxs-lookup"><span data-stu-id="3e0ff-118">For more information, see [Installing a Service on a Host Computer](installing-a-service-on-a-host-computer.md).</span></span>


```C++
// ScpCreate
//
// Create a new service connection point as a child object of the 
// local server computer object.
//
DWORD
ScpCreate(
       USHORT usPort, // Service's default port to store in SCP.
       LPTSTR szClass, // Service class string to store in SCP.
       LPTSTR szAccount, // Logon account that must access SCP.
       UINT ccDN, // Length of the pszDN buffer in characters
       TCHAR *pszDN) // Returns distinguished name of SCP.
{
DWORD dwStat, dwAttr, dwLen;
HRESULT hr;
IDispatch *pDisp;          // Returned dispinterface of new object.
IDirectoryObject *pComp;   // Computer object; parent of SCP.
IADs *pIADsSCP;            // IADs interface on new object.

if(!szClass || !szAccount || !pszDN || !(ccDN > 0))
{
       hr = ERROR_INVALID_PARAMETER;
       ReportError(TEXT("Invalid parameter."), hr);
       return hr;
}

// Values for SCPs keywords attribute.
TCHAR* KwVal[]={
        TEXT("83C29870-1DFC-11d3-A193-0000F87A9099"), // Vendor GUID.
        TEXT("A762885A-AA44-11d2-81F1-00C04FB9624E"), // Product GUID.
        TEXT("Microsoft"), // Vendor Name.
        TEXT("Windows 2000 Auth-O-Matic"), // Product Name.
};

TCHAR       szServer[MAX_PATH];
TCHAR       szDn[MAX_PATH];
TCHAR       szAdsPath[MAX_PATH];
TCHAR       szPort[6];

HKEY        hReg;
DWORD       dwDisp;

ADSVALUE cn,objclass,keywords[4],binding,classname,dnsname,nametype;

// SCP attributes to set during creation of SCP.
ADS_ATTR_INFO   ScpAttribs[] = 
{
    {
        TEXT("cn"),
        ADS_ATTR_UPDATE,
        ADSTYPE_CASE_IGNORE_STRING,
        &cn,
        1
    },
    {
        TEXT("objectClass"),
        ADS_ATTR_UPDATE,
        ADSTYPE_CASE_IGNORE_STRING,
        &objclass,
        1
    },
    {
         TEXT("keywords"),
         ADS_ATTR_UPDATE,
         ADSTYPE_CASE_IGNORE_STRING,
         keywords,
         4
    },
    {
         TEXT("serviceDnsName"),
         ADS_ATTR_UPDATE,
         ADSTYPE_CASE_IGNORE_STRING,
         &dnsname,
         1
    },
    {
        TEXT("serviceDnsNameType"),
        ADS_ATTR_UPDATE,
        ADSTYPE_CASE_IGNORE_STRING,
        &nametype,
        1
    },
    {
        TEXT("serviceClassName"),
        ADS_ATTR_UPDATE,
        ADSTYPE_CASE_IGNORE_STRING,
        &classname,
        1
    },
    {
        TEXT("serviceBindingInformation"),
        ADS_ATTR_UPDATE,
        ADSTYPE_CASE_IGNORE_STRING,
        &binding,
        1
    },
};

BSTR bstrGuid = NULL;
TCHAR pwszBindByGuidStr[1024]; 
VARIANT var;

// Get the DNS name of the local computer.
dwLen = sizeof(szServer);
if (!GetComputerNameEx(ComputerNameDnsFullyQualified,szServer,&dwLen))
    return GetLastError();
_tprintf(TEXT("GetComputerNameEx: %s\n"), szServer);
    
// Enter the attribute values to be stored in the SCP.
keywords[0].dwType = ADSTYPE_CASE_IGNORE_STRING;
keywords[1].dwType = ADSTYPE_CASE_IGNORE_STRING;
keywords[2].dwType = ADSTYPE_CASE_IGNORE_STRING;
keywords[3].dwType = ADSTYPE_CASE_IGNORE_STRING;

keywords[0].CaseIgnoreString=KwVal[0];
keywords[1].CaseIgnoreString=KwVal[1];
keywords[2].CaseIgnoreString=KwVal[2];
keywords[3].CaseIgnoreString=KwVal[3];

cn.dwType                   = ADSTYPE_CASE_IGNORE_STRING;
cn.CaseIgnoreString         = TEXT("SockAuthAD");
objclass.dwType             = ADSTYPE_CASE_IGNORE_STRING;
objclass.CaseIgnoreString   = TEXT("serviceConnectionPoint");

dnsname.dwType              = ADSTYPE_CASE_IGNORE_STRING;
dnsname.CaseIgnoreString    = szServer;
classname.dwType            = ADSTYPE_CASE_IGNORE_STRING;
classname.CaseIgnoreString  = szClass;

_stprintf_s(szPort,TEXT("%d"),usPort);
binding.dwType              = ADSTYPE_CASE_IGNORE_STRING;
binding.CaseIgnoreString    = szPort;
nametype.dwType             = ADSTYPE_CASE_IGNORE_STRING;
nametype.CaseIgnoreString   = TEXT("A");

/*
Get the distinguished name of the computer object for the local 
computer.
*/
dwLen = sizeof(szDn);
if (!GetComputerObjectName(NameFullyQualifiedDN,szDn,&dwLen))
    return GetLastError();
_tprintf(TEXT("GetComputerObjectName: %s\n"), szDn);

/*
Compose the ADSpath and bind to the computer object for the local 
computer.
*/
_tcsncpy_s(szAdsPath,TEXT("LDAP://"),MAX_PATH);
_tcsncat_s(szAdsPath,szDn,MAX_PATH - _tcslen(szAdsPath));
hr = ADsGetObject(szAdsPath, IID_IDirectoryObject, (void **)&pComp);
if (FAILED(hr)) {
    ReportError(TEXT("Failed to bind Computer Object."),hr);
    return hr;
}

//*******************************************************************
// Publish the SCP as a child of the computer object
//*******************************************************************

// Calculate attribute count.
dwAttr = sizeof(ScpAttribs)/sizeof(ADS_ATTR_INFO);  

// Complete the action.
hr = pComp->CreateDSObject(TEXT("cn=SockAuthAD"),
                           ScpAttribs, dwAttr, &pDisp);
if (FAILED(hr)) {
    ReportError(TEXT("Failed to create SCP:"), hr);
    pComp -> Release();
    return hr;
}

pComp -> Release();

// Query for an IADs pointer on the SCP object.
hr = pDisp->QueryInterface(IID_IADs,(void **)&pIADsSCP);
if (FAILED(hr)) {
    ReportError(TEXT("Failed to QueryInterface for IADs:"),hr);
    pDisp->Release();
    return hr;
}
pDisp->Release();

// Set ACEs on the SCP so a service can modify it.
hr = AllowAccessToScpProperties(
        szAccount,     // Service account to allow access.
        pIADsSCP);     // IADs pointer to the SCP object.
if (FAILED(hr)) {
    ReportError(TEXT("Failed to set ACEs on SCP DACL:"), hr);
    return hr;
}

// Get the distinguished name of the SCP.
VariantInit(&var); 
hr = pIADsSCP->Get(CComBSTR("distinguishedName"), &var); 
if (FAILED(hr)) {
    ReportError(TEXT("Failed to get distinguishedName:"), hr);
    pIADsSCP->Release();
    return hr;
}
_tprintf(TEXT("distinguishedName via IADs: %s\n"), var.bstrVal);

// Return the DN of the SCP, which is used to compose the SPN.
// The best practice is to either accept and return the buffer
// size or do this in a _try / _except block, both omitted here
// for clarity.
_tcsncpy_s(pszDN, var.bstrVal, ccDN);

// Retrieve the SCP objectGUID in format suitable for binding. 
hr = pIADsSCP->get_GUID(&bstrGuid); 
if (FAILED(hr)) {
    ReportError(TEXT("Failed to get GUID:"), hr);
    pIADsSCP->Release();
    return hr;
}

// Build a string for binding to the object by GUID.
_tcsncpy_s(pwszBindByGuidStr, 
    TEXT("LDAP://<GUID="),
    1024);
_tcsncat_s(pwszBindByGuidStr, 
    bstrGuid, 
    1024 -_tcslen(pwszBindByGuidStr));
_tcsncat_s(pwszBindByGuidStr, 
    TEXT(">"), 
    1024 -_tcslen(pwszBindByGuidStr));
_tprintf(TEXT("GUID binding string: %s\n"), 
    pwszBindByGuidStr);

pIADsSCP->Release();

// Create a registry key under 
// HKEY_LOCAL_MACHINE\SOFTWARE\Vendor\Product.
dwStat = RegCreateKeyEx(HKEY_LOCAL_MACHINE,
            TEXT("Software\\Fabrikam\\Auth-O-Matic"),
            0,
            NULL,
            REG_OPTION_NON_VOLATILE,
            KEY_ALL_ACCESS,
            NULL,
            &hReg,
            &dwDisp);
if (dwStat != NO_ERROR) {
    ReportError(TEXT("RegCreateKeyEx failed:"), dwStat);
    return dwStat;
}

// Cache the GUID binding string under the registry key.
dwStat = RegSetValueEx(hReg, TEXT("GUIDBindingString"), 0, REG_SZ,
                           (const BYTE *)pwszBindByGuidStr, 
                           2*(_tcslen(pwszBindByGuidStr)));
if (dwStat != NO_ERROR) {
    ReportError(TEXT("RegSetValueEx failed:"), dwStat);
    return dwStat;
}

RegCloseKey(hReg);

// Cleanup should delete the SCP and registry key if an error occurs.

return dwStat;
}
```



 

 