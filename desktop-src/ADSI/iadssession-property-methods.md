---
title: Методы свойств Иадссессион (iAds. h)
description: Методы свойств интерфейса Иадссессион получают или задают свойства, описанные в следующей таблице. Дополнительные сведения и общее обсуждение методов свойств см. в разделе методы свойств интерфейса.
ms.assetid: b2366da7-c51c-4279-8931-2000d3110d72
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадссессион ADSI
topic_type:
- apiref
api_name:
- IADsSession Property Methods
- IADsSession.Computer
- IADsSession.get_Computer
- IADsSession.ComputerPath
- IADsSession.get_ComputerPath
- IADsSession.ConnectTime
- IADsSession.get_ConnectTime
- IADsSession.IdleTime
- IADsSession.get_IdleTime
- IADsSession.User
- IADsSession.get_User
- IADsSession.UserPath
- IADsSession.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf7dd9abe25d731ba63385cd8d632c4212ea349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891793"
---
# <a name="iadssession-property-methods"></a>Методы свойств Иадссессион

Методы свойств интерфейса [**иадссессион**](/windows/desktop/api/Iads/nn-iads-iadssession) получают или задают свойства, описанные в следующей таблице. Дополнительные сведения и общее обсуждение методов свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**Компьютер**
</dt> <dd> <dl>

Имя клиентской рабочей станции.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Computer(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

**компутерпас**
</dt> <dd> <dl>

Путь к объекту компьютера для клиентской рабочей станции.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerPath(
  [out] BSTR* pbstrComputerPath
);
```


</dt> </dl> </dd> <dt>

**коннекттиме**
</dt> <dd> <dl>

Время, прошедшее с момента запуска сеанса (в секундах).

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ConnectTime(
  [out] LONG* plConnectTime
);
```


</dt> </dl> </dd> <dt>

**идлетиме**
</dt> <dd> <dl>

Время простоя в секундах сеанса.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IdleTime(
  [out] LONG* plIdleTime
);
```


</dt> </dl> </dd> <dt>

**Пользователь**
</dt> <dd> <dl>

Имя пользователя сеанса.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

**усерпас**
</dt> <dd> <dl>

Путь к объекту пользователя для пользователя этого сеанса.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Примеры

В следующем примере кода показано, как проверить сеансы для службы файлов.


```VB
Dim fso As IADsFileServiceOperations
On Error GoTo Cleanup

' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate sessions.
If (IsEmpty(fso) = False) Then
    For Each session In fso.sessions
        MsgBox "Session Computer: " & session.Computer
        MsgBox "Session User: " & session.User
    Next Session
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



В следующем примере кода перечисляются коллекции сеансов.


```C++
IADsFileServiceOperations *pFso = NULL;
IADsSession *pSes = NULL;
IADsCollection *pColl = NULL;
HRESULT hr = S_OK;
IUnknown *pUnk = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IEnumVARIANT *pEnum = NULL;

VariantInit(&var);

LPWSTR adsPath = L"WinNT://aMachine/LanmanServer";

hr = ADsGetObject(adsPath,IID_IADsFileServiceOperations,
                  (void**)&pFso);

if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Sessions(&pColl);

// Enumerate sessions. 
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsSession, (void**)&pSes);
        pSes->get_Computer(&bstr);
        printf("Session host: %S\n",bstr);
        SysFreeString(bstr);

        pSes->get_User(&bstr);
        printf("Session user: %S\n",bstr);
        SysFreeString(bstr);

        pRes->Release();
    }

    VariantClear(&var);
    pDisp=NULL;
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pFso) pFso->Release();
    if(pColl) pColl->Release();
    if(pUnk) pUnk->Release();
    if(pEnum) pEnum->Release();
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадссессион определен как 398B7DA0-4AAB-11CF-AE2C-00AA006EBFB9<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Иадсфилесервицеоператионс:: сеансы**](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-sessions)
</dt> <dt>

[**иадссессион**](/windows/desktop/api/Iads/nn-iads-iadssession)
</dt> </dl>

 

 





