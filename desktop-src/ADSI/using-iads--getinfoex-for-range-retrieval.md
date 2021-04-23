---
title: Использование функции IADs Жетинфоекс для получения диапазона
description: Метод IADs. Жетинфоекс можно использовать для получения диапазона значений атрибутов. Диапазон извлекаемых значений задается в массиве имен атрибутов, переданном методу.
ms.assetid: 2098862f-e5ec-4912-a941-8faceade22ee
ms.tgt_platform: multiple
keywords:
- Использование функции IADs Жетинфоекс для получения диапазона ADSI
- IADs Жетинфоекс ADSI, использование для получения диапазона
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50681facd811adf26a89754fecb5490ee059eed6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986082"
---
# <a name="using-iadsgetinfoex-for-range-retrieval"></a><span data-ttu-id="fb5aa-106">Использование метода IADs:: Жетинфоекс для получения диапазона</span><span class="sxs-lookup"><span data-stu-id="fb5aa-106">Using IADs::GetInfoEx for Range Retrieval</span></span>

<span data-ttu-id="fb5aa-107">Метод [**iAds. жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) можно использовать для получения диапазона значений атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fb5aa-107">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method can be used to retrieve a range of attribute values.</span></span> <span data-ttu-id="fb5aa-108">Диапазон извлекаемых значений задается в массиве имен атрибутов, переданном методу.</span><span class="sxs-lookup"><span data-stu-id="fb5aa-108">The range of values to retrieve is specified in the attribute name array passed to the method.</span></span>

<span data-ttu-id="fb5aa-109">Описатели диапазона для запроса свойства должны иметь следующую форму:</span><span class="sxs-lookup"><span data-stu-id="fb5aa-109">The range specifiers for a property query require the following form:</span></span>


```C++
<property name>;range=<low range>-<high range>
```



<span data-ttu-id="fb5aa-110">где " &lt; имя свойства &gt; " является атрибутом **LdapDisplayName** атрибута, " &lt; младший диапазон &gt; " — это Отсчитываемый от нуля индекс первого значения атрибута, который требуется получить, а " &lt; Верхний диапазон" &gt; — Отсчитываемый от нуля индекс последнего значения атрибута, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="fb5aa-110">where "&lt;property name&gt;" is the **ldapDisplayName** of the attribute, "&lt;low range&gt;" is the zero-based index of the first attribute value to retrieve and "&lt;high range&gt;" is the zero-based index of the last attribute value to retrieve.</span></span> <span data-ttu-id="fb5aa-111">Ноль используется для " &lt; неограниченный диапазон &gt; " для указания первой записи.</span><span class="sxs-lookup"><span data-stu-id="fb5aa-111">Zero is used for "&lt;low range&gt;" to specify the first entry.</span></span> <span data-ttu-id="fb5aa-112">Подстановочный знак ( \* ) можно использовать для " &lt; верхнего диапазона &gt; ", чтобы указать все оставшиеся записи.</span><span class="sxs-lookup"><span data-stu-id="fb5aa-112">The wildcard character (\*) can be used for "&lt;high range&gt;" to specify all remaining entries.</span></span>

<span data-ttu-id="fb5aa-113">Следующий пример кода содержит функцию, которая показывает, как использовать извлечение диапазона с помощью функции [**iAds:: жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) для перечисления членов группы.</span><span class="sxs-lookup"><span data-stu-id="fb5aa-113">The following code example contains a function that shows how to use range retrieval with [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) to enumerate the members of a group.</span></span>


```C++
HRESULT EnumGroupWithGetInfoEx(LPCWSTR pwszGroupDN, 
                               LPCWSTR pwszUsername, 
                               LPCWSTR pwszPassword)
{
    if(NULL == pwszGroupDN)
    {
        return E_POINTER;
    }
    
    HRESULT hr;
    IADs *pads;

    hr = ADsOpenObject( pwszGroupDN,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (void**)&pads);

    if(SUCCEEDED(hr))
    {
        const DWORD dwStep = 1000;
        DWORD dwLowRange;
        DWORD dwHighRange;
        WCHAR wszAttr[MAX_PATH];
        LPWSTR rgAttrs[1];

        rgAttrs[0] = wszAttr;

        dwLowRange = 0;
        dwHighRange = dwLowRange + (dwStep - 1);

        do
        {
            VARIANT var;

            // Perform this query with the "range=<lowRange>-<highRange>" range.
            swprintf_s(wszAttr, L"member;range=%d-%d", dwLowRange, dwHighRange);
    
            hr = ADsBuildVarArrayStr(rgAttrs, 1, &var);
            if(SUCCEEDED(hr))
            {
                hr = pads->GetInfoEx(var, 0);
                
                VariantClear(&var);

                if(SUCCEEDED(hr))
                {
                    hr = pads->Get(CComBSTR("member"), &var);
                    if(SUCCEEDED(hr))
                    {
                        if(var.vt == (VT_VARIANT | VT_ARRAY))
                        {
                            VARIANT *pVar;
                            long lLBound, lUBound;

                            // Get the array of VARIANTs.
                            hr = SafeArrayAccessData((SAFEARRAY*)(var.pparray), (void HUGEP* FAR*)&pVar);
                            if(SUCCEEDED(hr))
                            {
                                // Get the bounds for the array.
                                hr = SafeArrayGetLBound((SAFEARRAY*)(var.pparray), 1, &lLBound);
                                hr = SafeArrayGetUBound((SAFEARRAY*)(var.pparray), 1, &lUBound);

                                // Get the number of elements.
                                long cElements = lUBound - lLBound + 1;

                                // Enumerate the elements.
                                for(long i = 0; i < cElements; i++)
                                {
                                    switch(pVar[i].vt)
                                    {
                                    case VT_BSTR:
                                        wprintf(pVar[i].bstrVal); 
                                        wprintf(L"\n"); 
                                        break;
                                    }
                                }

                                // Release the array.
                                SafeArrayUnaccessData((SAFEARRAY*)(var.pparray));
                            }
                        }
                        // This occurs only if one element is retrieved.
                        else if (var.vt == VT_BSTR)
                        {
                            wprintf(var.bstrVal); 
                            wprintf(L"\n"); 
                        }

                        VariantClear(&var);
                    }

                    // Increment the high and low ranges to query for the next block of objects.
                    dwLowRange = dwHighRange + 1;
                    dwHighRange = dwLowRange + (dwStep - 1);
                }
            }
        }while(SUCCEEDED(hr));

        pads->Release();
    }

    return hr;
}
```



<span data-ttu-id="fb5aa-114">Следующий пример кода содержит функцию, которая показывает, как использовать извлечение диапазона с помощью функции [**iAds. жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) для перечисления членов группы.</span><span class="sxs-lookup"><span data-stu-id="fb5aa-114">The following code example contains a function that shows how to use range retrieval with [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) to enumerate the members of a group.</span></span>


```VB
Private Sub EnumGroupMembersWithGetInfoEx(strGroupDN As String, strUsername As String, strPassword As String)
    Dim oGroup As IADs
    Dim dso As IADsOpenDSObject
    
    On Error GoTo quit
        
    strPath = "LDAP://" & strGroupDN
    
    If "" <> strUsername Then
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("LDAP:")
        Set oGroup = dso.OpenDSObject(strPath, strUsername, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oGroup = GetObject(strPath)
    End If
    
    ' For compatibility with all operating systems, the number of objects
    ' retrieved by each query should not exceed 999. The number of objects
    ' to retrieve should be as close as possible to 999 to reduce the number
    ' of round trips to the server necessary to retrieve the objects.
    rangeStep = 999
    lowRange = 0
    highRange = lowRange + rangeStep
    
    Do
        ' Use the "member;range=<lowRange>-<highRange>" syntax.
        strCommandText = "member;range=" & lowRange & "-" & highRange
        Debug.Print "Current search command: " & strCommandText
        
        ' Load the specified range of members into the local cache. This will
        ' throw an error if the range exceeds the properties contained in the
        ' object. The "On Error GoTo quit" error handler will cause the loop
        ' to terminate when this happens.
        On Error GoTo quit
        oGroup.GetInfoEx Array(strCommandText), 0
        
        ' Enumerate the retrieved members.
        oMembers = oGroup.Get("member")
        If vbArray And VarType(oMembers) Then
            For Each oMember In oMembers
                ' Add the member.
                Debug.Print oMember
                nRetrieved = nRetrieved + 1
            Next
        Else
            ' oGroup.Get returned only one member, so add it to the list.
            Debug.Print oMembers
            nRetrieved = nRetrieved + 1
        End If
        
        ' Increment the high and low ranges to query for the next block of objects.
        lowRange = highRange + 1
        highRange = lowRange + rangeStep
    Loop While True
    
quit:
End Sub
```



 

 




