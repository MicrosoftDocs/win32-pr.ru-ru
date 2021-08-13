---
title: Класс Win32_SessionDirectoryVMMPlugin
description: Представляет подключаемый модуль Virtual Machine Manager (VMM), зарегистрированный в посреднике сеансов.
ms.assetid: b5c5deb1-6c1b-4547-a24a-db3ce6654144
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionDirectoryVMMPlugin службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionDirectoryVMMPlugin, описание
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin.sName
- Win32_SessionDirectoryVMMPlugin.sProvider
- Win32_SessionDirectoryVMMPlugin.sClassID
- Win32_SessionDirectoryVMMPlugin.sServiceLocation
- Win32_SessionDirectoryVMMPlugin.Priority
- Win32_SessionDirectoryVMMPlugin.Enabled
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7481022951664b49b912b854e96e2d30895b0716ee67b6eb01ce1a9f1b1561ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422364"
---
# <a name="win32_sessiondirectoryvmmplugin-class"></a>\_Класс Win32 сессиондиректоривммплугин

Представляет подключаемый модуль Virtual Machine Manager (VMM), зарегистрированный в посреднике сеансов.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYVMMPLUGIN_Prov"), AMENDMENT]
class Win32_SessionDirectoryVMMPlugin
{
  string  sName;
  string  sProvider;
  string  sClassID;
  string  sServiceLocation;
  sint32  Priority = 0;
  boolean Enabled = FALSE;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ сессиондиректоривммплугин** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ сессиондиректоривммплугин** содержит следующие методы.



| Метод                                                                             | Описание                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**жеткуррентвммплугин**](getcurrentvmmplugin-win32-sessiondirectoryvmmplugin.md) | Возвращает подключаемый модуль наивысшего приоритета, который включен.<br/> |
| [**регистервммплугин**](registervmmplugin-win32-sessiondirectoryvmmplugin.md)     | Регистрирует новый подключаемый модуль VMM.<br/>                       |
| [**сетенаблед**](setenabled-win32-sessiondirectoryvmmplugin.md)                   | Включает или отключает подключаемый модуль.<br/>                   |
| [**SetName**](setname-win32-sessiondirectoryvmmplugin.md)                         | Задает имя подключаемого модуля.<br/>                      |
| [**SetPriority**](setpriority-win32-sessiondirectoryvmmplugin.md)                 | Задает приоритет подключаемого модуля.<br/>                  |
| [**сетпровидер**](setprovider-win32-sessiondirectoryvmmplugin.md)                 | Задает имя поставщика подключаемого модуля.<br/>             |
| [**сетсервицелокатион**](setservicelocation-win32-sessiondirectoryvmmplugin.md)   | Задает расположение службы подключаемого модуля.<br/>          |
| [**унрегистервммплугин**](unregistervmmplugin-win32-sessiondirectoryvmmplugin.md) | Отменяет регистрацию подключаемого модуля.<br/>                           |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ сессиондиректоривммплугин** имеет следующие свойства.

<dl> <dt>

**Включен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, включен ли или отключен подключаемый модуль. **Значение true** , если подключаемый модуль включен или **false** в противном случае. По умолчанию подключаемый модуль отключен.

</dd> <dt>

**Приоритет**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Приоритет подключаемого модуля. Чем выше значение, тем выше приоритет подключаемого модуля. По умолчанию приоритет равен нулю.

</dd> <dt>

**склассид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор класса подключаемого модуля.

</dd> <dt>

**sName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя подключаемого модуля.

</dd> <dt>

**спровидер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя поставщика подключаемого модуля.

</dd> <dt>

**ссервицелокатион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Расположение службы, с которой должен связаться подключаемый модуль.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                      |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                               |
| MOF<br/>                      | <dl> <dt>Тссдвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

