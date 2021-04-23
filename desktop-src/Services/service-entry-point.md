---
description: Службы обычно пишутся как консольные приложения.
ms.assetid: ed6945fc-ac08-4776-8d75-d33e8df3882a
title: Точка входа службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de9e2683c4a69949b6f51c7d000c0ee3571fe118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991051"
---
# <a name="service-entry-point"></a><span data-ttu-id="2e844-103">Точка входа службы</span><span class="sxs-lookup"><span data-stu-id="2e844-103">Service Entry Point</span></span>

<span data-ttu-id="2e844-104">Службы обычно пишутся как консольные приложения.</span><span class="sxs-lookup"><span data-stu-id="2e844-104">Services are generally written as console applications.</span></span> <span data-ttu-id="2e844-105">Точкой входа консольного приложения является его **Основная** функция.</span><span class="sxs-lookup"><span data-stu-id="2e844-105">The entry point of a console application is its **main** function.</span></span> <span data-ttu-id="2e844-106">Функция **Main** получает аргументы из значения **ImagePath** из раздела реестра для службы.</span><span class="sxs-lookup"><span data-stu-id="2e844-106">The **main** function receives arguments from the **ImagePath** value from the registry key for the service.</span></span> <span data-ttu-id="2e844-107">Дополнительные сведения см. в разделе "Примечания" функции [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) .</span><span class="sxs-lookup"><span data-stu-id="2e844-107">For more information, see the Remarks section of the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function.</span></span>

<span data-ttu-id="2e844-108">Когда SCM запускает программу службы, она ожидает вызова функции [**сбой StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) .</span><span class="sxs-lookup"><span data-stu-id="2e844-108">When the SCM starts a service program, it waits for it to call the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function.</span></span> <span data-ttu-id="2e844-109">Используйте следующие рекомендации.</span><span class="sxs-lookup"><span data-stu-id="2e844-109">Use the following guidelines.</span></span>

-   <span data-ttu-id="2e844-110">Служба типа " \_ \_ собственный процесс Win32" \_ должна вызывать [**сбой StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) немедленно, из своего основного потока.</span><span class="sxs-lookup"><span data-stu-id="2e844-110">A service of type SERVICE\_WIN32\_OWN\_PROCESS should call [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) immediately, from its main thread.</span></span> <span data-ttu-id="2e844-111">Инициализацию можно выполнить после запуска службы, как описано в разделе [Service ServiceMain Function](service-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="2e844-111">You can perform any initialization after the service starts, as described in [Service ServiceMain Function](service-servicemain-function.md).</span></span>
-   <span data-ttu-id="2e844-112">Если типом службы является \_ \_ Общий \_ процесс Win32 и существует общая инициализация всех служб в программе, можно выполнить инициализацию в основном потоке перед вызовом [**сбой StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera), если он занимает менее 30 секунд.</span><span class="sxs-lookup"><span data-stu-id="2e844-112">If the service type is SERVICE\_WIN32\_SHARE\_PROCESS and there is common initialization for all services in the program, you can perform the initialization in the main thread before calling [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera), as long as it takes less than 30 seconds.</span></span> <span data-ttu-id="2e844-113">В противном случае необходимо создать другой поток для выполнения общей инициализации, в то время как главный поток вызывает **сбой StartServiceCtrlDispatcher**.</span><span class="sxs-lookup"><span data-stu-id="2e844-113">Otherwise, you must create another thread to do the common initialization, while the main thread calls **StartServiceCtrlDispatcher**.</span></span> <span data-ttu-id="2e844-114">При запуске службы все равно следует выполнять инициализацию, зависящую от службы.</span><span class="sxs-lookup"><span data-stu-id="2e844-114">You should still perform any service-specific initialization after the service starts.</span></span>

<span data-ttu-id="2e844-115">Функция [**сбой StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) принимает структуру [**\_ \_ записи таблицы службы**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya) для каждой службы, содержащейся в процессе.</span><span class="sxs-lookup"><span data-stu-id="2e844-115">The [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function takes a [**SERVICE\_TABLE\_ENTRY**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya) structure for each service contained in the process.</span></span> <span data-ttu-id="2e844-116">Каждая структура задает имя службы и точку входа для службы.</span><span class="sxs-lookup"><span data-stu-id="2e844-116">Each structure specifies the service name and the entry point for the service.</span></span> <span data-ttu-id="2e844-117">Пример см. в разделе [написание функции Main служебной программы](writing-a-service-program-s-main-function.md).</span><span class="sxs-lookup"><span data-stu-id="2e844-117">For an example, see [Writing a Service Program's main Function](writing-a-service-program-s-main-function.md).</span></span>

<span data-ttu-id="2e844-118">Если [**сбой StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) завершается успешно, вызывающий поток не возвращает значение, пока все выполняющиеся службы в процессе не перешли в \_ состояние остановлена.</span><span class="sxs-lookup"><span data-stu-id="2e844-118">If [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) succeeds, the calling thread does not return until all running services in the process have entered the SERVICE\_STOPPED state.</span></span> <span data-ttu-id="2e844-119">SCM отправляет управляющие запросы в этот поток через именованный канал.</span><span class="sxs-lookup"><span data-stu-id="2e844-119">The SCM sends control requests to this thread through a named pipe.</span></span> <span data-ttu-id="2e844-120">Поток выступает в качестве диспетчера управления, выполняя следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="2e844-120">The thread acts as a control dispatcher, performing the following tasks:</span></span>

-   <span data-ttu-id="2e844-121">Создание нового потока для вызова соответствующей точки входа при запуске новой службы.</span><span class="sxs-lookup"><span data-stu-id="2e844-121">Create a new thread to call the appropriate entry point when a new service is started.</span></span>
-   <span data-ttu-id="2e844-122">Вызовите соответствующую [функцию обработчика](service-control-handler-function.md) для обработки запросов управления службами.</span><span class="sxs-lookup"><span data-stu-id="2e844-122">Call the appropriate [handler function](service-control-handler-function.md) to handle service control requests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e844-123">См. также</span><span class="sxs-lookup"><span data-stu-id="2e844-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e844-124">Написание основной функции служебной программы</span><span class="sxs-lookup"><span data-stu-id="2e844-124">Writing a Service Program's main Function</span></span>](writing-a-service-program-s-main-function.md)
</dt> </dl>

 

 



