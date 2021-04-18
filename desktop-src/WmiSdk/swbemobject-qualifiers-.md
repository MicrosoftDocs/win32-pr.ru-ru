---
description: Свойство квалификаторов \_ объекта SWbemObject возвращает объект свбемкуалифиерсет, который является коллекцией квалификаторов для текущего класса или экземпляра. Это свойство доступно только для чтения.
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: Свойство SWbemObject.Qualifiers_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Qualifiers_
- ISWbemObject.Qualifiers_
- ISWbemObject.get_Qualifiers_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f9526596b7ae4a387cd0751ad95aff3b97dcc817
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711642"
---
# <a name="swbemobjectqualifiers_-property"></a>SWbemObject. квалификаторы, \_ свойство

Свойство **квалификаторов \_** объекта [**SWbemObject**](swbemobject.md) возвращает объект [**свбемкуалифиерсет**](swbemqualifierset.md) , который является коллекцией квалификаторов для текущего класса или экземпляра. Это свойство доступно только для чтения.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a>Значение свойства

## <a name="examples"></a>Примеры

[Список всех квалификаторов для](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) примера кода VBScript класса WMI в коллекции TechNet использует свойство квалификатора \_ для перечисления квалификаторов класса для указанного класса WMI.

В примере кода " [список всех абстрактных классов в инструментарии WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript" в галерее TechNet перечислены все абстрактные классы WMI, определенные в корневом \\ пространстве имен CIMV2.

В примере кода для [всех динамических классов в инструментарии WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript используется свойство квалификатора \_ для перечисления всех динамических классов WMI (включая классы ассоциаций), определенных в корневом \\ пространстве имен CIMV2.

В примере кода PowerShell [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) в галерее TechNet перечислены все записываемые свойства в указанном пространстве имен.

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



 

 




