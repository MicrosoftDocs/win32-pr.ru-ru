---
description: Поддержка ASF в Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: Поддержка ASF в Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db06c5a294e351b09d7f5327e8ee22891798671765bc5cc10eafd75785debde9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880965"
---
# <a name="asf-support-in-media-foundation"></a>Поддержка ASF в Media Foundation

Media Foundation поддерживает файлы мультимедиа в формате ASF:

-   Windows Мультимедийное видео (файлы WMV)
-   Windows Media Audio (WMA-файлы)

Media Foundation предоставляет несколько объектов для чтения и записи файлов ASF. Эти объекты предоставляются на двух разных архитектурных уровнях.

Во-первых, уровень *конвейера* содержит объекты, которые работают внутри [конвейера Media Foundation](media-foundation-pipeline.md) и соответствуют интерфейсам API, определенным в конвейере. Слой конвейера ASF содержит:

-   [Источник носителя ASF](asf-media-source.md): АНАЛИЗИРУЕТ файлы ASF и доставляет пакеты аудио-и видеоданных.
-   [Windows мультимедийные кодеки](windows-media-codecs.md): декодирование или кодирование Windows потоков аудио или видео.
-   [Приемник мультимедиа ASF](asf-media-sinks.md): получает пакеты данных и записывает файл ASF.

Во-вторых, уровень контейнера WM обеспечивает низкоуровневый контроль над синтаксическим анализом и записью файла ASF. Уровень конвейера использует Вмконтаинер внутренним образом. Приложения также могут использовать Вмконтаинер для анализа и записи в формате ASF низкого уровня.

![Диаграмма, на которой показаны элементы уровня конвейера и контейнера WM](images/asf-components.png)

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                         | Описание                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Структура файла ASF](asf-file-structure.md)<br/>                       | Общие сведения о структуре файлов ASF и объектах, предоставляемых Media Foundation для работы с файлами ASF.<br/> |
| [Компоненты ASF уровня конвейера](pipeline-layer-asf-components.md)<br/> | Описывает, как анализировать и создавать файлы ASF с помощью уровня конвейера.<br/>                                   |
| [Компоненты ASF Вмконтаинер](wmcontainer-asf-components.md)<br/>       | Описывает, как анализировать и создавать файлы ASF с помощью слоя Вмконтаинер.<br/>                                |



 

Подробные сведения о структуре файла ASF см. в спецификации ASF, которую можно загрузить с [веб-сайта Майкрософт](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Media Foundationое программное руководством](media-foundation-programming-guide.md)
</dt> </dl>

 

 




