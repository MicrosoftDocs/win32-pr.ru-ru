---
description: Время системных ссылок
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Время системных ссылок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b3b4fa69b2ff9b74b937dd38d8be83203d5cdd43ba9a26d2cac4077c40c811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651844"
---
# <a name="system-reference-clock"></a>Время системных ссылок

Объект часов системных ссылок реализует ссылочный период времени, который возвращает системное время. Если ни один из фильтров в графе не предоставляет эталонные часы, диспетчер графов фильтров использует этот компонент для синхронизации графа. Создайте этот объект, вызвав **CoCreateInstance**.



| Метка | Значение |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор класса | \_СИСТЕМКЛОКК CLSID                                                                                                                                       |
| Интерфейсы       | [**Иамклоккаджуст**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**иреференцеклокктимерконтрол**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Объект](directshow-objects.md)
</dt> <dt>

[Эталонные часы](reference-clocks.md)
</dt> <dt>

[Время и часы в DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



