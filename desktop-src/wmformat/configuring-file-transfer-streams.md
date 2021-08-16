---
title: настройка Потоки для перемещения файлов
description: настройка Потоки для перемещения файлов
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
ms.openlocfilehash: 9c0be95c9760a02275e223f56785149f6867d4aaf2462d07d158991b3cd21c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849067"
---
# <a name="configuring-file-transfer-streams"></a>настройка Потоки для перемещения файлов

Для потоков передачи файлов не требуются специальные параметры в структуре [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Им требуется расширение единицы данных, чтобы связать имя файла с каждым образцом. Чтобы отправить имя с примерами передачи файлов, необходимо реализовать систему расширения единиц обработки данных для потока.

Чтобы задать расширение единицы данных для потока, выполните следующие действия.

1.  Получите указатель на интерфейс [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) объекта конфигурации потока, вызвав **Ивмстреамконфиг:: QueryInterface**.
2.  Добавьте расширение единицы данных для потока, вызвав [**IWMStreamConfig2:: адддатаунитекстенсион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) следующим образом:
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**общая конфигурация для всех Потоки**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Настройка произвольных типов потоков**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Потоки файлов**](file-streams.md)
</dt> </dl>

 

 




