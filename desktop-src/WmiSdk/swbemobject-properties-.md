---
description: Свойство Properties \_ объекта SWbemObject возвращает объект SWbemPropertySet, являющийся коллекцией свойств текущего класса или экземпляра. Это свойство доступно только для чтения.
ms.assetid: 8dd49678-47e7-4c6b-ab12-42532065eaf2
ms.tgt_platform: multiple
title: Свойство SWbemObject.Properties_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Properties_
- ISWbemObject.Properties_
- ISWbemObject.get_Properties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 413e13b725fce117b9358a254a860c631fc5fbe3158bf7f6d277ebca22647168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857314"
---
# <a name="swbemobjectproperties_-property"></a>SWbemObject. Properties, \_ свойство

Свойство **Properties \_** объекта [**SWbemObject**](swbemobject.md) возвращает объект [**SWbemPropertySet**](swbempropertyset.md) , являющийся коллекцией свойств текущего класса или экземпляра. Это свойство доступно только для чтения.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
SWbemObject.Properties_ As Object
```



## <a name="property-value"></a>Значение свойства

## <a name="examples"></a>Примеры

Пример кода PowerShell " [Создание скриптов класса WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) " в коллекции TechNet использует \_ свойство Properties для создания скрипта для каждого класса WMI, в котором будут ПЕРЕЧИСЛЕНЫ имя класса WMI и свойства.

Приведенный ниже код, взятый из [списка всех свойств для](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) примера кода VBScript класса WMI в коллекции TechNet, содержит список свойств для УКАЗАННОГО класса WMI.


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Properties" 
WScript.Echo "------------------------------" 
  
For Each objClassProperty In objClass.Properties_ 
    WScript.Echo objClassProperty.Name 
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
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | IID \_ исвбемобжект<br/>                                                            |



 

 




