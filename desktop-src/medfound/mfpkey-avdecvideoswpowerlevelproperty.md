---
description: Задает уровень питания для декодера.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: Свойство MFPKEY_AVDecVideoSWPowerLevel (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce376a370ea6488c87c0266319de7e9bde0a94edab7137a81f015f416ea9fc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874068"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a>МФПКЭЙ \_ авдеквидеосвповерлевел, свойство

Задает уровень питания для декодера.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

**VT \_ UI4**

## <a name="default-value"></a>Значение по умолчанию

**100**

## <a name="remarks"></a>Remarks

Для этого свойства необходимо задать одно из следующих значений.



| Значение | Значение                                                             |
|-------|---------------------------------------------------------------------|
| 0     | Декодер использует уровень питания, оптимизированный для времени работы батареи.  |
| 50    | Декодер использует сбалансированный уровень электропитания.                            |
| 100   | Декодер использует уровень питания, оптимизированный для качества видео. |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
