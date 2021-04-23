---
description: Время системных ссылок
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Время системных ссылок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8de8b208e32b6ea4772f3183c38a816ea43bb6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909492"
---
# <a name="system-reference-clock"></a>Время системных ссылок

Объект часов системных ссылок реализует ссылочный период времени, который возвращает системное время. Если ни один из фильтров в графе не предоставляет эталонные часы, диспетчер графов фильтров использует этот компонент для синхронизации графа. Создайте этот объект, вызвав **CoCreateInstance**.



| Метка | Значение |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор класса | \_СИСТЕМКЛОКК CLSID                                                                                                                                       |
| Интерфейсы       | [**Иамклоккаджуст**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**иреференцеклокктимерконтрол**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Объекты DirectShow](directshow-objects.md)
</dt> <dt>

[Эталонные часы](reference-clocks.md)
</dt> <dt>

[Время и часы в DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



