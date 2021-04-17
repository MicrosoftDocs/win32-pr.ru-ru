---
description: Временная шкала
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: Временная шкала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6ac73b84409629f63ad4be469edf6b943f9e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684645"
---
# <a name="the-timeline"></a>Временная шкала

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

Временная шкала предоставляет интерфейс [**иамтимелине**](iamtimeline.md) . Этот интерфейс содержит методы для задания свойств на временной шкале. для добавления групп на временную шкалу; и для создания объектов временной шкалы, таких как группы, дорожки и источники. Чтобы создать новую временную шкалу, вызовите стандартную функцию **CoCreateInstance** следующим образом:


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



Новая временная шкала пуста. На этом этапе можно загрузить существующий файл проекта (см. статью [Загрузка и просмотр проекта](loading-and-previewing-a-project.md)) или создать временную шкалу путем создания и вставки новых объектов (см. раздел [Создание временной шкалы](constructing-a-timeline.md)).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Общие сведения о компонентах временной шкалы](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



