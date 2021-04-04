---
description: Определяет, можно ли перенести указанную виртуальную систему.
ms.assetid: 1bf1b385-162e-41c9-a408-f7ee755a9646
title: Метод Чекквиртуалсистемисмигратабле класса Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratable
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1aed843f3f0f4c6c30eb6125cdd5859cdba902d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896846"
---
# <a name="checkvirtualsystemismigratable-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Метод Чекквиртуалсистемисмигратабле \_ класса Виртуалсистеммигратионсервице мсвм

Определяет, можно ли перенести указанную виртуальную систему.

## <a name="syntax"></a>Синтаксис


```mof
uint32 CheckVirtualSystemIsMigratable(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ComputerSystem* \[ окне\]
</dt> <dd>

Ссылка на экземпляр класса платформы [**CIM \_**](cim-computersystem.md) , представляющий виртуальную машину для проверки возможности миграции.

</dd> <dt>

*Дестинатионхост* \[ окне\]
</dt> <dd>

Имя хостовой системы для миграции. Формат этого имени задается свойством **дестинатионхостформатссуппортед** класса [**мсвм \_ виртуалсистеммигратионкапабилитиес**](msvm-virtualsystemmigrationcapabilities.md) , связанного с этим классом.

</dd> <dt>

*Мигратионсеттингдата* \[ окне\]
</dt> <dd>

Встроенный экземпляр класса [**мсвм \_ виртуалсистеммигратионсеттингдата**](msvm-virtualsystemmigrationsettingdata.md) , представляющий параметры для операции миграции.

</dd> <dt>

*Невсистемсеттингдата* \[ окне\]
</dt> <dd>

Встроенный экземпляр класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , представляющий новые свойства, применимые к виртуальной системе после переноса.

</dd> <dt>

*Невресаурцесеттингдата* \[ окне\]
</dt> <dd>

Массив строк, содержащий встроенный экземпляр класса [**мсвм \_ ресаурцеаллокатионсеттингдата**](msvm-resourceallocationsettingdata.md) , который представляет новые свойства, применимые к виртуальным ресурсам виртуальной системы после переноса.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.

<dl> <dt>

**Параметры метода проверены — задание запущено** (4096)
</dt> <dt>

**Сбой** (32768)
</dt> <dt>

**Отказано в доступе** (32769)
</dt> <dt>

**Не поддерживается** (32770)
</dt> <dt>

**Состояние неизвестно** (32771)
</dt> <dt>

**Время ожидания** (32772)
</dt> <dt>

**Недопустимый параметр** (32773)
</dt> <dt>

**Система используется** (32774)
</dt> <dt>

**Недопустимое состояние для этой операции** (32775)
</dt> <dt>

**Неверный тип данных** (32776)
</dt> <dt>

**Система недоступна** (32777)
</dt> <dt>

**Недостаточно памяти** (32778)
</dt> </dl>

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

[**Мсвм \_ виртуалсистеммигратионсервице**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

