---
description: Инициализирует или повторно инициализирует список системных образов.
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: Функция Филеиконинит
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIconInit
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 1771e1f0bde83f0fc7d070787b7a19f87007e26bd1ad42dcaa88e230e61a60af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111814"
---
# <a name="fileiconinit-function"></a>Функция Филеиконинит

Инициализирует или повторно инициализирует список системных образов.

## <a name="syntax"></a>Синтаксис


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фресторекаче* \[ окне\]
</dt> <dd>

Тип: **bool** .

**Значение true** , чтобы восстановить кэш образа системы с диска; В противном случае — **значение false** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **bool** .

**Значение true** , если кэш успешно обновлен, и **false** в случае сбоя инициализации.

## <a name="remarks"></a>Remarks

Если вы используете списки системных образов в собственном процессе, необходимо вызвать **филеиконинит** в следующее время:

-   При запуске.
-   В ответ на сообщение [**\_ сеттингчанже WM**](../winmsg/wm-settingchange.md) , если установлен [**флаг \_ SPI сетнонклиентметрикс**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

**Филеиконинит** не включается в заголовочный файл. Его необходимо вызвать непосредственно из Shell32.dll с использованием порядкового номера 660.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
