---
title: Методы свойств Иадсконтаинер (iAds. h)
description: Методы свойств интерфейса Иадсконтаинер получают или задают свойства, описанные в следующей таблице. Дополнительные сведения и общее обсуждение методов свойств см. в разделе методы свойств интерфейса.
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсконтаинер ADSI
topic_type:
- apiref
api_name:
- IADsContainer Property Methods
- IADsContainer.Count
- IADsContainer.get_Count
- IADsContainer.Filter
- IADsContainer.get_Filter
- IADsContainer.put_Filter
- IADsContainer.Hints
- IADsContainer.get_Hints
- IADsContainer.put_Hints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13515bcf90c926db839aad60d49599967ee0d24bedbe0deb4b7d1d21c3c016e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428089"
---
# <a name="iadscontainer-property-methods"></a>Методы свойств Иадсконтаинер

Методы свойств интерфейса [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) получают или задают свойства, описанные в следующей таблице. Дополнительные сведения и общее обсуждение методов свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**Количество**
</dt> <dd> <dl>

Возвращает количество элементов в контейнере. Если параметр **Filter** установлен, функция **Count** возвращает только число отфильтрованных элементов.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> <dt>

**Filter**
</dt> <dd> <dl>

Возвращает или задает фильтр, используемый для выбора классов объектов в заданном перечислении. Это массив вариантов, каждый элемент которого является именем класса схемы. Если параметр **Filter** не установлен или установлен в значение Empty, перечислитель получает все объекты всех классов.

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


</dt> </dl> </dd> <dt>

**Указания**
</dt> <dd> <dl>

Массив вариантов строк **BSTR** . Каждый элемент определяет имя свойства, найденного в определении схемы. Параметр *вхинтс* позволяет клиенту указать, какие атрибуты загружать для каждого перечислимого объекта. Такие данные можно использовать для оптимизации сетевого доступа. Однако конкретная реализация зависит от поставщика и сейчас не используется поставщиком WinNT.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Hints(
  [out] VARIANT* pvHints
);
HRESULT put_Hints(
  [in] VARIANT vHints
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Remarks

Процессы перечисления в разделе [**иадсконтаинер:: Get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) и **иадсконтаинер:: Get \_** выполняются для содержащихся в кэше объектов. Если контейнер содержит большое количество объектов, это может повлиять на производительность. Чтобы повысить производительность, отключите кэш, настройте соответствующий размер страницы и используйте интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . По этой причине свойство " **число получаемых \_ объектов** " не поддерживается поставщиком Microsoft LDAP.

## <a name="examples"></a>Примеры

в следующем Visual Basic примере кода показано, как можно использовать методы свойств [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .


```VB
Dim cont As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup
 
Set cont = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
cont.Hints = Array("adminDescription") ' Load this attribute. Optional.
Debug.Print cont.Get("adminDescription")

' Filter users.
cont.Filter = Array("user")

For Each usr In cont
  Debug.Print usr.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set usr = Nothing
```



В следующем примере кода C++ показано, как можно использовать методы свойств [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) . Для краткости проверка ошибок пропущена.


```C++
IADsContainer *pCont;
IADs *pChild;
IADs *pADs;
 
HRESULT hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM",
                          IID_IADsContainer, 
                          (void**)&pCont);

if(FAILED(hr)){goto Cleanup;}

LPWSTR pszArray[] = { L"adminDescription" };
DWORD dwNumber = sizeof(pszArray)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszArray, dwNumber, &var);
if(FAILED(hr)){goto Cleanup;}

hr = pCont->put_Hints( var );
if(FAILED(hr)){goto Cleanup;}

VariantClear(&var);
 
hr = pCont->QueryInterface(IID_IADs, (void**)pADs);
if(FAILED(hr)){goto Cleanup;}
 
hr = pADs->Get(CComBSTR("adminDescription"), var);
 
LPWSTR pszUsers = {L"user"};
dwNumber = sizeof(pszUsers)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr(pszUsers, dwNumber, &var);
hr = pCont->put_Filter( var );
VariantClear(&var);
 
// Enumerate user objects in the container.
IEnumVARIANT *pEnum = NULL;
hr = ADsBuildEnumerator(pCont, &pEnum);
pCont->Release();    // Not required when users are enumerated.
 
ULONG lFetch;
VariantClear(&var);
while (SUCCEEDED(ADsEnumerateNext(pEnum, 1, &var, &lFetch)) && 
                      lFetch==1) {
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, (void**)&pChild)
    if(SUCCEEDED(hr)) {
        BSTR bstrName;
        pChild->get_Name(&bstrName);
        printf("  %S\n", bstrName);
        SysFreeString(bstrName);
        pChild->Release();
    }
    VariantClear(&var);
}
Cleanup:
    if(pADs)
        pADs->Release();

    if(pCont)
        pCont->Release();

    if(pChild)
        pChild->Release();

    VariantClear(&var);
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадсконтаинер определен как 001677D0-FD16-11CE-ABC4-02608C9E7553<br/>        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 





