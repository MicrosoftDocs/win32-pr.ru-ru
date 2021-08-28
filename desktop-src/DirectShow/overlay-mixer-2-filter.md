---
description: фильтр оверлея Mixer 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: фильтр оверлея Mixer 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b51dceb2a7f82a91fe30275cacfaad4ad78eded
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987357"
---
# <a name="overlay-mixer-2-filter"></a>фильтр оверлея Mixer 2

фильтр оверлея Mixer 2 идентичен фильтру [Mixer наложения](overlay-mixer-filter.md) , за исключением следующих:

-   Он поддерживает только типы мультимедиа с форматами [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .
-   Он имеет более высокий уровень, что позволяет автоматически добавлять его в граф фильтра.

наложение Mixer 2 обеспечивается таким образом, что диспетчер Graph фильтра добавит его к графу при подготовке к просмотру видео в формате MPEG-2, отличном от DVD. выбрать, использовать ли наложение Mixer или оверлей Mixer 2, можно с помощью компонента, который строит граф, либо фильтра Graph Manager, Graph записи или построителя DVD-Graph. С точки зрения приложения они представляют собой один и тот же фильтр с одинаковыми интерфейсами и функциональными возможностями.

следующая таблица содержит сведения, относящиеся к наложению Mixer 2. Сведения о всех других данных фильтра см. в документации по наложением Mixer.




| Метка | Применение |
|--------|-------|
| Типы носителей входных закрепления | Тип формата: Format_VIDEOINFO2 | 
| Фильтровать CLSID | CLSID_OverlayMixer2 | 
| <a href="merit.md">Заслуживают</a> | <ul><li>MERIT_UNLIKELY</li><li>Windows Vista или более поздней версии: MERIT_DO_NOT_USE</li></ul> | 




 

в Windows Vista и более поздних версиях фильтр оверлея Mixer 2 не \_ \_ \_ используется, так как новые модули подготовки видео (vmr-7, vmr-9 и евр) поддерживают форматы **VIDEOINFOHEADER2** , поэтому необязательно использовать наложение Mixer.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 



