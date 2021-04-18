---
description: В этом разделе описывается общий дизайн Microsoft Media Foundation. Сведения об использовании Media Foundation для конкретных задач программирования см. в разделе Media Foundation Guide по программированию.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Архитектура Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0914b0f4c43966edcdc6d30efa7c9dbdbbd4e8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105720043"
---
# <a name="media-foundation-architecture"></a>Архитектура Media Foundation

В этом разделе описывается общий дизайн Microsoft Media Foundation. Сведения об использовании Media Foundation для конкретных задач программирования см. в разделе [Media Foundation Guide по программированию](media-foundation-programming-guide.md).

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                                         | Описание                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Общие сведения об архитектуре Media Foundation](overview-of-the-media-foundation-architecture.md)<br/> | Предоставляет высокоуровневый обзор архитектуры Media Foundation.<br/>                                                                                                                                                                                                               |
| [Примитивы Media Foundation](media-foundation-primitives.md)<br/>                                     | Описание некоторых основных интерфейсов, используемых в Media Foundation.<br/> Почти все Media Foundation приложения будут использовать эти интерфейсы.<br/>                                                                                                                       |
| [Media Foundation API платформы](media-foundation-platform-apis.md)<br/>                               | Описание основных функций Media Foundation, таких как асинхронные обратные вызовы и рабочие очереди.<br/> Некоторые приложения могут использовать интерфейсы уровня платформы. Кроме того, Пользовательские подключаемые модули, такие как источники мультимедиа и МФТС, используют эти интерфейсы.<br/>                                       |
| [Конвейер Media Foundation](media-foundation-pipeline.md)<br/>                                         | Media Foundationный уровень конвейера состоит из источников мультимедиа, МФТС и приемников мультимедиа. Большинство приложений не вызывают методы непосредственно на уровне конвейера. Вместо этого приложения используют один из более высоких уровней, например сеанс мультимедиа или модуль чтения исходного кода и модуль записи приемника.<br/> |
| [Сеанс мультимедиа](media-session.md)<br/>                                                                 | Сеанс мультимедиа управляет потоком данных в конвейере Media Foundation.<br/>                                                                                                                                                                                                           |
| [Модуль чтения исходного кода](source-reader.md)<br/>                                                                 | Модуль чтения исходного кода позволяет приложению получать данные из источника мультимедиа без необходимости непосредственно вызывать API источника мультимедиа. Модуль чтения исходного кода может также выполнять декодирование сжатых потоков.<br/>                                                            |
| [Путь к защищенному носителю](protected-media-path.md)<br/>                                                   | Защищенный путь к носителю (PMP) предоставляет защищенную среду для воспроизведения видеоматериалов уровня "Премиум". Необязательно использовать PMP при написании приложения Media Foundation. <br/>                                                                                             |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[О Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Media Foundation: основные понятия](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Media Foundation и COM](media-foundation-and-com.md)
</dt> <dt>

[Media Foundationое программное руководством](media-foundation-programming-guide.md)
</dt> </dl>

 

 




