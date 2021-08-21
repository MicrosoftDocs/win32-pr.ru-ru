---
title: волумеслидер
description: Это Стандартный ПОЛЗУНок со следующими значениями по умолчанию. | волумеслидер
ms.assetid: 7533863b-49de-4c1b-8750-fd333c573a17
keywords:
- волумеслидер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- VOLUMESLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ebc2e6ec82327be9cb423d05661a5a38bbcc445450fc6d4f56ceaf7caa8b270d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054012"
---
# <a name="volumeslider"></a>волумеслидер

Это Стандартный ПОЛЗУНок со следующими значениями по умолчанию.

``` syntax
toolTip="Volume"
max="100"
min="0"
value="wmpprop:player.settings.volume"
value_onchange="jscript:player.settings.volume=value;
player.settings.mute=false;"
```

## <a name="remarks"></a>Remarks

При этом создается элемент управления "ПОЛЗУНок", который задает громкость звука. Всплывающие подсказки локализованы. Все свойства этого ПОЛЗУНка можно переопределить, явно указав их.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 7,0 или более поздней версии<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Элемент SLIDER**](slider-element.md)
</dt> </dl>

 

 





