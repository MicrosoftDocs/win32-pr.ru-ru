---
title: Как указать значения для сравнения
description: Каждый тип атрибута имеет синтаксис, который определяет тип значений сравнения, которые можно указать в фильтре поиска для этого атрибута.
ms.assetid: 72bd58e4-e1c3-40a5-9917-4910f40c52c5
ms.tgt_platform: multiple
keywords:
- Как задать значения для сравнения в AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edba238961cdc18b088b6b5bd5b06ff4be383add
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386754"
---
# <a name="how-to-specify-comparison-values"></a><span data-ttu-id="c0265-104">Как указать значения для сравнения</span><span class="sxs-lookup"><span data-stu-id="c0265-104">How to Specify Comparison Values</span></span>

<span data-ttu-id="c0265-105">Каждый тип атрибута имеет синтаксис, который определяет тип значений сравнения, которые можно указать в фильтре поиска для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="c0265-105">Each attribute type has a syntax that determines the type of comparison values that you can specify in a search filter for that attribute.</span></span>

<span data-ttu-id="c0265-106">В следующих разделах описаны требования для каждого синтаксиса атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c0265-106">The following sections describe requirements for each attribute syntax.</span></span> <span data-ttu-id="c0265-107">Дополнительные сведения о синтаксисе атрибутов см. [в разделе синтаксис атрибутов в домен Active Directory Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="c0265-107">For more information about attribute syntaxes, see [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span></span>

<dl> <dt>

<span data-ttu-id="c0265-108"><span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Логическая</span><span class="sxs-lookup"><span data-stu-id="c0265-108"><span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Boolean</span></span>
</dt> <dd>

<span data-ttu-id="c0265-109">Значение, указанное в фильтре, должно быть строковым значением "TRUE" или "FALSE".</span><span class="sxs-lookup"><span data-stu-id="c0265-109">The value specified in a filter must be a string value that is either "TRUE" or "FALSE".</span></span> <span data-ttu-id="c0265-110">В следующих примерах показано, как задать логическую строку сравнения.</span><span class="sxs-lookup"><span data-stu-id="c0265-110">The following examples show how to specify a Boolean comparison string.</span></span>

<span data-ttu-id="c0265-111">В следующем примере выполняется поиск объектов, для которых параметр **шовинадванцедвиевонли** имеет значение **true**:</span><span class="sxs-lookup"><span data-stu-id="c0265-111">The following example will search for objects that have a **showInAdvancedViewOnly** set to **TRUE**:</span></span>


```C++
(showInAdvancedViewOnly=TRUE)
```



<span data-ttu-id="c0265-112">В следующем примере выполняется поиск объектов, для которых параметр **шовинадванцедвиевонли** имеет значение **false**:</span><span class="sxs-lookup"><span data-stu-id="c0265-112">The following example will search for objects that have a **showInAdvancedViewOnly** set to **FALSE**:</span></span>


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span data-ttu-id="c0265-113"><span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Целое число и перечисление</span><span class="sxs-lookup"><span data-stu-id="c0265-113"><span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Integer and Enumeration</span></span>
</dt> <dd>

<span data-ttu-id="c0265-114">Значение, указанное в фильтре, должно быть десятичным целым числом.</span><span class="sxs-lookup"><span data-stu-id="c0265-114">The value specified in a filter must be a decimal Integer.</span></span> <span data-ttu-id="c0265-115">Шестнадцатеричные значения должны быть преобразованы в десятичные.</span><span class="sxs-lookup"><span data-stu-id="c0265-115">Hexadecimal values must be converted to decimal.</span></span> <span data-ttu-id="c0265-116">Строка сравнения значений имеет следующий вид:</span><span class="sxs-lookup"><span data-stu-id="c0265-116">A value comparison string takes the following form:</span></span>


```C++
<attribute name>:<value>
```



<span data-ttu-id="c0265-117">" <attribute name> " является атрибутом **lDAPDisplayName** атрибута и "</span><span class="sxs-lookup"><span data-stu-id="c0265-117">"<attribute name>" is the **lDAPDisplayName** of the attribute and "</span></span><value><span data-ttu-id="c0265-118">"— значение, используемое для сравнения.</span><span class="sxs-lookup"><span data-stu-id="c0265-118">" is the value to use for comparison.</span></span>

<span data-ttu-id="c0265-119">В следующем примере кода показан фильтр, который будет искать объекты, имеющие значение **groupType** , равное флагу **\_ \_ \_ универсальной \_ группы AD** (8), и флагу **\_ безопасности группы баннеров \_ \_ \_ Enabled** (0x80000000).</span><span class="sxs-lookup"><span data-stu-id="c0265-119">The following code example shows a filter that will search for objects that have a **groupType** value that is equal to the **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** (8) flag and the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000) flag.</span></span> <span data-ttu-id="c0265-120">Два флага объединены равными 0x80000008, которые преобразовываются в Decimal, — 2147483656.</span><span class="sxs-lookup"><span data-stu-id="c0265-120">The two flags combined equal 0x80000008, which converted to decimal is 2147483656.</span></span>


```C++
(groupType=2147483656)
```



<span data-ttu-id="c0265-121">Операторы правил сопоставления LDAP также можно использовать для выполнения побитовых сравнений.</span><span class="sxs-lookup"><span data-stu-id="c0265-121">The LDAP matching rule operators can also be used to perform bitwise comparisons.</span></span> <span data-ttu-id="c0265-122">Дополнительные сведения о правилах сопоставления см. в разделе [синтаксис фильтра поиска](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="c0265-122">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span> <span data-ttu-id="c0265-123">В следующем примере кода показан фильтр, который будет выполнять поиск объектов с **groupType** с установленным битом **группы ADS с \_ \_ \_ \_ включенной безопасностью** (0x80000000 = 2147483648).</span><span class="sxs-lookup"><span data-stu-id="c0265-123">The following code example shows a filter that will search for objects that have a **groupType** with the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000 = 2147483648) bit set.</span></span>


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span data-ttu-id="c0265-124"><span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>октетстринг</span><span class="sxs-lookup"><span data-stu-id="c0265-124"><span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString</span></span>
</dt> <dd>

<span data-ttu-id="c0265-125">Значение, указанное в фильтре, — это данные, которые необходимо найти.</span><span class="sxs-lookup"><span data-stu-id="c0265-125">The value specified in a filter is the data to be found.</span></span> <span data-ttu-id="c0265-126">Данные должны быть представлены в виде строки в виде двух байт в кодировке, где каждому байту предшествует обратная косая черта ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="c0265-126">The data must be represented as a two character encoded byte string where each byte is preceded by a backslash (\\).</span></span> <span data-ttu-id="c0265-127">Например, значение 0x05 будет отображаться в строке как « \\ 05».</span><span class="sxs-lookup"><span data-stu-id="c0265-127">For example, the value 0x05 will appear in the string as "\\05".</span></span>

<span data-ttu-id="c0265-128">Функцию [**адсенкодебинаридата**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) можно использовать для создания закодированного строкового представления двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="c0265-128">The [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) function can be used to create an encoded string representation of binary data.</span></span> <span data-ttu-id="c0265-129">Функция **адсенкодебинаридата** не кодирует байтовые значения, представляющие буквенно-цифровые символы.</span><span class="sxs-lookup"><span data-stu-id="c0265-129">The **ADsEncodeBinaryData** function does not encode byte values that represent alpha-numeric characters.</span></span> <span data-ttu-id="c0265-130">Вместо этого он помещает символ в строку без его кодирования.</span><span class="sxs-lookup"><span data-stu-id="c0265-130">It will, instead, place the character into the string without encoding it.</span></span> <span data-ttu-id="c0265-131">В результате получается строка, содержащая сочетание закодированных и незакодированных символов.</span><span class="sxs-lookup"><span data-stu-id="c0265-131">This results in the string containing a mixture of encoded and unencoded characters.</span></span> <span data-ttu-id="c0265-132">Например, если двоичные данные имеют значение 0x05 \| 0x1a \| 0x1B \| 0x43 \| 0x32, то закодированная строка будет содержать « \\ 05 \\ 1A \\ 1BC2».</span><span class="sxs-lookup"><span data-stu-id="c0265-132">For example, if the binary data is 0x05\|0x1A\|0x1B\|0x43\|0x32, the encoded string will contain "\\05\\1A\\1BC2".</span></span> <span data-ttu-id="c0265-133">Это не влияет на фильтр, и фильтры поиска будут правильно работать с этими типами строк.</span><span class="sxs-lookup"><span data-stu-id="c0265-133">This has no effect on the filter and the search filters will work correctly with these types of strings.</span></span>

<span data-ttu-id="c0265-134">Подстановочные знаки принимаются.</span><span class="sxs-lookup"><span data-stu-id="c0265-134">Wildcards are accepted.</span></span>

<span data-ttu-id="c0265-135">В следующем примере кода показан фильтр, содержащий закодированную строку для **schemaIDGUID** со значением GUID "{BF967ABA-0DE6-11D0-A285-00AA003049E2}":</span><span class="sxs-lookup"><span data-stu-id="c0265-135">The following code example shows a filter that contains encoded string for **schemaIDGUID** with GUID value of "{BF967ABA-0DE6-11D0-A285-00AA003049E2}":</span></span>


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span data-ttu-id="c0265-136"><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Трансляцию</span><span class="sxs-lookup"><span data-stu-id="c0265-136"><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</span></span>
</dt> <dd>

<span data-ttu-id="c0265-137">Значение, указанное в фильтре, представляет собой закодированное строковое представление идентификатора SID.</span><span class="sxs-lookup"><span data-stu-id="c0265-137">The value specified in a filter is the encoded byte string representation of the SID.</span></span> <span data-ttu-id="c0265-138">Дополнительные сведения о кодированных строках байтов см. в предыдущем разделе этой статьи, в котором обсуждается синтаксис Октетстринг.</span><span class="sxs-lookup"><span data-stu-id="c0265-138">For more information about encoded byte strings, see the previous section in this topic which discusses OctetString syntax.</span></span>

<span data-ttu-id="c0265-139">В следующем примере кода показан фильтр, содержащий закодированную строку для **objectSid** со СТРОКОВЫМ значением sid "S-1-5-21-1935655697-308236825-1417001333":</span><span class="sxs-lookup"><span data-stu-id="c0265-139">The following code example shows a filter that contains an encoded string for **objectSid** with SID string value of "S-1-5-21-1935655697-308236825-1417001333":</span></span>


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span data-ttu-id="c0265-140"><span id="DN"></span><span id="dn"></span>DN</span><span class="sxs-lookup"><span data-stu-id="c0265-140"><span id="DN"></span><span id="dn"></span>DN</span></span>
</dt> <dd>

<span data-ttu-id="c0265-141">Необходимо указать полное различающееся имя для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="c0265-141">The entire distinguished name, to be matched, must be supplied.</span></span>

<span data-ttu-id="c0265-142">Подстановочные знаки не принимаются.</span><span class="sxs-lookup"><span data-stu-id="c0265-142">Wildcards are not accepted.</span></span>

<span data-ttu-id="c0265-143">Имейте в виду, что атрибут **objectCategory** также позволяет указать атрибут **lDAPDisplayName** класса, установленного для атрибута.</span><span class="sxs-lookup"><span data-stu-id="c0265-143">Be aware that the **objectCategory** attribute also enables you to specify the **lDAPDisplayName** of the class set on the attribute.</span></span>

<span data-ttu-id="c0265-144">В следующем примере показан фильтр, указывающий **элемент** , который содержит "CN = TESTUSER, DC = Fabrikam, DC = com":</span><span class="sxs-lookup"><span data-stu-id="c0265-144">The following example shows a filter that specifies a **member** that contains "CN=TestUser,DC=Fabrikam,DC=COM":</span></span>


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span data-ttu-id="c0265-145"><span id="INTEGER8"></span><span id="integer8"></span>INTEGER8</span><span class="sxs-lookup"><span data-stu-id="c0265-145"><span id="INTEGER8"></span><span id="integer8"></span>INTEGER8</span></span>
</dt> <dd>

<span data-ttu-id="c0265-146">Значение, указанное в фильтре, должно быть десятичным целым числом.</span><span class="sxs-lookup"><span data-stu-id="c0265-146">The value specified in a filter must be a decimal integer.</span></span> <span data-ttu-id="c0265-147">Преобразует шестнадцатеричные значения в десятичные.</span><span class="sxs-lookup"><span data-stu-id="c0265-147">Convert hexadecimal values to decimal.</span></span>

<span data-ttu-id="c0265-148">В следующем примере кода показан фильтр, указывающий **CreationTime** , для которого задано значение [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) "1999-12-31 23:59:59 (UTC/GMT)":</span><span class="sxs-lookup"><span data-stu-id="c0265-148">The following code example shows a filter that specifies a **creationTime** set to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) of "1999-12-31 23:59:59 (UTC/GMT)":</span></span>


```C++
(creationTime=125911583990000000)
```



<span data-ttu-id="c0265-149">Следующие функции создают фильтр точного соответствия (=) для большого целочисленного атрибута и проверяют атрибут в схеме и его синтаксис:</span><span class="sxs-lookup"><span data-stu-id="c0265-149">The following functions create an exact match (=) filter for a large integer attribute and verify the attribute in the schema and its syntax:</span></span>


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

<span data-ttu-id="c0265-150"><span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>принтаблестринг</span><span class="sxs-lookup"><span data-stu-id="c0265-150"><span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString</span></span>
</dt> <dd>

<span data-ttu-id="c0265-151">Атрибуты с этими синтаксисами должны соответствовать конкретным наборам символов.</span><span class="sxs-lookup"><span data-stu-id="c0265-151">Attributes with these syntaxes should adhere to specific character sets.</span></span> <span data-ttu-id="c0265-152">Дополнительные сведения см. [в разделе синтаксис атрибутов в домен Active Directory Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="c0265-152">For more information, see [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="c0265-153">В настоящее время службы домен Active Directory не применяют эти наборы символов.</span><span class="sxs-lookup"><span data-stu-id="c0265-153">Currently, Active Directory Domain Services do not enforce those character sets.</span></span>

<span data-ttu-id="c0265-154">Значение, указанное в фильтре, является строкой.</span><span class="sxs-lookup"><span data-stu-id="c0265-154">The value specified in a filter is a string.</span></span> <span data-ttu-id="c0265-155">При сравнении учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="c0265-155">The comparison is case-sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="c0265-156"><span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>женерализедтиме</span><span class="sxs-lookup"><span data-stu-id="c0265-156"><span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime</span></span>
</dt> <dd>

<span data-ttu-id="c0265-157">Значение, указанное в фильтре, является строкой, представляющей дату в следующей форме:</span><span class="sxs-lookup"><span data-stu-id="c0265-157">The value specified in a filter is a string that represents the date in the following form:</span></span>


```C++
YYYYMMDDHHMMSS.0Z
```



<span data-ttu-id="c0265-158">"0Z" указывает на отсутствие разностной копии времени.</span><span class="sxs-lookup"><span data-stu-id="c0265-158">"0Z" indicates no time differential.</span></span> <span data-ttu-id="c0265-159">Имейте в виду, что Active Directory сервер хранит дату и время как время по Гринвичу (GMT).</span><span class="sxs-lookup"><span data-stu-id="c0265-159">Be aware that the Active Directory server stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="c0265-160">Если временная разница не указана, по умолчанию используется значение GMT.</span><span class="sxs-lookup"><span data-stu-id="c0265-160">If a time differential is not specified, the default is GMT.</span></span>

<span data-ttu-id="c0265-161">Если местный часовой пояс — не GMT, используйте разностное значение, чтобы указать местный часовой пояс и применить разностную копию к GMT.</span><span class="sxs-lookup"><span data-stu-id="c0265-161">If the local time zone is not GMT, use a differential value to specify your local time zone and apply the differential to GMT.</span></span> <span data-ttu-id="c0265-162">Разностное резервное копирование основано на: GMT = Local + DIFFERENTIAL.</span><span class="sxs-lookup"><span data-stu-id="c0265-162">The differential is based on: GMT=Local+differential.</span></span>

<span data-ttu-id="c0265-163">Чтобы указать разностную копию, используйте:</span><span class="sxs-lookup"><span data-stu-id="c0265-163">To specify a differential, use:</span></span>


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



<span data-ttu-id="c0265-164">В следующем примере показан фильтр, указывающий время **вхенкреатед** , установленное в 3/23/99 8:52:58 PM GMT:</span><span class="sxs-lookup"><span data-stu-id="c0265-164">The following example shows a filter that specifies a **whenCreated** time set to 3/23/99 8:52:58 PM GMT:</span></span>


```C++
(whenCreated=19990323205258.0Z)
```



<span data-ttu-id="c0265-165">В следующем примере показан фильтр, указывающий время **вхенкреатед** , установленное в 3/23/99 8:52:58 PM (значение по Гринвичу + 12 часов):</span><span class="sxs-lookup"><span data-stu-id="c0265-165">The following example shows a filter that specifies a **whenCreated** time set to 3/23/99 8:52:58 PM New Zealand Standard Time (differential is +12 hours):</span></span>


```C++
(whenCreated=19990323205258.0+1200)
```



<span data-ttu-id="c0265-166">В следующем примере кода показано, как вычислить разностное значение часового пояса.</span><span class="sxs-lookup"><span data-stu-id="c0265-166">The following code example shows how to calculate time zone differential.</span></span> <span data-ttu-id="c0265-167">Функция возвращает разностную копию текущего местного часового пояса и GMT.</span><span class="sxs-lookup"><span data-stu-id="c0265-167">The function returns the differential between the current local time zone and GMT.</span></span> <span data-ttu-id="c0265-168">Возвращаемое значение является строкой в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="c0265-168">The value returned is a string in the following format:</span></span>


```C++
[+/-]HHMM
```



<span data-ttu-id="c0265-169">Например, тихоокеанское стандартное время —-0800.</span><span class="sxs-lookup"><span data-stu-id="c0265-169">For example, Pacific Standard Time is -0800.</span></span>


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

<span data-ttu-id="c0265-170"><span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>утктиме</span><span class="sxs-lookup"><span data-stu-id="c0265-170"><span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime</span></span>
</dt> <dd>

<span data-ttu-id="c0265-171">Значение, указанное в фильтре, является строкой, представляющей дату в следующей форме:</span><span class="sxs-lookup"><span data-stu-id="c0265-171">The value specified in a filter is a string that represents the date in the following form:</span></span>


```C++
YYMMDDHHMMSSZ
```



<span data-ttu-id="c0265-172">Z означает отсутствие разностного времени.</span><span class="sxs-lookup"><span data-stu-id="c0265-172">Z indicates no time differential.</span></span> <span data-ttu-id="c0265-173">Имейте в виду, что Active Directory сервер хранит дату и время как время по ГРИНВИЧу.</span><span class="sxs-lookup"><span data-stu-id="c0265-173">Be aware that the Active Directory server stores date and time as GMT time.</span></span> <span data-ttu-id="c0265-174">Если временная разница не указана, по умолчанию используется значение GMT.</span><span class="sxs-lookup"><span data-stu-id="c0265-174">If a time differential is not specified, GMT is the default.</span></span>

<span data-ttu-id="c0265-175">Значение секунд (SS) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c0265-175">The seconds value ("SS") is optional.</span></span>

<span data-ttu-id="c0265-176">Если GMT не является местным часовым поясом, примените локальное разностное значение, чтобы указать местный часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="c0265-176">If GMT is not the local time zone, apply a local differential value to specify your local time zone.</span></span> <span data-ttu-id="c0265-177">Разностная копия: GMT = Local + DIFFERENTIAL.</span><span class="sxs-lookup"><span data-stu-id="c0265-177">The differential is: GMT=Local+differential.</span></span>

<span data-ttu-id="c0265-178">Чтобы указать разностную копию, используйте следующую форму:</span><span class="sxs-lookup"><span data-stu-id="c0265-178">To specify a differential, use the following form:</span></span>


```C++
YYMMDDHHMMSS[+/-]HHMM
```



<span data-ttu-id="c0265-179">В следующем примере показан фильтр, указывающий время **митимеаттриб** , установленное в 3/23/99 8:52:58 PM GMT:</span><span class="sxs-lookup"><span data-stu-id="c0265-179">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM GMT:</span></span>


```C++
(myTimeAttrib=990323205258Z)
```



<span data-ttu-id="c0265-180">В следующем примере показан фильтр, указывающий время **митимеаттриб** , установленное в 3/23/99 8:52:58 PM без заданных секунд:</span><span class="sxs-lookup"><span data-stu-id="c0265-180">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM without seconds specified:</span></span>


```C++
(myTimeAttrib=9903232052Z)
```



<span data-ttu-id="c0265-181">В следующем примере показан фильтр, указывающий время **митимеаттриб** , установленное в 3/23/99 8:52:58 PM (значение по Гринвичу 12 часов).</span><span class="sxs-lookup"><span data-stu-id="c0265-181">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM New Zealand Standard Time (differential is 12 hours).</span></span> <span data-ttu-id="c0265-182">Это эквивалентно 3/23/99 8:52:58 AM GMT.</span><span class="sxs-lookup"><span data-stu-id="c0265-182">This is equivalent to 3/23/99 8:52:58 AM GMT.</span></span>


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span data-ttu-id="c0265-183"><span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>директористринг</span><span class="sxs-lookup"><span data-stu-id="c0265-183"><span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString</span></span>
</dt> <dd>

<span data-ttu-id="c0265-184">Значение, указанное в фильтре, является строкой.</span><span class="sxs-lookup"><span data-stu-id="c0265-184">The value specified in a filter is a string.</span></span> <span data-ttu-id="c0265-185">Директористринг может содержать символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="c0265-185">DirectoryString can contain Unicode characters.</span></span> <span data-ttu-id="c0265-186">При сравнении регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="c0265-186">The comparison is case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="c0265-187"><span id="OID"></span><span id="oid"></span>КОДА</span><span class="sxs-lookup"><span data-stu-id="c0265-187"><span id="OID"></span><span id="oid"></span>OID</span></span>
</dt> <dd>

<span data-ttu-id="c0265-188">Должен быть указан весь OID для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="c0265-188">The entire OID to be matched must be supplied.</span></span>

<span data-ttu-id="c0265-189">Подстановочные знаки не принимаются.</span><span class="sxs-lookup"><span data-stu-id="c0265-189">Wildcards are not accepted.</span></span>

<span data-ttu-id="c0265-190">Атрибут **objectCategory** позволяет указать атрибут **lDAPDisplayName** класса, установленного для атрибута.</span><span class="sxs-lookup"><span data-stu-id="c0265-190">The **objectCategory** attribute enables you to specify the **lDAPDisplayName** of the class set for the attribute.</span></span>

<span data-ttu-id="c0265-191">В следующем примере показан фильтр, указывающий **governsID** для класса Volume:</span><span class="sxs-lookup"><span data-stu-id="c0265-191">The following example shows a filter that specifies **governsID** for volume class:</span></span>


```C++
(governsID=1.2.840.113556.1.5.36)
```



<span data-ttu-id="c0265-192">Два эквивалентных фильтра, указывающие атрибут **системмустконтаин** , содержащий **uncname**, который имеет идентификатор объекта 1.2.840.113556.1.4.137:</span><span class="sxs-lookup"><span data-stu-id="c0265-192">Two equivalent filters that specifies **systemMustContain** attribute containing **uNCName**, which has an OID of 1.2.840.113556.1.4.137:</span></span>


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span data-ttu-id="c0265-193"><span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Другие синтаксисы</span><span class="sxs-lookup"><span data-stu-id="c0265-193"><span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Other Syntaxes</span></span>
</dt> <dd>

<span data-ttu-id="c0265-194">Следующие синтаксисы вычисляются в фильтре аналогично строке октета:</span><span class="sxs-lookup"><span data-stu-id="c0265-194">The following syntaxes are evaluated in a filter similar to an octet string:</span></span>

-   <span data-ttu-id="c0265-195">обжектсекуритидескриптор</span><span class="sxs-lookup"><span data-stu-id="c0265-195">ObjectSecurityDescriptor</span></span>
-   <span data-ttu-id="c0265-196">акцесспоинтдн</span><span class="sxs-lookup"><span data-stu-id="c0265-196">AccessPointDN</span></span>
-   <span data-ttu-id="c0265-197">пресентатионаддрессес</span><span class="sxs-lookup"><span data-stu-id="c0265-197">PresentationAddresses</span></span>
-   <span data-ttu-id="c0265-198">репликалинк</span><span class="sxs-lookup"><span data-stu-id="c0265-198">ReplicaLink</span></span>
-   <span data-ttu-id="c0265-199">днвисстринг</span><span class="sxs-lookup"><span data-stu-id="c0265-199">DNWithString</span></span>
-   <span data-ttu-id="c0265-200">днвисоктетстринг</span><span class="sxs-lookup"><span data-stu-id="c0265-200">DNWithOctetString</span></span>
-   <span data-ttu-id="c0265-201">орнаме</span><span class="sxs-lookup"><span data-stu-id="c0265-201">ORName</span></span>

</dd> </dl>

 

 