---
title: Класс Win32_SessionBrokerServiceProperties
description: Определяет запрос для службы посредника сеансов.
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionBrokerServiceProperties службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionBrokerServiceProperties, описание
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties.SBNetworkName
- Win32_SessionBrokerServiceProperties.SBDbConnectionString
- Win32_SessionBrokerServiceProperties.SBDbSecondaryConnectionString
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f095272ee0d836e77542e20badbe5bb1169206cc6b0e87d742e3fbd235acd52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656184"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a>\_Класс Win32 сессионброкерсервицепропертиес

Определяет запрос для службы посредника сеансов.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, singleton, provider("Win32_WIN32_SESSIONBROKERSERVICEPROPERTIES_Prov"), AMENDMENT]
class Win32_SessionBrokerServiceProperties
{
  string SBNetworkName;
  string SBDbConnectionString;
  string SBDbSecondaryConnectionString;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ сессионброкерсервицепропертиес** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](/windows)

### <a name="methods"></a>Методы

Класс **Win32 \_ сессионброкерсервицепропертиес** содержит следующие методы.



| Метод                                                                                                | Описание                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**делетесбдбконнектионстринг**](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | Удаляет строки подключения к базе данных (первичные и вторичные) из реестра.<br/> **Windows Server 2012 r2, Windows Server 2012 и Windows Server 2008 r2:** Этот метод недоступен до Windows Server 2016<br/> |
| [**инсталлброкердатабасе**](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | Устанавливает RDCB DB на Центральный SQL Server<br/>                                                                                                                                                                    |
| [**исдбреачабле**](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | Проверяет доступность базы данных<br/>                                                                                                                                                                                                 |
| [**сетброкерхамоде**](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | переносит данные из локальной базы данных WID в новую базу данных на основе SQL Server. Он также настраивает сервер брокера для использования центрального SQL Server<br/>                                                                                        |
| [**сетброкернонхамоде**](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | переносит данные из центрального SQL Server в локальную базу данных. Он также настраивает сервер брокера для использования локальной базы данных.<br/>                                                                                                              |
| [**сетсбдбконнектионстрингс**](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | Сохраняет строки подключения к базе данных (первичные и вторичные) в реестре.<br/> **Windows Server 2012 r2, Windows Server 2012 и Windows Server 2008 r2:** Этот метод недоступен до Windows Server 2016<br/>     |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ сессионброкерсервицепропертиес** имеет следующие свойства.

<dl> <dt>

**сбдбконнектионстринг**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Строка подключения к базе данных, используемая службой посредника сеансов.

**Windows Server 2008 R2:** Это свойство недоступно до Windows Server 2012

</dd> <dt>

**сбдбсекондариконнектионстринг**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Необязательный элемент. Строка подключения к базе данных-получателю, используемая службой посредника сеансов для поддержки истечения срока действия пароля.

**Windows Server 2012 r2, Windows Server 2012 и Windows Server 2008 r2:** Это свойство недоступно до Windows Server 2016

</dd> <dt>

**сбнетворкнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Сетевое имя, используемое службой посредника сеансов.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                      |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                               |
| MOF<br/>                      | <dl> <dt>Тссдвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

