---
description: описание защищенных режимов (режимов S) для Windows устройства.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: Перечисление WLDP_WINDOWS_LOCKDOWN_MODE (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_WINDOWS_LOCKDOWN_MODE
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 93a3ae8ef00c306d93995a3a97236fc9086185147144c4314726c507d8b52e57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911344"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a>\_ \_ Перечисление в режиме блокировки Windows \_ WLDP

описание защищенных режимов (режимов S) для Windows устройства. Используется в основном в [**влдпкуеривиндовслоккдовнмоде**](wldpquerywindowslockdownmode.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _WLDP_WINDOWS_LOCKDOWN_MODE { 
  WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED  = 0,
  WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL     = 1,
  WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED    = 2,
  WLDP_WINDOWS_LOCKDOWN_MODE_MAX       = 3
} WLDP_WINDOWS_LOCKDOWN_MODE, *PWLDP_WINDOWS_LOCKDOWN_MODE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**WLDP \_ \_ режим блокировки \_ Windows \_ разблокирован**
</dt> <dd>

Разблокирован. используется в основном для Windows устройств без режима S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**\_ \_ \_ \_ пробная версия режима блокировки Windows WLDP**
</dt> <dd>

ПК. используется в основном для Windows 10 пробного устройства с режимом S. режим пробной версии — особый случай для Windows 10 устройств с режимом S: политики применяются, но защита от отката для принудительной установки политики отсутствует.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP \_ \_ режим блокировки \_ Windows \_ заблокирован**
</dt> <dd>

Блокирован. используется в основном для Windows 10 устройства с режимом S. заблокированное устройство будет принудительно применять подписанные политики device Guard, поставляемые с Windows 10 образом ос с режимом S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**\_ \_ \_ максимальный режим блокировки Windows \_ WLDP**
</dt> <dd>

Максимальное значение перечисления.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Wldp. h</dt> </dl> |



 

 




