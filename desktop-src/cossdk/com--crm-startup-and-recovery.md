---
description: Запуск и восстановление COM+ CRM
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: Запуск и восстановление COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0e631e2e5ecef1621705c9af74aa48898d733b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710795"
---
# <a name="com-crm-startup-and-recovery"></a><span data-ttu-id="c3a91-103">Запуск и восстановление COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="c3a91-103">COM+ CRM Startup and Recovery</span></span>

<span data-ttu-id="c3a91-104">Если для серверного приложения установлен флажок **Включить компенсирующие диспетчеры ресурсов** (с помощью средства администрирования "службы компонентов" на вкладке " **Дополнительно** " страницы свойств приложения COM+), при первом запуске создается файл журнала CRM, который будет использоваться всеми крмс в этом процессе серверного приложения.</span><span class="sxs-lookup"><span data-stu-id="c3a91-104">If a server application has the **Enable compensating resource managers** checkbox selected (using the Component Services administrative tool, on the **Advanced** tab of the COM+ application's property page), the first time it starts up it creates a CRM log file to be used by all CRMs in that server application process.</span></span> <span data-ttu-id="c3a91-105">(Подробные инструкции по настройке CRM см. в разделе [Настройка компонентов COM+ CRM](configuring-com--crm-components.md).)</span><span class="sxs-lookup"><span data-stu-id="c3a91-105">(For detailed instructions about configuring the CRM, see [Configuring COM+ CRM Components](configuring-com--crm-components.md).)</span></span>

<span data-ttu-id="c3a91-106">Имя файла журнала CRM, созданного для серверного приложения, основано на идентификаторе AppId (GUID) серверного приложения, а файл журнала CRM помещается в тот же каталог, что и файл журнала DTC (обычно это каталог% SystemRoot% \\ WinNT \\ system32 \\ дтклог).</span><span class="sxs-lookup"><span data-stu-id="c3a91-106">The name of the CRM log file created for the server application is based on the AppId (a GUID) of the server application, and the CRM log file is placed in the same directory as the DTC log file (normally your %SystemRoot%\\winnt\\system32\\DtcLog directory).</span></span> <span data-ttu-id="c3a91-107">Файлы журналов CRM имеют расширение крмлог.</span><span class="sxs-lookup"><span data-stu-id="c3a91-107">CRM log files have the extension .crmlog.</span></span>

> [!Note]  
> <span data-ttu-id="c3a91-108">Может потребоваться изменить расположение файла журнала CRM по умолчанию по соображениям производительности (для файла журнала DTC на диске, отличном от диска, на котором находится файл журнала CRM) или, возможно, из-за использования CRM в кластерной среде.</span><span class="sxs-lookup"><span data-stu-id="c3a91-108">It may be necessary to change the default location of a CRM log file due to performance reasons (to have the DTC log file on a different disk than the CRM log file) or perhaps due to use of the CRM in a cluster environment.</span></span> <span data-ttu-id="c3a91-109">Расположение файлов журнала CRM можно изменить с помощью пакета SDK администрирования COM+.</span><span class="sxs-lookup"><span data-stu-id="c3a91-109">The location of the CRM log files can be changed using the COM+ administration SDK.</span></span> <span data-ttu-id="c3a91-110">Имя свойства — Крмлогфиле, и оно существует в объекте коллекции [**приложений**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="c3a91-110">The property name is CRMLogFile, and it exists on the [**Applications**](applications.md) collection object.</span></span>

 

<span data-ttu-id="c3a91-111">Когда запускается серверное приложение (с поддержкой CRM) и обнаруживает, что файл журнала CRM для этого серверного приложения уже существует, он выполняет восстановление в этом файле журнала CRM.</span><span class="sxs-lookup"><span data-stu-id="c3a91-111">When a server application (that is CRM-enabled) starts up and finds that a CRM log file already exists for that server application, it performs recovery on that CRM log file.</span></span> <span data-ttu-id="c3a91-112">*Восстановление* — это процесс выполнения любых транзакций, которые были прерваны сбоем, и включает в себя инфраструктуру CRM, считывающую файл журнала CRM для всех транзакций, которые не были полностью завершены.</span><span class="sxs-lookup"><span data-stu-id="c3a91-112">*Recovery* is the process of completing any transactions that were interrupted by a failure and involves the CRM infrastructure reading the CRM log file for any transactions that were not fully completed.</span></span> <span data-ttu-id="c3a91-113">Если обнаруживается, он связывается с DTC для определения результата транзакции.</span><span class="sxs-lookup"><span data-stu-id="c3a91-113">If it finds any, it contacts the DTC to determine the transaction outcome.</span></span> <span data-ttu-id="c3a91-114">Затем он создает компенсатор CRM и передает при необходимости уведомления о фиксации или прерывании вместе со связанными записями журнала.</span><span class="sxs-lookup"><span data-stu-id="c3a91-114">It then creates the CRM Compensator and passes on the commit or abort notifications as required, together with the associated log records.</span></span>

<span data-ttu-id="c3a91-115">Подготовка уведомлений CRM во время восстановления не принимается.</span><span class="sxs-lookup"><span data-stu-id="c3a91-115">Prepare notifications are not received by the CRM Compensator during recovery.</span></span> <span data-ttu-id="c3a91-116">Компенсатор CRM имеет флаг, позволяющий определить, вызывается ли он во время нормальной работы или при восстановлении.</span><span class="sxs-lookup"><span data-stu-id="c3a91-116">The CRM Compensator has a flag to distinguish whether it is being called during normal operation or during recovery.</span></span>

<span data-ttu-id="c3a91-117">Восстановление, как правило, найдет незавершенные транзакции только в случае аварийного завершения работы серверного приложения из-за сбоя процесса серверного приложения или сбоя компьютера.</span><span class="sxs-lookup"><span data-stu-id="c3a91-117">Recovery will normally find uncompleted transactions only if the server application has been shutdown abnormally, due to either a server application process crash or a computer crash.</span></span> <span data-ttu-id="c3a91-118">Если серверному приложению разрешено нормальное завершение работы из-за истечения времени ожидания простоя или ручного завершения работы с помощью средства администрирования "службы компонентов", файл журнала будет очищен.</span><span class="sxs-lookup"><span data-stu-id="c3a91-118">If the server application is allowed to shut down normally, due either to the idle time-out or to manual shutdown via the Component Services administrative tool, the log file will be clean.</span></span>

<span data-ttu-id="c3a91-119">Запуск серверного приложения CRM для восстановления не инициируется автоматически.</span><span class="sxs-lookup"><span data-stu-id="c3a91-119">Starting of a CRM server application for recovery is not automatically initiated.</span></span> <span data-ttu-id="c3a91-120">Для запуска приложения сервера CRM, где требуется восстановление, необходимо выполнить некоторое внешнее действие.</span><span class="sxs-lookup"><span data-stu-id="c3a91-120">Some external action must be taken to start the CRM server application where recovery is required.</span></span> <span data-ttu-id="c3a91-121">Как правило, в этом серверном приложении создается компонент.</span><span class="sxs-lookup"><span data-stu-id="c3a91-121">Typically this would be creating a component in that server application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3a91-122">См. также</span><span class="sxs-lookup"><span data-stu-id="c3a91-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3a91-123">Основные понятия о компенсации диспетчер ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="c3a91-123">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[<span data-ttu-id="c3a91-124">Операционный процесс COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="c3a91-124">COM+ CRM Operating Process</span></span>](com--crm-operating-process.md)
</dt> </dl>

 

 



