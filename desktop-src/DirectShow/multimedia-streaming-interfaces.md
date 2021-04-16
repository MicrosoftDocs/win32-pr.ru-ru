---
description: Интерфейсы потоковой передачи мультимедиа
ms.assetid: 53d639e2-8717-4552-b0d3-b8c500bd38a8
title: Интерфейсы потоковой передачи мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d654bae73ee822f553a1494e3b374cf35b8ac4a1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547439"
---
# <a name="multimedia-streaming-interfaces"></a>Интерфейсы потоковой передачи мультимедиа

> [!Note]  
> Эти API-интерфейсы являются устаревшими. Приложения должны использовать [**образец фильтра захвата**](sample-grabber-filter.md) или реализовать настраиваемый фильтр для получения данных из графа фильтра DirectShow.

 

Этот раздел содержит справочные сведения обо всех интерфейсах потоковой передачи мультимедиа и их методах, включая те, которые поддерживает Microsoft DirectShow.



| Интерфейс                                                  | Описание                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иаммедиастреам**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream)                   | Обрабатывает внутренние соединения между фильтрами DirectShow и графами фильтров в приложениях, использующих потоковую передачу мультимедиа.                            |
| [**иаммедиатипесампле**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample)           | Содержит методы для управления примерами потока с произвольными типами мультимедиа.                                                                            |
| [**иаммедиатипестреам**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream)           | Содержит методы для создания потоков мультимедиа с произвольными типами мультимедиа.                                                                            |
| [**иаммултимедиастреам**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream)         | Предоставляет функциональные возможности DirectShow для разработчиков потоковых потоков мультимедиа.                                                                                       |
| [**иаудиодата**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                           | Предоставляет методы, позволяющие приложениям устанавливать и получать базовые звуковые данные, на которые будут ссылаться звуковые потоки.                                   |
| [**иаудиомедиастреам**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)             | Управляет потоками аудио мультимедиа, предоставляя методы, которые задают и получают формат потока.                                                                 |
| [**иаудиостреамсампле**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample)           | Получает сведения из базовых объектов данных [**иаудиодата**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) .                                                                |
| [**идиректдравмедиастреам**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Управляет потоками мультимедиа, которые отображаются на поверхностях® Microsoft® DirectDraw.                                                                                  |
| [**идиректдравстреамсампле**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Предоставляет методы, которые устанавливают и извлекают указатели на поверхность DirectDraw, связанную с примером текущего потока.                                    |
| [**имедиастреам**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)                       | Предоставляет доступ к характеристикам потока мультимедиа, например типу носителя потока и ИДЕНТИФИКАТОРу цели. У него также есть методы, создающие образцы данных. |
| [**имедиастреамфилтер**](/previous-versions/windows/desktop/api/amstream/nn-amstream-imediastreamfilter)           | Поддерживается фильтром потоков мультимедиа, который внутренне используется объектом потока мультимедиа. .                                                       |
| [**имеморидата**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)                         | Содержит методы, которые устанавливают и извлекают данные памяти для объектов звуковых данных.                                                                               |
| [**имултимедиастреам**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)             | Предоставляет методы, управляющие потоком мультимедиа и обеспечивающие доступ к его базовым потокам мультимедиа.                                                   |
| [**истреамсампле**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)                     | Предоставляет контроль над поведением образцов потоков.                                                                                                   |



 

 

 



