---
description: Фильтр WST декодера
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Фильтр WST декодера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d61da0540c683e8c4646074715b0518717b4e1958beea5b8ca2ae41fb4629790
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290774"
---
# <a name="wst-decoder-filter"></a>Фильтр WST декодера

этот компонент был удален из Windows Vista и более поздних операционных систем. он доступен для использования в операционных системах Windows XP и Windows Server 2003.

> [!Note]  
> начиная с Windows Vista DirectShow не предоставляет фильтр для расшифровки стандартного телетекста (WST).

 

WST декодер — это фильтр в режиме ядра, который принимает раскодированные стандартные телетекстовые телепрограммы из [кодека wst](wst-codec-filter.md) и доставляет точечные рисунки для крепления 2 на [наложение Mixer](overlay-mixer-filter.md) используя шрифты, предоставляемые корпорацией майкрософт. В настоящее время поддерживаются только Западноевропейские языки; в настоящее время шрифты Юникода не предоставляются.

Этот фильтр можно автоматически добавить в граф, вызвав метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), используя выходной ПИН-код WST.



| Метка | Значение |
|------------------------------------------|---------------------------------------------------------------|
| Интерфейсы фильтра                        | ИспеЦифипропертипажес, [ **иамвстдекодер**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder) |
| Типы носителей входных закрепления                    | MEDIATYPE \_ ВБИ, медиасубтипе \_ телетекст                        |
| Интерфейсы входных закрепления                     | [**ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Типы носителей для выходного ПИН-кода                   | \_Видео MEDIATYPE                                              |
| Интерфейсы выходного ПИН-кода                    | [**ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Фильтровать CLSID                             | \_ВСТДЕКОДЕР CLSID                                             |
| CLSID страницы свойств                      | \_ВСТДЕКОДЕРПРОПЕРТИПАЖЕ CLSID                                 |
| Исполняемый объект                               | Wstdecod.DLL                                                  |
| [Заслуживают](merit.md)                       | неуспешный \_ режим                                                 |
| [Категория фильтра](filter-categories.md) | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID                                 |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> <dt>

[Просмотр стандартного телетекста в мире](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



