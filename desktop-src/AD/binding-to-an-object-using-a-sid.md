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
# <a name="binding-to-an-object-using-a-sid"></a>Привязка к объекту с помощью идентификатора безопасности

В Windows Server 2003 можно выполнить привязку к объекту с помощью идентификатора безопасности объекта (SID), а также идентификатора GUID. Идентификатор безопасности объекта хранится в атрибуте **objectSid** . Привязка к идентификатору безопасности не работает в Windows 2000.

Поставщик LDAP для служб домен Active Directory предоставляет метод для привязки к объекту с помощью идентификатора безопасности объекта. Формат строки привязки:


```C++
LDAP://servername/<SID=XXXXX>
```



В этом примере "servername" — это имя сервера каталогов, а "XXXXX" — строковое представление шестнадцатеричного значения идентификатора безопасности. "Servername" является необязательным. Строка идентификатора безопасности указывается в форме, где каждый символ в строке является шестнадцатеричным представлением каждого байта идентификатора SID. Например, если массив имеет следующее значение:


```C++
0xAB 0x14 0xE2
```



Строка привязки SID будет иметь значение &lt; SID = AB14E2 &gt; . Функция [**адсенкодебинаридата**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) не должна использоваться для преобразования массива SID в строку, поскольку она предшествует каждому символу с обратной косой чертой, что не является допустимым форматом строки привязки.

Строка идентификатора безопасности может также принимать форму " &lt; SID = S-x-x-XX-кскскскскскскскскскс-кскскскскскскскскскс-XXXXXXXXX-XXX &gt; ", где часть "S-X-x-XX-КСКСКСКСКСКСКСКСКСКС-КСКСКСКСКСКСКСКСКСКС-XXXXXXXXX-XXX" совпадает со строкой, возвращаемой функцией [**функция ConvertSidToStringSid вернула**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) .

При привязке с использованием идентификатора безопасности объекта некоторые методы и свойства метода [**iAds**](/windows/desktop/api/iads/nn-iads-iads) и [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) не поддерживаются. Следующие свойства **iAds** не поддерживаются объектами, полученными при привязке с помощью идентификатора безопасности объекта:

-   [**Действитель**](/windows/desktop/ADSI/iads-property-methods)
-   [**Имя**](/windows/desktop/ADSI/iads-property-methods)
-   [**Parent**](/windows/desktop/ADSI/iads-property-methods)

Следующие методы **иадсконтаинер** не поддерживаются объектами, полученными с помощью привязки с использованием идентификатора безопасности объекта:

-   [**GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**Создать**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**Удалить**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**копихере**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**мовехере**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Чтобы использовать эти методы и свойства после привязки к объекту с помощью идентификатора безопасности объекта, используйте метод [**iAds. Get**](/windows/desktop/api/iads/nf-iads-iads-get) , чтобы получить различающееся имя объекта, а затем используйте различающееся имя для повторной привязки к объекту.

В следующем примере кода показано, как преобразовать **objectSid** в строку с возможностью привязки.


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



 

 