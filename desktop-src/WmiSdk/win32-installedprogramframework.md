---
title: '\_Класс Win32 инсталледпрограмфрамеворк'
description: Класс Win32 \_ инсталледпрограмфрамеворк представляет платформу технологии, которая \_ компилируется в экземпляре Win32 InstalledWin32Program или используется во время выполнения.
ms.assetid: bb5c18c7-ec71-4579-8190-942de4fccd9e
keywords:
- Поставщик учетных Win32_InstalledProgramFramework приложений и устройств класса
- Поставщик инвентаризации приложений и устройств класса Win32_InstalledProgramFramework, описание
topic_type:
- apiref
api_name:
- Win32_InstalledProgramFramework
- Win32_InstalledProgramFramework.FrameworkName
- Win32_InstalledProgramFramework.FrameworkPublisher
- Win32_InstalledProgramFramework.FrameworkVersion
- Win32_InstalledProgramFramework.FrameworkVersionActual
- Win32_InstalledProgramFramework.ProgramId
- Win32_InstalledProgramFramework.IsPrivate
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
ms.openlocfilehash: 3e447544dbfdebd6e4f4dd12752171089b8da041
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917927"
---
# <a name="win32_installedprogramframework-class"></a>\_Класс Win32 инсталледпрограмфрамеворк

Класс **Win32 \_ инсталледпрограмфрамеворк** представляет платформу технологии, которая компилируется в экземпляре [**Win32 \_ InstalledWin32Program**](win32-installedwin32program.md) или используется во время выполнения. в настоящее время этот класс может иметь такие платформы, как OpenSSL, Visual Basic, Visual C++ .net, Visual C++, Java (обнаруживаются только двоичные файлы среды выполнения java) и CLR.

> [!Note]  
> Набор платформ, которые может обнаружить этот класс, может быть обновлен с течением времени.

 

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class Win32_InstalledProgramFramework
{
  string  FrameworkName;
  string  FrameworkPublisher;
  string  FrameworkVersion;
  string  FrameworkVersionActual;
  string  ProgramId;
  boolean IsPrivate;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ инсталледпрограмфрамеворк** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ инсталледпрограмфрамеворк** имеет следующие свойства.

<dl> <dt>

**FrameworkName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Имя платформы, от которой зависит приложение, идентифицируемое **ProgramId** .

</dd> <dt>

**фрамеворкпублишер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Издатель платформы.

</dd> <dt>

**FrameworkVersion**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Версия платформы, от которой зависит приложение.

</dd> <dt>

**фрамеворкверсионактуал**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Версия платформы, которая фактически используется приложением во время выполнения, если платформа может быть обнаружена.

</dd> <dt>

**Частный**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Значение TRUE, если приложение объединяет закрытую копию платформы.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникальный идентификатор экземпляра [**Win32 \_ InstalledWin32Program**](win32-installedwin32program.md) , с которым связаны данные платформы.

</dd> </dl>

## <a name="requirements"></a>Требования



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                           |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Аеинв. mof</dt> </dl> |



 

 





