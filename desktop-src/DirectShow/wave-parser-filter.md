---
description: Фильтр синтаксического анализатора волн
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: Фильтр синтаксического анализатора волн
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91508500b02743f7cac8b4ed5cff718d12e3b03
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987857"
---
# <a name="wave-parser-filter"></a>Фильтр синтаксического анализатора волн

Фильтр средства синтаксического анализа WAVE анализирует звуковые данные в формате WAV, Au или AIF. Вышестоящий фильтр должен быть фильтром [источника асинхронного файла](file-source--async--filter.md) , фильтром [источников URL-адресов](file-source--url--filter.md) или совместимым сторонним фильтром исходного кода, который содержит звуковые данные WAV. Поток вывода — это звуковые данные, которые можно напрямую подключаться к фильтру рендеринга аудио или к промежуточному фильтру преобразования.




| Метка | Применение |
|--------|-------|
| Интерфейсы фильтра | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>Иаммедиаконтент</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>иперсистмедиапропертибаг</strong></a> | 
| Типы носителей входных закрепления | Основной тип: MEDIATYPE_StreamThe следующие подтипы являются допустимыми:<br /><ul><li>MEDIASUBTYPE_AIFF</li><li>MEDIASUBTYPE_AU</li><li>MEDIASUBTYPE_WAVE</li></ul> | 
| Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a> | 
| Типы носителей для выходного ПИН-кода | Основной тип: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM или другой тип сжатия. (См. раздел <a href="audio-subtypes.md"><strong>звуковые подтипы</strong></a>.)<br /> Тип формата: FORMAT_WaveFormatEx<br /> | 
| Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>имедиасикинг</strong></a> | 
| Фильтровать CLSID | {D51BD5A1-7548-11cf-A520-0080C77EF58A} | 
| CLSID страницы свойств | Нет страницы свойств. | 
| Исполняемый объект | quartz.dll | 
| <a href="merit.md">Заслуживают</a> | MERIT_UNLIKELY | 
| <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Комментарии

Этот фильтр поддерживает следующие типы файлов:

-   ВОЛНА (. wav)
-   AIFF и AIFF-C (. AIF)
-   AU (Au)

Однако он имеет следующие ограничения в аудио формате:

-   Звук должен быть 8-или 16-разрядным линейным PCM.
-   Для файлов AIFF-C звук должен быть распакован, в порядке байтов с обратным порядком (тип сжатия "NONE").

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 




