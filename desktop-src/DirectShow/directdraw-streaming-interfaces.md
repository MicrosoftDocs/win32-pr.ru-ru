---
description: Интерфейсы потоковой передачи DirectDraw
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: Интерфейсы потоковой передачи DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc922bfed03fd2fac3581168bda35f072871a52
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072233"
---
# <a name="directdraw-streaming-interfaces"></a>Интерфейсы потоковой передачи DirectDraw

> [!Note]  
> Эти API-интерфейсы являются устаревшими. Приложения должны использовать [**образец фильтра захвата**](sample-grabber-filter.md) или реализовать настраиваемый фильтр для получения данных из графа фильтра DirectShow.

 

При использовании в потоках форматов видео, поддерживаемых DirectDraw, следующие интерфейсы предоставляют более мощный контроль над данными, чем более универсальные базовые интерфейсы.



| Интерфейс                                                  | Описание                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**идиректдравмедиастреам**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Задает и получает формат потока и объект DirectDraw, связанный с потоком мультимедиа. Этот интерфейс является производным от [**имедиастреам**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream). Этот интерфейс также можно использовать для создания видеороликов. |
| [**идиректдравстреамсампле**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Позволяет подключать образцы видео к поверхности DirectDraw; Этот интерфейс является производным от интерфейса [**истреамсампле**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) . Каждая Присоединенная область содержит прямоугольник обрезки для упрощения отрисовки. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Список интерфейсов потоковой передачи мультимедиа](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



