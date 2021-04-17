---
description: Изменяет параметры виртуальной машины.
ms.assetid: 3266bd0d-398b-4d3b-9248-e29c069aab11
title: Метод Модифисистемсеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4e6bf40b3dd206affcdc014e98554bfa8f88b4c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663983"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Метод Модифисистемсеттингс \_ класса Виртуалсистемманажементсервице мсвм

Изменяет параметры виртуальной машины. При применении к параметрам системы "Текущая" Конфигурация виртуальной машины в качестве побочного результата можно изменить экземпляр виртуальной машины.

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

Встроенный экземпляр класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , который содержит измененные аспекты виртуальной машины. Свойство **InstanceId** определяет изменяемый параметр виртуальной машины.

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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Модифивиртуалсистем (v1)**](/previous-versions/windows/desktop/virtual/modifyvirtualsystem-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**Мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

