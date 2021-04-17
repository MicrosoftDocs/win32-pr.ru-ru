---
description: В следующем списке содержатся открытые методы Кмспкаллмултиграф, вызываемые пулом потоков.
ms.assetid: f0a5f621-99c4-40f0-8a0e-0e43792e00a1
title: Кмспкаллмултиграф открытые методы, вызываемые пулом потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3878298024164a4c940b96dceb88e0ff005d59ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673851"
---
# <a name="cmspcallmultigraph-public-methods-called-by-thread-pool"></a><span data-ttu-id="61fd5-103">Кмспкаллмултиграф открытые методы, вызываемые пулом потоков</span><span class="sxs-lookup"><span data-stu-id="61fd5-103">CMSPCallMultiGraph Public Methods, Called by Thread Pool</span></span>



| <span data-ttu-id="61fd5-104">Кмспкаллмултиграф открытые методы</span><span class="sxs-lookup"><span data-stu-id="61fd5-104">CMSPCallMultiGraph public methods</span></span>                                   | <span data-ttu-id="61fd5-105">Описание</span><span class="sxs-lookup"><span data-stu-id="61fd5-105">Description</span></span>                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61fd5-106">**диспатчграфевент**</span><span class="sxs-lookup"><span data-stu-id="61fd5-106">**DispatchGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) | <span data-ttu-id="61fd5-107">Вызывается, когда граф фильтра сигнализирует о событии.</span><span class="sxs-lookup"><span data-stu-id="61fd5-107">Called when the filter graph signals an event.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="61fd5-108">**хандлеграфевент**</span><span class="sxs-lookup"><span data-stu-id="61fd5-108">**HandleGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-handlegraphevent)     | <span data-ttu-id="61fd5-109">Вызывается статическим методом [**диспатчграфевент**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) .</span><span class="sxs-lookup"><span data-stu-id="61fd5-109">Called by the [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) static method.</span></span> <span data-ttu-id="61fd5-110">Помещает в очередь [**процессграфевент**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) в основном рабочем потоке MSP.</span><span class="sxs-lookup"><span data-stu-id="61fd5-110">Queues [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) on the main MSP worker thread.</span></span> |
| [<span data-ttu-id="61fd5-111">**процессграфевент**</span><span class="sxs-lookup"><span data-stu-id="61fd5-111">**ProcessGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent)   | <span data-ttu-id="61fd5-112">Разрешает экземпляру объекта вызова MSP обработку события фильтра графа.</span><span class="sxs-lookup"><span data-stu-id="61fd5-112">Allows the MSP call object instance to handle the filter graph event.</span></span>                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="61fd5-113">См. также</span><span class="sxs-lookup"><span data-stu-id="61fd5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61fd5-114">**кмспкаллмултиграф**</span><span class="sxs-lookup"><span data-stu-id="61fd5-114">**CMSPCallMultiGraph**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)
</dt> </dl>

 

 



