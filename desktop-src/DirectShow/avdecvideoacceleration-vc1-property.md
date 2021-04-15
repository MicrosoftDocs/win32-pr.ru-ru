---
description: Включает или отключает аппаратное ускорение для декодирования видео VC-1.
ms.assetid: eee85330-098e-4f21-81b7-a493abbd599b
title: Свойство AVDecVideoAcceleration_VC1 (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fcdbe265f5a65212a2846b724f570b024ea0ab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655603"
---
# <a name="avdecvideoacceleration_vc1-property"></a>Авдеквидеоакцелератион \_ VC1, свойство

Включает или отключает аппаратное ускорение для декодирования видео VC-1.

Это свойство доступно для чтения и записи.

## <a name="data-type"></a>Тип данных

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авдеквидеоакцелератион \_ VC1**

## <a name="remarks"></a>Комментарии

Если значение равно нулю, декодер не использует ускорение видео DirectX (ДКСВА) для декодирования видео VC-1. Для фильтров DirectShow установите это свойство перед подключением выходного ПИН-кода декодера.

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

 

 




