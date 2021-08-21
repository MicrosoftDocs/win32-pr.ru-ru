---
description: Разделитель MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Разделитель MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417fcca0bfc7a5c24416cfc2cb915f968c12105d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465260"
---
# <a name="mpeg-2-splitter"></a>Разделитель MPEG-2

начиная с Microsoft® Windows® XP, фильтр разделителя MPEG-2 является устаревшим. Вместо этого используйте [демультиплексор MPEG-2](mpeg-2-demultiplexer.md) .

На предыдущих платформах используйте разделитель MPEG-2 для потоков программы MPEG-2, доставляемых в режиме опроса, который содержит по крайней мере один из следующих типов потоков: MPEG-2 Video; Звук MPEG-2; AC3 аудио в кодировке, определенную для видео DVD; или в формате PCM, заданном для видео DVD. Этот фильтр анализирует потоки, создает выходной закрепление для каждого потока и выводит сжатые аудио-или видеопакеты MPEG в фильтр декодера MPEG-2.

Для программных и транспортных потоков, доставляемых в режиме Push-уведомлений, используйте [демультиплексор MPEG-2](mpeg-2-demultiplexer.md)на всех платформах.

> [!Note]  
> Разделитель MPEG-2 не поддерживает поиск в точном фрейме.

 




| | | Интерфейсы фильтра | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <strong>испеЦифипропертипажес</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>иампарсе</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>иамстреамселект</strong></a> | | Типы входных закрепления <ul><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_NULL</li></ul> | | Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | | Типы выходных закрепления Зависит от типа потока. См. раздел <a href="mpeg-2-splitter-media-types.md">типы мультимедиа с разделителями MPEG-2</a> | | Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a> | | Фильтровать CLSID | CLSID_MMSPLITTER | | CLSID страницы свойств | Неприменимо | | Исполняемый файл | mpg2splt.ax | | <a href="merit.md"></a> Кому | MERIT_NORMAL + 1 | | <a href="filter-categories.md">Категория фильтра</a> | CLSID_AudioInputDeviceCategory | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> <dt>

[Использование разделителя MPEG-2](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



