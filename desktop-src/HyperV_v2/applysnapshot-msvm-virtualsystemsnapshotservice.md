---
description: Применяет моментальный снимок виртуальной машины к виртуальной машине, из которой он был создан.
ms.assetid: 45f1ec8f-aa96-4060-8f8c-0471d0ad4a21
title: Метод Апплиснапшот класса Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6a03a76bb874ac63c8684841f3a13e413a193db8b17d85a6cad4dd62e361bc60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765604"
---
# <a name="applysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>Метод Апплиснапшот \_ класса Виртуалсистемснапшотсервице мсвм

Применяет моментальный снимок виртуальной машины к виртуальной машине, из которой он был создан.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Моментальный снимок* \[ окне\]
</dt> <dd>

Ссылка на класс, производный от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)) , который представляет моментальный снимок виртуальной машины, который необходимо применить.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Эта операция всегда выполняется асинхронно. Этот метод возвращает 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Не поддерживается** (1)
</dt> <dt>

**Сбой** (2)
</dt> <dt>

**Время ожидания** (3)
</dt> <dt>

**Недопустимый параметр** (4)
</dt> <dt>

**Недопустимое состояние** (5)
</dt> <dt>

**Недопустимый тип** (6)
</dt> <dt>

**Зарезервировано DMTF** (..)
</dt> <dt>

**Параметры метода проверены — задание запущено** (4096)
</dt> <dt>

**Отказано в доступе** (32769)
</dt> <dt>

**Недопустимый параметр** (32773)
</dt> <dt>

**Недопустимое состояние** (32775)
</dt> <dt>

**Метод зарезервирован** (4097.. 32767)
</dt> <dt>

**Зависит от поставщика** (32768.65 535)
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

[**Мсвм \_ виртуалсистемснапшотсервице**](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[**Аппливиртуалсистемснапшот (v1)**](/previous-versions/windows/desktop/virtual/applyvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**Аппливиртуалсистемснапшотекс (v1)**](/previous-versions/windows/desktop/virtual/msvm-virtualsystemmanagementservice-applyvirtualsystemsnapshotex)
</dt> </dl>

 

