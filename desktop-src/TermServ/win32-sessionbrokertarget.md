---
title: Класс Win32_SessionBrokerTarget
description: Определяет запрос для целевого объекта посредника сеанса.
ms.assetid: 35de25da-cb89-4836-be14-9544b1264248
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionBrokerTarget службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionBrokerTarget, описание
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTarget
- Win32_SessionBrokerTarget.PluginName
- Win32_SessionBrokerTarget.TargetName
- Win32_SessionBrokerTarget.FarmName
- Win32_SessionBrokerTarget.Guid
- Win32_SessionBrokerTarget.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ceca0df64eeb9cd285737fee7c6ca6fa3a2e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892654"
---
# <a name="win32_sessionbrokertarget-class"></a>\_Класс Win32 сессионброкертаржет

Определяет запрос для целевого объекта посредника сеанса.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERTARGET_Prov"), AMENDMENT]
class Win32_SessionBrokerTarget
{
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ сессионброкертаржет** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ сессионброкертаржет** имеет следующие свойства.

<dl> <dt>

**Среда**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя среды. В случае целевого объекта виртуальной машины это может быть имя узла виртуальной машины.

</dd> <dt>

**фармнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя фермы, которой принадлежит целевой объект.

</dd> <dt>

**Устройства**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Идентификатор GUID (если он есть) целевого объекта.

</dd> <dt>

**PluginName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя подключаемого модуля.

</dd> <dt>

**TargetName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя целевого объекта.

</dd> </dl>

## <a name="examples"></a>Примеры

Следующая строка запроса демонстрирует использование \_ класса Win32 сессионброкертаржет в запросе.


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerTarget WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                      |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                               |
| MOF<br/>                      | <dl> <dt>Тссдвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

