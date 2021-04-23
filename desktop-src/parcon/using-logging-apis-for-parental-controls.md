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
# <a name="using-logging-apis-for-parental-controls"></a><span data-ttu-id="a6703-103">Использование API ведения журнала для родительского контроля</span><span class="sxs-lookup"><span data-stu-id="a6703-103">Using Logging APIs for Parental Controls</span></span>

### <a name="activity-reporting-logging"></a><span data-ttu-id="a6703-104">Отчеты по действиям (ведение журнала)</span><span class="sxs-lookup"><span data-stu-id="a6703-104">Activity Reporting (Logging)</span></span>

<span data-ttu-id="a6703-105">Файл заголовка Впцевент. h содержит определения полей для каждого предопределенного типа события действия и пользовательского типа.</span><span class="sxs-lookup"><span data-stu-id="a6703-105">The WpcEvent.h header file contains definitions of the fields for each predefined activity event type and the custom type.</span></span> <span data-ttu-id="a6703-106">В этом примере кода показаны действия по записи в журнал события приглашения на беседу мгновенных сообщений с помощью API публикации ETW:</span><span class="sxs-lookup"><span data-stu-id="a6703-106">This sample code shows the steps for logging an instant messaging conversation invitation event using the ETW publishing API:</span></span>


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



### <a name="custom-logging"></a><span data-ttu-id="a6703-107">Настраиваемое ведение журнала</span><span class="sxs-lookup"><span data-stu-id="a6703-107">Custom Logging</span></span>

<span data-ttu-id="a6703-108">Чтобы приложение было расширять события, регистрируемые за пределами набора предопределенных событий или одного пользовательского типа, необходимо определить поставщика для этого в манифесте приложения.</span><span class="sxs-lookup"><span data-stu-id="a6703-108">For an application to extend the events logged outside the set of predefined events or the one custom type, you will need to define a provider for that in the application manifest.</span></span> <span data-ttu-id="a6703-109">Затем можно будет импортировать канал WPC по умолчанию, а также зафиксировать в нем события, определяемые приложением.</span><span class="sxs-lookup"><span data-stu-id="a6703-109">The WPC default channel can then be imported and application-defined events can then be logged.</span></span>

### <a name="logging-rights"></a><span data-ttu-id="a6703-110">Права на ведение журнала</span><span class="sxs-lookup"><span data-stu-id="a6703-110">Logging Rights</span></span>

<span data-ttu-id="a6703-111">Канал ведения журнала WPC контролируется [*списком управления доступом*](/windows/desktop/SecGloss/a-gly) (ACL), чтобы обеспечить полный доступ только для администраторов.</span><span class="sxs-lookup"><span data-stu-id="a6703-111">The WPC logging channel is controlled by [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) to provide full access for administrators only.</span></span> <span data-ttu-id="a6703-112">Учетные записи без прав администратора могут выполнять запись в канал, но не имеют доступа на чтение или удаление.</span><span class="sxs-lookup"><span data-stu-id="a6703-112">Non-administrator accounts may write to the channel but have no read or delete access.</span></span> <span data-ttu-id="a6703-113">Доступ к каналу осуществляется с помощью API ETW.</span><span class="sxs-lookup"><span data-stu-id="a6703-113">Access to the channel is by using the ETW API.</span></span>

### <a name="parental-controls-logging-provider-details"></a><span data-ttu-id="a6703-114">Сведения о поставщике ведения журнала родительского контроля</span><span class="sxs-lookup"><span data-stu-id="a6703-114">Parental Controls Logging Provider Details</span></span>

<span data-ttu-id="a6703-115">Поставщик WPC имеет имя Microsoft.com/Windows/ParentalControls с GUID {01090065-B467-4503-9B28-533766761087}.</span><span class="sxs-lookup"><span data-stu-id="a6703-115">The WPC provider is named Microsoft.com/Windows/ParentalControls with GUID {01090065-B467-4503-9B28-533766761087}.</span></span> <span data-ttu-id="a6703-116">Локальный канал ведения журнала по умолчанию — Microsoft.com/Windows/ParentalControls/LocalEvents.</span><span class="sxs-lookup"><span data-stu-id="a6703-116">The default local logging channel is Microsoft.com/Windows/ParentalControls/LocalEvents.</span></span>

<span data-ttu-id="a6703-117">Файлы журнала хранятся в \\ \\ папке журналов WPC Windows System32 \\ .</span><span class="sxs-lookup"><span data-stu-id="a6703-117">Log files are stored in the Windows\\System32\\Wpc\\Logs folder.</span></span>

### <a name="notification-of-impending-time-limits-logout"></a><span data-ttu-id="a6703-118">Уведомление об ограничениях времени ожидания выхода из системы</span><span class="sxs-lookup"><span data-stu-id="a6703-118">Notification of Impending Time Limits Logout</span></span>

<span data-ttu-id="a6703-119">Система родительского контроля запустит событие предупреждения через 15 минут и снова через 1 минуту, прежде чем выйти из контролируемого пользователя на основе временных ограничений.</span><span class="sxs-lookup"><span data-stu-id="a6703-119">The Parental Controls system will fire a warning event at 15 minutes and again at 1 minute before logout of a controlled user based on time restrictions.</span></span> <span data-ttu-id="a6703-120">Приложения могут подписываться на эти события, особенно если они работают в полноэкранном режиме DirectX, где стандартные уведомления Windows не отображаются.</span><span class="sxs-lookup"><span data-stu-id="a6703-120">Applications can subscribe to these events, especially when they are running in DirectX full-screen mode where standard Windows notifications are not displayed.</span></span> <span data-ttu-id="a6703-121">Приведен пример кода, который показывает, как подписаться на события, зарегистрировать функцию обратного вызова и получить события.</span><span class="sxs-lookup"><span data-stu-id="a6703-121">Sample code is provided that shows how to subscribe to the events, register a callback function, and receive the events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6703-122">См. также</span><span class="sxs-lookup"><span data-stu-id="a6703-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6703-123">Общие сведения о функциях расширяемости родительского контроля</span><span class="sxs-lookup"><span data-stu-id="a6703-123">Parental Controls Extensibility Features Overview</span></span>](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[<span data-ttu-id="a6703-124">**\_дескриптор данных \_ события**</span><span class="sxs-lookup"><span data-stu-id="a6703-124">**EVENT\_DATA\_DESCRIPTOR**</span></span>](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[<span data-ttu-id="a6703-125">**EventDataDescCreate**</span><span class="sxs-lookup"><span data-stu-id="a6703-125">**EventDataDescCreate**</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[<span data-ttu-id="a6703-126">**WPC \_ args \_ конверсатионинитевент**</span><span class="sxs-lookup"><span data-stu-id="a6703-126">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 
