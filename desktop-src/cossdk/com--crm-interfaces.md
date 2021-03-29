---
description: Интерфейсы CRM должны обеспечивать поддержку для работников CRM и компенсаторов CRM, разработанных с помощью Visual Basic и Visual C++.
ms.assetid: 68a75da7-1f35-41a4-8872-e3f4ad1fc30d
title: Интерфейсы COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ba3235b1cd2a82fc913dd676bbb78324f340cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807906"
---
# <a name="com-crm-interfaces"></a><span data-ttu-id="6e842-103">Интерфейсы COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="6e842-103">COM+ CRM Interfaces</span></span>

<span data-ttu-id="6e842-104">Интерфейсы CRM должны обеспечивать поддержку для работников CRM и компенсаторов CRM, разработанных с помощью Visual Basic и Visual C++.</span><span class="sxs-lookup"><span data-stu-id="6e842-104">The CRM interfaces are required to provide support for CRM Workers and CRM Compensators developed using Visual Basic and Visual C++.</span></span>

<span data-ttu-id="6e842-105">Можно использовать компенсирующий диспетчер ресурсов COM+ (CRM) для быстрой и простой интеграции ресурсов приложений с транзакциями Microsoft координатор распределенных транзакций (DTC).</span><span class="sxs-lookup"><span data-stu-id="6e842-105">You can use the COM+ Compensating Resource Manager (CRM) to quickly and easily integrate application resources with Microsoft Distributed Transaction Coordinator (DTC) transactions.</span></span>

<span data-ttu-id="6e842-106">Для компонентов, написанных с помощью Visual Basic, проще создавать записи журнала в виде коллекции вариантов.</span><span class="sxs-lookup"><span data-stu-id="6e842-106">It is easier for components written with Visual Basic to build up a log record as a collection of Variants.</span></span> <span data-ttu-id="6e842-107">Кроме того, Visual Basic компоненты являются потоковыми потоками, что подразумевает возможность маршалирования интерфейсов из многопоточного апартамента в однопотоковое подразделение.</span><span class="sxs-lookup"><span data-stu-id="6e842-107">Also, Visual Basic components are apartment threaded, which implies that it must be possible to marshal the interfaces from the multithreaded apartment to a single-threaded apartment.</span></span> <span data-ttu-id="6e842-108">Компоненты CRM, разработанные с помощью Visual C++, могут также использовать модель потоков подразделений, хотя вместо этого рекомендуется использовать как потоковую модель.</span><span class="sxs-lookup"><span data-stu-id="6e842-108">CRM components developed with Visual C++ could also use the Apartment threading model, although it is recommended that these use the Both threading model instead.</span></span>

<span data-ttu-id="6e842-109">Интерфейсы, описанные в следующей таблице, содержат подробные справочные сведения для разработчиков COM+ Крмс.</span><span class="sxs-lookup"><span data-stu-id="6e842-109">The interfaces described in the following table provide detailed reference information for developers of COM+ CRMs.</span></span>



| <span data-ttu-id="6e842-110">Интерфейсы CRM</span><span class="sxs-lookup"><span data-stu-id="6e842-110">CRM interfaces</span></span>                                             | <span data-ttu-id="6e842-111">Описание</span><span class="sxs-lookup"><span data-stu-id="6e842-111">Description</span></span>                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e842-112">**икрмкомпенсатор**</span><span class="sxs-lookup"><span data-stu-id="6e842-112">**ICrmCompensator**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator)                 | <span data-ttu-id="6e842-113">Этот интерфейс предоставляет неструктурированные записи журнала в Visual C++.</span><span class="sxs-lookup"><span data-stu-id="6e842-113">This interface delivers unstructured log records in Visual C++.</span></span>                                                           |
| [<span data-ttu-id="6e842-114">**икрмкомпенсаторвариантс**</span><span class="sxs-lookup"><span data-stu-id="6e842-114">**ICrmCompensatorVariants**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) | <span data-ttu-id="6e842-115">Этот интерфейс предоставляет данные структурированного журнала компенсатору CRM при использовании Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6e842-115">This interface delivers structured log records to the CRM Compensator when using Visual Basic.</span></span>                            |
| [<span data-ttu-id="6e842-116">**икрмформатлогрекордс**</span><span class="sxs-lookup"><span data-stu-id="6e842-116">**ICrmFormatLogRecords**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmformatlogrecords)       | <span data-ttu-id="6e842-117">Этот интерфейс преобразует записи журнала в отображаемый формат, чтобы их можно было представить с помощью универсального средства мониторинга.</span><span class="sxs-lookup"><span data-stu-id="6e842-117">This interface converts the log records to viewable format so that they can be presented using a generic monitoring tool.</span></span> |
| [<span data-ttu-id="6e842-118">**икрмлогконтрол**</span><span class="sxs-lookup"><span data-stu-id="6e842-118">**ICrmLogControl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)                   | <span data-ttu-id="6e842-119">Этот интерфейс используется работником CRM и компенсатором CRM для записи записей в журнал и обеспечения их надежности.</span><span class="sxs-lookup"><span data-stu-id="6e842-119">This interface is used by the CRM Worker and CRM Compensator to write records to the log and make them durable.</span></span>           |
| [<span data-ttu-id="6e842-120">**икрммонитор**</span><span class="sxs-lookup"><span data-stu-id="6e842-120">**ICrmMonitor**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)                         | <span data-ttu-id="6e842-121">Этот интерфейс фиксирует моментальный снимок текущего состояния CRM и содержит конкретный клерк CRM.</span><span class="sxs-lookup"><span data-stu-id="6e842-121">This interface captures a snapshot of the current state of a CRM and holds a specific CRM clerk.</span></span>                          |
| [<span data-ttu-id="6e842-122">**икрммониторклеркс**</span><span class="sxs-lookup"><span data-stu-id="6e842-122">**ICrmMonitorClerks**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)             | <span data-ttu-id="6e842-123">Этот интерфейс получает сведения о состоянии клерков.</span><span class="sxs-lookup"><span data-stu-id="6e842-123">This interface obtains information about the state of clerks.</span></span>                                                             |
| [<span data-ttu-id="6e842-124">**икрммониторлогрекордс**</span><span class="sxs-lookup"><span data-stu-id="6e842-124">**ICrmMonitorLogRecords**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)     | <span data-ttu-id="6e842-125">Этот интерфейс отслеживает отдельные записи журнала, поддерживаемые определенным клерком CRM для заданной транзакции.</span><span class="sxs-lookup"><span data-stu-id="6e842-125">This interface monitors the individual log records maintained by a specific CRM clerk for a given transaction.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="6e842-126">См. также</span><span class="sxs-lookup"><span data-stu-id="6e842-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e842-127">Основные понятия о компенсации диспетчер ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="6e842-127">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



