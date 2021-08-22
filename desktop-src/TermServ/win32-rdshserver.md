---
title: Класс Win32_RDSHServer
description: Управляет сервером узла сеансов удаленный рабочий стол.
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDSHServer службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDSHServer, описание
topic_type:
- apiref
api_name:
- Win32_RDSHServer
- Win32_RDSHServer.Name
- Win32_RDSHServer.ConnectionBroker
- Win32_RDSHServer.CollectionAlias
- Win32_RDSHServer.ServerState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066cea4044330ab79122e9346f6f32999202f854245e5508448e40aea3521fe0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422604"
---
# <a name="win32_rdshserver-class"></a>\_Класс Win32 рдшсервер

Управляет сервером узла сеансов удаленный рабочий стол.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHServer
{
  string Name;
  string ConnectionBroker;
  string CollectionAlias;
  uint32 ServerState;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ рдшсервер** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ рдшсервер** содержит следующие методы.



| Метод                                                                          | Описание                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetInt32Property**](getint32property-win32-rdshserver.md)                   | Извлекает значение целочисленного свойства объекта **\_ рдшсервер Win32** .<br/>                                                                                                 |
| [**жетпендингстартсерверлист**](win32-rdshserver-getpendingstartserverlist.md) | Возвращает список серверов, ожидающих запуска.<br/>                                                                                                                           |
| [**жетстрингпроперти**](getstringproperty-win32-rdshserver.md)                 | Извлекает значение свойства строки объекта **Win32 \_ рдшсервер** .<br/>                                                                                                   |
| [**SetInt32Property**](setint32property-win32-rdshserver.md)                   | Обновляет значение целочисленного свойства объекта **Win32 \_ рдшсервер** .<br/>                                                                                                   |
| [**сетстрингпроперти**](setstringproperty-win32-rdshserver.md)                 | Обновляет значение свойства строки объекта **Win32 \_ рдшсервер** .<br/>                                                                                                     |
| [**тестандсетстате**](win32-rdshserver-testandsetstate.md)                     | Сравнивает текущее состояние с указанным сравниваемый операнд; Если два совпадения, то для состояния задается новое значение. Независимо от соответствия, также возвращается текущее состояние.<br/> |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ рдшсервер** имеет следующие свойства.

<dl> <dt>

**коллектионалиас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Возвращает и задает псевдоним коллекции узлов сеансов удаленных рабочих столов, которой назначен сервер удаленных рабочих столов.

</dd> <dt>

**коннектионброкер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает имя компонента подключение к удаленному рабочему столу Broker (РДКБ), который управляет доступом пользователей к серверу удаленных рабочих столов.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает и задает имя сервера удаленных рабочих столов.

</dd> <dt>

**ServerState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Описывает состояние сервера. Любое значение, отличное **от \_ Targeted** (3), зарезервировано и должно считаться недопустимым состоянием.

Возможные значения:.

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

**Целевой объект \_ НЕИЗВЕСТНО** (1)


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

**Целевой объект \_ РАБОТАЕТ** (3)


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

**Целевой объект \_ НЕДОПУСТИМое** (8)


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

**Целевой объект \_ Запуск** (9)


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

**Целевой объект \_ ОСТАНОВКА** (10)


</dt> <dd></dd> </dl>

**Windows Server 2012 R2 и Windows Server 2012:** Это свойство недоступно до Windows Server 2016.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



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

 

