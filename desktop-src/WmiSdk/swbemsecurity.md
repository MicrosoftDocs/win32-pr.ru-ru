---
description: Объект Свбемсекурити Возвращает или задает параметры безопасности, такие как привилегии, олицетворения COM и уровни проверки подлинности, назначенные объекту.
ms.assetid: 794587fa-5feb-455b-be28-ecfaa25625ad
ms.tgt_platform: multiple
title: Объект Свбемсекурити (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity
- ISWbemSecurity
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: da59c3b996a80384c133336503124141f0907f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662729"
---
# <a name="swbemsecurity-object"></a>Объект Свбемсекурити

Объект **свбемсекурити** Возвращает или задает параметры безопасности, такие как привилегии, олицетворения COM и уровни проверки подлинности, назначенные объекту. Объекты [**SWbemLocator**](swbemlocator.md), [**SwbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**свбемобжектпас**](swbemobjectpath.md), [**свбемластеррор**](swbemlasterror.md)и [**свбемевентсаурце**](swbemeventsource.md) имеют свойство **безопасности \_** , которое является объектом **свбемсекурити** . При получении экземпляра или просмотре журнала безопасности WMI может потребоваться задать свойства объекта **безопасности \_** .

Вызов функции [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) VBScript не может создать объект безопасности. Параметры безопасности в этом объекте не указывают параметры проверки подлинности, олицетворения или привилегии для соединения с WMI или безопасность, действующая для прокси-сервера, когда объект доставляется в приемник при асинхронном вызове. Дополнительные сведения см. в разделе [обслуживание безопасности WMI](maintaining-wmi-security.md).

## <a name="members"></a>Элементы

Объект **свбемсекурити** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Объект **свбемсекурити** имеет следующие свойства.



| Свойство                                                                    | Тип доступа           | Описание                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аусентикатионлевел**](swbemsecurity-authenticationlevel.md)<br/> | Чтение/запись<br/> | Числовое значение, определяющее уровень проверки подлинности COM, назначенный этому объекту. Этот параметр определяет, как вы защищаете данные, отправляемые из WMI.<br/>                                                                 |
| [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md)<br/>   | Чтение/запись<br/> | Числовое значение, определяющее уровень олицетворения COM, назначенный этому объекту. Этот параметр определяет, могут ли процессы, которыми владеет WMI, обнаруживать или использовать учетные данные безопасности при вызове других процессов.<br/> |
| [**Права**](swbemsecurity-privileges.md)<br/>                   | Только для чтения<br/>  | Объект [**свбемпривилежесет**](swbemprivilegeset.md) , определяющий привилегии для этого объекта. Дополнительные сведения см. [в разделе выполнение с особыми привилегиями](/windows/desktop/SecBP/running-with-special-privileges).<br/>                    |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМСЕКУРИТИ CLSID<br/>                                                         |
| IID<br/>                      | IID \_ исвбемсекурити<br/>                                                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> <dt>

[Поддержание безопасности WMI](maintaining-wmi-security.md)
</dt> <dt>

[Настройка \_ \_ безопасности процесса клиентского приложения](setting-client-application-process-security.md)
</dt> <dt>

[**вбемаусентикатионлевеленум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**вбемимперсонатионлевеленум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> </dl>

 

