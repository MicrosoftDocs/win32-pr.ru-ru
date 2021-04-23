---
title: Пример кода для поиска контейнера секций
description: Этот раздел содержит примеры кода, в которых находится контейнер секций.
ms.assetid: 7aa6ad5a-7baf-484a-9296-eafb61da5f4e
ms.tgt_platform: multiple
keywords:
- Пример кода для поиска контейнера секций Active Directory
- Разделы каталога приложений Active Directory, пример кода для поиска контейнера секций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f10156894a71a3308b58d125c16782497e5f29
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "105654299"
---
# <a name="example-code-for-locating-the-partitions-container"></a><span data-ttu-id="a7646-105">Пример кода для поиска контейнера секций</span><span class="sxs-lookup"><span data-stu-id="a7646-105">Example Code for Locating the Partitions Container</span></span>

<span data-ttu-id="a7646-106">Этот раздел содержит примеры кода, в которых находится контейнер секций.</span><span class="sxs-lookup"><span data-stu-id="a7646-106">This topic includes code examples that locate the partition container.</span></span>

<span data-ttu-id="a7646-107">Следующий пример кода C/C++ Возвращает различающееся имя контейнера секций путем поиска объекта [**кроссрефконтаинер**](/windows/desktop/ADSchema/c-crossrefcontainer) в контейнере конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a7646-107">The following C/C++ code example gets the distinguished name of the Partitions container by searching the configuration container for the [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) object.</span></span>


```C++
/***************************************************************************

    GetPartitionsDNSearch()

    Description: Gets the distinguished name of the Partitions container in 
    the current enterprise forest.

    Parameters:

    ppwszPartitionsDN - Pointer to an LPWSTR that receives the distinguished 
    name string. The caller must free this memory with 
    FreeADsMem when it is no longer required.

***************************************************************************/

HRESULT GetPartitionsDNSearch(LPWSTR *ppwszPartitionsDN)
{
 
    *ppwszPartitionsDN = NULL;
    
    HRESULT hr;

    IADs *padsRootDSE;

    // Bind to the RootDSE to get the configurationNamingContext property.
    hr = ADsOpenObject( L"LDAP://RootDSE",
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&padsRootDSE);

    if(SUCCEEDED(hr))
    {
        CComVariant svar;

        // Get the configurationNamingContext property.
        hr = padsRootDSE->Get(CComBSTR("configurationNamingContext"), &svar);
        if(SUCCEEDED(hr))
        {
            IDirectorySearch *pConfigSearch;

            // Bind to the Configuration container.
            CComBSTR sbstrPath = "LDAP://";
            sbstrPath += svar.bstrVal;

            hr = ADsOpenObject( sbstrPath,
                                NULL,
                                NULL,
                                ADS_SECURE_AUTHENTICATION,
                                IID_IDirectorySearch, 
                                (LPVOID*)&pConfigSearch);

            if(SUCCEEDED(hr))
            {
                // Search for an object that is of type crossRefContainer.
                ADS_SEARCHPREF_INFO SearchPref[1];

                // Set the search scope.
                SearchPref[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
                SearchPref[0].vValue.dwType = ADSTYPE_INTEGER;
                SearchPref[0].vValue.Integer = ADS_SCOPE_ONELEVEL;
                
                hr = pConfigSearch->SetSearchPreference(SearchPref, sizeof(SearchPref)/sizeof(ADS_SEARCHPREF_INFO));
                if(SUCCEEDED(hr))
                {
                    ADS_SEARCH_HANDLE hSearch = NULL;
                    LPWSTR pwszAttributes[1] = {L"distinguishedName"};
                    LPWSTR pwszSearchFilter = L"(&(objectClass=crossRefContainer))";
                    
                    // Execute the search.
                    hr = pConfigSearch->ExecuteSearch(pwszSearchFilter, 
                        pwszAttributes, 
                        sizeof(pwszAttributes)/sizeof(LPWSTR), 
                        &hSearch);
                    if(SUCCEEDED(hr))
                    {
                        // Get the first result row. There should never be more than one match.
                        hr = pConfigSearch->GetFirstRow(hSearch);
                        if(S_OK == hr)
                        {
                            ADS_SEARCH_COLUMN col;

                            // Get the search result. The distinguishedName attribute will be a string.
                            hr = pConfigSearch->GetColumn(hSearch, pwszAttributes[0], &col);
                            if(SUCCEEDED(hr))
                            {
                                // col.pADsValues[0].DNString;
                                DWORD dwChars = lstrlenW(col.pADsValues[0].DNString) + 1;
                                
                                *ppwszPartitionsDN = (LPWSTR)AllocADsMem(dwChars * sizeof(WCHAR));
                                
                                if(*ppwszPartitionsDN)
                                {
                                    wcsncpy_s(*ppwszPartitionsDN, col.pADsValues[0].DNString, dwChars);
                                }
                                else
                                {
                                    hr = E_OUTOFMEMORY;
                                }

                                pConfigSearch->FreeColumn(&col);
                            }
                        }
                        else
                        {
                            hr = HRESULT_FROM_WIN32(ERROR_NOT_FOUND);
                        }
                        
                        // Close the search handle to cleanup.
                        pConfigSearch->CloseSearchHandle(hSearch);
                    }
                }

                pConfigSearch->Release();
            }
        }
        
        padsRootDSE->Release();
    }

    return hr;
}
```



<span data-ttu-id="a7646-108">Следующий пример кода Visual Basic сценариев выпуска получает различающееся имя контейнера секций путем поиска объекта [**кроссрефконтаинер**](/windows/desktop/ADSchema/c-crossrefcontainer) в контейнере конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a7646-108">The following Visual Basic Scripting Edition code example gets the distinguished name of the Partitions container by searching the configuration container for the [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) object.</span></span>


```VB
Const ADS_SECURE_AUTHENTICATION = 1

'
'   GetPartitionsDNSearch
'
'   Description: Gets the distinguished name of the Partitions container in
'   the current enterprise forest.
'
Function GetPartitionsDNSearch()
    ' Bind to RootDSE.
    Set oRootDSE = GetObject("LDAP://RootDSE")
    
    Set oConn = CreateObject("ADODB.Connection")
    Set oComm = CreateObject("ADODB.Command")
     
    oConn.Provider = "ADsDSOObject"

    ' Set the binding options for the search.
    oConn.Properties("ADSI Flag") = ADS_SECURE_AUTHENTICATION
    
    oConn.Open
    oComm.ActiveConnection = oConn
    
    oComm.CommandText = "<LDAP://" + oRootDSE.Get("configurationNamingContext") + ">;(&(objectClass=crossRefContainer));distinguishedName;onelevel"
    
    ' WScript.Echo oComm.CommandText
    
    ' Execute the query.
    Set oResults = oComm.Execute
    
    ' Get the first result. This should be the only result.
    Set oField = oResults(0)
    
    GetPartitionsDNSearch = oField.Value
End Function
```



<span data-ttu-id="a7646-109">В следующем примере кода C/C++ получается различающееся имя контейнера секций путем создания различающегося имени вручную.</span><span class="sxs-lookup"><span data-stu-id="a7646-109">The following C/C++ code example gets the distinguished name of the Partitions container by manually building the distinguished name.</span></span>


```C++
/***************************************************************************

    GetPartitionsDNManual()

    Description: Gets the distinguished name of the Partitions container in 
    the current enterprise forest.

    Parameters:

    ppwszPartitionsDN - Pointer to an LPWSTR that receives the distinguished 
    name string. The caller must free this memory with 
    FreeADsMem when it is no longer required.

***************************************************************************/

HRESULT GetPartitionsDNManual(LPWSTR *ppwszPartitionsDN)
{

    *ppwszPartitionsDN = NULL;

    HRESULT hr;

    IADs *padsRootDSE;

    // Bind to the RootDSE to get the configurationNamingContext property.
    hr = ADsOpenObject( L"LDAP://RootDSE",
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&padsRootDSE);

    if(SUCCEEDED(hr))
    {
        CComVariant svar;

        // Get the configurationNamingContext property.
        hr = padsRootDSE->Get(CComBSTR("configurationNamingContext"), &svar);
        if(SUCCEEDED(hr))
        {
            CComBSTR sbstrDN = "CN=Partitions,";
            sbstrDN += svar.bstrVal;
            DWORD dwChars = sbstrDN.Length() + 1;

            *ppwszPartitionsDN = (LPWSTR)AllocADsMem(dwChars * sizeof(WCHAR));
            
            if(*ppwszPartitionsDN)
            {
                wcsncpy_s(*ppwszPartitionsDN, sbstrDN.m_str, dwChars);
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
        
        padsRootDSE->Release();
    }

    return hr;
}
```



<span data-ttu-id="a7646-110">В следующем Visual Basic примере кода получается различающееся имя контейнера секций путем создания различающегося имени вручную.</span><span class="sxs-lookup"><span data-stu-id="a7646-110">The following Visual Basic code example gets the distinguished name of the Partitions container by manually building the distinguished name.</span></span>


```VB
'
'   GetPartitionsDNManual
'
'   Description: Gets the distinguished name of the Partitions container in
'   the current enterprise forest.
'
Function GetPartitionsDNManual()
    ' Bind to RootDSE.
    Set oRootDSE = GetObject("LDAP://RootDSE")
    
    ' Get the configurationNamingContext property.
    GetPartitionsDNManual = "CN=Partitions," + oRootDSE.Get("configurationNamingContext")
End Function
```



<span data-ttu-id="a7646-111">В следующем примере кода C# получается различающееся имя контейнера секций путем поиска объекта [**кроссрефконтаинер**](/windows/desktop/ADSchema/c-crossrefcontainer) в контейнере конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a7646-111">The following C# code example gets the distinguished name of the Partitions container by searching the configuration container for the [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) object.</span></span> <span data-ttu-id="a7646-112">В этом примере используется C# с System. DirectoryServices.</span><span class="sxs-lookup"><span data-stu-id="a7646-112">This example uses C# with System.DirectoryServices.</span></span>


```CSharp
/***************************************************************************

    GetPartitionsDN()

    Description: Gets the distinguished name of the Partition container in 
    the current enterprise forest.

***************************************************************************/

static string GetPartitionsDN()
{
    // Bind to the RootDSE to get the configurationNamingContext property.
    DirectoryEntry RootDSE = new DirectoryEntry("LDAP://RootDSE");
    DirectoryEntry ConfigContainer = new DirectoryEntry("LDAP://" + 
        RootDSE.Properties["configurationNamingContext"].Value);

    // Search for an object that is of type crossRefContainer.
    DirectorySearcher ConfigSearcher = new DirectorySearcher(ConfigContainer);
    ConfigSearcher.Filter = "(&(objectClass=crossRefContainer))";
    ConfigSearcher.PropertiesToLoad.Add("distinguishedName");
    ConfigSearcher.SearchScope = SearchScope.OneLevel;

    SearchResult result = ConfigSearcher.FindOne();

    return result.Properties["distinguishedName"][0].ToString();
}
```



<span data-ttu-id="a7646-113">В следующем Visual Basic примере кода .NET получается различающееся имя контейнера секций путем поиска объекта [**кроссрефконтаинер**](/windows/desktop/ADSchema/c-crossrefcontainer) в контейнере конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a7646-113">The following Visual Basic .NET code example gets the distinguished name of the Partition container by searching the configuration container for the [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) object.</span></span> <span data-ttu-id="a7646-114">В этом примере используется Visual Basic .NET с System. DirectoryServices.</span><span class="sxs-lookup"><span data-stu-id="a7646-114">This example uses Visual Basic .NET with System.DirectoryServices.</span></span>


```VB
'**************************************************************************
'
'   GetPartitionsDN()
'
'
'   Description: Gets the distinguished name of the Partitions container in 
'   the current enterprise forest.
'
'**************************************************************************

Function GetPartitionsDN() As String
    ' Bind to the RootDSE to get the configurationNamingContext property.
    Dim RootDSE As New DirectoryEntry("LDAP://RootDSE")

    ' Bind to the Configuraiton container.
    Dim Path As String = "LDAP://" + RootDSE.Properties("configurationNamingContext").Value
    Dim ConfigContainer As New DirectoryEntry(Path)

    ' Search for an object that is of type crossRefContainer.
    Dim ConfigSearcher As New DirectorySearcher(ConfigContainer)
    ConfigSearcher.Filter = "(&(objectClass=crossRefContainer))"
    ConfigSearcher.SearchScope = SearchScope.OneLevel

    Dim result As SearchResult = ConfigSearcher.FindOne()

    Return result.Properties("distinguishedName")(0).ToString()
End Function
```



 

 