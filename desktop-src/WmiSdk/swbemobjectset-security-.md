---
description: Свойство безопасности \_ объекта SWbemObjectSet используется для получения или задания параметров безопасности для объекта SWbemObjectSet. Это свойство является объектом Свбемсекурити.
ms.assetid: ee2ad6d5-c0aa-4510-ba1b-4a152d56011f
ms.tgt_platform: multiple
title: Свойство SWbemObjectSet.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Security_
- ISWbemObjectSet.Security_
- ISWbemObjectSet.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690c5c23a40ed3333468beeeab8ccc1f8c9a6ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701945"
---
# <a name="swbemobjectsetsecurity_-property"></a>SWbemObjectSet. Security, \_ свойство

Свойство **безопасности \_** объекта [**SWbemObjectSet**](swbemobjectset.md) используется для получения или задания параметров безопасности для объекта **SWbemObjectSet** . Это свойство является объектом [**свбемсекурити**](swbemsecurity.md) .

> [!Note]  
> Установка свойства [**безопасности \_**](swbemobject-security-.md) объекта [**SWbemObjectSet**](swbemobjectset.md) в **значение NULL** предоставляет всем пользователям неограниченный доступ. Дополнительные сведения о влиянии неограниченного доступа см. в разделе [**свбемсекурити**](swbemsecurity.md).

 

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
SWbemObjectSet.Security_ As Object
```



## <a name="property-value"></a>Значение свойства

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTSET CLSID<br/>                                                        |
| IID<br/>                      | IID \_ исвбемобжектсет<br/>                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**SWbemObjectSet**](swbemobjectset.md)
</dt> <dt>

[Создание приложения или скрипта WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Защита клиентов скриптов](securing-scripting-clients.md)
</dt> </dl>

 

 




