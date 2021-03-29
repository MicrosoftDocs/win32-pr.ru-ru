---
description: Изменяет параметры виртуальной системы.
ms.assetid: 9c3d28f8-9806-411a-866f-d062c6d31818
title: Метод Модифисистемсеттингс класса CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da610d03e683b06ad743d1b6d4fe413dc5b31d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991591"
---
# <a name="modifysystemsettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Метод Модифисистемсеттингс \_ класса CIM виртуалсистемманажементсервице

Изменяет параметры виртуальной системы.

При применении к параметрам системы "Текущая" Конфигурация виртуальной системы в качестве побочного результата можно изменить экземпляр виртуальной системы.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*SystemSettings* \[ окне\]
</dt> <dd>

Строка, содержащая экземпляр класса [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) , который используется для изменения параметров виртуальной системы. Для указания изменяемого параметра виртуальной системы экземпляр должен иметь допустимый идентификатор **InstanceId** .

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется долго, может быть возвращена также [**\_ конкретежоб CIM**](cim-concretejob.md) , представляющая задание.

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

**Несовместимые параметры** (6)
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

[**\_ВИРТУАЛСИСТЕММАНАЖЕМЕНТСЕРВИЦЕ CIM**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




