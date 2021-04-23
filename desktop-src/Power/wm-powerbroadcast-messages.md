---
description: Система передает сообщение всем приложениям и устанавливаемым драйверам при каждом возникновении события управления питанием.
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: Сообщения WM_POWERBROADCAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f70c5848ec5d71666c26fcd4b5b161e31465543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673783"
---
# <a name="wm_powerbroadcast-messages"></a><span data-ttu-id="6c39c-103">\_Сообщения ПОВЕРБРОАДКАСТ WM</span><span class="sxs-lookup"><span data-stu-id="6c39c-103">WM\_POWERBROADCAST Messages</span></span>

<span data-ttu-id="6c39c-104">Система передает сообщение всем приложениям и устанавливаемым драйверам при каждом возникновении события управления питанием.</span><span class="sxs-lookup"><span data-stu-id="6c39c-104">The system broadcasts a message to all applications and installable drivers whenever a power management event occurs.</span></span> <span data-ttu-id="6c39c-105">Система передает эти события через сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) , устанавливая параметр *wParam* в соответствующее событие управления питанием.</span><span class="sxs-lookup"><span data-stu-id="6c39c-105">The system broadcasts these events through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message, setting the *wParam* parameter to the appropriate power management event.</span></span> <span data-ttu-id="6c39c-106">Например, событие [ПБТ \_ апмповерстатусчанже](pbt-apmpowerstatuschange.md) указывает на изменение состояния питания системы.</span><span class="sxs-lookup"><span data-stu-id="6c39c-106">For example, the [PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) event indicates a system power status change.</span></span> <span data-ttu-id="6c39c-107">Необходимо убедиться, что приложение правильно реагирует на сообщение **\_ поверброадкаст WM** .</span><span class="sxs-lookup"><span data-stu-id="6c39c-107">You must ensure that your application responds properly to the **WM\_POWERBROADCAST** message.</span></span>

<span data-ttu-id="6c39c-108">Система передает событие [ПБТ \_ апмсуспенд](pbt-apmsuspend.md) непосредственно перед приостановкой операции.</span><span class="sxs-lookup"><span data-stu-id="6c39c-108">The system broadcasts a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event immediately before suspending operation.</span></span> <span data-ttu-id="6c39c-109">Это дает приложениям и драйверам последнюю возможность подготовиться к событию.</span><span class="sxs-lookup"><span data-stu-id="6c39c-109">This gives applications and drivers one last chance to prepare for the event.</span></span> <span data-ttu-id="6c39c-110">Во многих случаях система передает эти сообщения без запроса разрешения на это.</span><span class="sxs-lookup"><span data-stu-id="6c39c-110">In many cases, the system broadcasts these messages without requesting permission to do so.</span></span> <span data-ttu-id="6c39c-111">Это происходит, например, если приложение принудительно применяет приостановку с помощью функции [**сетсуспендстате**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .</span><span class="sxs-lookup"><span data-stu-id="6c39c-111">This happens, for example, if an application forces suspension with the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

<span data-ttu-id="6c39c-112">Система выполняет широковещательную рассылку события [ПБТ \_ Апмресумесуспенд](pbt-apmresumesuspend.md) или [ПБТ \_ апмресумекритикал](pbt-apmresumecritical.md) при восстановлении системной операции.</span><span class="sxs-lookup"><span data-stu-id="6c39c-112">The system broadcasts the [PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md) or [PBT\_APMRESUMECRITICAL](pbt-apmresumecritical.md) event when system operation has been restored.</span></span> <span data-ttu-id="6c39c-113">Если приложение получило событие [ПБТ \_ апмсуспенд](pbt-apmsuspend.md) до того, как компьютер был приостановлен, он получит \_ событие ПБТ апмресумесуспенд.</span><span class="sxs-lookup"><span data-stu-id="6c39c-113">If an application received a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event before the computer was suspended, it will receive the PBT\_APMRESUMESUSPEND event.</span></span> <span data-ttu-id="6c39c-114">В противном случае будет получено \_ событие ПБТ апмресумекритикал.</span><span class="sxs-lookup"><span data-stu-id="6c39c-114">Otherwise, it will receive the PBT\_APMRESUMECRITICAL event.</span></span>

<span data-ttu-id="6c39c-115">Система отправляет событие [ПБТ \_ поверсеттингчанже](pbt-powersettingchange.md) в приложения, зарегистрированные для конкретного события с помощью [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification).</span><span class="sxs-lookup"><span data-stu-id="6c39c-115">The system sends a [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md) event to applications that have registered for the specific event using [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification).</span></span> <span data-ttu-id="6c39c-116">Дополнительные сведения см. в статье [Регистрация событий питания](registering-for-power-events.md).</span><span class="sxs-lookup"><span data-stu-id="6c39c-116">For more information, see [Registering for Power Events](registering-for-power-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c39c-117">См. также</span><span class="sxs-lookup"><span data-stu-id="6c39c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c39c-118">Сведения об управлении питанием</span><span class="sxs-lookup"><span data-stu-id="6c39c-118">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



