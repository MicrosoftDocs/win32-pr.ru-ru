---
description: В этом разделе описывается написание пользовательского Media Foundation преобразования (MFT).
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Запись пользовательского MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c113867c719fc9c8512b5b0e1172ee0694e3905
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471660"
---
# <a name="writing-a-custom-mft"></a>Запись пользовательского MFT

В этом разделе описывается написание пользовательского Media Foundation преобразования (MFT).

## <a name="mft-checklist"></a>Контрольный список MFT

При реализации пользовательского MFT используйте следующий контрольный список, чтобы определить требования.




| | | Все МФТС | Все МФТС должны реализовывать <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>имфтрансформ</strong></a>.<br /> Следующие разделы содержат дополнительные сведения о реализации этого интерфейса:<ul><li><a href="basic-mft-processing-model.md">Базовая модель обработки MFT</a></li><li><a href="time-stamps-and-durations.md">Метки времени и длительности</a></li><li><a href="handling-stream-changes.md">Обработка изменений в потоке</a></li></ul><br /> | | Кодировщики и декодеры | Требования. см. статью <a href="implementing-a-codec-mft.md">Реализация кодека MFT</a>.<br /> Рекомендуется: реализуйте <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>имфкуалитядвисе</strong></a> или <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>для поддержки уведомлений качества обслуживания (QoS).<br /> | | Видеодекодеры и обработчики видео | Необязательно: поддержка ускорения видео DirectX.<br /><ul><li><a href="direct3d-aware-mfts.md">МФТС с поддержкой Direct3D</a></li><li><a href="supporting-dxva-2-0-in-media-foundation.md">Поддержка ДКСВА 2,0 в Media Foundation</a></li></ul> | | Аппаратные кодеки | См. раздел <a href="hardware-mfts.md">Hardware МФТС</a>. | | Чтобы сделать таблицу MFT обнаруживаемой для приложений... | См. раздел <a href="registering-and-enumerating-mfts.md">Регистрация и перечисление МФТС</a>. | | Асинхронная обработка данных | Модель MFT по умолчанию использует синхронные (блокирующие) вызовы для обработки данных. Для некоторых МФТС асинхронная обработка может быть более эффективной. Однако его также сложнее реализовать.<br /> Дополнительные сведения см. в разделе <a href="asynchronous-mfts.md">асинхронная МФТС</a>.<br /> | | Управление скоростью, хитрой режим или обратная воспроизведение | См. раздел <a href="implementing-rate-control.md">Реализация управления скоростью</a>. | | Если таблица MFT создает потоки... | Реализуйте интерфейс <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>имфреалтимеклиент</strong></a> . | | Если в MFT есть ограничения лицензирования... | Рассмотрите возможность использования механизма использования поля. См. <a href="field-of-use-restrictions.md">поле ограничения использования</a>. | | При переносе существующего объекта мультимедиа DirectX (DMO)... | См. раздел <a href="comparison-of-mfts-and-dmos.md">Сравнение МФТС и дмос</a>. | 




 

В этом разделе рассматриваются следующие вопросы.

-   [Метки времени и длительности](time-stamps-and-durations.md)
-   [Обработка изменений в потоке](handling-stream-changes.md)
-   [Реализация MFT кодека](implementing-a-codec-mft.md)
-   [МФТС с поддержкой Direct3D](direct3d-aware-mfts.md)
-   [Оборудование МФТС](hardware-mfts.md)
-   [Успешный кодек](codec-merit.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Преобразования Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 




