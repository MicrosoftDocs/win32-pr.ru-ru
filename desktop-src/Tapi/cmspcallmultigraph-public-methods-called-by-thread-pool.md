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
# <a name="cmspcallmultigraph-public-methods-called-by-thread-pool"></a>Кмспкаллмултиграф открытые методы, вызываемые пулом потоков



| Кмспкаллмултиграф открытые методы                                   | Описание                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**диспатчграфевент**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) | Вызывается, когда граф фильтра сигнализирует о событии.                                                                                                                                                           |
| [**хандлеграфевент**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-handlegraphevent)     | Вызывается статическим методом [**диспатчграфевент**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) . Помещает в очередь [**процессграфевент**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) в основном рабочем потоке MSP. |
| [**процессграфевент**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent)   | Разрешает экземпляру объекта вызова MSP обработку события фильтра графа.                                                                                                                                    |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**кмспкаллмултиграф**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)
</dt> </dl>

 

 



