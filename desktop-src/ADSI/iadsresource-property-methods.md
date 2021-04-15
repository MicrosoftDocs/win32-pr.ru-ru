---
title: Методы свойств Иадсресаурце (iAds. h)
description: Методы свойств интерфейса Иадсресаурце получают или задают свойства, описанные в следующей таблице. Общее описание методов свойств см. в разделе методы свойств интерфейса.
ms.assetid: a2d6ed76-88e9-468f-928a-a038b73fb362
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсресаурце ADSI
topic_type:
- apiref
api_name:
- IADsResource Property Methods
- IADsResource.LockCount
- IADsResource.get_LockCount
- IADsResource.Path
- IADsResource.get_Path
- IADsResource.User
- IADsResource.get_User
- IADsResource.UserPath
- IADsResource.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0f2ab2642dd8d03062a26d096190cf7615977a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654484"
---
# <a name="iadsresource-property-methods"></a>Методы свойств Иадсресаурце

Методы свойств интерфейса [**иадсресаурце**](/windows/desktop/api/Iads/nn-iads-iadsresource) получают или задают свойства, описанные в следующей таблице. Общее описание методов свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**локккаунт**
</dt> <dd> <dl>

Количество блокировок ресурса.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockCount(
  [out] LONG* plLockCount
);
```


</dt> </dl> </dd> <dt>

**Путь**
</dt> <dd> <dl>

Путь файловой системы к открытому ресурсу.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
```


</dt> </dl> </dd> <dt>

**Пользователь**
</dt> <dd> <dl>

Имя пользователя, открывшего ресурс.

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

Путь к объекту пользователя для пользователя, открывшего ресурс.

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

В следующем примере кода показано, как проверить открытые ресурсы файловой службы.


```VB
Dim fso As IADsFileServiceOperations
' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate resources.
If (IsEmpty(fso) = False) Then
    For Each resource In fso.resources
        MsgBox "Resource name: " & resource.name
        MsgBox "Resource path: " & resource.path
    Next resource
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



В следующем примере кода перечисляются наборы ресурсов.


```C++
IADsFileServiceOperations *pFso = NULL;
IADsResource *pRes = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
IEnumVARIANT *pEnum = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
HRESULT hr = S_OK;

LPWSTR adsPath =L"WinNT://aMachine/LanmanServer";
hr = ADsGetObject(adsPath, IID_IADsFileServiceOperations,(void**)&pFso);
if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Resources(&pColl);
if(FAILED(hr)) {goto Cleanup;}


// Enumerate print jobs. Code omitted.
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
VariantInit(&var);
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsResource, (void**)&pRes);
        pRes->get_Name(&bstr);
        printf("Resource name: %S\n",bstr);
        SysFreeString(bstr);
        pRes->get_Path(&bstr);
        printf("Resource path: %S\n",bstr);
        SysFreeString(bstr);
        pRes->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pRes) pRes->Release();
    if(pDisp) pDisp->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pFso) pFso->Release();
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадсресаурце определен как 34A05B20-4AAB-11CF-AE2C-00AA006EBFB9<br/>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иадсресаурце**](/windows/desktop/api/Iads/nn-iads-iadsresource)
</dt> <dt>

[**Иадсфилесервицеоператионс:: ресурсы**](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-resources)
</dt> </dl>

 

 





