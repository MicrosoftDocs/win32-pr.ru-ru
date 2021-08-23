---
description: Операция WPD \_ \_ указывает, что значения перечисления описывают текущее состояние выполняемой операции.
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: Перечисление WPD_OPERATION_STATES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_OPERATION_STATES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3c2bc25fdbc040bd849d60f1e16e5d86d1916ced17eb6670ceb3bc6a75108772
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696487"
---
# <a name="wpd_operation_states-enumeration"></a>\_ \_ Перечисление состояний операций WPD

**Операция WPD \_ \_ указывает** , что значения перечисления описывают текущее состояние выполняемой операции.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagWPD_OPERATION_STATES { 
  WPD_OPERATION_STATE_UNSPECIFIED  = 0,
  WPD_OPERATION_STATE_STARTED      = 1,
  WPD_OPERATION_STATE_RUNNING      = 2,
  WPD_OPERATION_STATE_PAUSED       = 3,
  WPD_OPERATION_STATE_CANCELLED    = 4,
  WPD_OPERATION_STATE_FINISHED     = 5,
  WPD_OPERATION_STATE_ABORTED      = 6
} WPD_OPERATION_STATES;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**\_состояние операции WPD не \_ \_ указано**
</dt> <dd>

Текущая операция находится в неопределенном состоянии (не задано) и неизвестно.

</dd> <dt>

<span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**\_состояние операции \_ WPD \_ запущено**
</dt> <dd>

Операция запущена.

</dd> <dt>

<span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**\_выполняется операция \_ с состоянием "WPD" \_**
</dt> <dd>

Операция выполняется.

</dd> <dt>

<span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**\_состояние операции \_ WPD \_ приостановлено**
</dt> <dd>

Операция приостановлена.

</dd> <dt>

<span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**\_состояние операции \_ WPD \_ отменено**
</dt> <dd>

Операция отменена.

</dd> <dt>

<span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**\_состояние операции \_ WPD \_ завершено**
</dt> <dd>

Операция завершена.

</dd> <dt>

<span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**\_состояние операции \_ WPD \_ прервано**
</dt> <dd>

Операция прервана.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эти значения принимаются в определяемом приложением обратном вызове ([**ипортабледевицеевенткаллбакк**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




