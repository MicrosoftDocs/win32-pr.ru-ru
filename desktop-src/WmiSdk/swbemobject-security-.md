---
description: Свойство безопасности \_ объекта SWbemObject используется для чтения или установки параметров безопасности для объекта SWbemObject.
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: Свойство SWbemObject.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Security_
- ISWbemObject.Security_
- ISWbemObject.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d83a155057e445848e727615978c3414e96f63334ffc70c78d5f055a396b53f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313788"
---
# <a name="swbemobjectsecurity_-property"></a>SWbemObject. Security, \_ свойство

Свойство **безопасности \_** объекта [**SWbemObject**](swbemobject.md) используется для чтения или установки параметров безопасности для объекта **SWbemObject** . Это свойство является объектом [**свбемсекурити**](swbemsecurity.md) . параметры безопасности в этом объекте не указывают параметры проверки подлинности, олицетворения или привилегии, сделанные для подключения к инструментарий управления Windows (WMI) (WMI), или безопасность, действующая для прокси-сервера, когда объект доставляется в приемник при асинхронном вызове. Дополнительные сведения см. в разделе [обслуживание безопасности WMI](maintaining-wmi-security.md).

> [!Note]  
> Установка свойства **безопасности \_** объекта [**SWbemObject**](swbemobject.md) в **значение NULL** предоставляет всем всем времени неограниченный доступ. Дополнительные сведения см. в разделе [**свбемсекурити**](swbemsecurity.md).

 

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
SWbemObject.Security_ As Object
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
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | IID \_ исвбемобжект<br/>                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[Создание приложения или скрипта WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Настройка \_ \_ безопасности процесса клиентского приложения](setting-client-application-process-security.md)
</dt> <dt>

[**свбемсекурити**](swbemsecurity.md)
</dt> <dt>

[**вбемаусентикатионлевеленум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**вбемимперсонатионлевеленум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Константы прав доступа**](privilege-constants.md)
</dt> </dl>

 

 




