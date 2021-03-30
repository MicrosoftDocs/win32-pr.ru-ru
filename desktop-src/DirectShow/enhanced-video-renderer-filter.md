---
description: Расширенный фильтр модуля подготовки видео (Евр) является 16-канальным видеомикшером и модулем подготовки отчетов. Она имеет те же основные функции и модель подключаемых модулей, что и Media Foundation приемника мультимедиа Евр.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Расширенный фильтр визуализатора видео
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba6e7c14386ea37424364274263859844182ed7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072230"
---
# <a name="enhanced-video-renderer-filter"></a>Расширенный фильтр визуализатора видео

> [!Note]  
> Этот раздел относится к Windows Vista и более поздним версиям.

 

Расширенный фильтр модуля подготовки видео (Евр) является 16-канальным видеомикшером и модулем подготовки отчетов. Она имеет те же основные функции и модель подключаемых модулей, что и Media Foundation приемника мультимедиа Евр.

Фильтр Евр для DirectShow описан в документации по пакету SDK для Media Foundation. Дополнительные сведения см. в разделе [Улучшенный обработчик видео](../medfound/enhanced-video-renderer.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Фильтровать интерфейсы (с помощью <strong>QueryInterface</strong>)</td>
<td>Интерфейсы DirectShow:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>иамцертифиедаутпутпротектион</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>иамфилтермискфлагс</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></li>
<li><a href="ikspropertyset.md"><strong>икспропертисет</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>имедиаевентсинк</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>икуалпроп</strong></a></li>
</ul>
Media Foundation интерфейсы:<br/>
<ul>
<li><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>иеврфилтерконфиг</strong></a></li>
<li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>имфжетсервице</strong></a></li>
<li><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>имфвидеопоситионмаппер</strong></a></li>
<li><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>имфвидеорендерер</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td>Переменная в зависимости от графического драйвера.</td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления (через <strong>QueryInterface</strong>)</td>
<td>Интерфейсы DirectShow:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>ипин</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></li>
</ul>
Media Foundation интерфейсы:<br/>
<ul>
<li><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>идиректксвидеомемориконфигуратион</strong></a></li>
<li><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>иеврвидеостреамконтрол</strong></a></li>
<li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>имфжетсервице</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td>Не применяется</td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td>Не применяется</td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td>CLSID_EnhancedVideoRenderer</td>
</tr>
<tr class="odd">
<td>Исполняемый объект</td>
<td>evr.dll</td>
</tr>
<tr class="even">
<td><a href="merit.md">Заслуживают</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="odd">
<td><a href="filter-categories.md">Категория фильтра</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

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



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

