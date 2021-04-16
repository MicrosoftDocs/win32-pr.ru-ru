---
description: Изменяет режим запуска \_ службы Win32 SystemDriver.
ms.assetid: 34f4e0ac-d8a0-4be7-8c84-0252e50db441
ms.tgt_platform: multiple
title: Метод Чанжестартмоде класса Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: edb6dfc9d745f5e408871246b581e6fab7eb72d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538774"
---
# <a name="changestartmode-method-of-the-win32_systemdriver-class"></a>Метод Чанжестартмоде \_ класса Win32 SystemDriver

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) чанжестартмоде изменяет режим запуска службы [**\_ SystemDriver Win32**](win32-systemdriver.md) .

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*StartMode* \[ окне\]
</dt> <dd>

Режим запуска базовой службы Windows.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Запуск загрузки** ("Boot")


</dt> <dd>

Драйвер устройства запущен загрузчиком операционной системы. Это значение допустимо только для служб драйверов.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Система** ("System")


</dt> <dd>

Драйвер устройства запущен процессом инициализации операционной системы. Это значение допустимо только для служб драйверов.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Автоматический запуск** (автоматический)


</dt> <dd>

Служба запускается автоматически диспетчером управления службами во время запуска системы.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Запуск по требованию** (вручную)


</dt> <dd>

Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-systemdriver.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** ("отключено")


</dt> <dd>

Служба, которая больше не может быть запущена.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (нуль), если служба была успешно изменена, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.

<dl> <dt>

**Успешно** (0)
</dt> <dt>

**Не поддерживается** (1)
</dt> <dt>

**Отказано в доступе** (2)
</dt> <dt>

**Запуск зависимых служб** (3)
</dt> <dt>

**Недопустимый элемент управления службой** (4)
</dt> <dt>

**Служба не может принять управление** (5)
</dt> <dt>

**Служба неактивна** (6)
</dt> <dt>

**Время ожидания запроса на обслуживание** (7)
</dt> <dt>

**Неизвестный сбой** (8)
</dt> <dt>

**Путь не найден** (9)
</dt> <dt>

**Служба уже запущена** (10)
</dt> <dt>

**База данных службы заблокирована** (11)
</dt> <dt>

**Удалена зависимость службы** (12)
</dt> <dt>

**Сбой зависимости службы** (13)
</dt> <dt>

**Служба отключена** (14)
</dt> <dt>

**Сбой входа службы** (15)
</dt> <dt>

**Служба помечена для удаления** (16)
</dt> <dt>

**Служба без потока** (17)
</dt> <dt>

**Состояние "циклическая зависимость** " (18)
</dt> <dt>

**Состояние "повторяющееся имя** " (19)
</dt> <dt>

**Состояние недопустимое имя** (20)
</dt> <dt>

**Недопустимый параметр Status** (21)
</dt> <dt>

**Недопустимое состояние учетной записи службы** (22)
</dt> <dt>

**Служба состояния существует** (23)
</dt> <dt>

**Служба уже приостановлена** (24)
</dt> <dt>

**Другие** (25 4294967295)
</dt> </dl>

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

 

