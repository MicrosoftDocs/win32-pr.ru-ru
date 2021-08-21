---
description: EC_ERRORABORTEX — операция прервана из-за ошибки.
ms.assetid: de7b5222-3a29-40cc-af1a-2672bd68b7c9
title: EC_ERRORABORTEX (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18f0cb010e6ebf94f69cd8bbebfc7cdeea16d1d085069ad2f12fedb6fbf4a266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015982"
---
# <a name="ec_errorabortex"></a>EC \_ еррорабортекс

Операция прервана из-за ошибки.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**(HRESULT)** Код ошибки операции, которая завершилась ошибкой.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**(BSTR)** Строка, содержащая дополнительные сведения об ошибке.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Нет.

## <a name="remarks"></a>Remarks

фильтр [источника Windows носителя](windows-media-source-filter.md) прежних версий отправляет это событие. Новые фильтры не должны отсылать это событие.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




