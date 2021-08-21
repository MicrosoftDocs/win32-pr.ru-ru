---
description: Выбор видеокодека
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Выбор видеокодека (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b560666ddeebb88fc3bb720cbc9f1be26308e7ecd8a4ad872fbb1f0991826fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035372"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a>Выбор видеокодека (Microsoft Media Foundation)

кодировщик Windows Media Video 9 поддерживает три категории закодированных выходных данных: основной профиль, расширенный профиль и образ. Основная категория профиля обеспечивает Видеосжатие для сложного видеоматериала, например фильмов или музыкальных видео. Функции основного профиля предоставляют широкий спектр параметров кодирования. Основной профиль можно использовать для создания видео с очень низкими скоростями для доставки на карманные устройства или, на другом конце спектра, можно использовать для создания видео с высоким уровнем четкости для цифрового кинотеатра.

Выделение алгоритмов кодирования в основном профиле осуществляется на динамическом видеоматериале, но они подходят и для других видеоматериалов. Основной профиль должен быть категорией по умолчанию для содержимого видео. для удовлетворения конкретных потребностей можно использовать категорию расширенного профиля, категорию образа или отдельный кодировщик, называемый кодировщиком видео Windows Media 9. В следующей таблице перечислены четыре варианта.



<table>
<thead>
<tr class="header">
<th>Назначение</th>
<th>Кодек</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Кодировка видео общего назначения</td>
<td><a href="windowsmediavideo9encoder.md">Windows Кодировщик Media Video 9</a><dl> Профиль Main<br />
</dl></td>
</tr>
<tr class="even">
<td>Кодирование видео или видео с высоким определением, которое соответствует расширенному профилю VC-1 SMPTE Standard</td>
<td><a href="windowsmediavideo9encoder.md">Windows Кодировщик Media Video 9</a><dl> Расширенный профиль<br />
</dl></td>
</tr>
<tr class="odd">
<td>Преобразование растровых изображений в динамическое видео</td>
<td><a href="windowsmediavideo9encoder.md">Windows Кодировщик Media Video 9</a><dl> Образ<br />
</dl></td>
</tr>
<tr class="even">
<td>Кодирование компьютера — видео приложения (снимок экрана) или другое очень статическое видео</td>
<td><a href="windowsmediavideo9screenencoder.md"><strong>Windows Кодировщик экрана видео в Media 9</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Работа с видео](workingwithvideo.md)
</dt> </dl>

 

 



