---
title: ЕКУАЛИЗЕРСЕТТИНГС. gainLevel1
description: Атрибут gainLevel1 указывает или получает уровень усиления диапазона 1.
ms.assetid: 3d681ade-3fd4-432d-ae92-c083d927346f
keywords:
- Проигрыватель Windows Media ЕКУАЛИЗЕРСЕТТИНГС. gainLevel1
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel1
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3299c2b9275eabb4812c83670f28bcbb3d2aeef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698846"
---
# <a name="equalizersettingsgainlevel1"></a>ЕКУАЛИЗЕРСЕТТИНГС. gainLevel1

Атрибут **gainLevel1** указывает или получает уровень усиления диапазона 1.

``` syntax
        elementID.gainLevel1
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **числом** для чтения и записи (**float**) со значением, которое обычно находится в диапазоне от 20 до + 20. Он имеет нулевое значение по умолчанию.

## <a name="remarks"></a>Комментарии

Этот атрибут корректирует часть спектра частот аудио в центре в 31Hz.

Если этот атрибут не указан, предыдущее значение будет храниться.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС, элемент**](equalizersettings-element.md)
</dt> <dt>

[**ЕКУАЛИЗЕРСЕТТИНГС. гаинлевелс**](equalizersettings-gainlevels.md)
</dt> </dl>

 

 





