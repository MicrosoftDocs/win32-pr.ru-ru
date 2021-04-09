---
description: Свойство Path \_ объекта свбемластеррор возвращает объект свбемобжектпас, представляющий путь к объекту текущего класса или экземпляра. Это свойство можно передать в качестве параметра методам, которым требуется путь к объекту.
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: Свойство SWbemLastError.Path_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Path_
- ISWbemLastError.Path_
- ISWbemLastError.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c979fd76ffb4ee97f62362d53fac4151de17bae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081002"
---
# <a name="swbemlasterrorpath_-property"></a>Свбемластеррор. Path, \_ свойство

Свойство **path \_** объекта [**свбемластеррор**](swbemlasterror.md) возвращает объект [**свбемобжектпас**](swbemobjectpath.md) , представляющий путь к объекту текущего класса или экземпляра. Это свойство можно передать в качестве параметра методам, которым требуется путь к объекту.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Можно изменить только свойство [**Class**](swbemobjectpath-class.md) возвращаемого экземпляра [**свбемобжектпас**](swbemobjectpath.md) . При попытке изменить любое другое свойство или попытаться вызвать методы [**сетаскласс**](swbemobjectpath-setasclass.md) или [**Сетассинглетон**](swbemobjectpath-setassingleton.md) возникает ошибка **вбемеррреадонли**.

Поэтому нельзя изменить объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который является значением свойства [**Keys**](swbemobjectpath-keys.md) возвращаемого экземпляра [**свбемобжектпас**](swbemobjectpath.md) . При попытке вызова метода [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)или [**DeleteAll**](swbemnamedvalueset-deleteall.md) для этого значения возникает ошибка **вбемеррреадонли** . Кроме того, нельзя изменить любые [**свбемнамедвалуе**](swbemnamedvalue.md) , полученные из этой коллекции. Попытки изменить свойство [**value**](swbemnamedvalue-value.md) возвращают тот же код ошибки.

Однако при вызове [**SWbemObject. Clone \_**](swbemobject-clone-.md) для создания копии свойство [**path \_**](swbemobject-path-.md) копии будет полностью изменяемым.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМЛАСТЕРРОР CLSID<br/>                                                        |
| IID<br/>                      | IID \_ исвбемластеррор<br/>                                                         |



 

 




