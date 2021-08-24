---
title: Поиск маркеров
description: Поиск маркеров
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- Расширенный системный формат (ASF), Поиск маркеров
- ASF (Расширенный системный формат), Поиск маркеров
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- Расширенный формат систем (ASF), маркеры
- ASF (Расширенный системный формат), маркеры
- асинхронные читатели, Поиск маркеров
- асинхронные читатели, маркеры
- маркеры, Поиск
- маркеры, асинхронные читатели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3361546f4087e0c2104809435d9d75e8711560ec4f3c55855d14b05ef4dfb8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807354"
---
# <a name="to-seek-to-markers"></a>Поиск маркеров

Маркер — это именованное расположение в файле ASF. Воспроизведение можно запустить только из расположения маркера с помощью асинхронного модуля чтения. Чтобы начать воспроизведение на маркере, выполните следующие действия.

1.  Вызовите метод **ивмреадер:: QueryInterface** , чтобы получить указатель на интерфейс [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) .
2.  Получите общее число маркеров в файле, вызвав [**ивмхеадеринфо:: жетмаркеркаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).
3.  Пройдите по маркерам, используя счетчик маркеров, полученный на шаге 2. Извлеките имя и время каждого маркера, вызвав [**ивмхеадеринфо:: Mark**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) для каждого из них. Сохраните индекс нужного маркера.
4.  Вызовите метод **ивмреадер:: QueryInterface** , чтобы получить указатель на интерфейс [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) .
5.  Укажите маркер, с которого следует начать воспроизведение, вызвав [**IWMReaderAdvanced2:: стартатмаркер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker). Необходимо передать индекс нужного маркера, который был сохранен на шаге 3.
6.  Обработайте примеры, как обычно в реализации метода [**ивмреадеркаллбакк:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Метки**](markers.md)
</dt> <dt>

[**Чтение файлов с помощью асинхронного модуля чтения**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Работа с индексами**](working-with-indexes.md)
</dt> </dl>

 

 




