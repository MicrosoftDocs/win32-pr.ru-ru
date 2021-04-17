---
description: Отключает указанное устройство PCI, чтобы его можно было назначить.
ms.assetid: 8ea3bc27-93ba-4db8-a4aa-cdfea225eaa9
title: Метод Дисмаунтассигнабледевице класса Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.DismountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 53036cd09113430d1045c8e9eae7a8d782b35960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683756"
---
# <a name="dismountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a>Метод Дисмаунтассигнабледевице \_ класса Ассигнабледевицесервице мсвм

Отключает указанное устройство PCI, чтобы его можно было назначить.

## <a name="syntax"></a>Синтаксис


```mof
uint32 DismountAssignableDevice(
  [in]  string              DismountSettingData,
  [out] string              DismountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Дисмаунтсеттингдата* \[ окне\]
</dt> <dd>

Внедренный экземпляр объекта данных параметра, указывающий устройство PCI для отключения.

</dd> <dt>

*Дисмаунтеддевицеинстанцепас* \[ заполняет\]
</dt> <dd>

Строка, содержащая путь к экземпляру устройства для отключенного устройства.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Ссылка на задание (может иметь значение null, если задача завершена).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении возвращает 0 или 4096; в противном случае возвращает ошибку.

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
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1703\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ ассигнабледевицесервице**](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




