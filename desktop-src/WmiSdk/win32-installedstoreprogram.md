---
title: '\_Класс Win32 инсталледсторепрограм'
description: класс Win32 \_ инсталледсторепрограм представляет установленное приложение Windows store.
ms.assetid: 154c19c7-f2e5-48bd-b05b-3022e45f2aa4
keywords:
- Поставщик учетных Win32_InstalledStoreProgram приложений и устройств класса
- Поставщик инвентаризации приложений и устройств класса Win32_InstalledStoreProgram, описание
topic_type:
- apiref
api_name:
- Win32_InstalledStoreProgram
- Win32_InstalledStoreProgram.ProgramId
- Win32_InstalledStoreProgram.Name
- Win32_InstalledStoreProgram.Vendor
- Win32_InstalledStoreProgram.Version
- Win32_InstalledStoreProgram.Language
- Win32_InstalledStoreProgram.Architecture
api_location:
- Root\CIMv2
api_type:
- Schema
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 613baba9990da8403417aa4f8639ed7e9b5a7a5f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917942"
---
# <a name="win32_installedstoreprogram-class"></a>\_Класс Win32 инсталледсторепрограм

класс **Win32 \_ инсталледсторепрограм** представляет установленное приложение Windows store.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class Win32_InstalledStoreProgram
{
  string ProgramId;
  string Name;
  string Vendor;
  string Version;
  string Language;
  string Architecture;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ инсталледсторепрограм** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ инсталледсторепрограм** имеет следующие свойства.

<dl> <dt>

**Архитектура**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

поддерживаемые архитектуры процессора для приложения магазина Windows.

</dd> <dt>

**Язык**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

поддерживаемые языки для приложения магазина Windows.

</dd> <dt>

**имя**;
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

имя приложения магазина Windows.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

уникальный идентификатор приложения хранилища Windows.

</dd> <dt>

**поставщик**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

издатель приложения магазина Windows.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

версия приложения для хранения Windows.

</dd> </dl>

## <a name="requirements"></a>Требования



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Аеинв. mof</dt> </dl> |



 

 





