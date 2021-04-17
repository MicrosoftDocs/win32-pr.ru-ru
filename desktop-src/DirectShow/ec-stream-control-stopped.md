---
description: Команда окончания управления потоком завершена.
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: EC_STREAM_CONTROL_STOPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c5488ba400d90623955c3e9adcba0dde07e04a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685400"
---
# <a name="ec_stream_control_stopped"></a>\_Управление ПОТОКОМ \_ EC \_ остановлено

Команда окончания управления потоком завершена.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*псендер*
</dt> <dd>

(**IUnknown** \* ) Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) ПИН-кода, который остановил поток.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*двкукие*
</dt> <dd>

(**DWORD**) Определяемое пользователем значение.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Нет.

## <a name="remarks"></a>Remarks

Фильтры отправляют это событие в ответ на метод [**иамстреамконтрол:: StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) . Метод **StopAt** задает время ссылки для завершения потоковой передачи ПИН-кода. При остановке потоковой передачи фильтр отправляет это событие.

Параметр *псендер* указывает ПИН-код, который выполняет команду «Завершение». В зависимости от реализации он может не быть ПИН-кодом, полученным при вызове [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .

Параметр *двкукие* задается приложением в методе [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) . Этот параметр позволяет приложению контролировать несколько вызовов метода.

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

 

 




