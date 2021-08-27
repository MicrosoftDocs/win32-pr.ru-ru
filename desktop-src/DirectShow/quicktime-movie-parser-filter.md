---
description: Фильтр синтаксического анализатора QuickTime Movie
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Фильтр синтаксического анализатора QuickTime Movie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0028b604efe31749144ca98cb80057685ed0c1db
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983617"
---
# <a name="quicktime-movie-parser-filter"></a>Фильтр синтаксического анализатора QuickTime Movie

этот компонент был удален из Windows Vista и более поздних операционных систем. он доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.

Фильтр синтаксического анализатора QuickTime Movie разделяет данные® Apple® QuickTime в аудио и видео потоки. Он поддерживает QuickTime 2,0 и более ранних версий. Входной ПИН-код подключается к фильтру источника, такому как фильтр [источника асинхронного файла](file-source--async--filter.md) или фильтр [источника файла URL-адреса](file-source--url--filter.md) . Средство синтаксического анализа использует фильтр [AVI распаковки](avi-decompressor-filter.md) или [Qt](qt-decompressor-filter.md) для распаковки файлов QuickTime. Фильтр создает один выходной ПИН-код для потока видео и один выходной ПИН-код для аудиопотока.




| Метка | Применение |
|--------|-------|
| Интерфейсы фильтра | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>Иаммедиаконтент</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>ибасефилтер</strong></a> | 
| Типы носителей входных закрепления | MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie; | 
| Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>икуалитиконтрол</strong></a> | 
| Типы носителей для выходного ПИН-кода | <ul><li>MEDIATYPE_Video, MEDIASUBTYPE_NULL FORMAT_VideoInfo</li><li>MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx</li></ul> | 
| Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | 
| Фильтровать CLSID | CLSID_QuickTimeParser | 
| CLSID страницы свойств | Нет страницы свойств. | 
| Исполняемый объект | quartz.dll | 
| <a href="merit.md">Заслуживают</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 



