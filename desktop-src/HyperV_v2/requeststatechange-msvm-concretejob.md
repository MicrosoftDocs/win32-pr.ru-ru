---
description: Запрашивает изменение состояния задания на указанное состояние.
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: Метод RequestStateChange класса Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0e7abf5f4bf78ac469e528ab72bb5786130e9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663724"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a>Метод RequestStateChange \_ класса мсвм конкретежоб

Запрашивает изменение состояния задания на указанное состояние. Вызов метода **RequestStateChange** несколько раз может привести к перезаписанию или потере предыдущих запросов. Если возвращается значение 0, задача выполнена успешно. Любой другой код возврата указывает на состояние ошибки.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*RequestedState* \[ окне\]
</dt> <dd>

Тип: **UInt16**

Новое состояние задания.

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Запуск** (2)


</dt> <dd>

Изменяет состояние на "работает".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Приостановить** (3)


</dt> <dd>

Временно останавливает задание. Цель — последующее перезапустить задание с помощью "Start". В приостановленном состоянии можно ввести состояние службы. (Это зависит от задания.)

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Завершить** (4)


</dt> <dd>

Выполнение задания в чистом виде, сохранение данных, сохранение состояния и завершение работы всех базовых процессов в порядке.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Немедленно завершает задание без необходимости сохранять данные или сохранять состояние.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Служба** (6)


</dt> <dd>

Помещает задание в состояние службы, зависящее от поставщика. Может быть возможным перезапуск задания.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF**


</dt> <dd>

Зарезервировано.

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован**


</dt> <dd>

Зарезервировано.

</dd> </dl> </dd> <dt>

*Тимеаутпериод* \[ окне\]
</dt> <dd>

Тип: **DateTime**

Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние. Для указания времени ожидания необходимо использовать формат интервала. Значение 0 или **null** указывает, что у клиента нет требований к времени для перехода. Если это свойство не содержит значений 0 или **null** и реализация не поддерживает этот параметр, должен возвращаться код возврата 4098 (использование параметра времени ожидания не поддерживается).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Этот метод возвращает одно из следующих значений.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Не поддерживается** (1)
</dt> <dt>

**Неизвестная или Неуказанная ошибка** (2)
</dt> <dt>

**Невозможно завершить в течение времени ожидания** (3)
</dt> <dt>

**Сбой** (4)
</dt> <dt>

**Недопустимый параметр** (5)
</dt> <dt>

**Используется** (6)
</dt> <dt>

**Зарезервировано DMTF** (7 4095)
</dt> <dt>

**Параметры метода проверены — начато переход** (4096)
</dt> <dt>

**Недопустимая смена состояния** (4097)
</dt> <dt>

**Использование параметра времени ожидания не поддерживается** (4098)
</dt> <dt>

**Занято** (4099)
</dt> <dt>

**Метод зарезервирован** (4100 32767)
</dt> <dt>

**Зависит от поставщика** (32768 65535)
</dt> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу [**\_ конкретежоб мсвм**](msvm-concretejob.md) может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ конкретежоб**](msvm-concretejob.md)
</dt> </dl>

 

