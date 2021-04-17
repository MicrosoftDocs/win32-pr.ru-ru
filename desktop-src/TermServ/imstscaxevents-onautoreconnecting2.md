---
title: Имстскаксевентс OnAutoReconnecting2, метод
description: Вызывается, когда клиент находится в процессе автоматического повторного подключения к сеансу с сервером узла сеансов удаленный рабочий стол (на узле сеансов удаленных рабочих столов). | Имстскаксевентс OnAutoReconnecting2, метод
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода OnAutoReconnecting2
- Службы удаленных рабочих столов метода OnAutoReconnecting2, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод OnAutoReconnecting2
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901bb196922d1772782ab7f1c911c96573c88b36
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684930"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a>Метод Имстскаксевентс:: OnAutoReconnecting2

Вызывается, когда клиент находится в процессе автоматического повторного подключения к сеансу с сервером узла сеансов удаленный рабочий стол (на узле сеансов удаленных рабочих столов). Это улучшенная версия метода [**онаутореконнектинг**](-imstscaxevents--onautoreconnecting.md) .

## <a name="syntax"></a>Синтаксис


```C++
void OnAutoReconnecting2(
  [in] LONG         disconnectReason,
  [in] VARIANT_BOOL networkAvailable,
  [in] LONG         attemptCount,
  [in] LONG         maxAttemptCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*дисконнектреасон* \[ окне\]
</dt> <dd>

Код, описывающий причину последнего отключения сеанса.

</dd> <dt>

*нетворкаваилабле* \[ окне\]
</dt> <dd>

Указывает, доступна ли сеть.

</dd> <dt>

*аттемпткаунт* \[ окне\]
</dt> <dd>

Число попыток, выполненных в текущем процессе автоматического повторного подключения. Это число увеличивается на единицу при каждой попытке.

</dd> <dt>

*максаттемпткаунт* \[ окне\]
</dt> <dd>

Максимальное число попыток, которое будет выполнено в текущем процессе автоматического повторного подключения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





