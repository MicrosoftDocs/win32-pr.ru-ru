---
title: Методы свойства IADs (iAds. h)
description: Методы свойств интерфейса IADs получают или задают свойства, описанные в следующей таблице. Дополнительные сведения о методах свойств см. в разделе методы свойств интерфейса.
ms.assetid: d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12
ms.tgt_platform: multiple
keywords:
- Свойства IADs методы интерфейса ADSI
topic_type:
- apiref
api_name:
- IADs Property Methods
- IADs.ADsPath
- IADs.get_ADsPath
- IADs.Class
- IADs.get_Class
- IADs.GUID
- IADs.get_GUID
- IADs.Name
- IADs.get_Name
- IADs.Parent
- IADs.get_Parent
- IADs.Schema
- IADs.get_Schema
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3326bbbf5ea7c2d2a98a6224f9b0a83a738c76a206d343a8629138d4d45e73b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082528"
---
# <a name="iads-property-methods"></a>Методы свойства IADs

Методы свойств интерфейса [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) получают или задают свойства, описанные в следующей таблице. Дополнительные сведения о методах свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**Действитель**
</dt> <dd> <dl>

Строка ADsPath этого объекта. Строка уникально идентифицирует этот объект в сетевой среде. Объект всегда может быть получен с помощью этого пути.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsPath(
  [out] BSTR* pbstrADsPath
);
```


</dt> </dl> </dd> <dt>

**Класс**
</dt> <dd> <dl>

Имя класса схемы объекта.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Class(
  [out] BSTR* pbstrClass
);
```


</dt> </dl> </dd> <dt>

**GUID**
</dt> <dd> <dl>

Глобальный уникальный идентификатор объекта каталога. Интерфейс [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) преобразует **идентификатор GUID** из строки октета, которая хранится на сервере каталогов, в строковом формате.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GUID(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> <dt>

**Имя**
</dt> <dd> <dl>

Относительное имя объекта, именованное в базовой службе каталогов. Это имя отличает этот объект от его одноуровневых элементов.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
```


</dt> </dl> </dd> <dt>

**Родительский объект**
</dt> <dd> <dl>

Строка ADsPath родительского контейнера. Active Directory не допускают формирования ADsPath для данного объекта путем сцепления свойств **Parent** и **Name** . Хотя эта операция может работать в некоторых поставщиках, не гарантируется, что она будет работать для всех реализаций. Значение ADsPath гарантированно является допустимым и всегда должно использоваться для получения указателя интерфейса объекта.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parent(
  [out] BSTR* pbstrParent
);
```


</dt> </dl> </dd> <dt>

**Схема**
</dt> <dd> <dl>

Строка ADsPath объекта класса схемы данного объекта.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Schema(
  [out] BSTR* pbstrSchema
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Remarks

В Active Directory **идентификатор GUID** , возвращенный из GUID, является строкой шестнадцатеричного числа. Используйте результирующий **идентификатор GUID** для непосредственной привязки к объекту.


```VB
Dim x As IADs
Set x = GetObject("LDAP://servername/<GUID=xxx>")
```



где XXX — значение, возвращаемое свойством GUID. Дополнительные сведения см. в разделе [Использование objectGUID для привязки к объекту](/windows/desktop/AD/using-objectguid-to-bind-to-an-object). Имейте в виду, что при использовании идентификатора GUID для привязки к объекту метод свойства **ADsPath** возвращает значения, отличные от обычных значений, которые будут возвращаться, если для привязки к тому же объекту использовалось различающееся имя (DN). Например, в следующей таблице перечислены значения, возвращаемые при использовании двух различных методов привязки для привязки к одному и тому же объекту пользователя.



|             | Привязка с помощью DN                                           | Привязка с использованием идентификатора GUID                                             |
|-------------|---------------------------------------------------------|-------------------------------------------------------------|
| **Имя**    | CN = Джефф Иванов                                           | CN = Джефф Иванов                                               |
| **Родительский объект**  | LDAP://server/CN=Users,DC=Fabrikam,DC=com               | LDAP://server/CN=Users,DC=Fabrikam,DC=com                   |
| **Действитель** | LDAP://server/CN=Jeff Смит, CN = Users, DC = Fabrikam, DC = com | LDAP://server/<GUID = c0f59dfcf507d311a99e0000f879f7c7> |



 

> [!Note]  
> Поставщик WinNT не поддерживает привязку с использованием **идентификатора GUID** объекта и возвращает свойство **GUID** в слегка другом строковом формате.

 

## <a name="examples"></a>Примеры

В следующем примере кода показано, как получить данные объекта с помощью методов свойств интерфейса [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) .


```VB
Dim x As IADs
Dim parent As IADsContainer
Dim cls As IADsClass
Dim op As Variant

On Error GoTo Cleanup

Set x = GetObject("WinNT://Fabrikam/Administrator")
Debug.Print "Object Name: " & x.Name
Debug.Print "Object Path: " & x.ADsPath
Debug.Print "Object Class: " & x.Class
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Debug.Print "Class Name is: " & cls.Name
For Each op In cls.OptionalProperties
    Debug.Print "Optional Property: " & op
Next op

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
    Set parent = Nothing
    Set cls = Nothing
```



В следующем примере кода показано, как получить данные объекта с помощью методов свойств интерфейса [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) .


```VB
<HTML>
<head><title></title></head>

<body>
<%
Dim x 
On Error Resume Next
 
Set x = GetObject("WinNT://Fabrikam/Administrator")
Response.Write "Object Name: " & x.Name & "<br>"
Response.Write "Object Path: " & x.ADsPath & "<br>"
Response.Write "Object Class: " & x.Class & "<br>"
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Response.Write "Class Name is: " & cls.Name & "<br>"
For Each op In cls.OptionalProperties
    Response.Write "Optional Property: " & op & "<br>"
Next op
%>

</body>
</html>
```



В следующем примере кода показано, как работать со методами свойств интерфейса [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) .


```C++
#include <stdio.h>
#include <activeds.h>
 
int main(int argc, char* argv[])
{
    IADs *pADs = NULL;
    IADsUser *pADsUser = NULL;
    IADsClass *pCls = NULL;
    CComBSTR sbstr;
 
    HRESULT hr = CoInitialize(NULL);
    if (hr != S_OK) { return 0; }
 
    hr=ADsGetObject(L"WinNT://Fabrikam/Administrator",
                IID_IADsUser,
                (void**) &pADsUser);
    if (hr != S_OK) { goto Cleanup; }
 
    hr = pADsUser->QueryInterface(IID_IADs, (void**) &pADs);
    if( hr !=S_OK) { goto Cleanup;}
 
    pADsUser->Release();
 
    if( S_OK == pADs->get_Name(&sbstr) ) {
        printf("Object Name: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_ADsPath(&sbstr) ) {
        printf("Object path: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_Class(&sbstr) ) {
        printf("Object class: %S\n",sbstr);
    }
 
    hr = pADs->get_Schema(&sbstr);
    if ( hr != S_OK) {goto Cleanup;}
 
    hr = ADsGetObject(sbstr,IID_IADsClass, (void**)&pCls);
    if ( hr != S_OK) {goto Cleanup;}
    if( S_OK == pCls->get_Name(&sbstr) ) {
        printf("Class name is %S\n", sbstr);
    }
 
 Cleanup:
    if(pADs)
        pADs->Release();

    if(pIADsUser)
        pADsUser->Release();

    if(IADsClass)
        pADsClass->Release();

    CoUninitialize();

    if(hr==S_OK)
    {
        return 1;
    }
    else
    {
        return 0;
    }
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iAds определяется как FD8256D0-FD15-11CE-ABC4-02608C9E7553<br/>                 |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> </dl>

 

