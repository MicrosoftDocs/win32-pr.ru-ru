---
description: В фильтре записи звука произошла ошибка устройства.
ms.assetid: 13f8641b-7881-4f1c-816c-77c140e48ed4
title: EC_SNDDEV_IN_ERROR (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f9b95055483b1bda812179f1a1bf132d12de7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652153"
---
# <a name="ec_snddev_in_error"></a>\_Ошибка EC \_ снддев \_

В фильтре записи звука произошла ошибка устройства.

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

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




