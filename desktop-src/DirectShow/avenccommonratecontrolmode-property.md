---
description: Задает режим управления скоростью.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: Свойство Авенккоммонратеконтролмоде (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aaa914f445fcbc535ec423b41306938890d64b747258cb0159add5e4fd43c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794674"
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

## <a name="remarks"></a>Remarks

Это свойство также используется с [кодировщиками камер H. 264 увк 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

[Кодекапи \_ Авенквидеотемпораллайеркаунт](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [кодекапи \_ авенквидеаусаже](/windows/desktop/medfound/codecapi-avencvideousage)и кодекапи \_ авенккоммонратеконтролмоде являются статическими свойствами кодировщика. После установки они вступят в силу только после того, как на выходном контакте камеры будет вызван тип набора носителей.

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

 

