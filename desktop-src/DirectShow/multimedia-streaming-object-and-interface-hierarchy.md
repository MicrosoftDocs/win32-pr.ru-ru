---
description: Объект потоковой передачи мультимедиа и иерархия интерфейсов
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Объект потоковой передачи мультимедиа и иерархия интерфейсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b73da4777c2d05ff6455758ebde6e64a9a4c8277e8445ed59dca7f17088baea0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075780"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a>Объект потоковой передачи мультимедиа и иерархия интерфейсов

> [!Note]  
> Эти API-интерфейсы являются устаревшими. приложения должны использовать [**образец фильтра захвата**](sample-grabber-filter.md) или реализовать настраиваемый фильтр для получения данных из графа фильтра DirectShow.

 

На следующей диаграмме показана иерархия объектов, используемая в потоковой передаче мультимедиа.

![Иерархия объектов мултимедиастреаминг](images/mmstream02.png)

Архитектура потоковой передачи мультимедиа определяет три общих типа объектов:

-   Объект **аммултимедиастреам** предоставляет интерфейс [**иаммултимедиастреам**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) . на внутреннем уровне этот объект служит оболочкой для DirectShow графа фильтра.
-   Объекты *потока мультимедиа* предоставляют интерфейс [**имедиастреам**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) и являются специфичными для данных. Объект Аммултимедиастреам содержит один или несколько потоков мультимедиа.
-   *Образцы объектов Stream* содержат данные для определенного потока.

Поддерживаются следующие объекты потока мультимедиа:

-   Аудиопоток. Предоставляет интерфейс [**иаудиомедиастреам**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) .
-   Поток DirectDraw. Представляет поток видео, отображаемый на поверхности DirectDraw. Предоставляет интерфейс [**идиректдравмедиастреам**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) .
-   Поток типа мультимедиа. Представляет произвольные данные. Предоставляет интерфейс [**иаммедиатипестреам**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) .

Каждый объект потока мультимедиа создает свой собственный образец объекта Stream:

-   Звуковые потоки создают образцы звука, которые предоставляют интерфейс [**иаудиостреамсампле**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) .
-   В потоках DirectDraw создаются примеры DirectDraw, которые предоставляют интерфейс [**идиректдравстреамсампле**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) .
-   Потоки типа мультимедиа создают образцы типов носителей, которые предоставляют интерфейс [**иаммедиатипесампле**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) .

На следующей диаграмме показана иерархия интерфейсов для интерфейсов, перечисленных ранее.

![Иерархия интерфейса мултимедиастреаминг](images/mmstream01.png)

 

 



