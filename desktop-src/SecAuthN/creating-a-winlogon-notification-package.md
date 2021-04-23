---
description: Пакет уведомлений Winlogon — это библиотека DLL, которая экспортирует функции, которые обрабатывали события Winlogon. Например, когда пользователь входит в систему, Winlogon вызывает функцию обработчика событий logon каждого пакета уведомлений для предоставления сведений о событии.
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: Создание пакета уведомлений Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0127674967ee3155d42e143a1b142d8c83137c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650796"
---
# <a name="creating-a-winlogon-notification-package"></a><span data-ttu-id="65abc-104">Создание пакета уведомлений Winlogon</span><span class="sxs-lookup"><span data-stu-id="65abc-104">Creating a Winlogon Notification Package</span></span>

<span data-ttu-id="65abc-105">Пакет уведомлений [*Winlogon*](/windows/desktop/SecGloss/w-gly) — это библиотека DLL, которая экспортирует функции, которые обрабатывали события Winlogon.</span><span class="sxs-lookup"><span data-stu-id="65abc-105">A [*Winlogon*](/windows/desktop/SecGloss/w-gly) notification package is a DLL that exports functions that handle Winlogon events.</span></span> <span data-ttu-id="65abc-106">Например, когда пользователь входит в систему, Winlogon вызывает функцию обработчика событий logon каждого пакета уведомлений для предоставления сведений о событии.</span><span class="sxs-lookup"><span data-stu-id="65abc-106">For example, when a user logs onto the system, Winlogon calls each notification package's logon event handler function to provide information about the event.</span></span>

<span data-ttu-id="65abc-107">Имена функций обработчиков событий, реализованных в пакете уведомлений, остаются до разработчика; Winlogon проверяет реестр, чтобы получить имена функций обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="65abc-107">The names of the event handler functions implemented in a notification package are left up to the developer; Winlogon checks the registry to obtain the names of the event handler functions.</span></span> <span data-ttu-id="65abc-108">Например, один пакет уведомлений может реализовать функцию обработчика событий logon, в `WLEventLogon` то время как другой может использовать `HandleLogonEvent` .</span><span class="sxs-lookup"><span data-stu-id="65abc-108">For example, one notification package might implement the logon event handler function as `WLEventLogon` whereas another might use `HandleLogonEvent`.</span></span>

<span data-ttu-id="65abc-109">Нет необходимости реализовывать и регистрировать обработчики событий для каждого события Winlogon, только для событий, полезных для приложения.</span><span class="sxs-lookup"><span data-stu-id="65abc-109">You do not have to implement and register event handlers for every Winlogon event, only for events that are useful to your application.</span></span> <span data-ttu-id="65abc-110">Каждая функция обработчика событий должна использовать прототип функции, описанный в [прототипе функции обработчика событий](event-handler-function-prototype.md).</span><span class="sxs-lookup"><span data-stu-id="65abc-110">Each event handler function must use the function prototype described in [Event Handler Function Prototype](event-handler-function-prototype.md).</span></span> <span data-ttu-id="65abc-111">Этот прототип имеет один параметр: [**\_ \_ информационная структура уведомления влкс**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) , содержащая сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="65abc-111">This prototype has a single parameter: a [**WLX\_NOTIFICATION\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) structure that contains details about the event.</span></span>

<span data-ttu-id="65abc-112">Winlogon игнорирует выходные данные функций обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="65abc-112">Winlogon ignores the output of event handler functions.</span></span> <span data-ttu-id="65abc-113">Если для обработки события требуется взаимодействие с Winlogon, используйте [функции поддержки Winlogon](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="65abc-113">If handling an event requires interacting with Winlogon, use the [Winlogon Support Functions](authentication-functions.md).</span></span>

<span data-ttu-id="65abc-114">Чтобы использовать пакет уведомлений Winlogon, необходимо скопировать библиотеку DLL в папку% SystemRoot% \\ System32, а для пакета уведомлений должно быть установлено обновление реестра.</span><span class="sxs-lookup"><span data-stu-id="65abc-114">To use your Winlogon notification package, the DLL must be copied to the %SystemRoot%\\system32 folder, and a registry update must be made for the notification package.</span></span> <span data-ttu-id="65abc-115">Сведения об обновлении реестра см. в разделе [Регистрация пакета уведомлений Winlogon](registering-a-winlogon-notification-package.md).</span><span class="sxs-lookup"><span data-stu-id="65abc-115">For information about the registry update, see [Registering a Winlogon Notification Package](registering-a-winlogon-notification-package.md).</span></span>

 

 
