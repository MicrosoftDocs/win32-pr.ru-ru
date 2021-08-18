---
title: сикслидер
description: Это Стандартный ПОЛЗУНок со следующими значениями по умолчанию. | сикслидер
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- сикслидер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a294eede05ec2b2f0f84e925aa299c9bcb2388ee2151385e48f2c68e6b4c1328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833343"
---
# <a name="seekslider"></a>сикслидер

Это Стандартный **ползунок** со следующими значениями по умолчанию.

``` syntax
toolTip="Seek"
foregroundProgress="wmpprop:player.network.downloadProgress"
max="wmpprop:player.currentMedia.duration"
min="0"
value="wmpprop:player.controls.currentPosition"
onDragEnd="jscript:player.controls.currentPosition=value;"
useForegroundProgress="true"
```

## <a name="remarks"></a>Remarks

При этом создается элемент управления " **ползунок** ", который ищет файл мультимедиа в любое положение. Всплывающие подсказки локализованы. Все свойства этого **ползунка** можно переопределить, явно указав их.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 7,0 или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент SLIDER**](slider-element.md)
</dt> </dl>

 

 





