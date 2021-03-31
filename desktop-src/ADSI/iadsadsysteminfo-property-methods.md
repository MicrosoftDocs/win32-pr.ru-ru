---
title: Методы свойств Иадсадсистеминфо (iAds. h)
description: Методы свойств интерфейса Иадсадсистеминфо получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 1cdaa610-4341-4825-b2f9-dd495a9147ff
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсадсистеминфо ADSI
topic_type:
- apiref
api_name:
- IADsADSystemInfo Property Methods
- IADsADSystemInfo.UserName
- IADsADSystemInfo.get_UserName
- IADsADSystemInfo.ComputerName
- IADsADSystemInfo.get_ComputerName
- IADsADSystemInfo.SiteName
- IADsADSystemInfo.get_SiteName
- IADsADSystemInfo.DomainShortName
- IADsADSystemInfo.get_DomainShortName
- IADsADSystemInfo.DomainDNSName
- IADsADSystemInfo.get_DomainDNSName
- IADsADSystemInfo.ForestDNSName
- IADsADSystemInfo.get_ForestDNSName
- IADsADSystemInfo.PDCRoleOwner
- IADsADSystemInfo.get_PDCRoleOwner
- IADsADSystemInfo.SchemaRoleOwner
- IADsADSystemInfo.get_SchemaRoleOwner
- IADsADSystemInfo.IsNativeMode
- IADsADSystemInfo.get_IsNativeMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8dba53dfda4bb8f4dd3290cb2737cdeb4e8a6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136890"
---
# <a name="iadsadsysteminfo-property-methods"></a>Методы свойств Иадсадсистеминфо

Методы свойств интерфейса [**иадсадсистеминфо**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**ИмяКомпьютера**
</dt> <dd> <dl>

Получает различающееся имя локального компьютера.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

**домаинднснаме**
</dt> <dd> <dl>

Возвращает DNS-имя домена локального компьютера, например "domainName.companyName.com".

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

**домаиншортнаме**
</dt> <dd> <dl>

Получает короткое имя домена локального компьютера, например "имя_домена".

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainShortName(
  [out] BSTR* pbstrDSN
);
```


</dt> </dl> </dd> <dt>

**форестднснаме**
</dt> <dd> <dl>

Возвращает DNS-имя леса локального компьютера.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ForestDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

**иснативемоде**
</dt> <dd> <dl>

Определяет, находится ли домен локального компьютера в собственном или смешанном режиме.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsNativeMode(
  [out] BOOL* pvBool
);
```


</dt> </dl> </dd> <dt>

**пдкролеовнер**
</dt> <dd> <dl>

Извлекает различающееся имя объекта агента службы каталогов (DSA), владеющего ролью основного контроллера домена в домене локального компьютера.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDCRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

**SchemaRoleOwner**
</dt> <dd> <dl>

Извлекает различающееся имя объекта агента службы каталогов (DSA) для контроллера домена, владеющего ролью хозяина схемы в лесу локального компьютера.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SchemaRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

**Значением**
</dt> <dd> <dl>

Возвращает имя сайта локального компьютера.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SiteName(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

**UserName**
</dt> <dd> <dl>

Возвращает Active Directory различающееся имя текущего пользователя, вошедшего в систему или пользователя, олицетворяемого вызывающим потоком.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Примеры

В следующем примере кода C++ извлекаются сведения о системе Windows. Для краткости проверка ошибок пропущена.


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsADSystemInfo *pSys;
    hr = CoCreateInstance(CLSID_ADSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsADSystemInfo,
                          (void**)&pSys);
 
   BSTR bstr;
   hr = pSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_DomainDNSName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_PDCRoleOwner(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC Role owner: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pSys) {
      pSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



В следующем Visual Basic примере кода извлекаются сведения о системе Windows.


```VB
Dim sys As New ADSystemInfo
Debug.print "User: " & sys.UserName
Debug.print "Computer: " & sys.ComputerName
Debug.print "Domain: " & sys.DomainDNSName
Debug.print "PDC Role Owner: " & sys.PDCRoleOwner
```



Следующий пример кода VBScript/ASP извлекает сведения о системе Windows.


```VB
<%
Dim sys
Set sys = CreateObject("ADSystemInfo")
Response.Write "User: " & sys.UserName
Response.Write "Computer: " & sys.ComputerName
Response.Write "Domain: " & sys.DomainDNSName
Response.Write "PDC Role Owner: " & sys.PDCRoleOwner
%>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадсадсистеминфо определен как 5BB11929-AFD1-11d2-9CB9-0000F87A369E<br/>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

