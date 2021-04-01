---
description: Разделитель MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Разделитель MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f04062660df7711a573dd17deb82f90897454a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262438"
---
# <a name="mpeg-2-splitter"></a>Разделитель MPEG-2

Начиная с Microsoft® Windows® XP, фильтр разделителя MPEG-2 является устаревшим. Вместо этого используйте [демультиплексор MPEG-2](mpeg-2-demultiplexer.md) .

На предыдущих платформах используйте разделитель MPEG-2 для потоков программы MPEG-2, доставляемых в режиме опроса, который содержит по крайней мере один из следующих типов потоков: MPEG-2 Video; Звук MPEG-2; AC3 аудио в кодировке, определенную для видео DVD; или в формате PCM, заданном для видео DVD. Этот фильтр анализирует потоки, создает выходной закрепление для каждого потока и выводит сжатые аудио-или видеопакеты MPEG в фильтр декодера MPEG-2.

Для программных и транспортных потоков, доставляемых в режиме Push-уведомлений, используйте [демультиплексор MPEG-2](mpeg-2-demultiplexer.md)на всех платформах.

> [!Note]  
> Разделитель MPEG-2 не поддерживает поиск в точном фрейме.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <strong>испеЦифипропертипажес</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>иампарсе</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>иамстреамселект</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td><ul>
<li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</li>
<li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</li>
<li>MEDIATYPE_Stream, MEDIASUBTYPE_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td>Зависит от типа потока. См. раздел <a href="mpeg-2-splitter-media-types.md">типы мультимедиа с разделителями MPEG-2</a></td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>имедиасикинг</strong></a></td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>CLSID_MMSPLITTER</td>
</tr>
<tr class="odd">
<td>CLSID страницы свойств</td>
<td>Неприменимо</td>
</tr>
<tr class="even">
<td>Исполняемый объект</td>
<td>mpg2splt.ax</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Заслуживают</a></td>
<td>MERIT_NORMAL + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Категория фильтра</a></td>
<td>CLSID_AudioInputDeviceCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> <dt>

[Использование разделителя MPEG-2](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



