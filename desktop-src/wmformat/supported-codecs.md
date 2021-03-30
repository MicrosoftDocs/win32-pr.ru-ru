---
title: Поддерживаемые кодеки
description: Поддерживаемые кодеки
ms.assetid: d5907d38-2e26-442e-a0d1-1d7e267b9948
keywords:
- Windows Media Format SDK, Поддерживаемые кодеки
- Windows Media Format SDK, интерфейс IWMCodecInfo3
- Поддерживаемые кодеки
- IWMCodecInfo3, о программе
- кодеки, интерфейс IWMCodecInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac06ad3d58d066254fa666f96283dca9b8b6ae
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788832"
---
# <a name="supported-codecs"></a>Поддерживаемые кодеки

Пакет Windows Media Format SDK обеспечивает поддержку следующих кодеков, которые включаются при установке пакета SDK.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Кодек</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Media Audio</td>
<td>Аудиокодек для общего использования при кодировании сложных звуковых файлов, таких как музыка. Последние версии этого кодека — кодек Windows Media Audio 9 и кодек Windows Media Audio 9,1.<br/></td>
</tr>
<tr class="even">
<td>Windows Media Audio Professional</td>
<td>Аудиокодек для сложных аудио, например музыки. Поддерживает многоканальную и 24-разрядную кодировку. Существует две версии этого кодека:<br/>
<ul>
<li>Windows Media Audio 9 Professional</li>
<li>Windows Media Audio 9,1 Professional</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows Media Audio без потерь</td>
<td>Аудиокодек для кодирования без потерь. Существует две версии этого кодека:<br/>
<ul>
<li>Windows Media Audio 9 без потерь</li>
<li>Windows Media Audio 9,1 без потерь</li>
</ul></td>
</tr>
<tr class="even">
<td>Голосовая связь Windows Media Audio 9</td>
<td>Аудиокодек, оптимизированный для кодирования человеческого голоса при высоком коэффициенте сжатия. Это предпочтительный кодек для потоков, состоящих в основном на произнесенных словах. Для содержимого, которое является смешанной музыкой и речью, этот кодек может динамически изменять алгоритм кодирования, используемый для достижения оптимального качества.</td>
</tr>
<tr class="odd">
<td>Windows Media Video 9</td>
<td>Видеокодек для общего использования при кодировании сложных видео, например фильмов.</td>
</tr>
<tr class="even">
<td>Расширенный профиль Windows Media Video 9</td>
<td>Видеокодек, включающий расширенные возможности кодирования, включая чередование кодирования.</td>
</tr>
<tr class="odd">
<td>Экран Windows Media видео 9</td>
<td>Видеокодек, оптимизированный для кодирования последовательных снимков экрана. Этот кодек часто используется для обучения программного обеспечения или поддержки путем записи образов мониторов при использовании компьютерных приложений.</td>
</tr>
<tr class="even">
<td>Изображение Windows Media Video</td>
<td>Видеокодек для преобразования растровых изображений с информацией об отсчете в сжатое видео. Существует две версии этого кодека:<br/>
<ul>
<li>Образ Windows Media видео 9</li>
<li>Windows Media Video 9, образ v2</li>
</ul></td>
</tr>
</tbody>
</table>



 

Различные версии кодеков аудио и видео Windows Media доступны для кодирования в зависимости от установленной версии пакета SDK Windows Media Format. При использовании методов, если интерфейс [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) для перечисления кодеков и форматов кодеков, перечисляются только последние Поддерживаемые версии.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Выбор метода кодирования**](choosing-an-encoding-method.md)
</dt> <dt>

[**Функции кодеков**](codec-features.md)
</dt> </dl>

 

 





