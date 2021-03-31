---
description: Пытается отправить определяемый пользователем код элемента управления службе, управляемой драйвером системы.
ms.assetid: 62e66c35-f264-43d0-9e94-fb5e85f936e0
ms.tgt_platform: multiple
title: Метод Усерконтролсервице класса Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99974206f6487d90e1660f5a64c1d00904912c66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990736"
---
# <a name="usercontrolservice-method-of-the-win32_systemdriver-class"></a>Метод Усерконтролсервице \_ класса Win32 SystemDriver

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) усерконтролсервице пытается отправить определяемый пользователем код элемента управления службе, управляемой драйвером системы.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Контролкоде* \[ окне\]
</dt> <dd>

Задает определенные значения (от 128 до 255), которые предоставляют управляющие команды, характерные для пользователя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (ноль), если запрос **усерконтролсервице** был принят, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_SystemDriver Win32**](win32-systemdriver.md)
</dt> </dl>

 

