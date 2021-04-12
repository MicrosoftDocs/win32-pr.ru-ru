---
title: Методы свойств Иадспропертивалуе (iAds. h)
description: Методы свойств интерфейса Иадспропертивалуе обеспечивают доступ к свойствам, описанным в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 1039d4a9-bef8-457d-9a32-3743c14adef1
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадспропертивалуе ADSI
topic_type:
- apiref
api_name:
- IADsPropertyValue Property Methods
- IADsPropertyValue.ADsType
- IADsPropertyValue.get_ADsType
- IADsPropertyValue.put_ADsType
- IADsPropertyValue.DNString
- IADsPropertyValue.get_DNString
- IADsPropertyValue.put_DNString
- IADsPropertyValue.CaseExactString
- IADsPropertyValue.get_CaseExactString
- IADsPropertyValue.put_CaseExactString
- IADsPropertyValue.CaseIgnoreString
- IADsPropertyValue.get_CaseIgnoreString
- IADsPropertyValue.put_CaseIgnoreString
- IADsPropertyValue.PrintableString
- IADsPropertyValue.get_PrintableString
- IADsPropertyValue.put_PrintableString
- IADsPropertyValue.NumericString
- IADsPropertyValue.get_NumericString
- IADsPropertyValue.put_NumericString
- IADsPropertyValue.Boolean
- IADsPropertyValue.get_Boolean
- IADsPropertyValue.put_Boolean
- IADsPropertyValue.Integer
- IADsPropertyValue.get_Integer
- IADsPropertyValue.put_Integer
- IADsPropertyValue.OctetString
- IADsPropertyValue.get_OctetString
- IADsPropertyValue.put_OctetString
- IADsPropertyValue.SecurityDescriptor
- IADsPropertyValue.get_SecurityDescriptor
- IADsPropertyValue.put_SecurityDescriptor
- IADsPropertyValue.LargeInteger
- IADsPropertyValue.get_LargeInteger
- IADsPropertyValue.put_LargeInteger
- IADsPropertyValue.UTCTime
- IADsPropertyValue.get_UTCTime
- IADsPropertyValue.put_UTCTime
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196e8097e5beaa5350738971be29de89b43c17a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490245"
---
# <a name="iadspropertyvalue-property-methods"></a>Методы свойств Иадспропертивалуе

Методы свойств интерфейса [**иадспропертивалуе**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) обеспечивают доступ к свойствам, описанным в следующей таблице. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**адстипе**
</dt> <dd> <dl>

Тип данных значения свойства, взятого из перечисления [**адстипинум**](/windows/win32/api/iads/ne-iads-adstypeenum) для свойства Value.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* ADsType
);
HRESULT put_ADsType(
  [in] LONG ADsType
);
```


</dt> </dl> </dd> <dt>

**Boolean**
</dt> <dd> <dl>

.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Boolean(
  [out] LONG* lnBoolean
);
HRESULT put_Boolean(
  [in] LONG lnBoolean
);
```


</dt> </dl> </dd> <dt>

**касиксактстринг**
</dt> <dd> <dl>

Строка для интерпретации. С учетом регистра.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseExactString(
  [out] BSTR* bstrCaseExactString
);
HRESULT put_CaseExactString(
  [in] BSTR bstrCaseExactString
);
```


</dt> </dl> </dd> <dt>

**касеигнорестринг**
</dt> <dd> <dl>

Строка для интерпретации. Без учета регистра.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreString(
  [out] BSTR* bstrCaseIgnoreString
);
HRESULT put_CaseIgnoreString(
  [in] BSTR bstrCaseIgnoreString
);
```


</dt> </dl> </dd> <dt>

**днстринг**
</dt> <dd> <dl>

Строка, определяющая различающееся имя (путь) объекта значения службы каталога.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* bstrDNString
);
HRESULT put_DNString(
  [in] BSTR bstrDNString
);
```


</dt> </dl> </dd> <dt>

**Integer**
</dt> <dd> <dl>

Целое значение.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Integer(
  [out] LONG* lnInteger
);
HRESULT put_Integer(
  [in] LONG lnInteger
);
```


</dt> </dl> </dd> <dt>

**ларжеинтежер**
</dt> <dd> <dl>

Указатель на интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) объекта, реализующего [**иадсларжеинтежер**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) для этого значения.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **IDispatch**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LargeInteger(
  [out] IDispatch** ppLargeInteger
);
HRESULT put_LargeInteger(
  [in] IDispatch* pLargeInteger
);
```


</dt> </dl> </dd> <dt>

**нумерикстринг**
</dt> <dd> <dl>

Текст для интерпретации. Числовой тип.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NumericString(
  [out] BSTR* bstrNumericString
);
HRESULT put_NumericString(
  [in] BSTR bstrNumericString
);
```


</dt> </dl> </dd> <dt>

**октетстринг**
</dt> <dd> <dl>

Массив вариантов из однобайтовых символов.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetString(
  [in] VARIANT* vOctetString
);
HRESULT put_OctetString(
  [in] VARIANT* vOctetString
);
```


</dt> </dl> </dd> <dt>

**принтаблестринг**
</dt> <dd> <dl>

Отображение или печать строки.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintableString(
  [out] BSTR* bstrPrintableString
);
HRESULT put_PrintableString(
  [in] BSTR bstrPrintableString
);
```


</dt> </dl> </dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl>

Указатель на интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) объекта, реализующего [**иадссекуритидескриптор**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) для этого значения.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **IDispatch**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SecurityDescriptor(
  [out] IDispatch** ppSecurityDescriptor
);
HRESULT put_SecurityDescriptor(
  [in] IDispatch* pSecurityDescriptor
);
```


</dt> </dl> </dd> <dt>

**утктиме**
</dt> <dd> <dl>

Дата типа **VT \_** , выраженная в формате всемирного координированного времени (UTC).

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Дата**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UTCTime(
  [out] DATE* daUTCTime
);
HRESULT put_UTCTime(
  [in] DATE daUTCTime
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Комментарии

Свойства [**иадспропертивалуе**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) задают или извлекают значение свойства указанного типа. Например, свойство **касеигнорестринг** атрибута типа **\_ \_ String Адстипе DN**, например атрибут **distinguishedName** , приведет к ошибке. Свойство **касеигнорестринг** будет работать только с атрибутами типа **ADS \_ \_ \_ строка Ignore**. В следующей таблице значение [**адстипинум**](/windows/win32/api/iads/ne-iads-adstypeenum) сопоставляется с соответствующим свойством **иадспропертивалуе** , которое можно использовать для доступа к этому типу атрибута. Если значение **адстипинум** не указано в этой таблице, оно недоступно из интерфейса **иадспропертивалуе** . Для получения данных в других форматах следует использовать интерфейс [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) .



| Значение [**адстипинум**](/windows/win32/api/iads/ne-iads-adstypeenum) | [**Иадспропертивалуе**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) , свойство |
|------------------------------------------|---------------------------------------------------------|
| **\_строка различающегося имени адстипе \_**                  | **днстринг**                                            |
| **\_точный регистр \_ адстипе \_ строки**         | **касиксактстринг**                                     |
| **АДСТИПЕ \_ не \_ учитывать регистр \_ строк**        | **касеигнорестринг**                                    |
| **АДСТИПЕ \_ Печатная \_ строка**           | **принтаблестринг**                                     |
| **АДСТИПЕ \_ числовая \_ строка**             | **нумерикстринг**                                       |
| **АДСТИПЕ \_ Boolean**                     | **Boolean**                                             |
| **АДСТИПЕ \_ целое число**                     | **Integer**                                             |
| **\_Строка октета адстипе \_**               | **октетстринг**                                         |
| **АДСТИПЕ \_ время в формате UTC \_**                   | **утктиме**                                             |
| **АДСТИПЕ \_ большое \_ целое**              | **ларжеинтежер**                                        |
| **\_ \_ дескриптор безопасности адстипе \_ NT**    | **SecurityDescriptor**                                  |



 

## <a name="examples"></a>Примеры

В следующем примере кода показано, как получить свойство из списка свойств.


```VB
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup
 
' Retrieve the property list.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Retrieve a property entry. If you are certain of the property type,
' replace ADSTYPE_UNKNOWN with the actual property type.
Set propEntry = propList.GetPropertyItem("description", ADSTYPE_UNKNOWN)
 
' Print the property entry values.
For Each v In propEntry.Values
    Set propVal = v
    Select Case propVal.ADsType
        Case ADSTYPE_CASE_EXACT_STRING
            Debug.Print propVal.CaseExactString
        Case ADSTYPE_CASE_IGNORE_STRING
            Debug.Print propVal.CaseIgnoreString
        Case Else
            Debug.Print "Unable to handle a property of type: " & propVal.ADsType
    End Select
    
Next

Cleanup:
    If (Err.Number<>0) Then
       Debug.Print "An error has occurred. " & Err.Number
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



В следующем коде показано, как использовать **иадспропертивалуе:: Get \_ касеигнорестринг** для получения значения свойства Description из списка свойств.


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADsPropertyValue *pVal = NULL;
IADs *pObj = NULL;
VARIANT var, varItem;
BSTR valStr;
IEnumVARIANT *pEnum = NULL;
LONG lstart = 0;
LONG lend = 0;
LONG lADsType = ADSTYPE_UNKNOWN;
 
VariantInit(&var);
VariantInit(&varItem);
 
// Bind to the directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);

if(FAILED(hr)){goto Cleanup;}

// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}

pObj->GetInfo();
pObj->Release();
 
// Retrieve the property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), ADSTYPE_CASE_IGNORE_STRING, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}

hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Retrieve the value array of the property entry.
hr = pEntry->get_Values(&var);
if(FAILED(hr)){goto Cleanup;}

SAFEARRAY *sa = V_ARRAY( &var );
 
// Retrieve the lower and upper bound. Iterate and print the values.
hr = SafeArrayGetLBound( sa, 1, &lstart );
hr = SafeArrayGetUBound( sa, 1, &lend );
printf(" Property value(s) = ");
for ( long idx=lstart; idx < lend+1; idx++ )    {
    hr = SafeArrayGetElement( sa, &idx, &varItem );
    hr = V_DISPATCH(&varItem)->QueryInterface(IID_IADsPropertyValue,
                                              (void**)&pVal);
    if(FAILED(hr)){goto Cleanup;}

    pVal->get_ADsType(&lADsType);

    switch(lADsType)
    {
        case ADSTYPE_CASE_IGNORE_STRING:
        {
            hr = pVal->get_CaseIgnoreString(&valStr);
            break;
        }
        case ADSTYPE_CASE_EXACT_STRING:
        {
            hr = pVal->get_CaseExactString(&valStr);
            break;
        }
        default:
        {
            valStr = SysAllocString(L"Unable to handle a property of this type");
            break;
        }
    }

    if(FAILED(hr)){goto Cleanup;}
    printf(" %S ", valStr);
    SysFreeString(valStr);
    VariantClear(&varItem);
}
printf("\n");

Cleanup:
    if(pList)
        pList = NULL;

    if(pEntry)
        pEntry = NULL;

    if(pVal)
        pVal = NULL;

    if(pObj)
        pObj = NULL;

    if(pEnum)
        pEnum = NULL;

    SysFreeString(valStr);
    VariantClear(&varItem);
    VariantClear(&var);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадспропертивалуе определен как 79FA9AD0-A97C-11D0-8534-00C04FD8D503<br/>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иадспропертивалуе**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[**адстипинум**](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[**иадспропертентри**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[**иадспропертилист**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
</dt> <dt>

[**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

