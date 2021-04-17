---
title: Класс Win32_RDMSVirtualDesktop
description: Представляет виртуальный рабочий стол.
ms.assetid: e2952ec0-38d0-4a1c-b423-3ae1fbc701b3
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSVirtualDesktop службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSVirtualDesktop, описание
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop.Name
- Win32_RDMSVirtualDesktop.HostName
- Win32_RDMSVirtualDesktop.Status
- Win32_RDMSVirtualDesktop.CollectionAlias
- Win32_RDMSVirtualDesktop.SessionState
- Win32_RDMSVirtualDesktop.SessionUserName
- Win32_RDMSVirtualDesktop.UserName
- Win32_RDMSVirtualDesktop.UserDomain
- Win32_RDMSVirtualDesktop.VMState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 247c49c7ad069b4feff3469ac21ec803ebc9f741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672614"
---
# <a name="win32_rdmsvirtualdesktop-class"></a>\_Класс Win32 рдмсвиртуалдесктоп

Представляет виртуальный рабочий стол.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktop
{
  string Name;
  string HostName;
  uint32 Status;
  string CollectionAlias;
  string SessionState;
  string SessionUserName;
  string UserName;
  string UserDomain;
  uint32 VMState;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ рдмсвиртуалдесктоп** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ рдмсвиртуалдесктоп** содержит следующие методы.



| Метод                                                                                              | Описание                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**жетусерассигнмент**](getuserassignment-win32-rdmsvirtualdesktop.md)                             | Получение имени пользователя и домена пользователя, назначенного виртуальному рабочему столу.<br/> |
| [**жетвиртуалдесктопассигнедтаусер**](getvirtualdesktopassignedtouser-win32-rdmsvirtualdesktop.md) | Извлекает виртуальный рабочий стол, назначенный указанному пользователю.<br/>                       |
| [**жетвиртуалдесктопдетаилс**](getvirtualdesktopdetails-win32-rdmsvirtualdesktop.md)               | Получение дополнительных сведений о виртуальном рабочем столе.<br/>                             |
| [**жетвиртуалдесктопстате**](getvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | Получает состояние виртуального рабочего стола.<br/>                                                 |
| [**ремовеусерассигнмент**](removeuserassignment-win32-rdmsvirtualdesktop.md)                       | Удаляет назначение пользователя из виртуального рабочего стола.<br/>                                       |
| [**сетусерассигнмент**](setuserassignment-win32-rdmsvirtualdesktop.md)                             | Назначает пользователю виртуальный рабочий стол.<br/>                                                        |
| [**сетвиртуалдесктопстате**](setvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | Обновляет состояние виртуального рабочего стола.<br/>                                                   |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ рдмсвиртуалдесктоп** имеет следующие свойства.

<dl> <dt>

**коллектионалиас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Возвращает псевдоним коллекции виртуальных рабочих столов, которая управляет виртуальной машиной.

</dd> <dt>

**HostName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает имя компьютера, на котором размещена виртуальная машина.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает имя виртуальной машины.

</dd> <dt>

**SessionState**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Возвращает состояние сеанса виртуального рабочего стола.

</dd> <dt>

**сессионусернаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Возвращает имя пользователя, выполнившего вход в сеанс виртуального рабочего стола.

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает состояние виртуальной машины.

</dd> <dt>

**Доменпользователя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Возвращает доменное имя пользователя, назначенного виртуальному рабочему столу.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Возвращает имя пользователя, назначенного виртуальному рабочему столу.

</dd> <dt>

**VMState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает состояние виртуального рабочего стола.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMV2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Поставщик служб удаленный рабочий стол Management Services](rdms-api-reference.md)
</dt> </dl>

 

