---
title: Методы свойств Иадссинтакс (iAds. h)
description: Методы свойств интерфейса Иадссинтакс получают или задают свойства, перечисленные в следующей таблице. Дополнительные сведения о методах свойств см. в разделе методы свойств интерфейса.
ms.assetid: a216a55d-63eb-4fdf-a67f-8d4b5eb74262
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадссинтакс ADSI
topic_type:
- apiref
api_name:
- IADsSyntax Property Methods
- IADsSyntax.OleAutoDataType
- IADsSyntax.get_OleAutoDataType
- IADsSyntax.put_OleAutoDataType
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c193bba78bfe215d37bdfdedf5d45bd73f1a85606b3dab6e5a3c233cece8db18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961903"
---
# <a name="iadssyntax-property-methods"></a>Методы свойств Иадссинтакс

Методы свойств интерфейса [**иадссинтакс**](/windows/desktop/api/Iads/nn-iads-iadssyntax) получают или задают свойства, перечисленные в следующей таблице. Дополнительные сведения о методах свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**олеаутодататипе**
</dt> <dd> <dl>

Извлекает и задает значение типа **Long** , содержащее значения константы **VT \_ xxx** для типов данных автоматизации, представляющих этот синтаксис.

Active Directory поддерживает следующие константы **VT \_ xxx** для типа данных автоматизации, представляющие этот синтаксис:

-   **VT \_ логический bool**
-   **VT \_ BSTR** BSTR
-   **VT \_ BSTR, BSTR**
-   **VT \_ Валюта CY**
-   **VT \_ Дата даты**
-   **VT \_ ПУСТое** **значение NULL**
-   **VT \_** Недопустимая ошибка
-   **VT \_ I2** Short
-   **VT \_ I4** Long
-   **VT \_** Real в R4
-   **VT \_ R8** , двойной
-   **VT \_ UI1** байт

<dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OleAutoDataType(
  [out] LONG* plAutoDataType
);
HRESULT put_OleAutoDataType(
  [in] LONG lAutoDataType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Remarks

Массив неподписанных байтов, **VT \_ UI1** \| **VT \_** , может означать, что поставщик сопоставил синтаксис, который не может быть сопоставлен с виртуальным типом службы автоматизации.

## <a name="examples"></a>Примеры

В следующем примере кода рассматривается синтаксис атрибута **оператингсистемверсион** компьютера в сети с помощью поставщика WinNT. Синтаксис результата представляет собой строку.


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sy As IADsSyntax
Dim sc As IADsContainer
On Error GoTo Cleanup

Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystemVersion")
Set sy = GetObject(sc.ADsPath & "/" & pr.Syntax)
 
MsgBox "Automation data types: " & sy.OleAutoDataType

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sy = Nothing
    Set sc = Nothing
```



В следующем примере кода рассматривается синтаксис атрибута **оператингсистемверсион** компьютера в сети с помощью поставщика WinNT. Синтаксис результата представляет собой строку. Для краткости проверка ошибок пропущена.


```C++
#include <stdio.h>
#include <activeds.h>
#include <atlbase.h>
 
IADs *pObj = NULL;
IADsClass *pCls = NULL;
IADsProperty *pProp = NULL;
IADsSyntax *pSyn = NULL;
IADsContainer *pCont = NULL;
 
HRESULT hr = ADsGetObject(L"WinNT://myMachine,computer",
                          IID_IADs,
                          (void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
VARIANT var;
VariantInit(&var);
CComBSTR sbstr;
 
pObj->get_Schema(&sbstr);
printf("Object schema: %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsClass,(void**)&pCls);
if(FAILED(hr)){goto Cleanup;}

pCls->get_Parent(&sbstr);
printf("Object class's container:  %S\n", sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr)){goto Cleanup;}
pCont->QueryInterface(IID_IADs,(void**)&pObj);
pObj->get_ADsPath(&sbstr);
printf("Container's AdsPath:  %S\n",sbstr);
 
IDispatch *pDisp;
hr = pCont->GetObject(CComBSTR("Property"),
                      CComBSTR("OperatingSystemVersion"),
                      (IDispatch**)&pDisp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pDisp->QueryInterface(IID_IADsProperty, (void**)&pProp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pProp->get_Syntax(&sbstr);
if(FAILED(hr)){goto Cleanup;}
printf("Property Syntax:  %S\n",sbstr);
 
printf("ADsPath of the syntax object %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsSyntax, (void**)&pSyn);
if(FAILED(hr)){goto Cleanup;}

long lType;
pSyn->get_OleAutoDataType(&lType);
printf("Property syntax's OleAutoDataType: %d\n", lType);

Cleanup:
    if(pObj)
        pObj->Release();

    if(pProp)
        pProp->Release();

    if(pCls)
        pCls->Release();

    if(pSyn)
        pSyn->Release();

    if(pCont)
        pCont->Release();
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ иадссинтакс определен как C8F93DD2-4ae0-11CF-9E73-00AA004A5691<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иадскласс**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**иадспроперти**](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[**иадссинтакс**](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





