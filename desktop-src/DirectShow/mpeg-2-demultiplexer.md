---
description: Этот фильтр используется для демультиплексирования транспорта MPEG-2 и программных потоков, которые доставляются в принудительном режиме.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: Демультиплексор MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21898cb4fa3c16b07508dc3370c519d3edfbced
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983957"
---
# <a name="mpeg-2-demultiplexer"></a>Демультиплексор MPEG-2

Этот фильтр используется для демультиплексирования транспорта MPEG-2 и программных потоков, которые доставляются в принудительном режиме. начиная с Windows XP этот фильтр также поддерживает потоки программы в режиме опроса (воспроизведение файла). На более ранних платформах используйте фильтр [разделителя MPEG-2](mpeg-2-splitter.md) для потоков программы в режиме опроса. Этот фильтр можно использовать в любом типе графа фильтра, включая граф фильтра BDA Digital TV.

> [!Note]  
> Демультиплексор MPEG-2 не поддерживает поиск в точном фрейме.

 




| Метка | Применение |
|--------|-------|
| Интерфейсы фильтра | Все режимы:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></li><li><strong>испеЦифипропертипажес</strong></li></ul>Только режим принудительной отправки:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>иамфилтермискфлагс</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>иреференцеклокк</strong></a></li></ul> | 
| Типы носителей входных закрепления | Основной тип: MEDIATYPE_STREAM<br /> Подтип<br /><ul><li>KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</li><li>MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIASUBTYPE_MPEG2_TRANSPORT</li><li>MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</li></ul>Дополнительные сведения см. в статье <a href="mpeg-2-demultiplexer-media-types.md"><strong>типы мультимедиа для демультиплексирования MPEG-2</strong></a>.<br /> | 
| Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | 
| Типы носителей для выходного ПИН-кода | Простейшие потоки аудио и видео должны иметь основной тип MEDIATYPE_Audio или MEDIATYPE_Video.<br /> Дополнительные сведения см. в статье <a href="mpeg-2-demultiplexer-media-types.md"><strong>типы мультимедиа для демультиплексирования MPEG-2</strong></a>.<br /> | 
| Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, только режим принудительной отправки <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a>: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>иампушсаурце</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a><br /> Только режим опроса: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>имедиасикинг</strong></a><br /> | 
| Фильтровать CLSID | CLSID_MPEG2Demultiplexer | 
| CLSID страницы свойств | Доступно только для тестирования. Использование интерфейса <strong>испеЦифипропертипажес</strong> для доступа к страницам свойств | 
| Исполняемый объект | mpg2splt.ax | 
| <a href="merit.md">Заслуживают</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Комментарии

Для вывода простых потоков аудио и видео демультиплексирование должен получить потоки PCR и SCR. На стороне входа это означает, что транспортный поток должен содержать таблицы PAT и ПЛТ, определяющие идентификатор процесса для потока PCR; и потоки программ должны содержать по крайней мере один заголовок Pack.

## <a name="requirements"></a>Требования



| Требование | Применение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |
| Поддержка конца сервера<br/>    | Windows Server 2003 R2<br/>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> <dt>

[Использование демультиплексора MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




