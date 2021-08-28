---
description: Мсвм \_ гуестфилесервице содержит метод, который можно использовать для копирования файла на виртуальную машину с узла Hyper-V.
ms.assetid: 3599d5a8-415f-48f8-b887-00a93b7abb83
title: Класс Msvm_GuestFileService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService
- Msvm_GuestFileService.StartService
- Msvm_GuestFileService.StopService
- Msvm_GuestFileService.Caption
- Msvm_GuestFileService.CreationClassName
- Msvm_GuestFileService.Description
- Msvm_GuestFileService.InstallDate
- Msvm_GuestFileService.Name
- Msvm_GuestFileService.Started
- Msvm_GuestFileService.StartMode
- Msvm_GuestFileService.Status
- Msvm_GuestFileService.SystemCreationClassName
- Msvm_GuestFileService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fa307a55963f6773682e81a08bf7d45e064c9a5bd7213f5d2d426a8d44be70b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789894"
---
# <a name="msvm_guestfileservice-class"></a>\_Класс мсвм гуестфилесервице

**Мсвм \_ Гуестфилесервице** содержит метод, который можно использовать для копирования файла на виртуальную машину с узла Hyper-V. Этот класс является производным от [**мсвм \_ гуестсервице**](msvm-guestservice.md).

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestFileService : Msvm_GuestService
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ гуестфилесервице** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **мсвм \_ гуестфилесервице** содержит следующие методы.



| Метод                                                             | Описание                                                                                                                                                                  |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**копифилестогуест**](copyfilestoguest-msvm-guestfileservice.md) | Копирует файлы с узла Hyper-V на виртуальную машину.<br/> **Windows 8.1:** этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.<br/> |
| **StartService**                                                   | Этот метод не поддерживается.<br/>                                                                                                                                     |
| **StopService**                                                    | Этот метод не поддерживается.<br/>                                                                                                                                     |



 

### <a name="properties"></a>Свойства

Класс **мсвм \_ гуестфилесервице** имеет следующие свойства.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое текстовое описание объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса или подкласса, используемого при создании экземпляра. При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время установки объекта. Для этого свойства не требуется значение, указывающее, что объект установлен. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальный идентификатор службы, который также содержит сведения об управляемых функциях. Дополнительные сведения о функциональных возможностях см. в описании свойства объекта **Description** . Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Запуск**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение равно true**, служба запущена.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, запускается ли служба автоматически (например, операционная система) или только после запроса.

В эти значения входят:

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

**Автоматическое**
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

**Документации**
</dt> </dl>

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

В эти значения входят:

<dl><span id="OK"></span><span id="ok"></span><dt>

**'**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**План**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**Пониженной функциональности**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**Неизвестный**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**"Пред Fail"**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**Start**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**Идет**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**Служеб**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**Груз**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**"Recover"**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**"Нет контакта"**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**"Потеря связи"**
</dt> </dl>

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса создания системы области.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя системы, в которой размещена служба.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                                 |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Мсвм \_ гуестсервице**](msvm-guestservice.md)
</dt> </dl>

 

