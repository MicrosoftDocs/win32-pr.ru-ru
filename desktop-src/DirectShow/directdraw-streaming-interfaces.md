---
description: Интерфейсы потоковой передачи DirectDraw
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: Интерфейсы потоковой передачи DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11e7eec0ec7ad82c0046b8c052ff00093b496c05495ec38590d201724d7620e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983054"
---
# <a name="directdraw-streaming-interfaces"></a>Интерфейсы потоковой передачи DirectDraw

> [!Note]  
> Эти API-интерфейсы являются устаревшими. приложения должны использовать [**образец фильтра захвата**](sample-grabber-filter.md) или реализовать настраиваемый фильтр для получения данных из графа фильтра DirectShow.

 

При использовании в потоках форматов видео, поддерживаемых DirectDraw, следующие интерфейсы предоставляют более мощный контроль над данными, чем более универсальные базовые интерфейсы.



| Интерфейс                                                  | Описание                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**идиректдравмедиастреам**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Задает и получает формат потока и объект DirectDraw, связанный с потоком мультимедиа. Этот интерфейс является производным от [**имедиастреам**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream). Этот интерфейс также можно использовать для создания видеороликов. |
| [**идиректдравстреамсампле**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Позволяет подключать образцы видео к поверхности DirectDraw; Этот интерфейс является производным от интерфейса [**истреамсампле**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) . Каждая Присоединенная область содержит прямоугольник обрезки для упрощения отрисовки. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Список интерфейсов потоковой передачи мультимедиа](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



