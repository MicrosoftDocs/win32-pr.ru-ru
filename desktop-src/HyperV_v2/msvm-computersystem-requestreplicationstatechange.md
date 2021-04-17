---
description: Запрашивает изменение состояния репликации виртуальной машины на указанное значение и действует в отношении первичной репликации виртуальной машины.
ms.assetid: 65FCDADD-1C50-4816-B10B-A951D1FC9C3B
title: Метод Рекуестрепликатионстатечанже класса Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 32f0136662f043627a5fad152ee0e0aaa1845e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544735"
---
# <a name="requestreplicationstatechange-method-of-the-msvm_computersystem-class"></a>Метод Рекуестрепликатионстатечанже \_ класса ComputerSystem мсвм

Запрашивает изменение состояния репликации виртуальной машины на указанное значение и действует в отношении первичной репликации виртуальной машины. Пока изменение состояния выполняется, свойство **ReplicationState** изменяется на значение параметра *RequestedState* . Этот метод поддерживается только для экземпляров класса [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , представляющих виртуальную машину.

> [!Note]  
> Начиная с Windows 8.1 мы рекомендуем не использовать **рекуестрепликатионстатечанже** для запроса изменения состояния репликации. Вместо этого используйте [**рекуестрепликатионстатечанжеекс**](msvm-requestreplicationstatechangeex-computersystem.md).

 

## <a name="syntax"></a>Синтаксис


```mof
uint32 RequestReplicationStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*RequestedState* \[ окне\]
</dt> <dd>

Новое состояние репликации. Параметр должен иметь одно из следующих значений.

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Все готово для запуска начальной репликации** (1)


</dt> <dd>

Все готово для запуска начальной репликации.

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Ожидание завершения начальной репликации** (2)


</dt> <dd>

Ожидание завершения начальной репликации.

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Репликация** (3)


</dt> <dd>

репликация.

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Синхронизированная репликация завершена** (4)


</dt> <dd>

Синхронизированная репликация завершена.

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Приостановка** (7)


</dt> <dd>

Приостановить репликацию.

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Отменить повторную синхронизацию** (9)


</dt> <dd>

Отменить повторную синхронизацию.

</dd> </dl> </dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Необязательная ссылка на объект [**мсвм \_ конкретежоб**](msvm-concretejob.md) , который возвращается, если операция выполняется асинхронно. При наличии возвращаемой ссылки можно использовать для отслеживания хода выполнения и получения результата метода.

</dd> <dt>

*Тимеаутпериод* \[ окне\]
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.



| Возвращаемый код и значение                                                                                                                                                                | Описание                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Завершено без ошибки**</dt> <dt>0</dt> </dl>                    | Успешно<br/>                                                                                                          |
| <dl> <dt>**Параметры метода проверены — задание запущено**</dt> <dt>4096</dt> </dl> | Переход является асинхронным.<br/>                                                                                  |
| <dl> <dt>**Сбой**</dt> <dt>32768</dt> </dl>                                 |                                                                                                                             |
| <dl> <dt>**Отказано в доступе**</dt> <dt>32769</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Не поддерживается**</dt> <dt>32770</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Состояние неизвестно**</dt> <dt>32771</dt> </dl>                      |                                                                                                                             |
| <dl> <dt>**Время ожидания**</dt> <dt>32772</dt> </dl>                                |                                                                                                                             |
| <dl> <dt>**Недопустимый параметр**</dt> <dt>32773</dt> </dl>                      | Значение, указанное в одном из параметров, не поддерживается.<br/>                                                   |
| <dl> <dt>**Система используется**</dt> <dt>32774</dt> </dl>                       |                                                                                                                             |
| <dl> <dt>**Недопустимое состояние для этой операции**</dt> <dt>32775</dt> </dl>       | Значение, указанное в параметре *RequestedState* , не поддерживается в текущем режиме репликации или состоянии.<br/> |
| <dl> <dt>**Недопустимый тип данных**</dt> <dt>32776</dt> </dl>                    |                                                                                                                             |
| <dl> <dt>**Система недоступна**</dt> <dt>32777</dt> </dl>                |                                                                                                                             |
| <dl> <dt>**Недостаточно памяти**</dt> <dt>32778</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Файл не найден**</dt> <dt>32779</dt> </dl>                         |                                                                                                                             |



 

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

[**Мсвм \_ ComputerSystem**](msvm-computersystem.md)
</dt> </dl>

 

 




