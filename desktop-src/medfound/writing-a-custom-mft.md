---
description: В этом разделе описывается написание пользовательского Media Foundation преобразования (MFT).
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Запись пользовательского MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15b9d5ae655ba67d4a526aeb8a82eb9d3912da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910188"
---
# <a name="writing-a-custom-mft"></a>Запись пользовательского MFT

В этом разделе описывается написание пользовательского Media Foundation преобразования (MFT).

## <a name="mft-checklist"></a>Контрольный список MFT

При реализации пользовательского MFT используйте следующий контрольный список, чтобы определить требования.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Все МФТС</td>
<td>Все МФТС должны реализовывать <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>имфтрансформ</strong></a>.<br/> Следующие разделы содержат дополнительные сведения о реализации этого интерфейса:
<ul>
<li><a href="basic-mft-processing-model.md">Базовая модель обработки MFT</a></li>
<li><a href="time-stamps-and-durations.md">Метки времени и длительности</a></li>
<li><a href="handling-stream-changes.md">Обработка изменений в потоке</a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Кодировщики и декодеры</td>
<td>Требования. см. статью <a href="implementing-a-codec-mft.md">Реализация кодека MFT</a>.<br/> Рекомендуется: реализуйте <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>имфкуалитядвисе</strong></a> или <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>для поддержки уведомлений качества обслуживания (QoS).<br/></td>
</tr>
<tr class="odd">
<td>Видеодекодеры и обработчики видео</td>
<td>Необязательно: поддержка ускорения видео DirectX.<br/>
<ul>
<li><a href="direct3d-aware-mfts.md">МФТС с поддержкой Direct3D</a></li>
<li><a href="supporting-dxva-2-0-in-media-foundation.md">Поддержка ДКСВА 2,0 в Media Foundation</a></li>
</ul></td>
</tr>
<tr class="even">
<td>Аппаратные кодеки</td>
<td>См. раздел <a href="hardware-mfts.md">Hardware МФТС</a>.</td>
</tr>
<tr class="odd">
<td>Чтобы сделать таблицу MFT обнаруживаемой для обнаружения приложениями...</td>
<td>См. раздел <a href="registering-and-enumerating-mfts.md">Регистрация и перечисление МФТС</a>.</td>
</tr>
<tr class="even">
<td>Асинхронная обработка данных</td>
<td>Модель MFT по умолчанию использует синхронные (блокирующие) вызовы для обработки данных. Для некоторых МФТС асинхронная обработка может быть более эффективной. Однако его также сложнее реализовать.<br/> Дополнительные сведения см. в разделе <a href="asynchronous-mfts.md">асинхронная МФТС</a>.<br/></td>
</tr>
<tr class="odd">
<td>Управление скоростью, хитрость или обратная воспроизведение</td>
<td>См. раздел <a href="implementing-rate-control.md">Реализация управления скоростью</a>.</td>
</tr>
<tr class="even">
<td>Если таблица MFT создает потоки...</td>
<td>Реализуйте интерфейс <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>имфреалтимеклиент</strong></a> .</td>
</tr>
<tr class="odd">
<td>Если в MFT есть ограничения лицензирования...</td>
<td>Рассмотрите возможность использования механизма использования поля. См. <a href="field-of-use-restrictions.md">поле ограничения использования</a>.</td>
</tr>
<tr class="even">
<td>При переносе существующего объекта мультимедиа DirectX (DMO)...</td>
<td>См. раздел <a href="comparison-of-mfts-and-dmos.md">Сравнение МФТС и дмос</a>.</td>
</tr>
</tbody>
</table>



 

В этом разделе рассматриваются следующие вопросы.

-   [Метки времени и длительности](time-stamps-and-durations.md)
-   [Обработка изменений в потоке](handling-stream-changes.md)
-   [Реализация MFT кодека](implementing-a-codec-mft.md)
-   [МФТС с поддержкой Direct3D](direct3d-aware-mfts.md)
-   [Оборудование МФТС](hardware-mfts.md)
-   [Успешный кодек](codec-merit.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Преобразования Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 




