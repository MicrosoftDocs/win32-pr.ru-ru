---
title: Методы свойств Иадсвиннтсистеминфо (iAds. h)
description: Методы свойств интерфейса Иадсвиннтсистеминфо получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 5ba36851-3d03-4179-8cee-dbebe24b7c4e
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсвиннтсистеминфо ADSI
topic_type:
- apiref
api_name:
- IADsWinNTSystemInfo Property Methods
- IADsWinNTSystemInfo.UserName
- IADsWinNTSystemInfo.get_UserName
- IADsWinNTSystemInfo.ComputerName
- IADsWinNTSystemInfo.get_ComputerName
- IADsWinNTSystemInfo.DomainName
- IADsWinNTSystemInfo.get_DomainName
- IADsWinNTSystemInfo.PDC
- IADsWinNTSystemInfo.get_PDC
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87942adb526b88ae2b538841cd274da69aa0ea5150f6b528ea4ef299ad478f2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179476"
---
# <a name="iadswinntsysteminfo-property-methods"></a>Методы свойств Иадсвиннтсистеминфо

Методы свойств интерфейса [**иадсвиннтсистеминфо**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo) получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**ИмяКомпьютера**
</dt> <dd> <dl>

Имя главного компьютера, на котором работает приложение.

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

**DomainName**
</dt> <dd> <dl>

Имя домена, к которому принадлежит пользователь.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainName(
  [out] BSTR* pbstrDomain
);
```


</dt> </dl> </dd> <dt>

**ХОЗЯИН**
</dt> <dd> <dl>

Имя основного контроллера домена, к которому принадлежит главный компьютер.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDC(
  [out] BSTR* pbstrPDC
);
```


</dt> </dl> </dd> <dt>

**UserName**
</dt> <dd> <dl>

Имя учетной записи пользователя, под которой создается объект **виннтсистеминфо** .

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

В следующем примере кода C/C++ извлекаются сведения о системе WinNT. Для краткости проверка ошибок пропущена.


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsWinNTSystemInfo *pNtSys;
    hr = CoCreateInstance(CLSID_WinNTSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsWinNTSystemInfo,
                          (void**)&pNTsys);
 
   BSTR bstr;
   hr = pNtSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_DomainName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_PDC(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pNtSys) {
      pNtSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



в следующем Visual Basic примере кода извлекаются сведения о системе WinNT.


```VB
Dim ntsys As New WinNTSystemInfo
Debug.print "User: " & ntsys.UserName
Debug.print "Computer: " & ntsys.ComputerName
Debug.print "Domain: " & ntsys.DomainName
Debug.print "PDC: " & ntsys.PDC
```



следующий пример кода Visual Basic scripting Edition/Active Server pages извлекает сведения о системе WinNT.


```VB
<%
Dim ntsys
Set ntsys = CreateObject("WinNTSystemInfo")
Response.Write "User: " & ntsys.UserName
Response.Write "Computer: " & ntsys.ComputerName
Response.Write "Domain: " & ntsys.DomainName
Response.Write "PDC: " & ntsys.PDC
%>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадсвиннтсистеминфо определен как 6C6D65DC-AFD1-11d2-9CB9-0000F87A369E<br/>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иадсвиннтсистеминфо**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo)
</dt> </dl>

 

 





