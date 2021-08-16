---
description: Возвращает число закодированных видеокадров.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Свойство Авенкстатвидеокодедфрамес (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f8858aba7a36d79096eccad40990e1859d4073695aaf80910587bac4005d6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342565"
---
# <a name="avencstatvideocodedframes-property"></a>Авенкстатвидеокодедфрамес, свойство

Возвращает число закодированных видеокадров.

Это свойство доступно для чтения и записи.

## <a name="data-type"></a>Тип данных

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авенкстатвидеокодедфрамес**

## <a name="remarks"></a>Remarks

Это свойство доступно после завершения кодирования.

Значение этого свойства равно значению свойства [**авенкстатвидеототалфрамес**](avencstatvideototalframes-property.md) минус число пропущенных кадров. Кодировщик может удалить кадры, чтобы остаться в заданных ограничениях скорости. Он также может удалять кадры в конце потока (см. свойство [**авенккоммонстреамендхандлинг**](avenccommonstreamendhandling-property.md) ).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional приложения \[ UWP для классических приложений \|\]<br/>                     |
| Минимальная версия сервера<br/> | \[приложения UWP для классических приложений Windows 2000 \|\]<br/>                           |
| Заголовок<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства кодека API](codec-api-properties.md)
</dt> <dt>

[**Интерфейс Икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




