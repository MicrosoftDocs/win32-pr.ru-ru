---
description: Метод РемовеассоЦиатеддата класса Msvm_VirtualSystemReferencePointService — удаляет журнал данных, связанный с точкой ссылки.
ms.assetid: b6206bda-c195-4c6f-9b80-508c20b53ce5
title: Метод РемовеассоЦиатеддата класса Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3f8cef79e55379df1f91a0e1291144a7f4fdf92378e44cd9ed3588c83b3a3d4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147907"
---
# <a name="removeassociateddata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Метод РемовеассоЦиатеддата \_ класса Виртуалсистемреференцепоинтсервице мсвм

Удаляет журнал данных, связанный с точкой ссылки.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RemoveAssociatedData(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Аффектедреференцепоинт* \[ окне\]
</dt> <dd>

Ссылка на экземпляр [**\_ виртуалсистемреференцепоинт мсвм**](msvm-virtualsystemreferencepoint.md) , представляющий удаляемую точку ссылки.

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
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуалсистемреференцепоинтсервице**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




