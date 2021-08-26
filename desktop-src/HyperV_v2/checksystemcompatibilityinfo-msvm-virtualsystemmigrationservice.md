---
description: Проверяет сведения о совместимости для обеспечения совместимости с системой размещающего компьютера.
ms.assetid: 1991c58e-2d0b-4fc3-a04a-c18f358451f6
title: Метод Чекксистемкомпатибилитинфо класса Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7492d3f7dcdc20abca5cd574d1006b5e2090d02d28f7446dd94ec7b777541b39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041984"
---
# <a name="checksystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Метод Чекксистемкомпатибилитинфо \_ класса Виртуалсистеммигратионсервице мсвм

Проверяет сведения о совместимости для обеспечения совместимости с системой размещающего компьютера.

## <a name="syntax"></a>Синтаксис


```mof
uint32 CheckSystemCompatibilityInfo(
  [in]  uint8  CompatibilityInfo[],
  [out] string Reasons[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Компатибилитинфо* \[ окне\]
</dt> <dd>

Большой двоичный объект данных, полученный путем вызова метода [**жетсистемкомпатибилитинфо**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) в системе размещающего компьютера.

</dd> <dt>

*Причины* \[ заполняет\]
</dt> <dd>

Массив строк, получающих внедренные экземпляры класса [**\_ ошибок мсвм**](msvm-error.md) , которые представляют все предупреждения или ошибки.

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
</dt> <dt>

**Не совместимо** (32784)
</dt> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуалсистеммигратионсервице**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




