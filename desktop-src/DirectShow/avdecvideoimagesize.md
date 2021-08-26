---
description: Возвращает размер декодированного изображения в пикселях.
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: Свойство Авдеквидеоимажесизе (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4c059dfb1b2aebad4da10e54a3ecc1224a00d9cffcdb13dc7c87f4e29d4e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000194"
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

## <a name="remarks"></a>Remarks

Число каналов включает канал с низкой частотой (НИЗКОЧАСТОТный), если он присутствует.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional приложения \[ UWP для классических приложений \|\]<br/>                     |
| Минимальная версия сервера<br/> | \[приложения UWP для классических приложений Windows 2000 \|\]<br/>                           |
| Заголовок<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства кодека API](codec-api-properties.md)
</dt> <dt>

[**Интерфейс Икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




