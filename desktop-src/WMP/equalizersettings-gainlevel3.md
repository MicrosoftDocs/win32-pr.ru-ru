---
title: ЕКУАЛИЗЕРСЕТТИНГС. gainLevel3
description: Атрибут gainLevel3 указывает или получает уровень усиления диапазона 3.
ms.assetid: 508d00c6-2429-4f35-b7ab-bf30f774e614
keywords:
- екуализерсеттингс. gainLevel3 проигрыватель Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8e719cd59a253ded35ad10e067f537d6f7d3a68d0d0b05a4cf79d0cd976f5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123654"
---
# <a name="equalizersettingsgainlevel3"></a>ЕКУАЛИЗЕРСЕТТИНГС. gainLevel3

Атрибут **gainLevel3** указывает или получает уровень усиления диапазона 3.

``` syntax
        elementID.gainLevel3
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **числом** для чтения и записи (**float**) со значением, которое обычно находится в диапазоне от 20 до + 20. Он имеет нулевое значение по умолчанию.

## <a name="remarks"></a>Remarks

Этот атрибут корректирует часть спектра частот аудио в центре в 125Hz.

Если этот атрибут не указан, предыдущее значение будет храниться.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС, элемент**](equalizersettings-element.md)
</dt> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС. гаинлевелс**](equalizersettings-gainlevels.md)
</dt> </dl>

 

 





