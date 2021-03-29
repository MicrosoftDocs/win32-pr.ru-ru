---
description: Включает или отключает аппаратное ускорение для декодирования H. 264.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: Свойство AVDecVideoAcceleration_H264 (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbcedf2d038c010ee781030baf0a8289e68eab4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895033"
---
# <a name="avdecvideoacceleration_h264-property"></a>Авдеквидеоакцелератион \_ H264 Single bitrate, свойство

Включает или отключает аппаратное ускорение для декодирования H. 264.

Это свойство доступно для чтения и записи.

## <a name="data-type"></a>Тип данных

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авдеквидеоакцелератион \_ H264 Single bitrate**

## <a name="remarks"></a>Комментарии

Если значение равно нулю, декодер не использует ускорение видео DirectX (ДКСВА) для декодирования H. 264. Для фильтров DirectShow установите это свойство перед подключением выходного ПИН-кода декодера.

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

 

 




