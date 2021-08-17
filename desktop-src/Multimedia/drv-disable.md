---
title: Сообщение DRV_DISABLE (Ммсистем. h)
description: Отключает драйвер. Драйвер должен разместить соответствующее устройство (если оно имеется) в неактивном состоянии и завершить любые функции обратного вызова или потоки.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- сообщение DRV_DISABLE Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_DISABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d9c5a99414f0b755efbae005365d89665a2b2bc5a4673436101066ec740564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144417"
---
# <a name="drv_disable-message"></a>DRV \_ отключить сообщение

Отключает драйвер. Драйвер должен разместить соответствующее устройство (если оно имеется) в неактивном состоянии и завершить любые функции обратного вызова или потоки.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*хдрвр*
</dt> <dd>

Описатель устанавливаемого экземпляра драйвера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Параметры *двдриверид*, *lParam1* и *lParam2* не используются.

После отключения драйвера система обычно отправляет драйверу краткое сообщение [**DRV \_**](drv-free.md) , прежде чем удалить драйвер из памяти.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Устанавливаемые драйверы](installable-drivers.md)
</dt> <dt>

[Устанавливаемые сообщения драйверов](installable-driver-messages.md)
</dt> </dl>

 

 





