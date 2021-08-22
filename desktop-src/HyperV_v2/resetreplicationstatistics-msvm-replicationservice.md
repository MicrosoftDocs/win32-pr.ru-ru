---
description: Сбрасывает статистику репликации для виртуальной машины и действует в отношении первичной репликации виртуальной машины.
ms.assetid: da4b60f8-6964-45af-8412-935234c7c0ff
title: Метод Ресетрепликатионстатистикс класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 30f9e975b1e0b49d62b844ebee3de7111259c1f12a48ee0ff1f766131c7a6eb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531024"
---
# <a name="resetreplicationstatistics-method-of-the-msvm_replicationservice-class"></a>Метод Ресетрепликатионстатистикс \_ класса Репликатионсервице мсвм

Сбрасывает статистику репликации для виртуальной машины и действует в отношении первичной репликации виртуальной машины.

> [!Note]  
> начиная с Windows 8.1 мы рекомендуем не использовать **ресетрепликатионстатистикс** для сброса статистики репликации. Вместо этого используйте [**ресетрепликатионстатистиксекс**](resetreplicationstatisticsex-msvm-replicationservice.md).

 

## <a name="syntax"></a>Синтаксис


```mof
uint32 ResetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ComputerSystem* \[ окне\]
</dt> <dd>

Ссылка на экземпляр класса платформы [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину для сброса статистики репликации.

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**жетрепликатионстатистикс**](getreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[**Мсвм \_ репликатионсервице**](msvm-replicationservice.md)
</dt> </dl>

 

