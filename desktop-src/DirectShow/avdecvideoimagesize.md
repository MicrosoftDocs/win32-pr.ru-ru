---
description: Возвращает размер декодированного изображения в пикселях.
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: Свойство Авдеквидеоимажесизе (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cbe8fc3e77de920588ca1f0ee31d86f19c7e667
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662049"
---
# <a name="avdecvideoimagesize-property"></a>Авдеквидеоимажесизе, свойство

Возвращает размер декодированного изображения в пикселях.

Это свойство доступно только для чтения.

## <a name="data-type"></a>Тип данных

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авдеквидеоимажесизе**

## <a name="property-value"></a>Значение свойства

Старшие 16 бит содержат ширину, а младшие 16 бит содержат высоту.

## <a name="remarks"></a>Комментарии

Число каналов включает канал с низкой частотой (НИЗКОЧАСТОТный), если он присутствует.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Приложения Windows 2000 Professional \[ классические приложения \| UWP\]<br/>                     |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows 2000 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства кодека API](codec-api-properties.md)
</dt> <dt>

[**Интерфейс Икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




