---
title: Как указать значения для сравнения
description: Каждый тип атрибута имеет синтаксис, который определяет тип значений сравнения, которые можно указать в фильтре поиска для этого атрибута.
ms.assetid: 72bd58e4-e1c3-40a5-9917-4910f40c52c5
ms.tgt_platform: multiple
keywords:
- Как задать значения для сравнения в AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5babc7d9781895c9671594214e4e036a85ef951cdb4b97ba34d708d160dd8fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188125"
---
# <a name="how-to-specify-comparison-values"></a>Как указать значения для сравнения

Каждый тип атрибута имеет синтаксис, который определяет тип значений сравнения, которые можно указать в фильтре поиска для этого атрибута.

В следующих разделах описаны требования для каждого синтаксиса атрибутов. Дополнительные сведения о синтаксисе атрибутов см. [в разделе синтаксис атрибутов в домен Active Directory Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

<dl> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Логическая
</dt> <dd>

Значение, указанное в фильтре, должно быть строковым значением "TRUE" или "FALSE". В следующих примерах показано, как задать логическую строку сравнения.

В следующем примере выполняется поиск объектов, для которых параметр **шовинадванцедвиевонли** имеет значение **true**:


```C++
(showInAdvancedViewOnly=TRUE)
```



В следующем примере выполняется поиск объектов, для которых параметр **шовинадванцедвиевонли** имеет значение **false**:


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Целое число и перечисление
</dt> <dd>

Значение, указанное в фильтре, должно быть десятичным целым числом. Шестнадцатеричные значения должны быть преобразованы в десятичные. Строка сравнения значений имеет следующий вид:


```C++
<attribute name>:<value>
```



" <attribute name> " является атрибутом **lDAPDisplayName** атрибута и "<value>"— значение, используемое для сравнения.

В следующем примере кода показан фильтр, который будет искать объекты, имеющие значение **groupType** , равное флагу **\_ \_ \_ универсальной \_ группы AD** (8), и флагу **\_ безопасности группы баннеров \_ \_ \_ Enabled** (0x80000000). Два флага объединены равными 0x80000008, которые преобразовываются в Decimal, — 2147483656.


```C++
(groupType=2147483656)
```



Операторы правил сопоставления LDAP также можно использовать для выполнения побитовых сравнений. Дополнительные сведения о правилах сопоставления см. в разделе [синтаксис фильтра поиска](/windows/desktop/ADSI/search-filter-syntax). В следующем примере кода показан фильтр, который будет выполнять поиск объектов с **groupType** с установленным битом **группы ADS с \_ \_ \_ \_ включенной безопасностью** (0x80000000 = 2147483648).


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>октетстринг
</dt> <dd>

Значение, указанное в фильтре, — это данные, которые необходимо найти. Данные должны быть представлены в виде строки в виде двух байт в кодировке, где каждому байту предшествует обратная косая черта ( \\ ). Например, значение 0x05 будет отображаться в строке как « \\ 05».

Функцию [**адсенкодебинаридата**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) можно использовать для создания закодированного строкового представления двоичных данных. Функция **адсенкодебинаридата** не кодирует байтовые значения, представляющие буквенно-цифровые символы. Вместо этого он помещает символ в строку без его кодирования. В результате получается строка, содержащая сочетание закодированных и незакодированных символов. Например, если двоичные данные имеют значение 0x05 \| 0x1a \| 0x1B \| 0x43 \| 0x32, то закодированная строка будет содержать « \\ 05 \\ 1A \\ 1BC2». Это не влияет на фильтр, и фильтры поиска будут правильно работать с этими типами строк.

Подстановочные знаки принимаются.

В следующем примере кода показан фильтр, содержащий закодированную строку для **schemaIDGUID** со значением GUID "{BF967ABA-0DE6-11D0-A285-00AA003049E2}":


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span id="Sid"></span><span id="sid"></span><span id="SID"></span>Трансляцию
</dt> <dd>

Значение, указанное в фильтре, представляет собой закодированное строковое представление идентификатора SID. Дополнительные сведения о кодированных строках байтов см. в предыдущем разделе этой статьи, в котором обсуждается синтаксис Октетстринг.

В следующем примере кода показан фильтр, содержащий закодированную строку для **objectSid** со СТРОКОВЫМ значением sid "S-1-5-21-1935655697-308236825-1417001333":


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span id="DN"></span><span id="dn"></span>DN
</dt> <dd>

Необходимо указать полное различающееся имя для сопоставления.

Подстановочные знаки не принимаются.

Имейте в виду, что атрибут **objectCategory** также позволяет указать атрибут **lDAPDisplayName** класса, установленного для атрибута.

В следующем примере показан фильтр, указывающий **элемент** , который содержит "CN = TESTUSER, DC = Fabrikam, DC = com":


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span id="INTEGER8"></span><span id="integer8"></span>INTEGER8
</dt> <dd>

Значение, указанное в фильтре, должно быть десятичным целым числом. Преобразует шестнадцатеричные значения в десятичные.

В следующем примере кода показан фильтр, указывающий **CreationTime** , для которого задано значение [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) "1999-12-31 23:59:59 (UTC/GMT)":


```C++
(creationTime=125911583990000000)
```



Следующие функции создают фильтр точного соответствия (=) для большого целочисленного атрибута и проверяют атрибут в схеме и его синтаксис:


```C++
//***************************************************************************
//
//  CheckAttribute()
//
//***************************************************************************

HRESULT CheckAttribute(LPOLESTR szAttribute, LPOLESTR szSyntax)
{
    HRESULT hr = E_FAIL;
    BSTR bstr;
    IADsProperty *pObject = NULL;
    LPWSTR szPrefix = L"LDAP://schema/";
    LPWSTR szPath;
     
    if((!szAttribute) || (!szSyntax))
    {
        return E_POINTER;
    }

    // Allocate a buffer large enough to hold the ADsPath of the attribute.
    szPath = new WCHAR[lstrlenW(szPrefix) + lstrlenW(szAttribute) + 1];
    if(NULL == szPath)
    {
        return E_OUTOFMEMORY;
    }
     
    // Create the ADsPath of the attribute.
    wcscpy_s(szPath, szPrefix);
    wcscat_s(szPath, szAttribute);

    hr = ADsOpenObject( szPath,
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                        IID_IADsProperty,
                        (void**)&pObject);
    if(SUCCEEDED(hr)) 
    {
        hr = pObject->get_Syntax(&bstr);
        if (SUCCEEDED(hr)) 
        {
            if (0==lstrcmpiW(bstr, szSyntax)) 
            {
                hr = S_OK;
            }
            else
            {
                hr = S_FALSE;
            }
        }

        SysFreeString(bstr);
    }
    
    if(pObject)
    {
        pObject->Release();
    }

    delete szPath;
    
    return hr;
}

//***************************************************************************
//
//  CreateExactMatchFilterLargeInteger()
//
//***************************************************************************

HRESULT CreateExactMatchFilterLargeInteger( LPOLESTR szAttribute, 
                                            INT64 liValue, 
                                            LPOLESTR *pszFilter)
{
    HRESULT hr = E_FAIL;
     
    if ((!szAttribute) || (!pszFilter))
    {
        return E_POINTER;
    }
     
    // Verify that the attribute exists and has 
    // Integer8 (Large Integer) syntax.
     
    hr = CheckAttribute(szAttribute, L"Integer8");
    if (S_OK == hr) 
    {
        LPWSTR szFormat = L"%s=%I64d";
        LPWSTR szTempFilter = new WCHAR[lstrlenW(szFormat) + lstrlenW(szAttribute) + 20 + 1];

        if(NULL == szTempFilter)
        {
            return E_OUTOFMEMORY;
        }
        
        swprintf_s(szTempFilter, L"%s=%I64d", szAttribute, liValue);
     
        // Allocate buffer for the filter string.
        // Caller must free the buffer using CoTaskMemFree.
        *pszFilter = (OLECHAR *)CoTaskMemAlloc(sizeof(OLECHAR) * (lstrlenW(szTempFilter) + 1));
        if (*pszFilter) 
        {
            wcscpy_s(*pszFilter, szTempFilter);
            hr = S_OK;
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }

        delete szTempFilter;
    }

    return hr;
}
```



</dd> <dt>

<span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>принтаблестринг
</dt> <dd>

Атрибуты с этими синтаксисами должны соответствовать конкретным наборам символов. Дополнительные сведения см. [в разделе синтаксис атрибутов в домен Active Directory Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

В настоящее время службы домен Active Directory не применяют эти наборы символов.

Значение, указанное в фильтре, является строкой. При сравнении учитывается регистр.

</dd> <dt>

<span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>женерализедтиме
</dt> <dd>

Значение, указанное в фильтре, является строкой, представляющей дату в следующей форме:


```C++
YYYYMMDDHHMMSS.0Z
```



"0Z" указывает на отсутствие разностной копии времени. Имейте в виду, что Active Directory сервер хранит дату и время как время по Гринвичу (GMT). Если временная разница не указана, по умолчанию используется значение GMT.

Если местный часовой пояс — не GMT, используйте разностное значение, чтобы указать местный часовой пояс и применить разностную копию к GMT. Разностное резервное копирование основано на: GMT = Local + DIFFERENTIAL.

Чтобы указать разностную копию, используйте:


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



В следующем примере показан фильтр, указывающий время **вхенкреатед** , установленное в 3/23/99 8:52:58 PM GMT:


```C++
(whenCreated=19990323205258.0Z)
```



В следующем примере показан фильтр, указывающий время **вхенкреатед** , установленное в 3/23/99 8:52:58 PM (значение по Гринвичу + 12 часов):


```C++
(whenCreated=19990323205258.0+1200)
```



В следующем примере кода показано, как вычислить разностное значение часового пояса. Функция возвращает разностную копию текущего местного часового пояса и GMT. Возвращаемое значение является строкой в следующем формате:


```C++
[+/-]HHMM
```



Например, тихоокеанское стандартное время —-0800.


```C++
//***************************************************************************
//
//  GetLocalTimeZoneDifferential()
//
//***************************************************************************

HRESULT GetLocalTimeZoneDifferential(LPOLESTR *pszDifferential)
{
    if(NULL == pszDifferential)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr = E_FAIL;
    DWORD dwReturn;
    TIME_ZONE_INFORMATION timezoneinfo;
    LONG lTimeDifferential;
    LONG lHours;
    LONG lMinutes;
    
    dwReturn  = GetTimeZoneInformation(&timezoneinfo);

    switch (dwReturn)
    {
    case TIME_ZONE_ID_STANDARD:
        lTimeDifferential = timezoneinfo.Bias + timezoneinfo.StandardBias;
        
        // Bias is in minutes. Calculate the hours for HHMM format.
        lHours = -(lTimeDifferential/60);
        
        // Bias is in minutes. Calculate the minutes for HHMM format.
        lMinutes = lTimeDifferential%60L;

        hr = S_OK;
        break;

    case TIME_ZONE_ID_DAYLIGHT:
        lTimeDifferential = timezoneinfo.Bias + timezoneinfo.DaylightBias;
        
        // Bias is in minutes. Calculate the hours for HHMM format.
        // Apply the additive inverse.
        // Bias is based on GMT=Local+Bias.
        // A differential, based on GMT=Local-Bias, is required.
        lHours = -(lTimeDifferential/60);
        
        // Bias is in minutes. Calculate the minutes for HHMM format.
        lMinutes = lTimeDifferential%60L;
        
        hr = S_OK;
        break;

    case TIME_ZONE_ID_INVALID:
    default:
        hr = E_FAIL;
        break;
    }
     
    if (SUCCEEDED(hr))
    {
        // The caller must free the memory using CoTaskMemFree.
        *pszDifferential = (OLECHAR *)CoTaskMemAlloc(sizeof(OLECHAR) * (3 + 2 + 1));
        if (*pszDifferential)
        {
            swprintf_s(*pszDifferential, L"%+03d%02d", lHours, lMinutes);
            
            hr = S_OK;
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
     
    return hr;
}
```



</dd> <dt>

<span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>утктиме
</dt> <dd>

Значение, указанное в фильтре, является строкой, представляющей дату в следующей форме:


```C++
YYMMDDHHMMSSZ
```



Z означает отсутствие разностного времени. Имейте в виду, что Active Directory сервер хранит дату и время как время по ГРИНВИЧу. Если временная разница не указана, по умолчанию используется значение GMT.

Значение секунд (SS) является необязательным.

Если GMT не является местным часовым поясом, примените локальное разностное значение, чтобы указать местный часовой пояс. Разностная копия: GMT = Local + DIFFERENTIAL.

Чтобы указать разностную копию, используйте следующую форму:


```C++
YYMMDDHHMMSS[+/-]HHMM
```



В следующем примере показан фильтр, указывающий время **митимеаттриб** , установленное в 3/23/99 8:52:58 PM GMT:


```C++
(myTimeAttrib=990323205258Z)
```



В следующем примере показан фильтр, указывающий время **митимеаттриб** , установленное в 3/23/99 8:52:58 PM без заданных секунд:


```C++
(myTimeAttrib=9903232052Z)
```



В следующем примере показан фильтр, указывающий время **митимеаттриб** , установленное в 3/23/99 8:52:58 PM (значение по Гринвичу 12 часов). Это эквивалентно 3/23/99 8:52:58 AM GMT.


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>директористринг
</dt> <dd>

Значение, указанное в фильтре, является строкой. Директористринг может содержать символы Юникода. При сравнении регистр не учитывается.

</dd> <dt>

<span id="OID"></span><span id="oid"></span>КОДА
</dt> <dd>

Должен быть указан весь OID для сопоставления.

Подстановочные знаки не принимаются.

Атрибут **objectCategory** позволяет указать атрибут **lDAPDisplayName** класса, установленного для атрибута.

В следующем примере показан фильтр, указывающий **governsID** для класса Volume:


```C++
(governsID=1.2.840.113556.1.5.36)
```



Два эквивалентных фильтра, указывающие атрибут **системмустконтаин** , содержащий **uncname**, который имеет идентификатор объекта 1.2.840.113556.1.4.137:


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Другие синтаксисы
</dt> <dd>

Следующие синтаксисы вычисляются в фильтре аналогично строке октета:

-   обжектсекуритидескриптор
-   акцесспоинтдн
-   пресентатионаддрессес
-   репликалинк
-   днвисстринг
-   днвисоктетстринг
-   орнаме

</dd> </dl>

 

 