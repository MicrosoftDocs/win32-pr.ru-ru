---
title: Сообщение DRV_REMOVE (Ммсистем. h)
description: Уведомляет драйвер о том, что он собирается удалить из системы. Когда драйвер получает это сообщение, он должен удалить все разделы, созданные в реестре.
ms.assetid: e4f6ce7c-29e5-4256-b08a-13571256207c
keywords:
- сообщение DRV_REMOVE Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_REMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c08302d69e934ec77908b247f3c8f6368de8de4eab36809b6102b74858adde5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496424"
---
# <a name="drv_remove-message"></a>DRV \_ Удалить сообщение

Уведомляет драйвер о том, что он собирается удалить из системы. Когда драйвер получает это сообщение, он должен удалить все разделы, созданные в реестре.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*двдриверид*
</dt> <dd>

Идентификатор устанавливаемого драйвера. Это то же значение, которое ранее было возвращено драйвером [**из \_ открытого сообщения DRV**](drv-open.md) .

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*хдрвр*
</dt> <dd>

Описатель устанавливаемого экземпляра драйвера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Параметры *lParam1* и *lParam2* не используются.

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

 

 





