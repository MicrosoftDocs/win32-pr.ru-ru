---
description: Импортирует метаданные опорной точки виртуальной системы.
ms.assetid: 8e32fded-cd84-4586-83c4-c23200d4698e
title: Метод Импортреференцепоинтметадата класса Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ImportReferencePointMetadata
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2757464e8b101819dc46a778df142e4e8ed37d93b774a87a037a7d272812f883
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147937"
---
# <a name="importreferencepointmetadata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Метод Импортреференцепоинтметадата \_ класса Виртуалсистемреференцепоинтсервице мсвм

Импортирует метаданные опорной точки виртуальной системы.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ImportReferencePointMetadata(
  [in]  Msvm_ComputerSystem REF AffectedSystem,
  [in]  string                  ConfigFilePath,
  [in]  string                  RuntimeStateFilePath,
  [out] CIM_ConcreteJob     REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Аффектедсистем* \[ окне\]
</dt> <dd>

Ссылка на объект [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , описывающий затронутую систему.

</dd> <dt>

*Конфигфилепас* \[ окне\]
</dt> <dd>

Полный путь к файлу конфигурации, из которого будут импортированы метаданные точки ссылки.

</dd> <dt>

*Рунтиместатефилепас* \[ окне\]
</dt> <dd>

Полный путь к файлу состояния среды выполнения, из которого будут импортированы метаданные точки ссылки.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Необязательный параметр для отслеживания хода выполнения операции, который используется, если метод не может быть выполнен синхронно. Если операция выполняется асинхронно, возвращается значение 4096.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (нет ошибки) или одно из следующих сообщений об ошибке:

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
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1703\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуалсистемреференцепоинтсервице**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




