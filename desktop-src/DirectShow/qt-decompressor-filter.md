---
description: Фильтр раскомпрессоров QT
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: Фильтр раскомпрессоров QT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6f28058a1c729c9d42b20651a86ba31b4d98c7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467971"
---
# <a name="qt-decompressor-filter"></a>Фильтр раскомпрессоров QT

этот компонент был удален из Windows Vista и более поздних операционных систем. он доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.

Фильтр "декомпрессор QT" распаковывает видео Apple® QuickTime® 2,0. Этот формат обычно используется в старых файлах QuickTime.




| | | Интерфейсы фильтра | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a> | | Типы входных закрепления MEDIATYPE_Video, FORMAT_VideoInfo<br /> Допустимы следующие подтипы:<br /><ul><li>MEDIASUBTYPE_QTRpza</li><li>MEDIASUBTYPE_QTSmc</li><li>MEDIASUBTYPE_QTRle</li><li>MEDIASUBTYPE_QTJpeg</li></ul> | | Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | | Типы выходных закрепления MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo | | Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | | Фильтровать CLSID | CLSID_QTDec | | CLSID страницы свойств | Нет страницы свойств. | | Исполняемый файл | quartz.dll | | <a href="merit.md"></a> Кому | MERIT_NORMAL | | <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 




