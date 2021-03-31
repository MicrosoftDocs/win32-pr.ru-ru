---
description: Мсвм \_ гуестсервице — это абстрактный базовый класс для служб в гостевой системе, к которому можно получить доступ с узла.
ms.assetid: F9E6FFE6-B8C5-4F06-BF22-A4BDB20F813A
title: Класс Msvm_GuestService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService
- Msvm_GuestService.Caption
- Msvm_GuestService.CreationClassName
- Msvm_GuestService.Description
- Msvm_GuestService.InstallDate
- Msvm_GuestService.Name
- Msvm_GuestService.Started
- Msvm_GuestService.StartMode
- Msvm_GuestService.Status
- Msvm_GuestService.SystemCreationClassName
- Msvm_GuestService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 99d1936a2678fc2d8357974f9c11a250a1d9bce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423698"
---
# <a name="msvm_guestservice-class"></a>\_Класс мсвм гуестсервице

**Мсвм \_ Гуестсервице** — это абстрактный базовый класс для служб в гостевой системе, к которому можно получить доступ с узла. Этот класс является производным от [**класса \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service) .

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, AMENDMENT]
class Msvm_GuestService : CIM_Service
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

Класс **мсвм \_ гуестсервице** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **мсвм \_ гуестсервице** содержит следующие методы.



| Метод                                                             | Описание                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**Равен**](requeststatechange-msvm-guestservice.md) | Запрашивает изменение состояния гостевой службы на указанное значение.<br/> |
| [**StartService**](startservice-msvm-guestservice.md)             | Перевод гостевой службы в состояние запуска. <br/>                                     |
| [**StopService**](stopservice-msvm-guestservice.md)               | Останавливает гостевую службу. <br/>                                                       |



 

### <a name="properties"></a>Свойства

Класс **мсвм \_ гуестсервице** имеет следующие свойства.

<dl> <dt>

**Заголовок**
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

**Name**
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                                 |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Служба CIM**](cim-service.md)
</dt> <dt>

[**\_Служба CIM**](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

