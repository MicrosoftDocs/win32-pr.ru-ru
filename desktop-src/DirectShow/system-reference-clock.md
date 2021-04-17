---
description: Время системных ссылок
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Время системных ссылок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67fab63c4ba8bfd6a7db9c476179d6e649869fb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674093"
---
# <a name="system-reference-clock"></a>Время системных ссылок

Объект часов системных ссылок реализует ссылочный период времени, который возвращает системное время. Если ни один из фильтров в графе не предоставляет эталонные часы, диспетчер графов фильтров использует этот компонент для синхронизации графа. Создайте этот объект, вызвав **CoCreateInstance**.



|                  |                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор класса | \_СИСТЕМКЛОКК CLSID                                                                                                                                       |
| Интерфейсы       | [**Иамклоккаджуст**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**иреференцеклокктимерконтрол**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Объекты DirectShow](directshow-objects.md)
</dt> <dt>

[Эталонные часы](reference-clocks.md)
</dt> <dt>

[Время и часы в DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



