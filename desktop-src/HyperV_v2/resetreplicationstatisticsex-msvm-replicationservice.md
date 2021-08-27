---
description: Сбрасывает статистику репликации, связанную с указанным отношением репликации указанной виртуальной машины.
ms.assetid: 6E49A7C0-2F60-444E-964E-420470EE1538
title: 'Метод Msvm_ReplicationService:: Ресетрепликатионстатистиксекс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 613d35a03d224032a07468c2ed2d830c73c3a899df455cc3e0cd68b335797b3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083074"
---
# <a name="msvm_replicationserviceresetreplicationstatisticsex-method"></a>Мсвм \_ репликатионсервице:: ресетрепликатионстатистиксекс, метод

Сбрасывает статистику репликации, связанную с указанным отношением репликации указанной виртуальной машины.

## <a name="syntax"></a>Синтаксис


```C++
uint32 ResetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ComputerSystem* \[ окне\]
</dt> <dd>

Ссылка на экземпляр [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину с поддержкой реплики.

</dd> <dt>

*Репликатионрелатионшип* \[ окне\]
</dt> <dd>

Строковое представление внедренного экземпляра класса [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , определяющего отношение репликации, для которого сбрасывается статистика репликации.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)). Если задача завершена, ссылка может иметь **значение NULL** .

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                                 |
| Пространство имен<br/>                | \\\\Корневая \\ виртуализация \\ версии 2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**жетрепликатионстатистиксекс**](getreplicationstatisticsex-msvm-replicationservice.md)
</dt> <dt>

[**Мсвм \_ репликатионсервице**](msvm-replicationservice.md)
</dt> </dl>

 

