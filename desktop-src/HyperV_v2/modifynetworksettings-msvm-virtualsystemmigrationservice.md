---
description: Изменяет сетевые подсети миграции для службы миграции виртуальной системы.
ms.assetid: 54ea230a-cda9-4fff-8f79-88f2922b2b15
title: Метод Модифинетворксеттингс класса Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.ModifyNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b57cd3ee594bda704c1bd3b6c344c90eb6a1f7fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999032"
---
# <a name="modifynetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Метод Модифинетворксеттингс \_ класса Виртуалсистеммигратионсервице мсвм

Изменяет сетевые подсети миграции для службы миграции виртуальной системы.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ModifyNetworkSettings(
  [in]  string              NetworkSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Нетворксеттингс* \[ окне\]
</dt> <dd>

Массив внедренных экземпляров класса [**мсвм \_ виртуалсистеммигратионнетворксеттингдата**](msvm-virtualsystemmigrationnetworksettingdata.md) , содержащих параметры сети миграции.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

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

[**адднетворксеттингс**](addnetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**ремовенетворксеттингс**](removenetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**Мсвм \_ виртуалсистеммигратионсервице**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

