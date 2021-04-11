---
description: Свойство Path \_ объекта SWbemObject возвращает объект свбемобжектпас, представляющий путь к объекту текущего класса или экземпляра. Это свойство можно передать в качестве параметра методам, которым требуется путь к объекту.
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.tgt_platform: multiple
title: Свойство SWbemObject.Path_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Path_
- ISWbemObject.Path_
- ISWbemObject.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 773f6f9bb04aa31290bc351550a45d849d74e06f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265181"
---
# <a name="swbemobjectpath_-property"></a>SWbemObject. Path, \_ свойство

Свойство **path \_** объекта [**SWbemObject**](swbemobject.md) возвращает объект [**свбемобжектпас**](swbemobjectpath.md) , представляющий путь к объекту текущего класса или экземпляра. Это свойство можно передать в качестве параметра методам, которым требуется путь к объекту.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
SWbemObject.Path_ As Object
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Можно изменить только свойство [**Class**](swbemobjectpath-class.md) возвращаемого экземпляра [**свбемобжектпас**](swbemobjectpath.md) . Если вы попытаетесь изменить какое-либо другое свойство или попытаетесь вызвать методы [**сетаскласс**](swbemobjectpath-setasclass.md) или [**сетассинглетон**](swbemobjectpath-setassingleton.md), вы получите ошибку **вбемеррреадонли** .

Поэтому нельзя изменить объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который является значением свойства [**Keys**](swbemobjectpath-keys.md) возвращаемого экземпляра [**свбемобжектпас**](swbemobjectpath.md) . Если вы попытаетесь вызвать методы [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)или [**DeleteAll**](swbemnamedvalueset-deleteall.md) для этого значения, вы получите ошибку вбемеррреадонли. Кроме того, нельзя изменить любые [**свбемнамедвалуе**](swbemnamedvalue.md) , полученные из этой коллекции. Попытки изменить свойство **value** возвращают тот же код ошибки.

Однако при вызове [**SWbemObject. Clone \_**](swbemobject-clone-.md) для создания копии свойство [**свбемобжектпас. Path**](swbemobjectpath-path.md) копии становится полностью изменяемым.

## <a name="examples"></a>Примеры

Следующий пример кода, взятый из [списка всех классов WMI cimV2](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) в коллекции TechNet, использует \_ свойство Path для ПЕРЕЧИСЛЕНИЯ всех классов WMI cimV2.


```VB
strComputer = "." 
Set objWMIService=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\root\cimv2") 
  
For Each objclass in objWMIService.SubclassesOf() 
    Wscript.Echo objClass.Path_.Class 
Next 
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | IID \_ исвбемобжект<br/>                                                            |



 

 




