---
title: Методы свойств Иадсфилесервице (iAds. h)
description: Методы свойств интерфейса Иадсфилесервице получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 1455df61-9218-450b-b956-1cf127364f24
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсфилесервице ADSI
topic_type:
- apiref
api_name:
- IADsFileService Property Methods
- IADsFileService.Description
- IADsFileService.get_Description
- IADsFileService.put_Description
- IADsFileService.MaxUserCount
- IADsFileService.get_MaxUserCount
- IADsFileService.put_MaxUserCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd12e1f9c52606f76cf6c0828767819e318874c323b22f5e1a91b70d71965465
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082448"
---
# <a name="iadsfileservice-property-methods"></a>Методы свойств Иадсфилесервице

Методы свойств интерфейса [**иадсфилесервице**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**Описание**
</dt> <dd> <dl>

Описание службы файлов.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

**максусеркаунт**
</dt> <dd> <dl>

Максимальное число пользователей, разрешенных в службе в любое время.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
HRESULT put_MaxUserCount(
  [in] LONG lMaxUserCount
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Remarks

Для доступа к общим папкам, сеансам и ресурсам на компьютере необходимо пройти через службу файлов.

## <a name="examples"></a>Примеры

В следующем примере кода записывается описание и проверяется предельное число пользователей в службе файлов.


```VB
Dim fs As IADsFileService
On Error GoTo Cleanup

' Bind to a file service object on "myComputer" in the local domain.
Set fs = GetObject("WinNT://myComputer/LanmanServer")

fs.Description = "WinNT file service."
n = fs.MaxUserCount
If n = -1 Then
   MsgBox "No limit has been imposed on number of users allowed."
Else
   MsgBox n & " users are allowed."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
```



В следующем примере кода записывается описание и проверяется предельное число пользователей для объекта службы файлов.


```C++
HRESULT CheckFileService()
{
    IADsFileService *pFs = NULL;
    LPWSTR adsPath = L"WinNT://myComputer/LanmanServer";
    HRESULT hr = S_OK;
    long count = 0;

    hr = ADsGetObject(adsPath, IID_IADsFileService, (void**)&pFs)
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->put_Description(CComBSTR("WinNT File Service"));
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->SetInfo();
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->get_MaxUserCount(&count);
    if(FAILED(hr)) {goto Cleanup;}

    if(count == -1) {
        printf("No limit has been imposed on the number of users.\n");
    } 
    else {
        printf("Number of allowed users are %d\n",count);
    }

Cleanup:
    if(pFs) pFs->Release();
    return S_OK;
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадсфилесервице определен как A89D1900-31CA-11CF-A98A-00AA006BC149<br/>      |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иадссервице**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[**иадсфилесервице**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[**иадсфилесервицеоператионс**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[**иадссервицеоператионс**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> <dt>

[Методы свойств интерфейса](interface-property-methods.md)
</dt> </dl>

 

 





