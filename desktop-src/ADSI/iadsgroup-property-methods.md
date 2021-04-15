---
title: Методы свойств Иадсграуп (iAds. h)
description: Методы свойств интерфейса Иадсграуп.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсграуп ADSI
topic_type:
- apiref
api_name:
- IADsGroup Property Methods
- IADsGroup.Description
- IADsGroup.get_Description
- IADsGroup.put_Description
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 665cb91a55298012e4e906c2972da5371e3960be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654617"
---
# <a name="iadsgroup-property-methods"></a>Методы свойств Иадсграуп

Методы свойств интерфейса [**иадсграуп**](/windows/desktop/api/Iads/nn-iads-iadsgroup) считывают и записывают следующие свойства. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**Описание**
</dt> <dd> <dl>

Указывает текстовое описание членства в группе.

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


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Комментарии

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a>Использование Иадсграуп для получения описания встроенных групп

В следующих примерах показано, как получить сведения об объектах группы Windows по имени. В многоязычной среде встроенные группы иногда называются разными локализованными именами. Это означает, что они не могут быть получены напрямую с помощью строковых идентификаторов, таких как "WinNT://Microsoft/Administrators". В этом случае пользователь может выполнить привязку к хорошо известному объекту идентификатора безопасности для группы, получить локализованное имя группы и предоставить его методу GetObject. Дополнительные сведения см. в разделе [хорошо известные идентификаторы безопасности](/windows/desktop/SecAuthZ/well-known-sids).

## <a name="examples"></a>Примеры

В следующем Visual Basic примере показано, как выполнить привязку к объекту группы и отобразить описание группы.


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Microsoft/Administrators")
Debug.Print grp.Description

Cleanup
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



В следующем примере C++ показано, как выполнить привязку к объекту группы и отобразить описание группы.


```C++
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://localHost/Administrators";
BSTR bstr;

hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&pGroup);

if(FAILED(hr)) {goto Cleanup;}

hr = pGroup->get_Description(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Description: %S\n",bstr);

Cleanup:
    SysFreeString(bstr);
    if(pGroup) 
        pGroup->Release();

    return hr;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадсграуп определен как 27636B00-410F-11CF-B1FF-02608C9E7553<br/>            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**иадсграуп**](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[Методы свойств интерфейса](interface-property-methods.md)
</dt> </dl>

 

