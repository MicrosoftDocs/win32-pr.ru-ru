---
description: Фильтр синтаксического анализатора QuickTime Movie
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Фильтр синтаксического анализатора QuickTime Movie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a65ba14cb748eb10c6afddf3e4747f11d68a4f9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476720"
---
# <a name="quicktime-movie-parser-filter"></a>Фильтр синтаксического анализатора QuickTime Movie

этот компонент был удален из Windows Vista и более поздних операционных систем. он доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.

Фильтр синтаксического анализатора QuickTime Movie разделяет данные® Apple® QuickTime в аудио и видео потоки. Он поддерживает QuickTime 2,0 и более ранних версий. Входной ПИН-код подключается к фильтру источника, такому как фильтр [источника асинхронного файла](file-source--async--filter.md) или фильтр [источника файла URL-адреса](file-source--url--filter.md) . Средство синтаксического анализа использует фильтр [AVI распаковки](avi-decompressor-filter.md) или [Qt](qt-decompressor-filter.md) для распаковки файлов QuickTime. Фильтр создает один выходной ПИН-код для потока видео и один выходной ПИН-код для аудиопотока.




| | | Интерфейсы фильтра | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>Иаммедиаконтент</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a> | | Типы входных закрепления MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie; | | Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | | Типы выходных закрепления <ul><li>MEDIATYPE_Video, MEDIASUBTYPE_NULL FORMAT_VideoInfo</li><li>MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx</li></ul> | | Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | | Фильтровать CLSID | CLSID_QuickTimeParser | | CLSID страницы свойств | Нет страницы свойств. | | Исполняемый файл | quartz.dll | | <a href="merit.md"></a> Кому | MERIT_NORMAL | | <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 



