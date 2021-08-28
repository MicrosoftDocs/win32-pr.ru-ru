---
description: Расширенный фильтр модуля подготовки видео (Евр) является 16-канальным видеомикшером и модулем подготовки отчетов. Она имеет те же основные функции и модель подключаемых модулей, что и Media Foundation приемника мультимедиа Евр.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Расширенный фильтр визуализатора видео
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075ab9149cdf219971c5d1c321474de784aaa8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987897"
---
# <a name="enhanced-video-renderer-filter"></a>Расширенный фильтр визуализатора видео

> [!Note]  
> эта статья относится к Windows Vista и более поздних версий.

 

Расширенный фильтр модуля подготовки видео (Евр) является 16-канальным видеомикшером и модулем подготовки отчетов. Она имеет те же основные функции и модель подключаемых модулей, что и Media Foundation приемника мультимедиа Евр.

фильтр DirectShow евр описан в документации по пакету SDK для Media Foundation. Дополнительные сведения см. в разделе [Улучшенный обработчик видео](../medfound/enhanced-video-renderer.md).




| Метка | Применение |
|--------|-------|
| Фильтровать интерфейсы (с помощью <strong>QueryInterface</strong>) | DirectShow интерфейсы:<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>иамцертифиедаутпутпротектион</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>иамфилтермискфлагс</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></li><li><a href="ikspropertyset.md"><strong>икспропертисет</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>имедиаевентсинк</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>икуалпроп</strong></a></li></ul>Media Foundation интерфейсы:<br /><ul><li><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>иеврфилтерконфиг</strong></a></li><li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>имфжетсервице</strong></a></li><li><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>имфвидеопоситионмаппер</strong></a></li><li><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>имфвидеорендерер</strong></a></li></ul> | 
| Типы носителей входных закрепления | Переменная в зависимости от графического драйвера. | 
| Интерфейсы входных закрепления (через <strong>QueryInterface</strong>) | DirectShow интерфейсы:<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>ипин</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></li></ul>Media Foundation интерфейсы:<br /><ul><li><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>идиректксвидеомемориконфигуратион</strong></a></li><li><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>иеврвидеостреамконтрол</strong></a></li><li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>имфжетсервице</strong></a></li></ul> | 
| Типы носителей для выходного ПИН-кода | Не применяется | 
| Интерфейсы выходного ПИН-кода | Не применяется | 
| Фильтровать CLSID | CLSID_EnhancedVideoRenderer | 
| Исполняемый объект | evr.dll | 
| <a href="merit.md">Заслуживают</a> | MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Комментарии

В дополнение к интерфейсам, предоставляемым через **QueryInterface**, ЕВР предоставляет другие интерфейсы через метод [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) . Некоторые из этих интерфейсов реализуются средством Евр Presenter или Евр, а не Евр. Если приложение устанавливает настраиваемый Presenter или микшер на евр, то пользовательские версии могут предоставлять другой набор интерфейсов.



| Объект     | Идентификатор службы                                              | Интерфейсы                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Фильтр Евр | \_ \_ Служба прорисовки видео Mr \_ (запросы Евр или Presenter)<br/> | [**имфвидеодевицеид**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**имфвидеодисплайконтрол**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [**имфвидеопоситионмаппер**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**имфвидеопресентер**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| Фильтр Евр | \_ \_ Служба ускорения видео Mr \_ (выступающие запросы)<br/>  | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| Фильтр Евр | \_ \_ Служба видеомикшера MR \_ (микшер запросов)<br/>             | [**имфвидеодевицеид**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**имфвидеомиксербитмап**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [**имфвидеомиксерконтрол**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [**имфвидеопоситионмаппер**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**имфвидеопроцессор**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| Входные контакты | \_ \_ Служба ускорения видео Mr \_                                | [**идиректксвидеомемориконфигуратион**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

Евр может сочетать до 16 потоков видео. Первый входной поток (ПИН-код 0) называется *ссылочным потоком*. Ссылочный поток всегда отображается первым в z-порядке. Любые дополнительные потоки называются подпотоками и смешиваются поверх потока ссылок. Приложение может изменить z-порядок для подпотоков, но ни один из подпотоков не может быть первым в z-порядке.

Графический драйвер определяет поддерживаемые форматы видео, но обычно они ограничены следующими элементами:

-   Ссылочный поток: прогрессивное или чередование YUV без альфа-составляющей для каждого пикселя (например, NV12 или YUY2); или прогрессивный RGB.
-   Подпотоки: прогрессивное YUV с поддержкой отдельных пикселей, например АЙУВ или AI44.

Доступные форматы подпотока могут зависеть от формата потока ссылок.

Евр пересылает команды Seek через ПИН-код 0. ПИН-коды подпотока не выполняют команд прямого поиска. С помощью фильтра источника или разделителя можно синхронизировать подпотоки со ссылочным потоком.

## <a name="requirements"></a>Требования



| Требование | Применение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

