---
title: Методы свойств Иадссекуритидескриптор (iAds. h)
description: Методы свойств интерфейса Иадссекуритидескриптор получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: e0c50740-de98-4913-b3df-6fd53263bcc8
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадссекуритидескриптор ADSI
topic_type:
- apiref
api_name:
- IADsSecurityDescriptor Property Methods
- IADsSecurityDescriptor.Revision
- IADsSecurityDescriptor.get_Revision
- IADsSecurityDescriptor.put_Revision
- IADsSecurityDescriptor.Control
- IADsSecurityDescriptor.get_Control
- IADsSecurityDescriptor.put_Control
- IADsSecurityDescriptor.Owner
- IADsSecurityDescriptor.get_Owner
- IADsSecurityDescriptor.put_Owner
- IADsSecurityDescriptor.OwnerDefaulted
- IADsSecurityDescriptor.get_OwnerDefaulted
- IADsSecurityDescriptor.put_OwnerDefaulted
- IADsSecurityDescriptor.Group
- IADsSecurityDescriptor.get_Group
- IADsSecurityDescriptor.put_Group
- IADsSecurityDescriptor.GroupDefaulted
- IADsSecurityDescriptor.get_GroupDefaultedY
- IADsSecurityDescriptor.put_GroupDefaulted
- IADsSecurityDescriptor.DiscretionaryAcl
- IADsSecurityDescriptor.get_DiscretionaryAcl
- IADsSecurityDescriptor.put_DiscretionaryAcl
- IADsSecurityDescriptor.DaclDefaulted
- IADsSecurityDescriptor.get_DaclDefaulted
- IADsSecurityDescriptor.put_DaclDefaulted
- IADsSecurityDescriptor.SystemAcl
- IADsSecurityDescriptor.get_SystemAcl
- IADsSecurityDescriptor.put_SystemAcl
- IADsSecurityDescriptor.SaclDefaulted
- IADsSecurityDescriptor.get_SaclDefaulted
- IADsSecurityDescriptor.put_SaclDefaulted
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a795195af94e248f304747ba7edcf4f7a55e11e051e1cb66937242de1d732bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427630"
---
# <a name="iadssecuritydescriptor-property-methods"></a>Методы свойств Иадссекуритидескриптор

Методы свойств интерфейса [**иадссекуритидескриптор**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) получают или задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**Управление**
</dt> <dd> <dl>

Флаги, которые соответствуют значению дескриптора безопасности. Значения берутся из структуры [**\_ \_ управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) Win32.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Control(
  [out] LONG* plControl
);
HRESULT put_Control(
  [in] LONG lControl
);
```


</dt> </dl> </dd> <dt>

**даклдефаултед**
</dt> <dd> <dl>

Флаг типа BOOL, который указывает, является ли список DACL производным от механизма по умолчанию, а не явно предоставленным исходным поставщиком дескриптора безопасности. Например, если создатель объекта не указывает DACL, объект получает DACL по умолчанию от маркера доступа создателя. Этот флаг может повлиять на то, как система рассматривает DACL, по отношению к наследованию ACE. система пропускает этот флаг, если \_ \_ не установлен флаг присутствия SE DACL.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant \_ bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DaclDefaulted(
  [out] VARIANT_BOOL* fDaclDefaulted
);
HRESULT put_DaclDefaulted(
  [in] VARIANT_BOOL fDaclDefaulted
);
```


</dt> </dl> </dd> <dt>

**дискретионарякл**
</dt> <dd> <dl>

Избирательный список управления доступом (DACL), указывающий типы доступа, предоставленные объекту для указанных пользователей и групп. Дополнительные сведения о списках DACL см. в разделе пустые [списки DACL и пустой список DACL](/windows/desktop/AD/null-dacls-and-empty-dacls).

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **IDispatch**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DiscretionaryAcl(
  [out] IDispatch** ppIDispDACL
);
HRESULT put_DiscretionaryAcl(
  [in] IDispatch* pIDispDACL
);
```


</dt> </dl> </dd> <dt>

**Группа**
</dt> <dd> <dl>

Группа, которой принадлежит идентификатор безопасности владельца.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Group(
  [out] BSTR* pbstrGroupl
);
HRESULT put_Group(
  [in] BSTR bstrGroup
);
```


</dt> </dl> </dd> <dt>

**граупдефаултед**
</dt> <dd> <dl>

Флаг типа BOOL, указывающий, являются ли данные группы производными от механизма по умолчанию, а не явно предоставленными исходным поставщиком дескриптора безопасности.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant \_ bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GroupDefaultedY(
  [out] VARIANT_BOOL* fGroupDefaulted
);
HRESULT put_GroupDefaulted(
  [in] VARIANT_BOOL fGroupDefaulted
);
```


</dt> </dl> </dd> <dt>

**Владелец**
</dt> <dd> <dl>

Владелец объекта.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwnerl
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

**овнердефаултед**
</dt> <dd> <dl>

Флаг типа BOOL, указывающий, что данные владельца являются производными от механизма по умолчанию, а не предоставляются явным образом исходным поставщиком дескриптора безопасности.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant \_ bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OwnerDefaulted(
  [out] VARIANT_BOOL* fOwnerDefaulted
);
HRESULT put_OwnerDefaulted(
  [in] VARIANT_BOOL fOwnerDefaulted
);
```


</dt> </dl> </dd> <dt>

**Редакции**
</dt> <dd> <dl>

Уровень редакции дескриптора безопасности. Это значение берется из структуры [**\_ \_ информации о редакции ACL**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) Win32. Все ACE в списке ACL должны иметь одинаковый уровень редакции.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Revision(
  [out] LONG* plRevision
);
HRESULT put_Revision(
  [in] LONG lRevision
);
```


</dt> </dl> </dd> <dt>

**саклдефаултед**
</dt> <dd> <dl>

Флаг типа BOOL, указывающий, что список SACL является производным от механизма по умолчанию, а не явно предоставленным исходным поставщиком дескриптора безопасности. Этот флаг может влиять на то, как система обрабатывает список SACL по отношению к наследованию ACE. система пропускает этот флаг, если \_ \_ флаг присутствия SE SACL не установлен.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant \_ bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SaclDefaulted(
  [out] VARIANT_BOOL* fSaclDefaulted
);
HRESULT put_SaclDefaulted(
  [in] VARIANT_BOOL fSaclDefaulted
);
```


</dt> </dl> </dd> <dt>

**системакл**
</dt> <dd> <dl>

Системный список управления доступом, используемый для создания записей аудита для объекта.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **IDispatch**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SystemAcl(
  [out] IDispatch** ppIDispSACL
);
HRESULT put_SystemAcl(
  [in] IDispatch* pIDispSACL
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Примеры

В следующем примере кода показано, как перечислить существующий дескриптор безопасности.


```VB
Dim ou As IADs
Dim sd As IADsSecurityDescriptor
Dim dacl As IADsAccessControlList
Dim sacl As IADsAccessControlList

On Error GoTo Cleanup 
 
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set sd = ou.Get("ntSecurityDescriptor")
Debug.Print sd.Owner
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
Set dacl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
' Add code to perform an operation with the Discretionary and System ACLs.

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
    Set sd = Nothing
    Set dacl = Nothing
    Set sacl = Nothing
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Заголовок<br/>                   | <dl> <dt>IAds. h</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>   |
| IID<br/>                      | IID \_ иадссекуритидескриптор определен как B8C787CA-9BDD-11D0-852C-00C04FD8D503<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> </dl>

 

