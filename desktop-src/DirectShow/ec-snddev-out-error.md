---
description: Произошла ошибка устройства в фильтре модуля подготовки звука.
ms.assetid: 60e36476-f553-468d-a28d-351fdf4a02f1
title: EC_SNDDEV_OUT_ERROR (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefe6dbe57b26bf167a7fbc668010930bacffc321d42d2847ae6776696e009fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792414"
---
# <a name="ec_snddev_out_error"></a>\_Ошибка EC снддев \_ out \_

Произошла ошибка устройства в фильтре модуля подготовки звука.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Значение типа DWORD из перечислимого типа [**снддев \_ Err**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) , указывающее, как осуществлялся доступ к устройству в момент возникновения сбоя.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Значение типа DWORD, указывающее на ошибку, возвращенную при вызове звукового устройства.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Отсутствует.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




