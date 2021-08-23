---
description: Возвращает объект SWbemPropertySet, содержащий коллекцию системных свойств WMI, которые применяются к объекту.
ms.assetid: e95c325a-8851-4f55-a99d-4346d064e308
ms.tgt_platform: multiple
title: Свойство SWbemObjectEx.SystemProperties_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.SystemProperties_
- ISWbemObjectEx.SystemProperties_
- ISWbemObjectEx.get_SystemProperties_
- ISWbemObjectEx.put_SystemProperties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 23de364e4616b7b7c2ac6b7de6daaf42edfd73e2e7b3920f7ac3b84b7a59bde5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857334"
---
# <a name="swbemobjectexsystemproperties_-property"></a>SWbemObjectEx.Sys, \_ свойство темпропертиес

Свойство **системпропертиес \_** объекта [**свбемобжектекс**](swbemobjectex.md) возвращает объект [**SWbemPropertySet**](swbempropertyset.md) , содержащий коллекцию [системных свойств WMI](wmi-system-properties.md) , которые применяются к объекту.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
SWbemObjectEx.SystemProperties_ As Object
```



## <a name="property-value"></a>Значение свойства

## <a name="examples"></a>Примеры

В следующем примере кода извлекаются значения свойств для \_ класса процесса Win32.


```VB
Set objWmi = GetObject ("winmgmts:root\cimv2")
Set objClass = objWmi.Get("Win32_Process")

' SWbemObjectEx.SystemProperties_ returns 
' an SWbemPropertySet object that contains the collection
' of sytem properties for Win32_Process class

For Each objProperty In objClass.SystemProperties_

    WScript.Echo vbCrLf & objProperty.Name & ":"

    ' Have to take into account that
    ' __Derivation is an array

    If Not objProperty.IsArray Then
        WScript.Echo vbTab & objProperty.Value
    Else
        For Each strValue In objProperty.Value
            WScript.Echo vbTab & strValue
        Next
    End If

Next
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМОБЖЕКТЕКС CLSID<br/>                                                         |
| IID<br/>                      | IID \_ исвбемобжектекс<br/>                                                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**свбемобжектекс**](swbemobjectex.md)
</dt> </dl>

 

 




