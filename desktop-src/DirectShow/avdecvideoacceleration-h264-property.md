---
description: Включает или отключает аппаратное ускорение для декодирования H. 264.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: Свойство AVDecVideoAcceleration_H264 (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84279c49e65586d07dbf1efa4c372a1b1f8770e19bd00eb827ba44b6ad43bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663968"
---
# <a name="avdecvideoacceleration_h264-property"></a>Авдеквидеоакцелератион \_ H264 Single bitrate, свойство

Включает или отключает аппаратное ускорение для декодирования H. 264.

Это свойство доступно для чтения и записи.

## <a name="data-type"></a>Тип данных

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авдеквидеоакцелератион \_ H264 Single bitrate**

## <a name="remarks"></a>Remarks

Если значение равно нулю, декодер не использует ускорение видео DirectX (ДКСВА) для декодирования H. 264. для DirectShow фильтров установите это свойство перед подключением выходного пин-кода декодера.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional приложения \[ UWP для классических приложений \|\]<br/>                     |
| Минимальная версия сервера<br/> | \[приложения UWP для классических приложений Windows 2000 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства кодека API](codec-api-properties.md)
</dt> <dt>

[**Интерфейс Икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




