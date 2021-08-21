---
title: ЕКУАЛИЗЕРСЕТТИНГС. gainLevel2
description: Атрибут gainLevel2 указывает или получает уровень усиления диапазона 2.
ms.assetid: e602d9cc-42b3-402e-9df5-8b970d878904
keywords:
- екуализерсеттингс. gainLevel2 проигрыватель Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe4979cb44fbd39b37acd29fe8e3303c879c45b40dfafc554180dad5301f0b0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339834"
---
# <a name="equalizersettingsgainlevel2"></a>ЕКУАЛИЗЕРСЕТТИНГС. gainLevel2

Атрибут **gainLevel2** указывает или получает уровень усиления диапазона 2.

``` syntax
        elementID.gainLevel2
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **числом** для чтения и записи (**float**) со значением, которое обычно находится в диапазоне от 20 до + 20. Он имеет нулевое значение по умолчанию.

## <a name="remarks"></a>Remarks

Этот атрибут корректирует часть спектра частот аудио в центре в 62Hz.

Если этот атрибут не указан, предыдущее значение будет храниться.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС, элемент**](equalizersettings-element.md)
</dt> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС. гаинлевелс**](equalizersettings-gainlevels.md)
</dt> </dl>

 

 





