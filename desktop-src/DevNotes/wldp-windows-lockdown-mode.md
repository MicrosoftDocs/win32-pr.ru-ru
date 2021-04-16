---
description: Описывает режимы защищенного режима (S) для устройства Windows.
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
ms.openlocfilehash: 438a44bec0745ea67b2b40c3f8aa9c0dd6bd0072
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657936"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a>\_ \_ Перечисление в режиме блокировки Windows \_ WLDP

Описывает режимы защищенного режима (S) для устройства Windows. Используется в основном в [**влдпкуеривиндовслоккдовнмоде**](wldpquerywindowslockdownmode.md).

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

Разблокирован. Используется в основном для устройств Windows без режима S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**\_ \_ \_ \_ пробная версия режима блокировки Windows WLDP**
</dt> <dd>

ПК. Используется в основном для пробного устройства Windows 10 с режимом S. Режим пробной версии — особый случай для устройств Windows 10 с режимом S: политики применяются принудительно, но защита от отката для принудительной установки политики отсутствует.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP \_ \_ режим блокировки \_ Windows \_ заблокирован**
</dt> <dd>

Блокирован. Используется в основном для устройства Windows 10 с режимом S. Заблокированное устройство будет принудительно применять подписанные политики Device Guard, поставляемые с образом ОС Windows 10 с режимом S.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**\_ \_ \_ максимальный режим блокировки Windows \_ WLDP**
</dt> <dd>

Максимальное значение перечисления.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wldp. h</dt> </dl> |



 

 




