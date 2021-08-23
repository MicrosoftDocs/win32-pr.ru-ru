---
title: Методы свойств Иадспропертилист (iAds. h)
description: Методы свойств интерфейса Иадспропертилист считывают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 3564b61a-5950-4d00-8ea1-86fecd5c6c4e
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадспропертилист ADSI
topic_type:
- apiref
api_name:
- IADsPropertyList Property Methods
- IADsPropertyList.PropertyCount
- IADsPropertyList.get_PropertyCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5db37280cd72d51e0f47daa67d3b277418c077d91c9d0a07a1631ac184b4a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023392"
---
# <a name="iadspropertylist-property-methods"></a>Методы свойств Иадспропертилист

Методы свойств интерфейса [**иадспропертилист**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) считывают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**пропертикаунт**
</dt> <dd> <dl>

Число элементов в списке свойств.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PropertyCount(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Примеры

В следующем примере кода показано, как определить количество элементов в списке свойств.


```VB
Dim propList As IADsPropertyList
Dim count As Long

On Error GoTo Cleanup
 
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
 
propList.GetInfo
count = propList.PropertyCount
Debug.Print "Number of Properties Found: " & count

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set propList = Nothing
```



В следующем примере кода показано, как определить количество элементов в списке свойств.


```C++
int GetPropertyCacheCount(LPWSTR adsPath)
{
    IADsPropertyList *pList;
    IADs *pObj;
    HRESULT hr = S_OK;

    if(!adsPath)
    {
        _tprintf(TEXT("Invalid ADsPath."));
        return -1;
    }

    HRESULT hr = ADsGetObject(adsPath,
                          IID_IADsPropertyList,
                          (void**)&pList);
    // Initialize the property cache.
    hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
    pObj->GetInfo();
    pObj->Release();

    // Get the property count.
    hr = pList->get_PropertyCount(&count);
    pList->Release();

    // Return the property count if it succeeded, otherwise
    // return -1.

    if(SUCCEEDED(hr))
    {
        return count;
    }
    else
    {
        return -1;
    }

}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадспропертилист определен как C6F602B6-8F69-11D0-8528-00C04FD8D503<br/>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иадспропертилист**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
</dt> <dt>

[Методы свойств интерфейса](interface-property-methods.md)
</dt> </dl>

 

 





