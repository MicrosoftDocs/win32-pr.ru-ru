---
description: Экспортирует опорную точку виртуальной системы.
ms.assetid: e4d80404-6b1b-4153-9ab2-aebab18c331a
title: Метод Експортреференцепоинт класса Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bedd051123e4f75d7438b2e3831a84204ff4aec3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664814"
---
# <a name="exportreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Метод Експортреференцепоинт \_ класса Виртуалсистемреференцепоинтсервице мсвм

Экспортирует опорную точку виртуальной системы.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ExportReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF ReferencePoint,
  [in]  string                               ExportDirectory,
  [in]  string                               ExportSettingData,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Референцепоинт* \[ окне\]
</dt> <dd>

Ссылка на экземпляр [**\_ виртуалсистемреференцепоинт мсвм**](msvm-virtualsystemreferencepoint.md) , представляющий эталонную точку для экспорта.

</dd> <dt>

*Експортдиректори* \[ окне\]
</dt> <dd>

Полный путь к каталогу, в который должна быть экспортирована эталонная точка.

</dd> <dt>

*Експортсеттингдата* \[ окне\]
</dt> <dd>

Экземпляр [**мсвм \_ виртуалсистемреференцепоинтекспортсеттингдата**](msvm-virtualsystemreferencepointexportsettingdata.md) , представляющий параметры для операции экспорта.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Необязательный параметр для отслеживания хода выполнения операции, который используется, если метод не может быть выполнен синхронно. Если операция выполняется асинхронно, возвращается значение 4096.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении возвращает значение 0 (завершено без ошибок) или 4096 (задание запущено); в противном случае возвратите ошибку.

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
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуалсистемреференцепоинтсервице**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




