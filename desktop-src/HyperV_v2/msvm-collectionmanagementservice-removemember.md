---
description: Удаляет указанный управляемый элемент в качестве члена данного \_ объекта КОЛЛЕКТИОНОФМСЕС CIM.
ms.assetid: ea945d24-bcff-476b-9adb-c6573cdbc0b5
title: Метод Ремовемембер класса Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RemoveMember
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 894230dcf5e9a537ca444815f8e941a8e6fcf09a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912587"
---
# <a name="removemember-method-of-the-msvm_collectionmanagementservice-class"></a>Метод Ремовемембер \_ класса Коллектионманажементсервице мсвм

Удаляет указанный управляемый элемент в качестве члена данного объекта [**\_ коллектионофмсес CIM**](cim-collectionofmses.md) .

## <a name="syntax"></a>Синтаксис


```mof
uint32 RemoveMember(
  [in]  CIM_ManagedElement   REF Member,
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Элемент* \[ окне\]
</dt> <dd>

Удаляемый элемент.

</dd> <dt>

*Коллекция* \[ окне\]
</dt> <dd>

Коллекция, из которой удаляется элемент.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Ссылка на задание (может иметь значение null, если задача завершена).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0 в случае успеха или 4096, если задание запущено; в противном случае возвращает ошибку.

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
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ коллектионманажементсервице**](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




