---
description: Возвращает число закодированных видеокадров.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Свойство Авенкстатвидеокодедфрамес (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aed3ed0a06003807a6bd0db90b8978282042daf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140190"
---
# <a name="avencstatvideocodedframes-property"></a>Авенкстатвидеокодедфрамес, свойство

Возвращает число закодированных видеокадров.

Это свойство доступно для чтения и записи.

## <a name="data-type"></a>Тип данных

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авенкстатвидеокодедфрамес**

## <a name="remarks"></a>Комментарии

Это свойство доступно после завершения кодирования.

Значение этого свойства равно значению свойства [**авенкстатвидеототалфрамес**](avencstatvideototalframes-property.md) минус число пропущенных кадров. Кодировщик может удалить кадры, чтобы остаться в заданных ограничениях скорости. Он также может удалять кадры в конце потока (см. свойство [**авенккоммонстреамендхандлинг**](avenccommonstreamendhandling-property.md) ).

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

 

 




