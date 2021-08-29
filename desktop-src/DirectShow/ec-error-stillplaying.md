---
description: Не удалось выполнить асинхронную команду для выполнения графа.
ms.assetid: 0bfcf4b4-b35a-4593-9956-8e1e8c9139cb
title: EC_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82383c541f2ba5294cf4d45844f096ff510f25444ce87a54b956d0a777a7fc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051784"
---
# <a name="ec_error_stillplaying"></a>EC \_ об ошибке \_ стиллплайинг

Не удалось выполнить асинхронную команду для выполнения графа.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Код ошибки операции, которая завершилась ошибкой.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Нет.

## <a name="remarks"></a>Remarks

Если диспетчер графа фильтров выдает команду асинхронного выполнения, которая завершается ошибкой, она отправляет это событие в приложение. Граф остается в состоянии выполнения. Состояние базовых фильтров не определено. Некоторые фильтры могут выполняться, другие могут не иметь.

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

 

 




