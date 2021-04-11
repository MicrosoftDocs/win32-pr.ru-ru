---
description: Переменные типа VARIANT имеют поле тега типа VT, которое указывает тип данных.
ms.assetid: 3436faf6-2e66-46a1-b1e8-84f513282c16
title: Установка поля тега типа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e443fae33b14bd4270e63188ff96a042a91c8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262850"
---
# <a name="setting-the-type-tag-field"></a>Установка поля тега типа

Переменные типа **Variant** имеют поле тега типа **VT** , которое указывает тип данных. Возвращаемые значения типа **Variant** возвращаются методам с полем тега типа, для которого задан тип данных возвращаемого значения. Входные параметры типа **Variant** в вызове метода должны иметь поле тега типа, установленное приложением, на одно из поддерживаемых значений. Соответствие типов параметров типам данных выглядит следующим образом.



| Тип параметра              | Тип данных                                      |
|-----------------------------|------------------------------------------------|
| ПРОПТИПЕ \_ Long<br/>   | VT \_ I2 или VT \_ I4<br/>                    |
| \_Дата проптипе<br/>   | \_Дата VT<br/>                            |
| \_двоичный файл проптипе<br/> | VT \_ BSTR или (VT \_ BSTR \| VT \_ ByRef)<br/> |
| \_строка проптипе<br/> | VT \_ BSTR или (VT \_ BSTR \| VT \_ ByRef)<br/> |



 

В следующем примере показано, как инициализировать типы данных Variant, перечисленные выше.


```C++
HRESULT hr;
VARIANT vEMail;
VARIANT vNotBefore;
VARIANT vCount;
VARIANT vByRef;
BSTR bstr = NULL;
SYSTEMTIME st;

//Set the BSTR variant data type.
VariantInit(&vEMail);
vEMail.vt = VT_BSTR;   
vEMail.bstrVal = SysAllocString(L"someone@example.com");
if (NULL == vEMail.bstrVal)
{
    hr = E_OUTOFMEMORY;
    //Handle error.   
}
//Use the variant.
VariantClear(&vEMail);  //when done


//Set the BSTR|BYREF variant data type.
VariantInit(&vByRef);
vByRef.vt = VT_BSTR | VT_BYREF;   
vByRef.pbstrVal = &bstr;
//Use the variant.
VariantClear(&vByRef);  //when done
SysFreeString(bstr);


//Set the DATE variant data type.
memset(&st, 0, sizeof(SYSTEMTIME));
st.wYear = 2000;
st.wMonth = 1;
st.wDay = 1;
st.wHour = 12;

VariantInit(&vNotBefore);
vNotBefore.vt = VT_DATE;
if (!SystemTimeToVariantTime(&st, &vNotBefore.date))
{
    hr = E_FAIL;
    //Handle error.
}
//Use the variant.
VariantClear(&vNotBefore);  //when done


//Set the LONG variant data type.
VariantInit(&vCount);
vCount.vt = VT_I4;
vCount.long = 123456;
//Use the variant.
VariantClear(&vCount);  //when done
```



 

 




