---
title: Перечисление реплик службы
description: Этот раздел содержит пример кода, который перечисляет установленные экземпляры реплицированной службы на разных главных компьютерах предприятия.
ms.assetid: 9dc3f932-c3e1-4ce1-a945-12d68838304e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 995cd665476a55b6bf717f356fafa54b0d2e10e6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104533095"
---
# <a name="enumerating-the-replicas-of-a-service"></a><span data-ttu-id="4bbfe-103">Перечисление реплик службы</span><span class="sxs-lookup"><span data-stu-id="4bbfe-103">Enumerating the Replicas of a Service</span></span>

<span data-ttu-id="4bbfe-104">Этот раздел содержит пример кода, который перечисляет установленные экземпляры реплицированной службы на разных главных компьютерах предприятия.</span><span class="sxs-lookup"><span data-stu-id="4bbfe-104">This topic includes a code example that enumerates the installed instances of a replicated service on different host computers throughout an enterprise.</span></span> <span data-ttu-id="4bbfe-105">Чтобы изменить пароль учетной записи службы для каждого экземпляра реплицируемой службы, используйте этот пример кода в сочетании с примером кода в разделе [изменение пароля учетной записи пользователя службы](changing-the-password-on-a-serviceampaposs-user-account.md) .</span><span class="sxs-lookup"><span data-stu-id="4bbfe-105">To change the service account password for each instance of a replicated service, use this code example in conjunction with the code example in the [Changing the Password on a Service's User Account](changing-the-password-on-a-serviceampaposs-user-account.md) topic.</span></span>

<span data-ttu-id="4bbfe-106">В примере кода предполагается, что каждый экземпляр службы имеет собственный объект точки подключения службы (SCP) в каталоге.</span><span class="sxs-lookup"><span data-stu-id="4bbfe-106">The code example assumes that each service instance has its own service connection point (SCP) object in the directory.</span></span> <span data-ttu-id="4bbfe-107">Точка подключения службы — это объект класса [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) .</span><span class="sxs-lookup"><span data-stu-id="4bbfe-107">An SCP is an object of the [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) class.</span></span> <span data-ttu-id="4bbfe-108">Этот класс имеет атрибут **keywords** , который является атрибутом с несколькими значениями, реплицируемым в каждый глобальный каталог в лесу.</span><span class="sxs-lookup"><span data-stu-id="4bbfe-108">This class has a **keywords** attribute, which is a multi-valued attribute replicated to each global catalog (GC) in the forest.</span></span> <span data-ttu-id="4bbfe-109">Атрибут **ключевых слов** для SCP каждого экземпляра содержит идентификатор GUID продукта службы.</span><span class="sxs-lookup"><span data-stu-id="4bbfe-109">The **keywords** attribute of each instance's SCP contains the service's product GUID.</span></span> <span data-ttu-id="4bbfe-110">Это позволяет найти все запрашивая для различных экземпляров службы, выполняя поиск объектов с атрибутом **keywords** , РАВНым идентификатору GUID продукта.</span><span class="sxs-lookup"><span data-stu-id="4bbfe-110">This enables finding all of the SCPs for the various service instances by searching a GC for objects with a **keywords** attribute that equals the product GUID.</span></span>

<span data-ttu-id="4bbfe-111">Пример кода получает указатель [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) на GC и использует метод [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) для поиска запрашивая.</span><span class="sxs-lookup"><span data-stu-id="4bbfe-111">The code example obtains an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer to a GC, and uses the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) method to search for the SCPs.</span></span> <span data-ttu-id="4bbfe-112">Имейте в виду, что сборщик мусора содержит частичную реплику для каждой точки подключения службы.</span><span class="sxs-lookup"><span data-stu-id="4bbfe-112">Be aware that the GC contains a partial replica for each SCP.</span></span> <span data-ttu-id="4bbfe-113">То есть он содержит некоторые атрибуты SCP, но не все.</span><span class="sxs-lookup"><span data-stu-id="4bbfe-113">That is, it contains some of the SCP attributes, but not all.</span></span> <span data-ttu-id="4bbfe-114">В этом примере кода основное внимание уделяется атрибуту **serviceDNSName** , который содержит DNS-имя сервера узла для данного экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="4bbfe-114">In this code example, focus on the **serviceDNSName** attribute, which contains the DNS name of the host server for that service instance.</span></span> <span data-ttu-id="4bbfe-115">Поскольку **serviceDNSName** не является одним из атрибутов, реплицируемых в GC, в примере кода используется двухэтапный процесс для его извлечения.</span><span class="sxs-lookup"><span data-stu-id="4bbfe-115">Because **serviceDNSName** is not one of the attributes replicated in a GC, the code example uses a two-step process to retrieve it.</span></span> <span data-ttu-id="4bbfe-116">Во-первых, он использует поиск GC для получения различающегося имени (DN) SCP, а затем использует это РАЗЛИЧАЮЩЕеся имя для непосредственной привязки к точке подключения службы для получения свойства **serviceDNSName** .</span><span class="sxs-lookup"><span data-stu-id="4bbfe-116">First, it uses the GC search to get the distinguished name (DN) of the SCP, then it uses that DN to bind directly to the SCP to retrieve the **serviceDNSName** property.</span></span>


```C++
HRESULT EnumerateServiceInstances(
       LPWSTR szQuery,                // Search string filter.
       LPWSTR *pszAttribs,            // An array of attributes 
                                      // to retrieve.
       DWORD dwAttribs,               // # of attributes requested.
       DWORD *pdwAttribs,             // # of attributes retrieved.
       ADS_ATTR_INFO **ppPropEntries  // Returns a pointer to the 
                                      // retrieved attributes.
        )
{
HRESULT hr;
IEnumVARIANT *pEnum = NULL;
IADsContainer *pCont = NULL;
VARIANT var;
IDispatch *pDisp = NULL;
BSTR  bstrPath = NULL;
ULONG lFetch;
IADs *pADs = NULL;
int iRows=0;
static IDirectorySearch *pSearch = NULL;
static ADS_SEARCH_HANDLE hSearch = NULL;

// Parameters for IDirectoryObject.
IDirectoryObject *pSCP = NULL;
 
// Structures and parameters for IDirectorySearch.
DWORD               dwPref;
ADS_SEARCH_COLUMN   Col;
ADS_SEARCHPREF_INFO SearchPref[2];
 
// First time through; set up the search.
if (pSearch == NULL) 
{
    // Bind to the GC: namespace container object. The GC DN 
    // is a single immediate child of the GC: namespace, which must 
    // be obtained through enumeration.
    hr = ADsGetObject(L"GC:", 
        IID_IADsContainer, 
        (void**) &pCont );
    if (FAILED(hr)) {
        _tprintf(TEXT("ADsGetObject(GC) failed: 0x%x\n"), hr);
        goto Cleanup;
    }
 
    // Obtain an enumeration interface for the GC container. 
    hr = ADsBuildEnumerator(pCont,&pEnum);
    if (FAILED(hr)) {
        _tprintf(TEXT("ADsBuildEnumerator failed: 0x%x\n"), hr);
        goto Cleanup;
    }
 
    // Enumerate. There is only one child of the GC: object.
    hr = ADsEnumerateNext(pEnum,1,&var,&lFetch);
    if (( hr == S_OK ) && ( lFetch == 1 ) ) 
    {
        pDisp = V_DISPATCH(&var);
        hr = pDisp->QueryInterface( IID_IADs, (void**)&pADs);
        if (hr == S_OK) 
            hr = pADs->get_ADsPath(&bstrPath);
    }
    if (FAILED(hr)) {
        _tprintf(TEXT("Enumeration failed: 0x%x\n"), hr);
        goto Cleanup;
    }
 
    // Now bstrPath contains the ADsPath for the current GC.  
    // Bind the GC to get the search interface.
    hr = ADsGetObject(bstrPath, 
                      IID_IDirectorySearch, 
                      (void**)&pSearch);
    if (FAILED(hr)) {
        _tprintf(TEXT("Failed to bind search root: 0x%x\n"), hr);
        goto Cleanup;
    } 
 
    // Set up a deep search.
    // Thousands of objects are not expected
    // in this example; request 1000 rows per page.
    dwPref=sizeof(SearchPref)/sizeof(ADS_SEARCHPREF_INFO);
    SearchPref[0].dwSearchPref =    ADS_SEARCHPREF_SEARCH_SCOPE;
    SearchPref[0].vValue.dwType =   ADSTYPE_INTEGER;
    SearchPref[0].vValue.Integer =  ADS_SCOPE_SUBTREE;
 
    SearchPref[1].dwSearchPref =    ADS_SEARCHPREF_PAGESIZE;
    SearchPref[1].vValue.dwType =   ADSTYPE_INTEGER;
    SearchPref[1].vValue.Integer =  1000;
 
    hr = pSearch->SetSearchPreference(SearchPref, dwPref);
    if (FAILED(hr))    {
        _tprintf(TEXT("Failed to set search prefs: 0x%x\n"), hr);
        goto Cleanup;
    } 
 
    // Execute the search. From the GC, get the distinguished name 
    // of the SCP. Use the DN to bind to the SCP and get the other 
    // properties.
    hr = pSearch->ExecuteSearch(szQuery, pszAttribs, 1, &hSearch);
    if (FAILED(hr)) {
        _tprintf(TEXT("ExecuteSearch failed: 0x%x\n"), hr);
        goto Cleanup;
    } 
}
 
// Get the next row.
hr = pSearch->GetNextRow(hSearch);
 
// Process the row.
if (SUCCEEDED(hr) && hr !=S_ADS_NOMORE_ROWS) 
{
    // Get the distinguished name of the object in this row.
    hr = pSearch->GetColumn(hSearch, L"distinguishedName", &Col);
    if FAILED(hr) { 
        _tprintf(TEXT("GetColumn failed: 0x%x\n"), hr);
        goto Cleanup;
    }
    // Bind to the DN to get the properties.
    if (Col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
    {
        LPWSTR szSCPPath = 
          new WCHAR[7 + lstrlenW(Col.pADsValues->CaseIgnoreString) + 1];
        wcscpy_s(szSCPPath, L"LDAP://");
        wcscat_s(szSCPPath, Col.pADsValues->CaseIgnoreString);
        hr = ADsGetObject(szSCPPath, 
                          IID_IDirectoryObject,
                          (void**)&pSCP);
        delete szSCPPath;
        if (SUCCEEDED(hr)) 
        {
            hr = pSCP->GetObjectAttributes(pszAttribs, dwAttribs,
                          ppPropEntries, pdwAttribs);
            if(FAILED(hr)) {
                _tprintf(TEXT("GetObjectAttributes Failed."), hr);
                goto Cleanup;
            }
        }
    }
    pSearch->FreeColumn(&Col);}
 
Cleanup:
if (bstrPath)
    SysFreeString(bstrPath);
if (pSCP) 
    pSCP->Release();
if (pCont) 
    pCont->Release();
if (pEnum)
    ADsFreeEnumerator(pEnum);
if (pADs) 
    pADs->Release();
if (pDisp)
    pDisp->Release();
 
return hr;
 
}
```



 

 