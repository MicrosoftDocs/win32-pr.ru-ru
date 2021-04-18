---
description: Изменяет общие параметры системных компонентов.
ms.assetid: e745be32-c26a-4343-99c8-950788243adf
title: Метод Модифисистемкомпонентсеттингс класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9495256d1b7610bebdac1fb2cc8b70960a63304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682496"
---
# <a name="modifysystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Метод Модифисистемкомпонентсеттингс \_ класса Виртуалсистемманажементсервице мсвм

Изменяет общие параметры системных компонентов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ModifySystemComponentSettings(
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Компонентсеттингс* \[ окне\]
</dt> <dd>

Массив параметров компонента для обновления.

</dd> <dt>

*Ресултингкомпонентсеттингс* \[ заполняет\]
</dt> <dd>

При успешном выполнении возвращает массив [**мсвм \_ системкомпонентсеттингдата**](msvm-systemcomponentsettingdata.md) , ссылающийся на результирующие параметры компонента.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении возвращает 0 или 4096; в противном случае возвращает ошибку.

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
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1703\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

