---
description: Фильтр оболочки ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Фильтр оболочки ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0688150ab417c6ebb71313a438f72ef7839042
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985357"
---
# <a name="acm-wrapper-filter"></a>Фильтр оболочки ACM

Фильтр оболочки ACM включает кодеки (ACM) для подключения к графу фильтра. Он может действовать как фильтр распаковки или как фильтр сжатия.

в качестве фильтра распаковки оболочка ACM отображается в категории «DirectShow фильтры» (CLSID \_ легациамфилтеркатегори) и имеет нештатную подмножество \_ . Тип носителя подключения для входного ПИН-кода определяет, какой кодек использует фильтр. Как правило, приложению не нужно добавлять фильтр к графу фильтра; он автоматически извлекается при необходимости фильтром Graph Manager. Распаковка применяется только к звуку PCM.

Как фильтр сжатия, оболочка ACM отображается в категории "звуковые компрессоры" (CLSID \_ аудиокомпрессоркатегори) и имеет недостаточное количество \_ \_ \_ . Каждый кодек отображается как отдельный экземпляр. Для сжатия нельзя напрямую создать фильтр с помощью CoCreateInstance. Вместо этого необходимо использовать перечислитель системных устройств. Дополнительные сведения см. [в разделе Использование перечислителя системных устройств](using-the-system-device-enumerator.md).




| Метка | Применение |
|--------|-------|
| Интерфейсы фильтра | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a>, IPersist, IPersistPropertyBag | 
| Типы носителей входных закрепления | MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx | 
| Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Имеминпутпин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | 
| Типы носителей для выходного ПИН-кода | MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx. возможны следующие сочетания следующих вариантов.<br /><ul><li>Выборок в секунду (кГц): 44,1, 22,05, 11,025 или 8,0.</li><li>Каналы: стерео или Mono.</li><li>Бит на выборку: 8 или 16.</li></ul> | 
| Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>Иамстреамконфиг</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>имедиапоситион</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | 
| Фильтровать CLSID | CLSID_ACMWrapper | 
| CLSID страницы свойств | Нет страницы свойств. | 
| Исполняемый объект | Quartz.dll | 
| <a href="merit.md">Заслуживают</a> | MERIT_NORMAL или MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory или CLSID_AudioCompressorCategory | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 




