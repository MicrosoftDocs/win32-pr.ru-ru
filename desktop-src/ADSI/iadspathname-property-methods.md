---
title: Методы свойств Иадспаснаме (iAds. h)
description: Возвращает или задает свойства Ескапедмоде.
ms.assetid: 007ec617-cff2-492a-a62c-50d65fefcd3b
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадспаснаме ADSI
topic_type:
- apiref
api_name:
- IADsPathname Property Methods
- IADsPathname.EscapedMode
- IADsPathname.get_EscapedMode
- IADsPathname.get_EscapedMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11d3321d58065d890d864ed967a4e6a66dad22cde2cc234b5907afab74986898
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023432"
---
# <a name="iadspathname-property-methods"></a>Методы свойств Иадспаснаме

Методы свойств интерфейса [**иадспаснаме**](/windows/desktop/api/Iads/nn-iads-iadspathname) получают или задают свойства **ескапедмоде** . Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**ескапедмоде**
</dt> <dd> <dl>

Проверьте или укажите, как экранированные символы обрабатываются в пути. Дополнительные сведения и определенные параметры см. в [**разделе \_ \_ \_ перечислимый режим экранирования ADS**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EscapedMode(
  [out] long* retval
);
HRESULT get_EscapedMode(
  [in] long* lnEscapedMode
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Remarks

**Ескапедмоде** представляет состояние. Его можно включить или отключить, задав для него AD \_ ескапедмоде \_ On или AD \_ ЕСКАПЕДМОДЕ \_ Off/AD \_ ескапедмоде \_ Off \_ ex. При включении или отключении все последующие извлечения создают экранированные или неэкранированные строки пути.

В ADSI только [**иадспаснаме**](/windows/desktop/api/Iads/nn-iads-iadspathname) поддерживает рассылку путей. Все остальные интерфейсы ADSI всегда возвращают экранированные пути. По умолчанию **ескапедмоде** является ADS \_ ескапедмоде \_ по умолчанию, как определено в [**\_ \_ \_ перечислении режима экранирования ADS**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).

## <a name="examples"></a>Примеры

В следующем примере кода показано, как использовать включение/выключение свойства **ескапедмоде** для экранирования следующих трех специальных символов: "=", "," и "/".


```VB
Dim path As New Pathname
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All escaped, producing:
                                          ' "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' Only "/" is unescaped:
                                          ' "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
```



В следующем примере кода показано, как использовать включение/выключение свойства **ескапедмоде** для экранирования следующих трех специальных символов: "=", "," и "/".


```VB
<%
Dim path
const ADS_SETTYPE_FULL = 1
const ADS_SETTYPE_DN   = 4
const ADS_FORMAT_WINDOWS = 1
const ADS_ESCAPEDMODE_ON = 2
const ADS_ESCAPEDMODE_OFF = 3
const ADS_ESCAPEDMODE_OFF_EX = 4
 
Set path = CreateObject("Pathname")
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' All escaped, producing:  "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' Only "/" is unescaped: "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
%>
```



В следующем примере кода показано, как работать со свойством **ескапедмоде** . Проверка ошибок игнорируется.


```C++
IADsPathname *pPathname=NULL;
HRESULT hr;
 
hr = CoCreateInstance(CLSID_Pathname,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsPathname,
                      (void**)&pPathname);
 
if(FAILED(hr)) 
{
    if(pPathname) pPathname->Release();
    return NULL;
}
 
pPathname->AddRef();
hr = pPathname->Set(CComBSTR("LDAP://CN=joy/ful\/*"), 
                    ADS_SETTYPE_FULL); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy/ful\/*"

SysFreeString(bstr);
 
// Set the path using ADS_SETTYPE_DN
 
hr = pPathname->Set(CComBSTR("CN=joy/ful\/*"), ADS_SETTYPE_DN); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy\/ful\/*"

SysFreeString(bstr);
 
hr = pPathname->Release();
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадспаснаме определен как D592AED4-F420-11D0-A36E-00C04FB950DC<br/>         |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname)
</dt> <dt>

[**\_ \_ перечислимый режим ЭКРАНИРОВАНия ADS \_**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)
</dt> </dl>

 

 





