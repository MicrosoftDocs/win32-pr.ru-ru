---
description: Смарт-карта диспетчер ресурсов
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: Смарт-карта диспетчер ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3ee8e0bf311539863502d3e789544717e6dff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664163"
---
# <a name="smart-card-resource-manager"></a><span data-ttu-id="1e0e5-103">Смарт-карта диспетчер ресурсов</span><span class="sxs-lookup"><span data-stu-id="1e0e5-103">Smart Card Resource Manager</span></span>

<span data-ttu-id="1e0e5-104">[*Диспетчер ресурсов*](../secgloss/r-gly.md) [*смарт-карт*](../secgloss/s-gly.md) управляет доступом к [*читателям*](../secgloss/r-gly.md) и *смарт-картам*.</span><span class="sxs-lookup"><span data-stu-id="1e0e5-104">The [*smart card*](../secgloss/s-gly.md) [*resource manager*](../secgloss/r-gly.md) manages access to [*readers*](../secgloss/r-gly.md) and to *smart cards*.</span></span> <span data-ttu-id="1e0e5-105">Для управления этими ресурсами выполняются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="1e0e5-105">To manage these resources, it performs the following functions.</span></span>

-   <span data-ttu-id="1e0e5-106">Определяет и отслеживает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="1e0e5-106">Identifies and tracks resources.</span></span>
-   <span data-ttu-id="1e0e5-107">Выделяет модули чтения и ресурсы для нескольких приложений.</span><span class="sxs-lookup"><span data-stu-id="1e0e5-107">Allocates readers and resources across multiple applications.</span></span>
-   <span data-ttu-id="1e0e5-108">Поддерживает примитивы [*транзакций*](../secgloss/t-gly.md) для доступа к службам, доступным на данной карточке.</span><span class="sxs-lookup"><span data-stu-id="1e0e5-108">Supports [*transaction*](../secgloss/t-gly.md) primitives for accessing services available on a given card.</span></span>
    > [!Note]  
    > <span data-ttu-id="1e0e5-109">Это важный момент, поскольку текущие карты являются однопотоковыми устройствами, которым часто требуется выполнение нескольких команд для выполнения одной функции.</span><span class="sxs-lookup"><span data-stu-id="1e0e5-109">This is an important point because current cards are single-threaded devices that often require the execution of multiple commands to complete a single function.</span></span> <span data-ttu-id="1e0e5-110">[*Транзакции*](../secgloss/t-gly.md) позволяют выполнять несколько команд без прерывания, гарантируя, что сведения о промежуточном [*состоянии*](../secgloss/s-gly.md) не повреждены.</span><span class="sxs-lookup"><span data-stu-id="1e0e5-110">[*Transactions*](../secgloss/t-gly.md) allow multiple commands to be executed without interruption, ensuring that intermediate [*state*](../secgloss/s-gly.md) information is not corrupted.</span></span>

     

<span data-ttu-id="1e0e5-111">Доступ к диспетчеру ресурсов можно получить непосредственно через API Resource Manager или косвенно с помощью любого [*поставщика услуг*](../secgloss/s-gly.md)смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="1e0e5-111">The resource manager can be accessed directly by way of the resource manager API or indirectly through any smart card [*service provider*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="1e0e5-112">API диспетчера ресурсов — это набор функций Windows, обеспечивающих прямой доступ к службам Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="1e0e5-112">The resource manager API is a set of Windows functions that provide direct access to the resource manager's services.</span></span> <span data-ttu-id="1e0e5-113">Общие сведения о функциях Windows, предоставляемых API, см. в статье [смарт-карта диспетчер ресурсов API](smart-card-resource-manager-api.md).</span><span class="sxs-lookup"><span data-stu-id="1e0e5-113">For an overview of the Windows functions provided by the API, see [Smart Card Resource Manager API](smart-card-resource-manager-api.md).</span></span> <span data-ttu-id="1e0e5-114">Для сравнения поставщики услуг смарт-карт используют COM-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1e0e5-114">In comparison, smart card service providers use COM interfaces.</span></span>

<span data-ttu-id="1e0e5-115">Многие функции Windows в API диспетчера ресурсов имеют эквивалент в свойствах и методах интерфейсов COM поставщиков услуг смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="1e0e5-115">Many of the Windows functions in the resource manager API have equivalents in the properties and methods of the smart card service providers' COM interfaces.</span></span> <span data-ttu-id="1e0e5-116">Несмотря на то, что большинство разработчиков приложений будут проще работать с COM, некоторым приложениям все равно потребуется использовать функции Windows для выполнения определенных задач.</span><span class="sxs-lookup"><span data-stu-id="1e0e5-116">And although most application developers will find COM easier to work with, some applications will still need to use the Windows functions to perform certain tasks.</span></span> <span data-ttu-id="1e0e5-117">Например, приложения, которым требуется управлять списком читателей или групп читателей в [*базе данных смарт-карт*](../secgloss/s-gly.md)и которым требуется прямое управление читателями, должны использовать API Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="1e0e5-117">For example, applications that need to manipulate the list of readers or reader groups in the [*smart card database*](../secgloss/s-gly.md), and those that need direct control of a reader, must use the resource manager API.</span></span> <span data-ttu-id="1e0e5-118">Службы, предоставляющие эти возможности, доступны только в функциях Windows, а не в COM, предоставляемом поставщиками служб.</span><span class="sxs-lookup"><span data-stu-id="1e0e5-118">The services that provide these capabilities are available only in the Windows functions, not in the COM provided by the service providers.</span></span>

<span data-ttu-id="1e0e5-119">Сведения о реализации [*диспетчера ресурсов*](../secgloss/r-gly.md) в Windows см. в разделе [Реализация диспетчер ресурсов](resource-manager-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="1e0e5-119">For information about how the [*resource manager*](../secgloss/r-gly.md) is implemented in Windows, see [Resource Manager Implementation](resource-manager-implementation.md).</span></span>

 

 
