---
description: Фильтр разделителя потока MPEG-1
ms.assetid: abadf37f-2876-496d-90e7-77c3475a0064
title: Фильтр разделителя потока MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec47e5ad8df16446c588beec2c5d1c2606b9b1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140466"
---
# <a name="mpeg-1-stream-splitter-filter"></a>Фильтр разделителя потока MPEG-1

Этот фильтр разделяет системный поток MPEG-1 в его компонентах аудио-и видеопотоках.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>Иаммедиаконтент</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>иамстреамселект</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td>Основной тип: MEDIATYPE_Stream<br/> Подтипы<br/>
<ul>
<li>MEDIASUBTYPE_MPEG1System</li>
<li>MEDIASUBTYPE_MPEG1VideoCD</li>
<li>MEDIASUBTYPE_Audio</li>
<li>MEDIASUBTYPE_Video</li>
</ul>
См. раздел <a href="mpeg-1-media-types.md"> <strong>типы носителей MPEG-1</strong></a><br/></td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td>Основной тип: MEDIATYPE_Audio или MEDIATYPE_Video<br/> Подтип: MEDIASUBTYPE_MPEG1Payload или MEDIASUBTYPE_MPEG1Packet<br/> См. раздел <a href="mpeg-1-media-types.md"> <strong>типы носителей MPEG-1</strong></a><br/></td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>имедиасикинг</strong></a></td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>CLSID_MPEG1Splitter</td>
</tr>
<tr class="odd">
<td>CLSID страницы свойств</td>
<td>Нет страницы свойств</td>
</tr>
<tr class="even">
<td>Исполняемый объект</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Заслуживают</a></td>
<td>MERIT_NORMAL</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Категория фильтра</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Комментарии

Этот файл поддерживает режим Pull только через [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Он не поддерживает режим принудительной отправки.

Так как содержимое MPEG-1 не индексируется, поиск может быть очень приблизительным. Обычно это удобно для фиксированной скорости системного потока MPEG-1 (обычно это оборудование, создаваемое для компакт-диска видео).

Фильтр поддерживает интерфейс [**иаммедиаконтент**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) для получения метаданных ID3.

Не все примеры MPEG имеют отметки времени. Отсутствие метки времени в образце MPEG не является ошибкой. Для разработчиков фильтров это означает, что не следует возвращать код ошибки из метода **Receive** входного ПИН-кода, если [**имедиасампле::-Time**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) завершается ошибкой. Если **Receive** возвращает любое значение, отличное от S \_ , это приведет к тому, что разделитель перестанет отправлять образцы.

Если файл содержит поток видео, разделитель потока MPEG-1 поддерживает поиск по номеру кадра. Чтобы включить поиск на основе кадров, вызовите [**имедиасикинг:: сеттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) в [диспетчере графов фильтров](filter-graph-manager.md) со значением **\_ \_ кадр формата времени**.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 




