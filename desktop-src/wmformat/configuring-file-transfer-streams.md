---
title: Настройка потоков обмена файлами
description: Настройка потоков обмена файлами
ms.assetid: faed54ae-9e80-492a-9602-e726bdb3b54a
keywords:
- потоки, Настройка потоков для обмена файлами
- кодеки, Настройка потоков для обмена файлами
- потоки для перемещения файлов
- потоки, расширения модулей данных
- кодеки, расширения модулей данных
- расширения модулей данных, потоки обмена файлами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fac7d2270da82f1f9e82ed9123611ae608dd3c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069605"
---
# <a name="configuring-file-transfer-streams"></a>Настройка потоков обмена файлами

Для потоков передачи файлов не требуются специальные параметры в структуре [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Им требуется расширение единицы данных, чтобы связать имя файла с каждым образцом. Чтобы отправить имя с примерами передачи файлов, необходимо реализовать систему расширения единиц обработки данных для потока.

Чтобы задать расширение единицы данных для потока, выполните следующие действия.

1.  Получите указатель на интерфейс [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) объекта конфигурации потока, вызвав **Ивмстреамконфиг:: QueryInterface**.
2.  Добавьте расширение единицы данных для потока, вызвав [**IWMStreamConfig2:: адддатаунитекстенсион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) следующим образом:
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Общая конфигурация для всех потоков**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Настройка произвольных типов потоков**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Файловые потоки**](file-streams.md)
</dt> </dl>

 

 




