---
title: Методы свойств Иадсмемберс (iAds. h)
description: Методы интерфейса Иадсмемберс считывают и записывают свойства, описанные в этом разделе. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: ed4e98e5-053c-4d3b-bcd0-3add96bbe120
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсмемберс ADSI
topic_type:
- apiref
api_name:
- IADsMembers Property Methods
- IADsMembers.Count
- IADsMembers.get_Count
- IADsMembers.Filter
- IADsMembers.get_Filter
- IADsMembers.put_Filter
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 384aa8a8f04afe8abbaa9627a0080b7a4ce219d4b58482d3eddc20bb33825c7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023462"
---
# <a name="iadsmembers-property-methods"></a>Методы свойств Иадсмемберс

Методы интерфейса [**иадсмемберс**](/windows/desktop/api/Iads/nn-iads-iadsmembers) считывают и записывают свойства, описанные в этом разделе. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**Количество**
</dt> <dd> <dl>

Указывает количество элементов в контейнере. Если фильтр установлен, то функция Count возвращает только число элементов, соответствующих описанию фильтра.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCountr
);
```


</dt> </dl> </dd> <dt>

**Filter**
</dt> <dd> <dl>

Указывает фильтр. Синтаксис записей в массиве фильтров совпадает с фильтром, используемым в интерфейсе [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Remarks

Поставщики систем ADSI не поддерживают метод свойства **иадсмемберс:: Get \_ Count** .

## <a name="examples"></a>Примеры

В следующем примере кода показано, как использовать методы свойств этого интерфейса.


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://myComputer/someGroup")
grp.members.filter = Array("user")
For Each usr In grp.Members
    MsgBox usr.Name & "," & usr.Class & "," & usr.AdsPath
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



В следующем примере кода используется метод **\_ фильтра иадсмемберс::p UT** для подготовки к перечислению коллекции членов группы.


```C++
IADsGroup *pGroup;
HRESULT hr = S_OK;

LPWSTR grpPath = L"WinNT://myComputer/someGroup";
hr = ADsGetObject(grpPath,IID_IADsGroup,(void**)&pGroup);
if(FAILED(hr)){goto Cleanup;}

IADsMembers *pMembers;
hr = pGroup->Members(&pMembers);
if(FAILED(hr)){goto Cleanup;}

hr = pGroup->Release();

SAFEARRAY *sa = CreateSafeArray(L"user");
hr = pMembers->put_Filter(sa);
if(FAILED(hr)){goto Cleanup;}

hr = EnumMembers(pMembers);    // For more information, and a 
                               // code example, see 
                               // IADsMembers::get__NewEnum.
if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pGroup) pGroup->Release();
    if(pMembers) pMembers->Release();
    return hr;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадсмемберс определен как 451A0030-72EC-11CF-B03B-00AA006E0975<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[**Иадсмемберс:: Get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum)
</dt> <dt>

[**иадсмемберс**](/windows/desktop/api/Iads/nn-iads-iadsmembers)
</dt> <dt>

[Методы свойств интерфейса](interface-property-methods.md)
</dt> </dl>

 

 





