---
title: Поддержка кода времени SMPTE
description: Поддержка кода времени SMPTE
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- Windows Пакет SDK для формата мультимедиа, коды времени SMPTE
- Расширенный формат систем (ASF), коды времени SMPTE
- ASF (Расширенный системный формат), коды времени SMPTE
- Windows Пакет SDK для формата мультимедиа, интерфейс Ивмреадертимекоде
- Расширенный системный формат (ASF), интерфейс Ивмреадертимекоде
- ASF (Расширенный системный формат), интерфейс Ивмреадертимекоде
- Коды времени SMPTE, сведения
- ивмреадертимекоде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19e3d7a85c797a3b0247bedb2359b4b40b60e8d4f243f14e2c94175bb1e2740
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929614"
---
# <a name="smpte-time-code-support"></a>Поддержка кода времени SMPTE

пакет SDK для Windows Media Format обеспечивает ограниченную поддержку кода времени SMPTE, который является стандартным форматом кода времени для фильмов и телевизоров. В качестве расширений модулей данных можно включить данные кода времени SMPTE с примерами. Часть данных расширения — это структура [**\_ \_ \_ данных расширения времени ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) , содержащая информацию из исходной метки SMPTE Time.

Поддержание кода времени SMPTE в файлах ASF имеет ограничения производительности. Каждому образцу с соответствующей отметкой времени SMPTE требуется транспорт 14 байт в структуре метки времени. В сценарии потоковой передачи это увеличение требований к пропускной способности может быть разрушительным. В результате мы рекомендуем, чтобы коды времени SMPTE сохранялись только в файлах ASF в процессе редактирования видео, что обычно выполняется с локальными файлами. При создании окончательного файла следует удалить расширения модулей данных.

Вы можете считывать метки времени SMPTE так же, как и любые другие расширения единиц обработки данных, но объекты чтения предоставляют интегрированную поддержку поиска по коду времени SMPTE. Чтобы иметь возможность искать метки времени SMPTE, необходимо сначала индексировать файл, SMPTE код времени. Вы можете настроить индексатор для индексирования кодов времени с помощью метода [**IWMIndexer2:: Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) .

С помощью асинхронного модуля чтения можно перемещаться по файлу, SMPTE отметки времени с помощью методов интерфейса [**ивмреадертимекоде**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) и метода [**IWMReaderAdvanced3:: стартатпоситион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) . В синхронном модуле чтения используйте [**IWMSyncReader2:: сетранжебитимекоде**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Функции файлов ASF**](asf-file-features.md)
</dt> <dt>

[**Настройка расширений модуля данных**](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




