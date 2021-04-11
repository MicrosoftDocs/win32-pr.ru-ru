---
description: Использование API ведения журнала для родительского контроля
ms.assetid: 6c38a634-53ba-4e76-83bf-1a3f36efb0bc
title: Использование API ведения журнала для родительского контроля
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d1cedb9ff02856be6ea1ae2069d8635b980681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910187"
---
# <a name="using-logging-apis-for-parental-controls"></a>Использование API ведения журнала для родительского контроля

### <a name="activity-reporting-logging"></a>Отчеты по действиям (ведение журнала)

Файл заголовка Впцевент. h содержит определения полей для каждого предопределенного типа события действия и пользовательского типа. В этом примере кода показаны действия по записи в журнал события приглашения на беседу мгновенных сообщений с помощью API публикации ETW:


```C++
#include <windows.h>
#include <evntprov.h>
#include <wpcevent.h>

#pragma comment(lib, "advapi32.lib")

#define BYTELEN(x) ((wcslen(x) + 1) * sizeof(WCHAR))

void main()
{
    REGHANDLE hWpc = 0;

    // Register
    ULONG res = EventRegister(&WPCPROV, NULL, NULL, &hWpc);

    // Log an event
    PCWSTR pcszAppName = L"SuperIM";
    PCWSTR pcszAppVersion = L"7.0";
    PCWSTR pcszAccountName = L"Kate";
    PCWSTR pcszConvID = L"102";
    PCWSTR pcszRequestingIP = L"192.168.2.100";
    PCWSTR pcszSender = L"imperson@isp.com";
    const DWORD dwReason = WPCFLAG_ISBLOCKED_NOTBLOCKED;
    const DWORD dwRecipCount = 1;
    PCWSTR pcszRecipient = L"otherim@isp.com";

    EVENT_DATA_DESCRIPTOR eventData[WPC_ARGS_CONVERSATIONINITEVENT_CARGS];

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_APPNAME],
        (const PVOID)pcszAppName, (ULONG)BYTELEN(pcszAppName));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_APPVERSION],
        (const PVOID)pcszAppVersion,(ULONG)BYTELEN(pcszAppVersion));

    EventDataDescCreate(
        &eventData[WPC_ARGS_CONVERSATIONINITEVENT_ACCOUNTNAME], 
        (const PVOID)pcszAccountName, (ULONG)BYTELEN(pcszAccountName));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_CONVID], 
        (const PVOID)pcszConvID, (ULONG)BYTELEN(pcszConvID));

    EventDataDescCreate(
        &eventData[WPC_ARGS_CONVERSATIONINITEVENT_REQUESTINGIP], 
        (const PVOID)pcszRequestingIP, (ULONG)BYTELEN(pcszRequestingIP));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_SENDER],
        (const PVOID)pcszSender, (ULONG)BYTELEN(pcszSender));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_REASON],
        (const PVOID)&dwReason, sizeof(dwReason));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_RECIPCOUNT],
        (const PVOID)&dwRecipCount, sizeof(dwRecipCount));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_RECIPIENT],
        (const PVOID)pcszRecipient, (ULONG)BYTELEN(pcszRecipient));


    ULONG lRet = EventWrite(hWpc, &WPCEVENT_IM_INVITATION, ARRAYSIZE(eventData), eventData);

    // Unregister
    EventUnregister(hWpc);
}
```



### <a name="custom-logging"></a>Настраиваемое ведение журнала

Чтобы приложение было расширять события, регистрируемые за пределами набора предопределенных событий или одного пользовательского типа, необходимо определить поставщика для этого в манифесте приложения. Затем можно будет импортировать канал WPC по умолчанию, а также зафиксировать в нем события, определяемые приложением.

### <a name="logging-rights"></a>Права на ведение журнала

Канал ведения журнала WPC контролируется [*списком управления доступом*](/windows/desktop/SecGloss/a-gly) (ACL), чтобы обеспечить полный доступ только для администраторов. Учетные записи без прав администратора могут выполнять запись в канал, но не имеют доступа на чтение или удаление. Доступ к каналу осуществляется с помощью API ETW.

### <a name="parental-controls-logging-provider-details"></a>Сведения о поставщике ведения журнала родительского контроля

Поставщик WPC имеет имя Microsoft.com/Windows/ParentalControls с GUID {01090065-B467-4503-9B28-533766761087}. Локальный канал ведения журнала по умолчанию — Microsoft.com/Windows/ParentalControls/LocalEvents.

Файлы журнала хранятся в \\ \\ папке журналов WPC Windows System32 \\ .

### <a name="notification-of-impending-time-limits-logout"></a>Уведомление об ограничениях времени ожидания выхода из системы

Система родительского контроля запустит событие предупреждения через 15 минут и снова через 1 минуту, прежде чем выйти из контролируемого пользователя на основе временных ограничений. Приложения могут подписываться на эти события, особенно если они работают в полноэкранном режиме DirectX, где стандартные уведомления Windows не отображаются. Приведен пример кода, который показывает, как подписаться на события, зарегистрировать функцию обратного вызова и получить события.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Общие сведения о функциях расширяемости родительского контроля](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[**\_дескриптор данных \_ события**](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[**EventDataDescCreate**](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[**WPC \_ args \_ конверсатионинитевент**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 
