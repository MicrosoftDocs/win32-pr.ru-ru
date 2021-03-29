---
description: Включает или отключает аппаратное ускорение для декодирования видео MPEG-2.
ms.assetid: 2e05f9e5-28a6-48f3-956d-a14eaf3bf4ba
title: Свойство AVDecVideoAcceleration_MPEG2 (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943459ae3810e1a0dc668c1f11c4c5d2354afaf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806587"
---
# <a name="avdecvideoacceleration_mpeg2-property"></a>Авдеквидеоакцелератион, \_ свойство MPEG2

Включает или отключает аппаратное ускорение для декодирования видео MPEG-2.

Это свойство доступно для чтения и записи.

## <a name="data-type"></a>Тип данных

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авдеквидеоакцелератион \_ MPEG2**

## <a name="remarks"></a>Комментарии

Если значение равно нулю, декодер не использует ускорение видео DirectX (ДКСВА) для декодирования видео MPEG-2. Для фильтров DirectShow установите это свойство перед подключением выходного ПИН-кода декодера.

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

 

 




