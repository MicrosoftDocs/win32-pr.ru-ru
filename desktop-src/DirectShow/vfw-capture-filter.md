---
description: Фильтр захвата VFW
ms.assetid: 663b6b3b-2a50-4586-9506-600a59869abe
title: Фильтр захвата VFW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 679f8e736564534948d05fe25ecb1bc18bbb787df370aca0f9a3752960f719ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071958"
---
# <a name="vfw-capture-filter"></a>Фильтр захвата VFW

Этот фильтр работает со старым оборудованием видеозаписи, которое использует видео для Windows.

Этот фильтр имеет два выходных контакта. Одна из них называется захватом, а другая — либо предварительной версией, либо наложением.



| Метка | Значение |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | **IPersistPropertyBag**, [**иамвфвкаптуредиалогс**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs), [**иамфилтермискфлагс**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **испеЦифипропертипажес**, [**иоверлайнотифи**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Типы носителей входных закрепления                    | Неприменимо.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Интерфейсы входных закрепления                     | Неприменимо.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Типы носителей для выходного ПИН-кода                   | Захват: MEDIATYPE \_ видео, медиасубтипе \_ null, Format \_ видеоинфуверлай: MEDIATYPE \_ Video, МЕДИАСУБТИПЕ \_ оверлей, Format \_ видеоинфо<br/> Предварительный просмотр. \_ видео MEDIATYPE, медиасубтипе \_ null, Format \_ видеоинфо<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Интерфейсы выходного ПИН-кода                    | ПИН-код захвата: [**иамбуффернеготиатион**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation), [**иамдроппедфрамес**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes), [**иампушсаурце**](/windows/desktop/api/Strmif/nn-strmif-iampushsource), [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**иамстреамконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IKsPropertySet**](ikspropertyset.md), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)оверлея PIN: [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IKsPropertySet**](ikspropertyset.md), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> Предварительный просмотр ПИН-кода: [**иампушсаурце**](/windows/desktop/api/Strmif/nn-strmif-iampushsource), [**иамстреамконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**икспропертисет**](ikspropertyset.md), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> |
| Фильтровать CLSID                             | \_ВФВКАПТУРЕ CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| CLSID страницы свойств                      | \_КАПТУРЕПРОПЕРТИЕС CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Исполняемый объект                               | qcap.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Заслуживают](merit.md)                       | \_ \_ не \_ использовать                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [Категория фильтра](filter-categories.md) | \_ВИДЕОИНПУТДЕВИЦЕКАТЕГОРИ CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Remarks

Несмотря на то, что ПИН-код записи предоставляет интерфейс [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) , для этого интерфейса реализованы только методы **Сетформат** и- **Format** .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> <dt>

[Видеозапись](video-capture.md)
</dt> </dl>

 

 




