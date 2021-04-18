---
description: Определяет, можно ли перенести указанную виртуальную систему в целевую систему.
ms.assetid: 2E340737-DEE9-4853-ACD8-BEE2A8C69D6D
title: Метод Чекквиртуалсистемисмигратаблетосистем класса Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3e8f294f7e30740e3afab8987c734dbbdbd12acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682483"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Метод Чекквиртуалсистемисмигратаблетосистем \_ класса Виртуалсистеммигратионсервице мсвм

Определяет, можно ли перенести указанную виртуальную систему в целевую систему.

## <a name="syntax"></a>Синтаксис


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  Msvm_ComputerSystem REF DestinationSystem,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ComputerSystem* \[ окне\]
</dt> <dd>

Ссылка на экземпляр класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , представляющий виртуальную машину для проверки возможности миграции.

</dd> <dt>

*Дестинатионсистем* \[ окне\]
</dt> <dd>

Ссылка на экземпляр класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , представляющий виртуальную машину для проверки возможности миграции.

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

*Переносимость* \[ заполняет\]
</dt> <dd>

Получает результат проверки миграции, указывающий, можно ли успешно выполнить миграцию виртуальной системы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Не поддерживается** (1)
</dt> <dt>

**Сбой** (2)
</dt> <dt>

**Время ожидания** (3)
</dt> <dt>

**Недопустимый параметр** (4)
</dt> <dt>

**Недопустимое состояние** (5)
</dt> <dt>

**Несовместимые параметры** (6)
</dt> <dt>

**Зарезервировано DMTF** (..)
</dt> <dt>

**Метод зарезервирован** (4097.. 32767)
</dt> <dt>

**Зависит от поставщика** (32768.65 535)
</dt> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуалсистеммигратионсервице**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




