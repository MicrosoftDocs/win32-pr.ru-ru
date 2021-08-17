---
description: Фильтр DVD Navigator
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: Фильтр DVD Navigator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a395001daeac5f90be85bea972d1d4f118198ee4343960cb4eed0d958e1677aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016012"
---
# <a name="dvd-navigator-filter"></a>Фильтр DVD Navigator

Фильтр "Навигатор DVD" является фильтром источников для диаграммы фильтра воспроизведения DVD-Video. Он открывает все необходимые файлы в DVD-Video томе, выполняет переходы по линейным DVD-Video. VOB-файлам и анализирует полученный поток программы MPEG-2, разбивая поток на три (видео, аудио, субтитры) выходного контакта.

Фильтр навигатора по DVD также реализует интерфейсы [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) и [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) , позволяющие приложению воспроизведения DVD управлять DVD-Video воспроизведения.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>ифилесаурцефилтер</strong></a>, <strong>испеЦифипропертипажес</strong></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td>Неприменимо.</td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td>Базовые типы:<br/>
<ul>
<li>Видео: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li>Аудио: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li>Подизображение: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
</ul>
Расширенные типы:<br/> Видео:<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
</ul>
Звук:<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
</ul>
Субтитров<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
<li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
</ul>
Чтобы включить расширенные типы, вызовите метод <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2:: SetOption</strong></a> и установите для свойства <br/></td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>CLSID_DVDNavigator</td>
</tr>
<tr class="odd">
<td>CLSID страницы свойств</td>
<td>Нет страницы свойств.</td>
</tr>
<tr class="even">
<td>Исполняемый объект</td>
<td>qdvd.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Заслуживают</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Категория фильтра</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> <dt>

[DVD-приложения](dvd-applications.md)
</dt> </dl>

 

 




