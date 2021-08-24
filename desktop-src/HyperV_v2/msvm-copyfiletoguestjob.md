---
description: Представляет задание операции гостевой файловой службы.
ms.assetid: 3750707e-e8c8-4188-aed8-1a394d142140
title: Класс Msvm_CopyFileToGuestJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob
- Msvm_CopyFileToGuestJob.StartService
- Msvm_CopyFileToGuestJob.StopService
- Msvm_CopyFileToGuestJob.Caption
- Msvm_CopyFileToGuestJob.CreationClassName
- Msvm_CopyFileToGuestJob.Description
- Msvm_CopyFileToGuestJob.InstallDate
- Msvm_CopyFileToGuestJob.Name
- Msvm_CopyFileToGuestJob.Started
- Msvm_CopyFileToGuestJob.StartMode
- Msvm_CopyFileToGuestJob.Status
- Msvm_CopyFileToGuestJob.SystemCreationClassName
- Msvm_CopyFileToGuestJob.SystemName
- Msvm_CopyFileToGuestJob.CopyFileToGuestSettingData
- Msvm_CopyFileToGuestJob.Cancellable
- Msvm_CopyFileToGuestJob.ErrorSummaryDescription
- Msvm_CopyFileToGuestJob.VirtualSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 33fe43612425c96a5374603e6bb3a3cb6a3a56083113cc7628075ccf75c71056
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531744"
---
# <a name="msvm_copyfiletoguestjob-class"></a>\_Класс мсвм копифилетогуестжоб

Представляет задание операции гостевой файловой службы. Этот класс является производным от [**мсвм \_ гуестфилесервице**](msvm-guestfileservice.md).

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CopyFileToGuestJob : CIM_ConcreteJob
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
  string   CopyFileToGuestSettingData[];
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  string   VirtualSystemName;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ копифилетогуестжоб** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **мсвм \_ копифилетогуестжоб** содержит следующие методы.



| Метод                                                                   | Описание                                                           |
|:-------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**копифилестогуест**](copyfilestoguest-msvm-guestfileservice.md)       | Копирует файлы с узла Hyper-V на виртуальную машину.<br/> |
| [**Ошибка**](geterror-msvm-copyfiletoguestjob.md)                     | Извлекает объект ошибки для задания.<br/>                    |
| [**жетеррорекс**](geterrorex-msvm-copyfiletoguestjob.md)                 | Извлекает объекты ошибок для задания.<br/>                   |
| [**Равен**](requeststatechange-msvm-copyfiletoguestjob.md) | Изменяет состояние задания.<br/>                              |
| **StartService**                                                         | Этот метод не поддерживается.<br/>                              |
| **StopService**                                                          | Этот метод не поддерживается.<br/>                              |



 

### <a name="properties"></a>Свойства

Класс **мсвм \_ копифилетогуестжоб** имеет следующие свойства.

<dl> <dt>

**Отменяемых**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, можно ли отменить задание. Значение этого свойства не гарантирует, что запрос на отмену задания будет выполнен. Если задано **значение true**, задание может быть отменено; в противном случае — **значение false**.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое текстовое описание объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**копифилетогуестсеттингдата**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Настройка данных, используемых для копирования файла.

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

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Задание CIM**](cim-job.md)".**ErrorCode**")
</dt> </dl>

Сводное описание ошибки, если оно есть. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

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

</dd> <dt>

**виртуалсистемнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор GUID затронутой виртуальной системы.

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

[**\_КОНКРЕТЕЖОБ CIM**](cim-concretejob.md)
</dt> <dt>

[**Мсвм \_ гуестфилесервице**](msvm-guestfileservice.md)
</dt> <dt>

[**Мсвм \_ гуестсервице**](msvm-guestservice.md)
</dt> </dl>

 

