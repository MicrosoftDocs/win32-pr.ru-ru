---
description: Применена команда запуска управления потоком.
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: EC_STREAM_CONTROL_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984562fde9001de14067e5865d5583636b264852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651726"
---
# <a name="ec_stream_control_started"></a>\_Управление ПОТОКОМ \_ EC \_ запущено

Применена команда запуска управления потоком.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*псендер*
</dt> <dd>

(**IUnknown** \* ) Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) ПИН-кода, который запустил поток.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*двкукие*
</dt> <dd>

(**DWORD**) Определяемое пользователем значение.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Нет.

## <a name="remarks"></a>Remarks

Фильтры отправляют это событие в ответ на метод [**иамстреамконтрол:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) . Этот метод задает время ссылки для начала потоковой передачи ПИН-кода. При начале потоковой передачи фильтр отправляет это событие.

Параметр *псендер* указывает ПИН-код, который выполняет команду Start. В зависимости от реализации это может быть не ПИН-код, получивший вызов [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .

Параметр *двкукие* задается приложением в методе [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) . Этот параметр позволяет приложению контролировать несколько вызовов метода.

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

 

 




