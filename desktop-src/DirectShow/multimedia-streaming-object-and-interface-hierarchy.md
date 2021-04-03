---
description: Объект потоковой передачи мультимедиа и иерархия интерфейсов
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Объект потоковой передачи мультимедиа и иерархия интерфейсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52339644730139af22fd21fa2c24b8448a1afaf3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914228"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a>Объект потоковой передачи мультимедиа и иерархия интерфейсов

> [!Note]  
> Эти API-интерфейсы являются устаревшими. Приложения должны использовать [**образец фильтра захвата**](sample-grabber-filter.md) или реализовать настраиваемый фильтр для получения данных из графа фильтра DirectShow.

 

На следующей диаграмме показана иерархия объектов, используемая в потоковой передаче мультимедиа.

![Иерархия объектов мултимедиастреаминг](images/mmstream02.png)

Архитектура потоковой передачи мультимедиа определяет три общих типа объектов:

-   Объект **аммултимедиастреам** предоставляет интерфейс [**иаммултимедиастреам**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) . На внутреннем уровне этот объект служит оболочкой для графа фильтра DirectShow.
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

 

 



