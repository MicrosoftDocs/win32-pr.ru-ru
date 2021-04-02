---
description: События WMI доставляются поставщиком событий временному или постоянному потребителю. Система событий WMI использует сравнение дескрипторов безопасности для событий и идентификаторов безопасности учетной записи пользователя для управления доступом к событиям.
ms.assetid: 86eaeb5c-c27e-4794-88e2-e0ffbb885290
ms.tgt_platform: multiple
title: Защита событий WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31280a4be25e358e28477bf6be060637f3f96bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263806"
---
# <a name="securing-wmi-events"></a><span data-ttu-id="75335-104">Защита событий WMI</span><span class="sxs-lookup"><span data-stu-id="75335-104">Securing WMI Events</span></span>

<span data-ttu-id="75335-105">События WMI доставляются [*поставщиком событий*](gloss-e.md) [*временному*](gloss-t.md) или [*постоянному*](gloss-p.md) потребителю.</span><span class="sxs-lookup"><span data-stu-id="75335-105">WMI events are delivered by the [*event provider*](gloss-e.md) to a [*temporary*](gloss-t.md) or [*permanent*](gloss-p.md) consumer.</span></span> <span data-ttu-id="75335-106">Система событий WMI использует сравнение [*дескрипторов безопасности*](gloss-s.md) для событий и [*идентификаторов*](gloss-s.md) безопасности учетной записи пользователя для управления доступом к событиям.</span><span class="sxs-lookup"><span data-stu-id="75335-106">The WMI event system uses the comparison of [*security descriptors*](gloss-s.md) on events and user account [*SIDs*](gloss-s.md) to control event access.</span></span>

<span data-ttu-id="75335-107">События доставляются в виде экземпляра класса событий (как правило, но не обязательно), производного от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="75335-107">Events are delivered in the form of an instance of an event class usually, but not necessarily, derived ultimately from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="75335-108">Инструментарий WMI предоставляет несколько общих классов событий в [системных классах WMI](wmi-system-classes.md), таких как [**\_ \_ инстанцемодификатионевент**](--instancemodificationevent.md).</span><span class="sxs-lookup"><span data-stu-id="75335-108">WMI supplies several general event classes in the [WMI System Classes](wmi-system-classes.md), such as [**\_\_InstanceModificationEvent**](--instancemodificationevent.md).</span></span> <span data-ttu-id="75335-109">Поставщики также могут предоставлять собственные классы событий.</span><span class="sxs-lookup"><span data-stu-id="75335-109">Providers may also supply their own event classes.</span></span> <span data-ttu-id="75335-110">Например, [поставщик системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider) имеет классы событий, которые сообщают об изменении раздела или значения реестра, например [**регистрикэйчанжеевент**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="75335-110">For example, the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) has event classes that report the change of a registry key or value, such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span>

<span data-ttu-id="75335-111">Следующие разделы содержат сведения о защите доставки событий поставщикам и о получении событий для клиентских сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="75335-111">The following topics supply information about securing delivery of events for providers and receiving events securely for client scripts and applications:</span></span>

-   [<span data-ttu-id="75335-112">Безопасное предоставление событий</span><span class="sxs-lookup"><span data-stu-id="75335-112">Providing Events Securely</span></span>](providing-events-securely.md)
-   [<span data-ttu-id="75335-113">Безопасное получение событий</span><span class="sxs-lookup"><span data-stu-id="75335-113">Receiving Events Securely</span></span>](receiving-events-securely.md)

## <a name="related-topics"></a><span data-ttu-id="75335-114">См. также</span><span class="sxs-lookup"><span data-stu-id="75335-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75335-115">Поддержание безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="75335-115">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

 
