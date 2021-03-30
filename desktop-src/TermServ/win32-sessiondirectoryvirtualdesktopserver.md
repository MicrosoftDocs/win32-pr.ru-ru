---
title: Класс Win32_SessionDirectoryVirtualDesktopServer
description: Представляет Узел виртуализации удаленных рабочих столов сервер (узел виртуализации удаленных рабочих столов), присоединенный к посреднику сеансов.
ms.assetid: a09221bd-d1b1-465b-91bb-9ca400a796b1
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionDirectoryVirtualDesktopServer службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionDirectoryVirtualDesktopServer, описание
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVirtualDesktopServer
- Win32_SessionDirectoryVirtualDesktopServer.Name
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2940679c13c5bd86f7d6b02340698f529e8149e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071342"
---
# <a name="win32_sessiondirectoryvirtualdesktopserver-class"></a>\_Класс Win32 сессиондиректоривиртуалдесктопсервер

Представляет Узел виртуализации удаленных рабочих столов сервер (узел виртуализации удаленных рабочих столов), присоединенный к посреднику сеансов.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_SDVirtualDesktopServer_Prov"), AMENDMENT]
class Win32_SessionDirectoryVirtualDesktopServer
{
  string Name;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ сессиондиректоривиртуалдесктопсервер** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ сессиондиректоривиртуалдесктопсервер** имеет следующие свойства.

<dl> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

DNS-имя сервера узла виртуализации удаленных рабочих столов. Это имя имеет вид "*MachineName*. *Domain*. com ".

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                      |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                               |
| MOF<br/>                      | <dl> <dt>Тссдвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

