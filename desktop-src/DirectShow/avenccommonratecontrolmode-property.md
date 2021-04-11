---
description: Задает режим управления скоростью.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: Свойство Авенккоммонратеконтролмоде (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d18d0d7cb68936326fb4c4ba08188e362fdc91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262464"
---
# <a name="avenccommonratecontrolmode-property"></a>Авенккоммонратеконтролмоде, свойство

Задает режим управления скоростью.

Приложения могут задать это свойство, чтобы задать режим управления скоростью. Кодировщики также могут возвращать это свойство как возможность.

Это свойство доступно для чтения и записи.

## <a name="data-type"></a>Тип данных

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авенккоммонратеконтролмоде**

## <a name="property-value"></a>Значение свойства

Значение этого свойства является членом перечисления [**еавенккоммонратеконтролмоде**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) .

## <a name="remarks"></a>Комментарии

Это свойство также используется с [кодировщиками камер H. 264 увк 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

[Кодекапи \_ Авенквидеотемпораллайеркаунт](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [кодекапи \_ авенквидеаусаже](/windows/desktop/medfound/codecapi-avencvideousage)и кодекапи \_ авенккоммонратеконтролмоде являются статическими свойствами кодировщика. После установки они вступят в силу только после того, как на выходном контакте камеры будет вызван тип набора носителей.

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

 

