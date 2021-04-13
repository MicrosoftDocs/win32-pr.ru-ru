---
description: Запускает репликацию виртуальной машины.
ms.assetid: 58e89329-1ad4-4473-856d-ebfd7a863fa8
title: Метод StartReplication класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.StartReplication
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4702b5b73a989e2889bf1da9e4d284afdfe5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343162"
---
# <a name="startreplication-method-of-the-msvm_replicationservice-class"></a>Метод StartReplication \_ класса Репликатионсервице мсвм

Запускает репликацию виртуальной машины. Когда клиент вызывает этот метод для реплики виртуальной машины, он запускает репликацию с помощью расширенной реплики.

## <a name="syntax"></a>Синтаксис


```mof
uint32 StartReplication(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  uint16                 InitialReplicationType,
  [in]  string                 InitialReplicationExportLocation,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ComputerSystem* \[ окне\]
</dt> <dd>

Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, для которой должна быть запущена репликация.

</dd> <dt>

*Инитиалрепликатионтипе* \[ окне\]
</dt> <dd>

Тип перемещения, используемый для выполнения начальной репликации.

<dt>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Сетевая перенаправление** (1)


</dt> <dd>

Сетевая перенаправление.

</dd> <dt>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Экспорт** (2)


</dt> <dd>

Экспорт.

</dd> <dt>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Начальная сетевая перенаправление** (3)


</dt> <dd>

Начальная сетевая перенаправление.

</dd> </dl> </dd> <dt>

*Инитиалрепликатионекспортлокатион* \[ окне\]
</dt> <dd>

Если *инитиалрепликатионтипе* имеет значение 2 (экспорт), этот параметр содержит полный путь к каталогу, в который должна быть экспортирована начальная репликация. Этот параметр не используется для других значений *инитиалрепликатионтипе* и может иметь **значение NULL**. Этот каталог можно использовать повторно для экспорта нескольких репликаций виртуальных машин. Этот метод размещает каждую репликацию виртуальной машины в отдельном подкаталоге по этому пути.

</dd> <dt>

Время *начала* \[ окне\]
</dt> <dd>

Запланированное время начала начальной репликации по сетевому подключению к серверу восстановления. Этот параметр игнорируется, если *инитиалрепликатионтипе* имеет 2 (экспорт). Если этот параметр имеет **значение NULL**, начальная репликация запускается немедленно.

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
</dt> <dt>

**Файл не найден** (32779)
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

[**Мсвм \_ репликатионсервице**](msvm-replicationservice.md)
</dt> </dl>

 

