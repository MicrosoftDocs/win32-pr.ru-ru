---
title: '\_Класс Win32 InstalledWin32Program'
description: Класс Win32 \_ InstalledWin32Program представляет установленное приложение Win32.
ms.assetid: 2eef00da-8597-4852-b4fb-4276d05fd724
keywords:
- Поставщик учетных Win32_InstalledWin32Program приложений и устройств класса
- Поставщик инвентаризации приложений и устройств класса Win32_InstalledWin32Program, описание
topic_type:
- apiref
api_name:
- Win32_InstalledWin32Program
- Win32_InstalledWin32Program.ProgramId
- Win32_InstalledWin32Program.Name
- Win32_InstalledWin32Program.Vendor
- Win32_InstalledWin32Program.Version
- Win32_InstalledWin32Program.Language
- Win32_InstalledWin32Program.MsiPackageCode
- Win32_InstalledWin32Program.MsiProductCode
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
ms.openlocfilehash: 51cfbf56591bca71f8364d97a9a4adb0d995c4c3
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917934"
---
# <a name="win32_installedwin32program-class"></a>\_Класс Win32 InstalledWin32Program

Класс **Win32 \_ InstalledWin32Program** представляет установленное приложение Win32.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class Win32_InstalledWin32Program
{
  string ProgramId;
  string Name;
  string Vendor;
  string Version;
  string Language;
  string MsiPackageCode;
  string MsiProductCode;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ InstalledWin32Program** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ InstalledWin32Program** имеет следующие свойства.

<dl> <dt>

**Язык**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Поддерживаемые языки для установленного приложения Win32.

</dd> <dt>

**мсипаккажекоде**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Код пакета MSI, если приложение Win32 было установлено с помощью MSI.

</dd> <dt>

**MsiProductCode**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Код продукта MSI, если приложение Win32 было установлено с помощью MSI.

</dd> <dt>

**имя**;
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя установленного приложения Win32.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникальный идентификатор установленного приложения Win32. Это значение помогает сопоставить **Win32 \_ InstalledWin32Program** с [**Win32 \_ инсталледпрограмфрамеворк**](win32-installedprogramframework.md).

</dd> <dt>

**поставщик**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Издатель установленного приложения Win32.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Версия установленного приложения Win32.

</dd> </dl>

## <a name="requirements"></a>Требования



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                           |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Аеинв. mof</dt> </dl> |



 

 





