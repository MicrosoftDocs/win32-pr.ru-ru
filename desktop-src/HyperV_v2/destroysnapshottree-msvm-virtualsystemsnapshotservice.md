---
description: Удаляет существующий моментальный снимок и все его дочерние элементы виртуальной машины.
ms.assetid: d7a6442a-41a5-4e82-8ec8-dbc8e14d9a89
title: Метод Дестройснапшоттри класса Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshotTree
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: eaa589b7f6c228624f14edbf5254e5b3f5c0cf7d5b6f19c696397d0b70d6e14e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254244"
---
# <a name="destroysnapshottree-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>Метод Дестройснапшоттри \_ класса Виртуалсистемснапшотсервице мсвм

Удаляет существующий моментальный снимок и все его дочерние элементы виртуальной машины.

## <a name="syntax"></a>Синтаксис


```mof
uint32 DestroySnapshotTree(
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Снапшотсеттингдата* \[ окне\]
</dt> <dd>

Ссылка на [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)) , представляющая дерево снимков виртуальной машины для уничтожения.

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуалсистемснапшотсервице**](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[**Ремовевиртуалсистемснапшоттри (v1)**](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshottree-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

