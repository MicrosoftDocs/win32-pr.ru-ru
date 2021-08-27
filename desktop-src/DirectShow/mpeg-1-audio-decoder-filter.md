---
description: Фильтр звукового декодера MPEG-1
ms.assetid: 2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d
title: Фильтр звукового декодера MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c3c014497d8b3db5aaf3031250e78edd8b59cb2
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983827"
---
# <a name="mpeg-1-audio-decoder-filter"></a>Фильтр звукового декодера MPEG-1

Декодирует слой MPEG-1 и звук уровня II в PCM.




| Метка | Применение |
|--------|-------|
| Интерфейсы фильтра | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, <strong>испеЦифипропертипажес</strong> | 
| Типы носителей входных закрепления | MEDIATYPE_Audio, FORMAT_WaveFormatEx<br /> Допустимы следующие подтипы:<br /><ul><li>MEDIASUBTYPE_MPEG1Packet</li><li>MEDIASUBTYPE_MPEG1Payload</li><li>MEDIASUBTYPE_MPEG1AudioPayload</li><li>GUID_NULL</li></ul> | 
| Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | 
| Типы носителей для выходного ПИН-кода | MEDIATYPE_Audio, MEDIASUBTYPE_PCM | 
| Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | 
| Фильтровать CLSID | CLSID_CMpegAudioCodec | 
| CLSID страницы свойств | CLSID_MpegAudioDecoderPropertyPage | 
| Исполняемый объект | quartz.dll | 
| <a href="merit.md">Заслуживают</a> | 0x03680001 | 
| <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 




