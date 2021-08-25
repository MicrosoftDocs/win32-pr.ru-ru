---
description: Интерфейсы потоковой передачи аудио
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Интерфейсы потоковой передачи аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1087ab127258fcd4f587cdd029d4604c35524689b5f0877476e1137e2ed924eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824474"
---
# <a name="audio-streaming-interfaces"></a>Интерфейсы потоковой передачи аудио

> [!Note]  
> Эти API-интерфейсы являются устаревшими. приложения должны использовать [**образец фильтра захвата**](sample-grabber-filter.md) или реализовать настраиваемый фильтр для получения данных из графа фильтра DirectShow.

 



| Интерфейс                                        | Описание                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иаудиомедиастреам**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | Управляет потоками аудио мультимедиа. Этот интерфейс наследуется от интерфейса [**имедиастреам**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) и используется для создания одного или нескольких объектов [**иаудиостреамсампле**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) . Он также используется для задания и получения текущего формата потоковых данных.                                                                                                            |
| [**иаудиостреамсампле**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | Получает сведения из базовых объектов данных [**иаудиодата**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) .                                                                                                                                                                                                                                                                                                        |
| [**имеморидата**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | Содержит методы, которые устанавливают и извлекают данные памяти для объектов звуковых данных. Объекты звуковых данных предоставляют базовые данные, доступ к которым осуществляется с помощью Streaming Samples. Этот интерфейс предоставляет способ инициализации буферов памяти и установки фактических объемов звуковых данных в объектах. Кроме того, метод [**имеморидата:: info**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) можно использовать для получения данных о звуковой памяти. |
| [**иаудиодата**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | Предоставляет методы, позволяющие приложениям устанавливать и получать базовые звуковые данные, на которые будут ссылаться звуковые потоки. Формат звуковых данных задается в структуре [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Список интерфейсов потоковой передачи мультимедиа](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
