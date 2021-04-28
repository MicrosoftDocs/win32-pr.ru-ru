---
description: EC_ERRORABORTEX — операция прервана из-за ошибки.
ms.assetid: de7b5222-3a29-40cc-af1a-2672bd68b7c9
title: EC_ERRORABORTEX (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3bf1e1f24f9d5b07312f542c1ce4ea671f601d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094612"
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

Устаревший фильтр [источника Windows Media](windows-media-source-filter.md) отправляет это событие. Новые фильтры не должны отсылать это событие.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




