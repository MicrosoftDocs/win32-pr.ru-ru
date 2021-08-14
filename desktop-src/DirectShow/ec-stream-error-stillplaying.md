---
description: Произошла ошибка в потоке, но поток по-прежнему воспроизводится.
ms.assetid: ff155c01-22ba-46dd-85b8-05eabf956908
title: EC_STREAM_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf78f1fba25316155e36eef1ed469a32bba1ce7c194a6dffb200f1fce5ede3ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820001"
---
# <a name="ec_stream_error_stillplaying"></a>EC \_ Stream \_ Error \_ стиллплайинг

Произошла ошибка в потоке, но поток по-прежнему воспроизводится.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Код ошибки операции, которая завершилась ошибкой.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Код незначительной ошибки. Обычно это значение равно нулю.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Нет. Приложение должно решить, следует ли прерывать граф.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




