---
title: Сообщение DRV_ENABLE (Ммсистем. h)
description: Включает драйвер. Драйвер должен инициализировать любые переменные и выбрать устройства с интерфейсом ввода-вывода.
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- DRV_ENABLE сообщения Windows мультимедиа
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
ms.openlocfilehash: 569b4ca5f3d0dc5f439b1e2b0e25887ffd1da4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989357"
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

## <a name="remarks"></a>Комментарии

Параметры *двдриверид*, *lParam1* и *lParam2* не используются.

Драйверы считаются включенными с момента получения этого сообщения, пока они не будут отключены с помощью сообщения об [**\_ отключении DRV**](drv-disable.md) .

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

 

 





