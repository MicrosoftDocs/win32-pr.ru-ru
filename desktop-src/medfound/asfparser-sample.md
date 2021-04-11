---
description: Пример Асфпарсер
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: Пример Асфпарсер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159b481e22d77b0bee9adccbbb74073398c12b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262823"
---
# <a name="asfparser-sample"></a>Пример Асфпарсер

Показывает, как анализировать данные из ASF-файла с помощью компонентов ASF нижнего уровня в Media Foundation. В этом примере демонстрируются следующие задачи:

-   Перечисление потоков аудио и видео в файле ASF.
-   Выбор аудио-или видеопотока для анализа.
-   Поиск пакета в требуемое время воспроизведения.
-   Создание сжатых образцов для выбранного потока.
-   Декодирование образцов аудио и видео.

## <a name="apis-demonstrated"></a>Продемонстрированные API

В этом образце демонстрируются следующие интерфейсы Microsoft Media Foundation:

-   [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [**имфасфиндексер**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [**имфасфсплиттер**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a>Использование

1.  Чтобы открыть файл ASF, нажмите кнопку " **Открыть файл мультимедиа...** ".
2.  Выберите файл ASF и нажмите кнопку **Открыть**. Сведения о файле отображаются на **информационной** панели.
3.  В разделе **Конфигурация средства синтаксического анализа** выберите поток для синтаксического анализа.
4.  Чтобы создать образцы в обратную, выберите **обратить**.
5.  Чтобы указать начальную точку, перетащите ползунок в нужное место.
6.  Чтобы начать анализ, нажмите кнопку **создать образцы** . Сведения о примерах показаны на **информационной** панели.
7.  Чтобы проверить образцы для аудиопотока, нажмите кнопку **тестовый звук** .
8.  Чтобы проверить образцы для видеопотока, нажмите кнопку **Показывать растровое изображение** .

## <a name="requirements"></a>Требования



| Продукт                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Загрузка образца

Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Примеры пакетов SDK Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Поддержка ASF в Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Руководство. чтение файла ASF](tutorial--reading-an-asf-file.md)
</dt> <dt>

[Компоненты ASF Вмконтаинер](wmcontainer-asf-components.md)
</dt> </dl>

 

 



