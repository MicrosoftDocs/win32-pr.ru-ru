---
description: извлекает текущий Windows безопасный режим. Windows может находиться в заблокированном режиме, в незаблокированном нормальном режиме или в режиме пробной версии.
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
ms.openlocfilehash: 94dc1665dcfa98b27fc15f68a799792b57f428875fefb88c6d35de57bad71b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911294"
---
# <a name="wldpquerywindowslockdownmode-function"></a>Функция Влдпкуеривиндовслоккдовнмоде

извлекает текущий Windows безопасный режим. Windows может находиться в заблокированном режиме, в незаблокированном нормальном режиме или в режиме пробной версии.

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

при успешном выполнении возвращает [**пвлдп \_ \_ \_ режим блокировки WINDOWS**](wldp-windows-lockdown-mode.md) , который указывает безопасный режим для текущего устройства Windows 10.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **значение \_ ОК** в случае успеха или код ошибки в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1803\]<br/>                           |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




