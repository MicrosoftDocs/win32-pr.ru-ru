---
title: Сообщение DRV_ENABLE (Ммсистем. h)
description: Включает драйвер. Драйвер должен инициализировать любые переменные и выбрать устройства с интерфейсом ввода-вывода.
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- сообщение DRV_ENABLE Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_ENABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ab74abf08380db97a15da22fa99d58d72b6aba124a430cad665f65bc94e26c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526284"
---
# <a name="drv_enable-message"></a>DRV \_ включить сообщение

Включает драйвер. Драйвер должен инициализировать любые переменные и выбрать устройства с интерфейсом ввода-вывода.

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

Драйверы считаются включенными с момента получения этого сообщения, пока они не будут отключены с помощью сообщения об [**\_ отключении DRV**](drv-disable.md) .

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

 

 





