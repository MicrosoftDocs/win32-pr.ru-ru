---
description: Фильтр WST декодера
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Фильтр WST декодера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb6804f82e5d15aa324feb163261544969e3c45
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908482"
---
# <a name="wst-decoder-filter"></a>Фильтр WST декодера

Этот компонент был удален из Windows Vista и более поздних операционных систем. Он доступен для использования в операционных системах Windows XP и Windows Server 2003.

> [!Note]  
> Начиная с Windows Vista, DirectShow не предоставляет фильтр для расшифровки стандартного телетекста (WST).

 

WST декодер — это фильтр в режиме ядра, который принимает декодированные стандартные телетекстовые телепрограммы из [кодека WST](wst-codec-filter.md) и доставляет точечные рисунки для крепления 2 в [микшере наложения](overlay-mixer-filter.md) с помощью шрифтов, предоставляемых корпорацией Майкрософт. В настоящее время поддерживаются только Западноевропейские языки; в настоящее время шрифты Юникода не предоставляются.

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

[Фильтры DirectShow](directshow-filters.md)
</dt> <dt>

[Просмотр стандартного телетекста в мире](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



