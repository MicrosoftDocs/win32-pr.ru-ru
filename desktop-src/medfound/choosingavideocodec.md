---
description: Выбор видеокодека
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Выбор видеокодека (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9186c7e7e60f5822ec2e50e3e5c7e16e96b91839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262818"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a>Выбор видеокодека (Microsoft Media Foundation)

Кодировщик Windows Media Video 9 поддерживает три категории закодированных выходных данных: основной профиль, расширенный профиль и образ. Основная категория профиля обеспечивает Видеосжатие для сложного видеоматериала, например фильмов или музыкальных видео. Функции основного профиля предоставляют широкий спектр параметров кодирования. Основной профиль можно использовать для создания видео с очень низкими скоростями для доставки на карманные устройства или, на другом конце спектра, можно использовать для создания видео с высоким уровнем четкости для цифрового кинотеатра.

Выделение алгоритмов кодирования в основном профиле осуществляется на динамическом видеоматериале, но они подходят и для других видеоматериалов. Основной профиль должен быть категорией по умолчанию для содержимого видео. Для удовлетворения конкретных потребностей можно использовать категорию расширенного профиля, категорию образа или отдельный кодировщик, называемый кодировщиком экрана Windows Media Video 9. В следующей таблице перечислены четыре варианта.



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
<td><a href="windowsmediavideo9encoder.md">Кодировщик Windows Media Video 9</a><dl> Профиль Main<br />
</dl></td>
</tr>
<tr class="even">
<td>Кодирование видео или видео с высоким определением, которое соответствует расширенному профилю VC-1 SMPTE Standard</td>
<td><a href="windowsmediavideo9encoder.md">Кодировщик Windows Media Video 9</a><dl> Расширенный профиль<br />
</dl></td>
</tr>
<tr class="odd">
<td>Преобразование растровых изображений в динамическое видео</td>
<td><a href="windowsmediavideo9encoder.md">Кодировщик Windows Media Video 9</a><dl> Образ<br />
</dl></td>
</tr>
<tr class="even">
<td>Кодирование компьютера — видео приложения (снимок экрана) или другое очень статическое видео</td>
<td><a href="windowsmediavideo9screenencoder.md"><strong>Кодировщик экрана Windows Media видео 9</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Работа с видео](workingwithvideo.md)
</dt> </dl>

 

 



