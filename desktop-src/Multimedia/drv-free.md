---
title: Сообщение DRV_FREE (Ммсистем. h)
description: Уведомляет драйвер о том, что он удаляется из памяти. Драйвер должен освободить память и другие выделенные системные ресурсы.
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- сообщение DRV_FREE Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_FREE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a558dc7a2c3ece040790b2351ff39dc3054d660eb9368567ed7ce79d40c8a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526214"
---
# <a name="drv_free-message"></a>\_Свободное сообщение DRV

Уведомляет драйвер о том, что он удаляется из памяти. Драйвер должен освободить память и другие выделенные системные ресурсы.

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

Сообщение **DRV \_ Free** всегда является последним сообщением, которое получает драйвер устройства.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Устанавливаемые драйверы](installable-drivers.md)
</dt> <dt>

[Устанавливаемые сообщения драйверов](installable-driver-messages.md)
</dt> </dl>

 

 





