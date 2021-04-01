---
description: Извлекает текущий безопасный режим Windows. Windows может находиться в заблокированном режиме, в незаблокированном нормальном режиме или в режиме пробной версии.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: Функция Влдпкуеривиндовслоккдовнмоде (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryWindowsLockdownMode
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: fc746270a0634525154417cfba7e1529bee7edfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262721"
---
# <a name="wldpquerywindowslockdownmode-function"></a>Функция Влдпкуеривиндовслоккдовнмоде

Извлекает текущий безопасный режим Windows. Windows может находиться в заблокированном режиме, в незаблокированном нормальном режиме или в режиме пробной версии.

## <a name="syntax"></a>Синтаксис


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*локкдовнмоде* \[ заполняет\]
</dt> <dd>

При успешном выполнении возвращает [**пвлдп \_ \_ \_ режим блокировки Windows**](wldp-windows-lockdown-mode.md) , который указывает безопасный режим для текущего устройства Windows 10.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **значение \_ ОК** в случае успеха или код ошибки в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1803\]<br/>                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




