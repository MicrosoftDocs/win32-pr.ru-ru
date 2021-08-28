---
description: Фильтр раскомпрессоров QT
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: Фильтр раскомпрессоров QT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cedb26acdcfabb3c0be4aeb2cbf306b654f9570
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983656"
---
# <a name="qt-decompressor-filter"></a>Фильтр раскомпрессоров QT

этот компонент был удален из Windows Vista и более поздних операционных систем. он доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.

Фильтр "декомпрессор QT" распаковывает видео Apple® QuickTime® 2,0. Этот формат обычно используется в старых файлах QuickTime.




| Метка | Применение |
|--------|-------|
| Интерфейсы фильтра | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a> | 
| Типы носителей входных закрепления | MEDIATYPE_Video, FORMAT_VideoInfo<br /> Допустимы следующие подтипы:<br /><ul><li>MEDIASUBTYPE_QTRpza</li><li>MEDIASUBTYPE_QTSmc</li><li>MEDIASUBTYPE_QTRle</li><li>MEDIASUBTYPE_QTJpeg</li></ul> | 
| Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | 
| Типы носителей для выходного ПИН-кода | MEDIATYPE_Video, MEDIASUBTYPE_NULL FORMAT_VideoInfo | 
| Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | 
| Фильтровать CLSID | CLSID_QTDec | 
| CLSID страницы свойств | Нет страницы свойств. | 
| Исполняемый объект | quartz.dll | 
| <a href="merit.md">Заслуживают</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 




