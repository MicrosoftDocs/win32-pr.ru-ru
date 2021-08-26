---
description: Временная шкала
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: Временная шкала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f298c2649a280bf5fd622d5fb5a2aef820d1f340d45f7e2beb83fe9edd6a402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050004"
---
# <a name="the-timeline"></a>Временная шкала

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

Временная шкала предоставляет интерфейс [**иамтимелине**](iamtimeline.md) . Этот интерфейс содержит методы для задания свойств на временной шкале. для добавления групп на временную шкалу; и для создания объектов временной шкалы, таких как группы, дорожки и источники. Чтобы создать новую временную шкалу, вызовите стандартную функцию **CoCreateInstance** следующим образом:


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



Новая временная шкала пуста. на этом этапе можно загрузить существующий файл проекта (см. раздел [загрузка и просмотр Project](loading-and-previewing-a-project.md)) или создать временную шкалу путем создания и вставки новых объектов (см. раздел [конструирование временной шкалы](constructing-a-timeline.md)).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Общие сведения о компонентах временной шкалы](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



