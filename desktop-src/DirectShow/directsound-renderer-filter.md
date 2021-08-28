---
description: Фильтр модуля подготовки DirectSound
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: Фильтр модуля подготовки DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc1dbd6fc39e7e102cbcd5d25075be6bf86bcc8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983847"
---
# <a name="directsound-renderer-filter"></a>Фильтр модуля подготовки DirectSound

Этот фильтр отображает звук с помощью DirectSound. Этот фильтр сейчас является модулем подготовки звука для звукозаписи по умолчанию.

В дополнение к базовым возможностям отрисовки звука этот фильтр может обрабатывать вызовы API DirectSound. Используйте методы [**иамдиректсаунд**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) , чтобы установить и извлечь окно, которое будет выполнять воспроизведение звука. Модуль подготовки звука DirectSound является фильтром рендеринга звука по умолчанию для DirectShow.




| Метка | Применение |
|--------|-------|
| Интерфейсы фильтра | <a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>Иамаудиорендерерстатс</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>иамклоккславе</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>иамдиректсаунд</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>иамресаурцеконтрол</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a> | 
| Типы носителей входных закрепления | Основной тип: MEDIATYPE_AudioSubtypes:<br /><ul><li>MEDIASUBTYPE_PCM</li><li>MEDIASUBTYPE_IEEE_FLOAT</li><li>MEDIASUBTYPE_DOLBY_AC3_SPDIF</li><li>MEDIASUBTYPE_RAW_SPORT</li><li>MEDIASUBTYPE_SPDIF_TAG_241h</li><li>MEDIASUBTYPE_DRM_Audio</li></ul>Тип формата: FORMAT_WaveFormatEx<br /> | 
| Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>ипинконнектион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | 
| Типы носителей для выходного ПИН-кода | Не применяется | 
| Интерфейсы выходного ПИН-кода | Не применяется | 
| Фильтровать CLSID | CLSID_DSoundRender | 
| CLSID страницы свойств | CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties | 
| Исполняемый объект | quartz.dll | 
| <a href="merit.md">Заслуживают</a> | MERIT_PREFERRED | 
| <a href="filter-categories.md">Категория фильтра</a> | CLSID_AudioRendererCategory | 




 

## <a name="remarks"></a>Комментарии

Этот фильтр выступает в качестве оболочки для звукового устройства. Чтобы перечислить звуковые устройства, доступные в системе пользователя, используйте интерфейс [**икреатедевенум**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) с категорией модуля подготовки звука (CLSID \_ аудиорендереркатегори). Для каждого звукового устройства категория модуля подготовки звука содержит два экземпляра фильтра. Один из них соответствует модулю рендеринга DirectSound, а второй соответствует фильтру модуля [подготовки звука (Wave)](audio-renderer--waveout--filter.md) . Экземпляр DirectSound имеет понятное имя "DirectSound: *DeviceName*,", где *DeviceName* — имя устройства. Экземпляр Wave имеет понятное имя *DeviceName*.

Категория "модуль подготовки звука" содержит два дополнительных экземпляра фильтра с именами "устройство DirectSound по умолчанию" и "устройство вывода по умолчанию". Они соответствуют звуковому устройству по умолчанию, выбранному пользователем с помощью панели управления. Они фактически сопоставляются с одной из пар, описанных в предыдущем абзаце. Например, если в системе есть два звуковых устройства, устройство A и устройство B, категория модуля подготовки звука будет содержать следующее:

-   Устройство A
-   DirectSound: устройство а
-   Устройство B
-   DirectSound: устройство B
-   Устройство DirectSound по умолчанию
-   Устройство для звука по умолчанию

Если пользователь выбрал устройство A в качестве устройства по умолчанию, то "устройство DirectSound по умолчанию" эквивалентно "DirectSound: устройство A,", а "устройство для звукового сигнала по умолчанию" эквивалентно "устройство а". Если пользователь выбирает устройство б в качестве устройства по умолчанию, эти сопоставления изменятся.

"Устройству DirectSound по умолчанию" назначена неуспешная версия \_ . У других есть неуспешные \_ \_ \_ работы. таким образом, интеллектуальные Подключение всегда будут выбирать устройство DirectSound по умолчанию.

Фильтр модуля обработки DirectSound поддерживает трехмерный звук через интерфейсы DirectSound **IDirectSound3DBuffer** и **IDirectSound3dListener** . Можно также запросить фильтр для текущих версий этих интерфейсов, **IDirectSound3DBuffer8** и **IDirectSound3dListener8**. Перед вызовом методов для этих интерфейсов запустите граф.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 




