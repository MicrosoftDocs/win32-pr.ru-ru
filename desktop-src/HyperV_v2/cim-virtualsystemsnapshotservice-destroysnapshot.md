---
description: Уничтожает существующий моментальный снимок виртуальной системы. Этот метод может оказаться побочным действием уничтожить другие моментальные снимки, зависящие от затронутого моментального снимка.
ms.assetid: 69f60d0e-50ef-4a38-ad4b-88534b7fb3f8
title: Метод Дестройснапшот класса CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80d618374d2da4a12f2ce31284d7b3fa36ba65ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542391"
---
# <a name="destroysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a>Метод Дестройснапшот \_ класса CIM виртуалсистемснапшотсервице

Уничтожает существующий моментальный снимок виртуальной системы. Этот метод может оказаться побочным действием уничтожить другие моментальные снимки, зависящие от затронутого моментального снимка.

## <a name="syntax"></a>Синтаксис


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Аффектедснапшот* \[ окне\]
</dt> <dd>

Ссылка [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) на затронутый моментальный снимок виртуальной системы.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется долго, может быть возвращена также [**\_ конкретежоб CIM**](cim-concretejob.md) , представляющая задание.

> [!Note]  
> Этот параметр был доступен для чтения и записи в Windows 8.1.

 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.

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
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ВИРТУАЛСИСТЕМСНАПШОТСЕРВИЦЕ CIM**](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




