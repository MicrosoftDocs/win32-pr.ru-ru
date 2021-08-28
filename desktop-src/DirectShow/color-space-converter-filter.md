---
description: Фильтр преобразователя цветового пространства
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: Фильтр преобразователя цветового пространства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cadc3f980116f6745d578a06220639b181fe13
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477370"
---
# <a name="color-space-converter-filter"></a>Фильтр преобразователя цветового пространства

Этот фильтр преобразования преобразует из одного типа цвета RGB в другой тип RGB, например, между 24-разрядным и 8-разрядным цветом RGB. Поскольку этот тип преобразования, как правило, более эффективно обрабатывается в рамках декомпрессора видео, в основном используется преобразователь цветового пространства, когда источник потока состоит из несжатых кадров RGB.




| | | Интерфейсы фильтра | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a> | | Типы входных закрепления MEDIATYPE_Video FORMAT_VideoInfo.<br /> Допустимы следующие подтипы:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | | Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | | Типы выходных закрепления MEDIATYPE_Video FORMAT_VideoInfo.<br /> Допустимы следующие подтипы:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | | Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | | Фильтровать CLSID | CLSID_Colour | | CLSID страницы свойств | Нет страницы свойств. | | Исполняемый файл | quartz.dll | | <a href="merit.md"></a> Кому | MERIT_UNLIKELY | | <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 




