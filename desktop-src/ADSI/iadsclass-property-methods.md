---
title: Методы свойств Иадскласс (iAds. h)
description: Методы свойств интерфейса Иадскласс получают или устанавливают следующие свойства. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 191f6873-c4bd-4e71-9d23-478454b7cec2
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадскласс ADSI
topic_type:
- apiref
api_name:
- IADsClass Property Methods
- IADsClass.Abstract
- IADsClass.get_Abstract
- IADsClass.put_Abstract
- IADsClass.AuxDerivedFrom
- IADsClass.get_AuxDerivedFrom
- IADsClass.put_AuxDerivedFrom
- IADsClass.Auxiliary
- IADsClass.get_Auxiliary
- IADsClass.put_Auxiliary
- IADsClass.CLSID
- IADsClass.get_CLSID
- IADsClass.put_CLSID
- IADsClass.Container
- IADsClass.get_Container
- IADsClass.put_Container
- IADsClass.Containment
- IADsClass.get_Containment
- IADsClass.put_Containment
- IADsClass.DerivedFrom
- IADsClass.get_DerivedFrom
- IADsClass.put_DerivedFrom
- IADsClass.HelpFileContext
- IADsClass.get_HelpFileContext
- IADsClass.put_HelpFileContext
- IADsClass.HelpFileName
- IADsClass.get_HelpFileName
- IADsClass.put_HelpFileName
- IADsClass.MandatoryProperties
- IADsClass.get_MandatoryProperties
- IADsClass.put_MandatoryProperties
- IADsClass.NamingProperties
- IADsClass.get_NamingProperties
- IADsClass.put_NamingProperties
- IADsClass.OID
- IADsClass.get_OID
- IADsClass.put_OID
- IADsClass.OptionalProperties
- IADsClass.get_OptionalProperties
- IADsClass.put_OptionalProperties
- IADsClass.PossibleSuperiors
- IADsClass.get_PossibleSuperiors
- IADsClass.put_PossibleSuperiors
- IADsClass.PrimaryInterface
- IADsClass.get_PrimaryInterface
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8640c6a1d1f12ef959530b72618a503245992fae791dce4e6b9e9aec05bcb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428303"
---
# <a name="iadsclass-property-methods"></a>Методы свойств Иадскласс

Методы свойств интерфейса [**иадскласс**](/windows/desktop/api/Iads/nn-iads-iadsclass) получают или устанавливают следующие свойства. Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**Аннотация**
</dt> <dd> <dl>

Логическое значение, указывающее, является ли этот класс абстрактным или неабстрактным. Если **значение равно true**, этот класс является абстрактным и не может быть создан напрямую в службе каталогов. Абстрактные классы могут использоваться только как классы суперклассов.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **логическое значение**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Abstract(
  [out] BOOLEAN* pbAbstract
);
HRESULT put_Abstract(
  [in] BOOLEAN bAbstract
);
```


</dt> </dl> </dd> <dt>

**ауксдериведфром**
</dt> <dd> <dl>

Массив ADsPath строк, указывающий классы Super, от которых наследует этот класс.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AuxDerivedFrom(
  [out] VARIANT* pvAuxDerivedFrom
);
HRESULT put_AuxDerivedFrom(
  [in] VARIANT vAuxDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**Четки**
</dt> <dd> <dl>

Логическое значение, указывающее, является ли этот класс вспомогательным. Если **значение равно true**, этот класс является вспомогательным классом и не может быть создан напрямую в службе каталогов. Вспомогательные классы могут использоваться только как суперклассы других вспомогательных классов или как источник дополнительных свойств в структурных классах.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **логическое значение**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Auxiliary(
  [out] BOOLEAN* pbAuxiliary
);
HRESULT put_Auxiliary(
  [in] BOOLEAN bAuxiliary
);
```


</dt> </dl> </dd> <dt>

**ЭТОМУ**
</dt> <dd> <dl>

Необязательный CLSID, зависящий от поставщика, определяющий COM-объект, реализующий этот класс.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CLSID(
  [out] BSTR* pbstrCLSID
);
HRESULT put_CLSID(
  [in] BSTR bstrCLSID
);
```


</dt> </dl> </dd> <dt>

**Контейнер**
</dt> <dd> <dl>

Логическое значение, указывающее, может ли этот класс быть контейнером других классов объектов. Если это значение равно **true**, можно вызвать метод **Get \_ Container** , чтобы получить массив классов объектов, которые может содержать этот класс.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **логическое значение**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Container(
  [out] BOOLEAN* pbContainer
);
HRESULT put_Container(
  [in] BOOLEAN bContainer
);
```


</dt> </dl> </dd> <dt>

**Containment**
</dt> <dd> <dl>

Массив **BSTR** , в котором каждый элемент является именем класса объекта, который может содержать этот класс.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Containment(
  [out] VARIANT* pvContainment
);
HRESULT put_Containment(
  [in] VARIANT vContainment
);
```


</dt> </dl> </dd> <dt>

**дериведфром**
</dt> <dd> <dl>

Массив ADsPath строк, указывающий, из каких классов этот класс был производным.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DerivedFrom(
  [out] VARIANT* pvDerivedFrom
);
HRESULT put_DerivedFrom(
  [in] VARIANT vDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**хелпфилеконтекст**
</dt> <dd> <dl>

Идентификатор контекста в **хелпфиленаме** , где можно найти конкретные сведения для этого класса.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileContext(
  [out] long* plHelpContext
);
HRESULT put_HelpFileContext(
  [in] long lHelpContext
);
```


</dt> </dl> </dd> <dt>

**хелпфиленаме**
</dt> <dd> <dl>

Имя файла справки, в котором содержатся дополнительные сведения об объектах этого класса.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileName(
  [out] BSTR* pbstrHelpFileName
);
HRESULT put_HelpFileName(
  [in] BSTR bstrHelpFileName
);
```


</dt> </dl> </dd> <dt>

**мандаторипропертиес**
</dt> <dd> <dl>

**SAFEARRAY** типа **Variant**, в котором перечислены свойства, которые должны быть заданы для записи этого класса в хранилище. Если класс содержит только одно свойство, **Get \_ мандаторипропертиес** будет возвращать **BSTR**.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MandatoryProperties(
  [out] VARIANT* pvarMandatoryProperties
);
HRESULT put_MandatoryProperties(
  [in] VARIANT varMandatoryProperties
);
```


</dt> </dl> </dd> <dt>

**намингпропертиес**
</dt> <dd> <dl>

**Массив SafeArray** типа **BSTR**, в котором перечислены свойства, используемые для именования атрибутов этого класса схемы.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamingProperties(
  [out] VARIANT* pvarNamingProperties
);
HRESULT put_NamingProperties(
  [in] VARIANT varNamingProperties
);
```


</dt> </dl> </dd> <dt>

**КОДА**
</dt> <dd> <dl>

Идентификатор объекта, зависящий от поставщика, который определяет этот класс. Это обеспечивает расширение схемы с помощью Active Directory в службах каталогов, для которых требуются OID, зависящие от поставщика, для классов.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* pbstrOID
);
HRESULT put_OID(
  [in] BSTR bstrOID
);
```


</dt> </dl> </dd> <dt>

**OptionalProperties**
</dt> <dd> <dl>

**SAFEARRAY** типа **Variant**, в котором перечислены необязательные свойства данного класса схемы. Если класс содержит только одно свойство, **Get \_ OptionalProperties** будет возвращать **BSTR**.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OptionalProperties(
  [out] VARIANT* pvarOptionalProperties
);
HRESULT put_OptionalProperties(
  [in] VARIANT varOptionalProperties
);
```


</dt> </dl> </dd> <dt>

**поссиблесупериорс**
</dt> <dd> <dl>

Массив ADsPath строк, указывающий классы схемы, которые могут содержать экземпляры этого класса.

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PossibleSuperiors(
  [out] VARIANT* pvSuperiors
);
HRESULT put_PossibleSuperiors(
  [in] VARIANT vSuperiors
);
```


</dt> </dl> </dd> <dt>

**примаринтерфаце**
</dt> <dd> <dl>

Необязательный идентификатор GUID идентификатора, зависящего от поставщика, который связывает интерфейс с объектами этого класса схемы. Например, класс User, который поддерживает [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) и **примаринтерфаце** , определяется с помощью **IID \_ IADsUser**. Он должен иметь стандартный строковый формат GUID в соответствии с определением в COM. Этот идентификатор GUID представляет собой значение, которое отображается в свойстве [**iAds:: Get \_ GUID**](/windows/desktop/api/Iads/nn-iads-iads) в экземплярах этого класса для поставщиков, реализующих это свойство. Определение класса схемы по идентификатору IID основного интерфейса кода класса позволяет использовать **QueryInterface** во время выполнения, чтобы определить, имеет ли объект нужный класс.

<dt>

Тип доступа: только для чтения
</dt> <dt>

Тип данных скрипта: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryInterface(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Примеры

В следующем примере кода показано, как использовать интерфейс [**иадскласс**](/windows/desktop/api/Iads/nn-iads-iadsclass) , чтобы определить, может ли объект быть контейнером, и, если да, выводит список имен всех содержащихся объектов.


```VB
Dim ads As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(ads.Schema)
if cls.Container = True Then
    MsgBox "This object contains the following children:"
    For Each o In cls.Containment
        MsgBox o
    Next
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
```



В следующем примере кода показано, как использовать интерфейс [**иадскласс**](/windows/desktop/api/Iads/nn-iads-iadsclass) , чтобы определить, может ли объект быть контейнером, и, если да, выводит список имен всех содержащихся объектов.


```C++
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs = NULL;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) {goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) {goto Cleanup;}
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) {goto Cleanup;}
 
VariantInit(&var);
VARIANT_BOOL bCont;
pCls->get_Container(&bCont);
if(bCont != false) {
    VariantClear(&var);
    pCls->get_Containment(&var);
    hr = printVarArray(var);
}

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    SysFreeString(bstrSchema);
    CoUninitialize();
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадскласс определен как C8F93DD0-4ae0-11CF-9E73-00AA004A5691<br/>            |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иадскласс**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**Иадскласс:: квалификаторы**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers)
</dt> </dl>

 

 





