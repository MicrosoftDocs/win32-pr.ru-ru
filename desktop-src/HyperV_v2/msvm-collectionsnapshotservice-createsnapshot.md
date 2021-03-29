---
description: Создает моментальный снимок коллекции виртуальных систем.
ms.assetid: 2512d82f-06b9-4613-b920-d3a9be884a75
title: Метод CreateSnapshot класса Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 653dae65cc5fe50416b069da6a66e8c678c1b512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812515"
---
# <a name="createsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Метод CreateSnapshot \_ класса Коллектионснапшотсервице мсвм

Создает моментальный снимок коллекции виртуальных систем.

## <a name="syntax"></a>Синтаксис


```mof
uint32 CreateSnapshot(
  [in]      CIM_CollectionOfMSEs REF Collection,
  [in]      string                   SnapshotSettings,
  [in]      uint16                   SnapshotType,
  [in, out] CIM_Collection       REF ResultingSnapshotCollection,
  [out]     CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Коллекция* \[ окне\]
</dt> <dd>

Ссылка на [**\_ коллектионофмсес CIM**](cim-collectionofmses.md) , описывающая затронутую коллекцию виртуальных систем.

</dd> <dt>

*Снапшотсеттингс* \[ окне\]
</dt> <dd>

Содержит настройки параметров.

</dd> <dt>

*Снапшоттипе* \[ окне\]
</dt> <dd>

Запрошенный тип моментального снимка:

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Стандартный моментальный снимок** (1)


</dt> <dd>

Стандартный моментальный снимок виртуальной системы.

</dd> <dt>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Моментальный снимок восстановления** (2)


</dt> <dd>

Моментальный снимок сценариев восстановления, включая репликацию и резервное копирование.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Зависит от поставщика** (32768.65 535)


</dt> <dd></dd> </dl> </dd> <dt>

*Ресултингснапшотколлектион* \[ в, out\]
</dt> <dd>

При успешном выполнении возвращает ссылку на [**\_ коллекцию CIM**](cim-collection.md) , содержащую моментальный снимок виртуальной системы.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Необязательная ссылка, которая возвращается, если операция выполняется асинхронно. При наличии возвращаемой ссылки на экземпляр [**CIM \_ конкретежоб**](cim-concretejob.md) можно использовать для отслеживания хода выполнения и получения результата метода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении возвращает значение 0 (завершено) или 4096 (задание запущено); в противном случае возвращает ошибку.

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

**Метод зарезервирован** (4097.. 32767)
</dt> <dt>

**Зависит от поставщика** (32768.65 535)
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

[**Мсвм \_ коллектионснапшотсервице**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




