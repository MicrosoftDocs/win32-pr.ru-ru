---
description: Фильтр преобразователя цветового пространства
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: Фильтр преобразователя цветового пространства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c0a519772a6d38971654cb92a895fcd95f5ecc8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987067"
---
# <a name="color-space-converter-filter"></a>Фильтр преобразователя цветового пространства

Этот фильтр преобразования преобразует из одного типа цвета RGB в другой тип RGB, например, между 24-разрядным и 8-разрядным цветом RGB. Поскольку этот тип преобразования, как правило, более эффективно обрабатывается в рамках декомпрессора видео, в основном используется преобразователь цветового пространства, когда источник потока состоит из несжатых кадров RGB.




| Метка | Применение |
|--------|-------|
| Интерфейсы фильтра | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a> | 
| Типы носителей входных закрепления | MEDIATYPE_Video FORMAT_VideoInfo.<br /> Допустимы следующие подтипы:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | 
| Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | 
| Типы носителей для выходного ПИН-кода | MEDIATYPE_Video FORMAT_VideoInfo.<br /> Допустимы следующие подтипы:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | 
| Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | 
| Фильтровать CLSID | CLSID_Colour | 
| CLSID страницы свойств | Нет страницы свойств. | 
| Исполняемый объект | quartz.dll | 
| <a href="merit.md">Заслуживают</a> | MERIT_UNLIKELY | 
| <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 




