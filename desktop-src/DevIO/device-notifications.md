---
description: Система передает набор событий изменения устройства по умолчанию всем приложениям и службам.
ms.assetid: 672ad753-210b-41c3-b8c7-e041ce7b1671
title: Уведомления устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caeee8ba50a62a3bc393172347be09d1ac58085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142217"
---
# <a name="device-notifications"></a><span data-ttu-id="1c66b-103">Уведомления устройства</span><span class="sxs-lookup"><span data-stu-id="1c66b-103">Device Notifications</span></span>

<span data-ttu-id="1c66b-104">Система передает набор событий изменения устройства по умолчанию всем приложениям и службам.</span><span class="sxs-lookup"><span data-stu-id="1c66b-104">The system broadcasts a set of default device change events to all applications and services.</span></span> <span data-ttu-id="1c66b-105">Для получения этих событий по умолчанию не нужно регистрироваться.</span><span class="sxs-lookup"><span data-stu-id="1c66b-105">You do not need to register to receive these default events.</span></span> <span data-ttu-id="1c66b-106">Дополнительные сведения см. в разделе "Примечания" в [**регистердевиценотификатион**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) .</span><span class="sxs-lookup"><span data-stu-id="1c66b-106">See the Remarks section in [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) for details.</span></span> <span data-ttu-id="1c66b-107">Чтобы указать другие события, которые должны быть получены вашим приложением или службой, используйте функцию **регистердевиценотификатион** .</span><span class="sxs-lookup"><span data-stu-id="1c66b-107">To specify other events your application or service should receive, use the **RegisterDeviceNotification** function.</span></span>

<span data-ttu-id="1c66b-108">Когда приложение или служба вызывает [**регистердевиценотификатион**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), оно также указывает окно, которое будет принимать события уведомления.</span><span class="sxs-lookup"><span data-stu-id="1c66b-108">When an application or service calls [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), it also specifies the window that will receive the notification events.</span></span> <span data-ttu-id="1c66b-109">Службы могут задавать обработчик состояния службы вместо обработчика окна.</span><span class="sxs-lookup"><span data-stu-id="1c66b-109">Services can specify a service status handle instead of a window handle.</span></span> <span data-ttu-id="1c66b-110">Если служба указывает дескриптор состояния службы, ее обработчик управления службами получит события уведомления.</span><span class="sxs-lookup"><span data-stu-id="1c66b-110">If a service specifies its service status handle, its service control handler will receive the notification events.</span></span> <span data-ttu-id="1c66b-111">Дополнительные сведения см. в разделе [**хандлерекс**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span><span class="sxs-lookup"><span data-stu-id="1c66b-111">For more information, see [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span></span>

<span data-ttu-id="1c66b-112">Не забудьте как можно быстрее обрабатывать события самонастраивающийся устройства.</span><span class="sxs-lookup"><span data-stu-id="1c66b-112">Be sure to handle Plug and Play device events as quickly as possible.</span></span> <span data-ttu-id="1c66b-113">В противном случае система может перестать отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="1c66b-113">Otherwise, the system may become unresponsive.</span></span> <span data-ttu-id="1c66b-114">Если обработчик событий выполняет операцию, которая может блокировать выполнение (например, ввод-вывод), лучше запустить другой поток для асинхронного выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="1c66b-114">If your event handler is to perform an operation that may block execution (such as I/O), it is best to start another thread to perform the operation asynchronously.</span></span>

<span data-ttu-id="1c66b-115">Дескрипторы уведомлений устройства, возвращаемые функцией [**регистердевиценотификатион**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) , должны быть закрыты путем вызова функции [**унрегистердевиценотификатион**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) , когда они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="1c66b-115">Device notification handles returned by [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) must be closed by calling the [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) function when they are no longer needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c66b-116">См. также</span><span class="sxs-lookup"><span data-stu-id="1c66b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c66b-117">Регистрация для получения уведомлений устройства</span><span class="sxs-lookup"><span data-stu-id="1c66b-117">Registering for device notification</span></span>](registering-for-device-notification.md)
</dt> </dl>

 

 
