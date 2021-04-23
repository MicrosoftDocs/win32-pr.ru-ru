---
description: Для отправки управляющих запросов работающей службе программа управления службами использует функцию ControlService.
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: Запросы управления службами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb5edf56137e2c98ea7db440a4db5e55df5e8f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662352"
---
# <a name="service-control-requests"></a><span data-ttu-id="1c413-103">Запросы управления службами</span><span class="sxs-lookup"><span data-stu-id="1c413-103">Service Control Requests</span></span>

<span data-ttu-id="1c413-104">Для отправки управляющих запросов работающей службе программа управления службами использует функцию [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) .</span><span class="sxs-lookup"><span data-stu-id="1c413-104">To send control requests to a running service, a service control program uses the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function.</span></span> <span data-ttu-id="1c413-105">Эта функция задает значение элемента управления, которое передается функции [**хандлерекс**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) указанной службы.</span><span class="sxs-lookup"><span data-stu-id="1c413-105">This function specifies a control value that is passed to the [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) function of the specified service.</span></span> <span data-ttu-id="1c413-106">Это значение элемента управления может быть определяемым пользователем кодом или одним из стандартных кодов, которые позволяют вызывающей программе выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1c413-106">This control value can be a user-defined code, or it can be one of the standard codes that enable the calling program to perform the following actions:</span></span>

-   <span data-ttu-id="1c413-107">Останавливает службу (служба \_ управления службами \_ останавливается).</span><span class="sxs-lookup"><span data-stu-id="1c413-107">Stop a service (SERVICE\_CONTROL\_STOP).</span></span>
-   <span data-ttu-id="1c413-108">Приостановка службы ( \_ \_ приостановка управления службой).</span><span class="sxs-lookup"><span data-stu-id="1c413-108">Pause a service (SERVICE\_CONTROL\_PAUSE).</span></span>
-   <span data-ttu-id="1c413-109">Возобновить выполнение приостановленной службы ( \_ продолжение управления службой \_ ).</span><span class="sxs-lookup"><span data-stu-id="1c413-109">Resume executing a paused service (SERVICE\_CONTROL\_CONTINUE).</span></span>
-   <span data-ttu-id="1c413-110">Получение обновленной информации о состоянии из службы ( \_ опрос управления службами \_ ).</span><span class="sxs-lookup"><span data-stu-id="1c413-110">Retrieve updated status information from a service (SERVICE\_CONTROL\_INTERROGATE).</span></span>

<span data-ttu-id="1c413-111">Каждая служба определяет значения элементов управления, которые будут приняты и обработаны.</span><span class="sxs-lookup"><span data-stu-id="1c413-111">Each service specifies the control values that it will accept and process.</span></span> <span data-ttu-id="1c413-112">Чтобы определить, какие из стандартных значений элементов управления принимаются службой, используйте функцию [**куерисервицестатусекс**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) или задайте \_ метод опроса управления службой, \_ чтобы запросить контрольное значение в вызове функции [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) .</span><span class="sxs-lookup"><span data-stu-id="1c413-112">To determine which of the standard control values are accepted by a service, use the [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function or specify the SERVICE\_CONTROL\_INTERROGATE control value in a call to the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function.</span></span> <span data-ttu-id="1c413-113">Элемент **двконтролсакцептед** структуры [**\_ состояния службы**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) , возвращаемой этими функциями, указывает, может ли служба быть остановлена, приостановлена или возобновлена.</span><span class="sxs-lookup"><span data-stu-id="1c413-113">The **dwControlsAccepted** member of the [**SERVICE\_STATUS**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) structure returned by these functions indicates whether the service can be stopped, paused, or resumed.</span></span> <span data-ttu-id="1c413-114">Все службы принимают управление службой \_ для \_ опроса контрольного значения.</span><span class="sxs-lookup"><span data-stu-id="1c413-114">All services accept the SERVICE\_CONTROL\_INTERROGATE control value.</span></span>

<span data-ttu-id="1c413-115">Функция [**куерисервицестатусекс**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) сообщает о последнем состоянии указанной службы, но не получает обновленное состояние от самой службы.</span><span class="sxs-lookup"><span data-stu-id="1c413-115">The [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function reports the most recent status for a specified service, but does not get an updated status from the service itself.</span></span> <span data-ttu-id="1c413-116">Использование управления службой \_ \_ для опроса контрольного значения при вызове [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) гарантирует, что возвращенная информация о состоянии будет актуальной.</span><span class="sxs-lookup"><span data-stu-id="1c413-116">Using the SERVICE\_CONTROL\_INTERROGATE control value in a call to [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) ensures that the status information returned is current.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c413-117">См. также</span><span class="sxs-lookup"><span data-stu-id="1c413-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c413-118">Управление службой с помощью SC</span><span class="sxs-lookup"><span data-stu-id="1c413-118">Controlling a Service Using SC</span></span>](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



