---
description: '\_Константы битового флага линекаллкомплмоде описывают различные способы выполнения вызова.'
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: Константы LINECALLCOMPLMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373a66b6ce13b7bfba00303bea824f542bf0016a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685422"
---
# <a name="linecallcomplmode_-constants"></a>\_Константы линекаллкомплмоде

Константы битового флага **линекаллкомплмоде \_** описывают различные способы выполнения вызова.

<dl> <dt>

<span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**\_обратный вызов линекаллкомплмоде**
</dt> <dd> <dl> <dt>



Запрашивает вызываемую станцию для возврата вызова, когда она возвращается в режим простоя.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**ЛИНЕКАЛЛКОМПЛМОДЕ \_ кампон**
</dt> <dd> <dl> <dt>



Ставит в очередь вызов до завершения вызова.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**ЛИНЕКАЛЛКОМПЛМОДЕ \_ атака**
</dt> <dd> <dl> <dt>



Добавляет приложение к существующему вызову на вызываемой станции (барже в).


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**\_сообщение линекаллкомплмоде**
</dt> <dd> <dl> <dt>



Оставляет короткое предопределенное сообщение для вызываемой станции (оставьте слово вызов). Отправляемое сообщение указывается отдельно.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Без расширяемости. Все 32 бит зарезервированы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




