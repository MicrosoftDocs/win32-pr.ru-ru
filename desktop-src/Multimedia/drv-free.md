---
title: Сообщение DRV_FREE (Ммсистем. h)
description: Уведомляет драйвер о том, что он удаляется из памяти. Драйвер должен освободить память и другие выделенные системные ресурсы.
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- DRV_FREE сообщения Windows мультимедиа
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
ms.openlocfilehash: abb9d70d269cb84e0d6ef0881618b67cfef11068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989354"
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

## <a name="remarks"></a>Комментарии

Параметры *двдриверид*, *lParam1* и *lParam2* не используются.

Сообщение **DRV \_ Free** всегда является последним сообщением, которое получает драйвер устройства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Ммсистем. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Устанавливаемые драйверы](installable-drivers.md)
</dt> <dt>

[Устанавливаемые сообщения драйверов](installable-driver-messages.md)
</dt> </dl>

 

 





