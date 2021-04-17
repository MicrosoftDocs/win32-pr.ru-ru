---
title: волумеслидер
description: Это Стандартный ПОЛЗУНок со следующими значениями по умолчанию. | волумеслидер
ms.assetid: 7533863b-49de-4c1b-8750-fd333c573a17
keywords:
- ВОЛУМЕСЛИДЕР Windows Media Player
topic_type:
- apiref
api_name:
- VOLUMESLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ea872b55f6657d9cf1c9f67230cb3debd955fb4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694868"
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

## <a name="remarks"></a>Комментарии

При этом создается элемент управления "ПОЛЗУНок", который задает громкость звука. Всплывающие подсказки локализованы. Все свойства этого ПОЛЗУНка можно переопределить, явно указав их.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 7,0 или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент SLIDER**](slider-element.md)
</dt> </dl>

 

 





