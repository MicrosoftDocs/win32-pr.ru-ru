---
title: Выполнение запроса к области атрибута
description: Запрос области атрибута — это предпочитаемый Поиск, позволяющий выполнять поиск атрибутов, возвращающих различающееся имя объекта.
ms.assetid: 026fbe17-5df7-4007-9d74-5c0abbe793b1
ms.tgt_platform: multiple
keywords:
- Выполнение запроса к области атрибута ADSI
- ADSI, поиск, IDirectorySearch, другие параметры поиска, запрос области атрибута
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10f5b666028c5fd46e7394b52a1328370e317bc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654363"
---
# <a name="performing-an-attribute-scope-query"></a><span data-ttu-id="d6bef-105">Выполнение запроса к области атрибута</span><span class="sxs-lookup"><span data-stu-id="d6bef-105">Performing an Attribute Scope Query</span></span>

<span data-ttu-id="d6bef-106">Запрос области атрибута — это предпочитаемый Поиск, позволяющий выполнять поиск атрибутов, возвращающих различающееся имя объекта.</span><span class="sxs-lookup"><span data-stu-id="d6bef-106">The attribute scope query is a search preference that enables a search of an object's distinguished name valued attributes to be performed.</span></span> <span data-ttu-id="d6bef-107">Искомый атрибут может иметь одно или несколько значений, но должен иметь **\_ \_ строковый тип DN** .</span><span class="sxs-lookup"><span data-stu-id="d6bef-107">The attribute to search can be either single or multi-valued, but must be of the **ADS\_DN\_STRING** type.</span></span> <span data-ttu-id="d6bef-108">При выполнении поиска ADSI перечисляет значения отличительного имени атрибута и выполняет поиск по объектам, представленным различающиеся именами.</span><span class="sxs-lookup"><span data-stu-id="d6bef-108">When the search is performed, ADSI will enumerate the distinguished name values of the attribute and perform the search on the objects represented by the distinguished names.</span></span> <span data-ttu-id="d6bef-109">Например, если в атрибуте [**member**](/windows/desktop/ADSchema/a-member) объекта группы выполняется поиск по области атрибута, ADSI будет перечислять отличительные имена в атрибуте **member** и искать все члены группы для указанных условий поиска.</span><span class="sxs-lookup"><span data-stu-id="d6bef-109">For example, if an attribute scoped search is performed of the [**member**](/windows/desktop/ADSchema/a-member) attribute of a group object, ADSI will enumerate the distinguished names in the **member** attribute and search each of the members of the group for the specified search criteria.</span></span>

<span data-ttu-id="d6bef-110">Если запрос, заданный для атрибута, выполняется для атрибута, не относящегося к **типу \_ AD \_ String DN**, поиск завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d6bef-110">If an attribute scoped query is performed on an attribute that is not of type **ADS\_DN\_STRING**, the search will fail.</span></span> <span data-ttu-id="d6bef-111">Запрос с областью действия атрибута также требует, чтобы для **ADS \_ сеарчпреф \_ \_ область поиска** было задано значение **\_ \_ база области ADS**.</span><span class="sxs-lookup"><span data-stu-id="d6bef-111">The attribute scoped query also requires that the **ADS\_SEARCHPREF\_SEARCH\_SCOPE** preference be set to **ADS\_SCOPE\_BASE**.</span></span> <span data-ttu-id="d6bef-112">Для **параметра \_ \_ \_ область поиска ADS сеарчпреф** автоматически будет задана **\_ \_ база области ADS**, но если для параметра **\_ \_ \_ область поиска ADS сеарчпреф** задано любое другое значение, [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) завершится ошибкой с **\_ \_ неверным \_ параметром E ADS**.</span><span class="sxs-lookup"><span data-stu-id="d6bef-112">The **ADS\_SEARCHPREF\_SEARCH\_SCOPE** preference will automatically be set to **ADS\_SCOPE\_BASE**, but if the **ADS\_SEARCHPREF\_SEARCH\_SCOPE** preference is set to any other value, [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) will fail with **E\_ADS\_BAD\_PARAMETER**.</span></span>

<span data-ttu-id="d6bef-113">Результаты запроса области атрибута могут охватывать несколько серверов, и сервер может не вернуть все данные, запрошенные для всех возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="d6bef-113">The results of an attribute-scope query may span multiple servers and a server may not return all the data requested for the all the rows returned.</span></span> <span data-ttu-id="d6bef-114">Если это происходит, то при получении последней строки путем вызова [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) или [**IDirectorySearch:: жетфирстров**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI возвратит **s \_ ADS \_ еррорсоккурред** вместо **S \_ ADS \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="d6bef-114">If this occurs, when the last row is retrieved by calling [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) or [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI will return **S\_ADS\_ERRORSOCCURRED** instead of **S\_ADS\_NOMORE\_ROWS**.</span></span>

<span data-ttu-id="d6bef-115">Чтобы задать запрос к области атрибута, задайте для параметра поиска **\_ \_ \_ запроса атрибута ADS Сеарчпреф** с параметром **адстипе \_ Case \_ игнорировать \_ строковое** значение, установленное в lDAPDisplayName атрибута, для поиска в массиве [**\_ \_ сведений сеарчпреф**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) , переданном в метод [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="d6bef-115">To specify an attribute scope query, set an **ADS\_SEARCHPREF\_ATTRIBUTE\_QUERY** search option with an **ADSTYPE\_CASE\_IGNORE\_STRING** value set to the lDAPDisplayName of the attribute to search in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="d6bef-116">Эта операция показана в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="d6bef-116">This operation is shown in the following code example.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
SearchPref.vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
SearchPref.vValue.Boolean = L"member";
```



<span data-ttu-id="d6bef-117">В следующем примере кода показано, как использовать параметр **поиска \_ \_ \_ запроса атрибута ADS сеарчпреф** .</span><span class="sxs-lookup"><span data-stu-id="d6bef-117">The following code example shows how to use the **ADS\_SEARCHPREF\_ATTRIBUTE\_QUERY** search option.</span></span>


```C++
/***************************************************************************

    SearchGroupMembers()

    Searches the members of a group that are of type user and prints each 
    user's cn and distinguishedName values to the console.

    Parameters:

    pwszGroupDN - Contains the distinguished name of the group whose 
    members will be searched.

***************************************************************************/

HRESULT SearchGroupMembers(LPCWSTR pwszGroupDN)
{
    HRESULT hr;
    CComPtr<IDirectorySearch> spSearch;
    CComBSTR sbstrADsPath;
 
    // Bind to the group and get the IDirectorySearch interface.
    sbstrADsPath = "LDAP://";
    sbstrADsPath += pwszGroupDN;
    hr = ADsOpenObject(sbstrADsPath,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IDirectorySearch,
        (void**)&spSearch);
    if(FAILED(hr))
    {
        return hr;
    }
 
    ADS_SEARCHPREF_INFO SearchPrefs[1];

    // Set the ADS_SEARCHPREF_ATTRIBUTE_QUERY search preference.
    SearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
    SearchPrefs[0].vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
    SearchPrefs[0].vValue.CaseIgnoreString = L"member";

    // Set the search preferences.
    hr = spSearch->SetSearchPreference(SearchPrefs, sizeof(SearchPrefs)/sizeof(ADS_SEARCHPREF_INFO));
    if(FAILED(hr))
    {
        return hr;
    }

    ADS_SEARCH_HANDLE hSearch;
    
    // Create the search filter.
    LPWSTR pwszSearchFilter = L"(&(objectClass=user))";
 
    // Set attributes to return.
    LPWSTR rgpwszAttributes[] = {L"cn", L"distinguishedName"};
    DWORD dwNumAttributes = sizeof(rgpwszAttributes)/sizeof(LPWSTR);
 
    // Execute the search.
    hr = spSearch->ExecuteSearch(pwszSearchFilter,
        rgpwszAttributes,
        dwNumAttributes,
        &hSearch);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the first result row.
    hr = spSearch->GetFirstRow(hSearch);
    while(S_OK == hr)
    {
        ADS_SEARCH_COLUMN col;

        // Enumerate the retrieved attributes.
        for(DWORD i = 0; i < dwNumAttributes; i++)
        {
            hr = spSearch->GetColumn(hSearch, rgpwszAttributes[i], &col);
            if(SUCCEEDED(hr))
            {
                switch(col.dwADsType)
                {
                case ADSTYPE_DN_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].DNString);
                    break;

                case ADSTYPE_CASE_IGNORE_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].CaseExactString);
                    break;

                default:
                    break;
                }
                
                // Free the column.
                spSearch->FreeColumn(&col);
            }
        }
        
        // Get the next row.
        hr = spSearch->GetNextRow(hSearch);
    }

    // Close the search handle to cleanup.
    hr = spSearch->CloseSearchHandle(hSearch);

    return hr;
}
```



<span data-ttu-id="d6bef-118">При выполнении этого поиска и перечислении результатов возвращается **имя**, **номер телефона** и **номер офиса** для всех объектов пользователя, содержащихся в списке атрибутов **членов** группы.</span><span class="sxs-lookup"><span data-stu-id="d6bef-118">When this search is executed and the results are enumerated, it would return the **name**, **telephone number**, and **office number** of all of the user objects contained in the group's **member** attribute list.</span></span>

<span data-ttu-id="d6bef-119">Обработка ошибок: результаты запроса области атрибута могут охватывать несколько серверов, и сервер может не вернуть все данные, запрошенные для всех возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="d6bef-119">Error handling: The results of an attribute-scope query may span multiple servers and a server may not return all the data requested for the all the rows returned.</span></span> <span data-ttu-id="d6bef-120">В этом случае, когда последняя строка извлекается путем вызова [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) или [**жетфирстров**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI возвращает **S \_ ADS \_ еррорсоккурред**, а не в **\_ объявлениях \_ \_ строки**.</span><span class="sxs-lookup"><span data-stu-id="d6bef-120">If this occurs, when the last row is retrieved by calling [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) or [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI will return **S\_ADS\_ERRORSOCCURRED**, instead of **S\_ADS\_NOMORE\_ROWS**.</span></span>

 

 