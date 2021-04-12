---
title: Привязка к объекту с помощью идентификатора безопасности
description: В Windows Server 2003 можно выполнить привязку к объекту с помощью идентификатора безопасности объекта (SID), а также идентификатора GUID. Идентификатор безопасности объекта хранится в атрибуте objectSID. Привязка к идентификатору безопасности не работает в Windows 2000.
ms.assetid: 18b4613c-eb93-4204-96f2-0f91d7900587
ms.tgt_platform: multiple
keywords:
- Привязка к объекту с помощью идентификатора безопасности Active Directory
- Active Directory, использование, привязка, привязка к объекту с помощью идентификатора безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ad4ecf2d6faa385ab8085730e4f1cb0689e403
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487508"
---
# <a name="binding-to-an-object-using-a-sid"></a><span data-ttu-id="7768c-107">Привязка к объекту с помощью идентификатора безопасности</span><span class="sxs-lookup"><span data-stu-id="7768c-107">Binding to an Object Using a SID</span></span>

<span data-ttu-id="7768c-108">В Windows Server 2003 можно выполнить привязку к объекту с помощью идентификатора безопасности объекта (SID), а также идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="7768c-108">In Windows Server 2003, it is possible to bind to an object using the object Security Identifier (SID) as well as a GUID.</span></span> <span data-ttu-id="7768c-109">Идентификатор безопасности объекта хранится в атрибуте **objectSid** .</span><span class="sxs-lookup"><span data-stu-id="7768c-109">The object SID is stored in the **objectSID** attribute.</span></span> <span data-ttu-id="7768c-110">Привязка к идентификатору безопасности не работает в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7768c-110">Binding to an SID does not work on Windows 2000.</span></span>

<span data-ttu-id="7768c-111">Поставщик LDAP для служб домен Active Directory предоставляет метод для привязки к объекту с помощью идентификатора безопасности объекта.</span><span class="sxs-lookup"><span data-stu-id="7768c-111">The LDAP provider for Active Directory Domain Services provides a method to bind to an object using the object SID.</span></span> <span data-ttu-id="7768c-112">Формат строки привязки:</span><span class="sxs-lookup"><span data-stu-id="7768c-112">The binding string format is:</span></span>


```C++
LDAP://servername/<SID=XXXXX>
```



<span data-ttu-id="7768c-113">В этом примере "servername" — это имя сервера каталогов, а "XXXXX" — строковое представление шестнадцатеричного значения идентификатора безопасности.</span><span class="sxs-lookup"><span data-stu-id="7768c-113">In this example, "servername" is the name of the directory server and "XXXXX" is the string representation of the hexadecimal value of the SID.</span></span> <span data-ttu-id="7768c-114">"Servername" является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7768c-114">The "servername" is optional.</span></span> <span data-ttu-id="7768c-115">Строка идентификатора безопасности указывается в форме, где каждый символ в строке является шестнадцатеричным представлением каждого байта идентификатора SID.</span><span class="sxs-lookup"><span data-stu-id="7768c-115">The SID string is specified in a form where each character in the string is the hexadecimal representation of each byte of the SID.</span></span> <span data-ttu-id="7768c-116">Например, если массив имеет следующее значение:</span><span class="sxs-lookup"><span data-stu-id="7768c-116">For example, if the array is:</span></span>


```C++
0xAB 0x14 0xE2
```



<span data-ttu-id="7768c-117">Строка привязки SID будет иметь значение &lt; SID = AB14E2 &gt; .</span><span class="sxs-lookup"><span data-stu-id="7768c-117">the SID binding string would be "&lt;SID=AB14E2&gt;".</span></span> <span data-ttu-id="7768c-118">Функция [**адсенкодебинаридата**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) не должна использоваться для преобразования массива SID в строку, поскольку она предшествует каждому символу с обратной косой чертой, что не является допустимым форматом строки привязки.</span><span class="sxs-lookup"><span data-stu-id="7768c-118">The [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) function should not be used to convert the SID array into a string because it precedes each byte character with a backslash, which is not a valid bind string format.</span></span>

<span data-ttu-id="7768c-119">Строка идентификатора безопасности может также принимать форму " &lt; SID = S-x-x-XX-кскскскскскскскскскс-кскскскскскскскскскс-XXXXXXXXX-XXX &gt; ", где часть "S-X-x-XX-КСКСКСКСКСКСКСКСКСКС-КСКСКСКСКСКСКСКСКСКС-XXXXXXXXX-XXX" совпадает со строкой, возвращаемой функцией [**функция ConvertSidToStringSid вернула**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) .</span><span class="sxs-lookup"><span data-stu-id="7768c-119">The SID string can also take the form "&lt;SID=S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX&gt;", where the "S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX" portion is the same as the string returned by the [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) function.</span></span>

<span data-ttu-id="7768c-120">При привязке с использованием идентификатора безопасности объекта некоторые методы и свойства метода [**iAds**](/windows/desktop/api/iads/nn-iads-iads) и [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="7768c-120">When binding using the object SID, some [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) methods and properties are not supported.</span></span> <span data-ttu-id="7768c-121">Следующие свойства **iAds** не поддерживаются объектами, полученными при привязке с помощью идентификатора безопасности объекта:</span><span class="sxs-lookup"><span data-stu-id="7768c-121">The following **IADs** properties are not supported by objects obtained by binding using the object SID:</span></span>

-   [<span data-ttu-id="7768c-122">**Действитель**</span><span class="sxs-lookup"><span data-stu-id="7768c-122">**ADsPath**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="7768c-123">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7768c-123">**Name**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="7768c-124">**Parent**</span><span class="sxs-lookup"><span data-stu-id="7768c-124">**Parent**</span></span>](/windows/desktop/ADSI/iads-property-methods)

<span data-ttu-id="7768c-125">Следующие методы **иадсконтаинер** не поддерживаются объектами, полученными с помощью привязки с использованием идентификатора безопасности объекта:</span><span class="sxs-lookup"><span data-stu-id="7768c-125">The following **IADsContainer** methods are not supported by objects obtained by binding using the object SID:</span></span>

-   [<span data-ttu-id="7768c-126">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="7768c-126">**GetObject**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [<span data-ttu-id="7768c-127">**Создать**</span><span class="sxs-lookup"><span data-stu-id="7768c-127">**Create**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [<span data-ttu-id="7768c-128">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="7768c-128">**Delete**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [<span data-ttu-id="7768c-129">**копихере**</span><span class="sxs-lookup"><span data-stu-id="7768c-129">**CopyHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [<span data-ttu-id="7768c-130">**мовехере**</span><span class="sxs-lookup"><span data-stu-id="7768c-130">**MoveHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

<span data-ttu-id="7768c-131">Чтобы использовать эти методы и свойства после привязки к объекту с помощью идентификатора безопасности объекта, используйте метод [**iAds. Get**](/windows/desktop/api/iads/nf-iads-iads-get) , чтобы получить различающееся имя объекта, а затем используйте различающееся имя для повторной привязки к объекту.</span><span class="sxs-lookup"><span data-stu-id="7768c-131">To use these methods and properties after binding to an object using the object SID, use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve the object distinguished name and then use the distinguished name to bind to the object again.</span></span>

<span data-ttu-id="7768c-132">В следующем примере кода показано, как преобразовать **objectSid** в строку с возможностью привязки.</span><span class="sxs-lookup"><span data-stu-id="7768c-132">The following code example shows how to convert an **objectSid** into a bindable string.</span></span>


```C++
HRESULT VariantArrayToBytes(VARIANT Variant, 
    LPBYTE *ppBytes, 
    DWORD *pdwBytes);

/********

    GetSIDBindStringFromVariant()

    Converts a SID in VARIANT form, such as an objectSid value, and 
    converts it into a bindable string in the form:

    LDAP://<SID=xxxxxxx...>

    The returned string is allocated with AllocADsMem and must be 
    freed by the caller with FreeADsMem.

*********/

LPWSTR GetSIDBindStringFromVariant(VARIANT vSID)
{
    LPWSTR pwszReturn = NULL;

    if(VT_ARRAY & vSID.vt) 
    {
        HRESULT hr;
        LPBYTE pByte;
        DWORD dwBytes = 0;

        hr = VariantArrayToBytes(vSID, &pByte, &dwBytes);
        if(S_OK == hr)
        {
            // Convert the BYTE array into a string of hex 
            // characters.
            CComBSTR sbstrTemp = "LDAP://<SID=";

            for(DWORD i = 0; i < dwBytes; i++)
            {
                WCHAR wszByte[3];

                swprintf_s(wszByte, L"%02x", pByte[i]);
                sbstrTemp += wszByte;
            }

            sbstrTemp += ">";
            pwszReturn = 
               (LPWSTR)AllocADsMem((sbstrTemp.Length() + 1) * 
                sizeof(WCHAR));
            if(pwszReturn)
            {
                wcscpy_s(pwszReturn, sbstrTemp.m_str);
            }

            FreeADsMem(pByte);
        }
    }

    return pwszReturn;
}

/*********

    VariantArrayToBytes()

    This function converts a VARIANT array into an array of BYTES. 
    This function allocates the buffer using AllocADsMem. The 
    caller must free this memory with FreeADsMem when it is no 
    longer required.

**********/

HRESULT VariantArrayToBytes(VARIANT Variant, 
    LPBYTE *ppBytes, 
    DWORD *pdwBytes)
{
    if(!(Variant.vt & VT_ARRAY) ||
        !Variant.parray ||
        !ppBytes ||
        !pdwBytes)
    {
        return E_INVALIDARG;
    }

    *ppBytes = NULL;
    *pdwBytes = 0;

    HRESULT hr = E_FAIL;
    SAFEARRAY *pArrayVal = NULL;
    CHAR HUGEP *pArray = NULL;
    
    // Retrieve the safe array.
    pArrayVal = Variant.parray;
    DWORD dwBytes = pArrayVal->rgsabound[0].cElements;
    *ppBytes = (LPBYTE)AllocADsMem(dwBytes);
    if(NULL == *ppBytes) 
    {
        return E_OUTOFMEMORY;
    }

    hr = SafeArrayAccessData(pArrayVal, (void HUGEP * FAR *) &pArray);
    if(SUCCEEDED(hr))
    {
        // Copy the bytes to the safe array.
        CopyMemory(*ppBytes, pArray, dwBytes);
        SafeArrayUnaccessData( pArrayVal );
        *pdwBytes = dwBytes;
    }
    
    return hr;
}
```



 

 