---
title: Класс Win32_RDMSPublishedApplication
description: Управляет опубликованным приложением.
ms.assetid: 7a529f1d-1aaf-42fb-8469-92d38a7b0ffc
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSPublishedApplication службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSPublishedApplication, описание
topic_type:
- apiref
api_name:
- Win32_RDMSPublishedApplication
- Win32_RDMSPublishedApplication.AppAlias
- Win32_RDMSPublishedApplication.PoolName
- Win32_RDMSPublishedApplication.DisplayName
- Win32_RDMSPublishedApplication.ShowInPortal
- Win32_RDMSPublishedApplication.SecurityDescriptor
- Win32_RDMSPublishedApplication.AppPath
- Win32_RDMSPublishedApplication.VirtualPath
- Win32_RDMSPublishedApplication.CommandLineSetting
- Win32_RDMSPublishedApplication.RequiredCommandLine
- Win32_RDMSPublishedApplication.Folder
- Win32_RDMSPublishedApplication.IconPath
- Win32_RDMSPublishedApplication.IconIndex
- Win32_RDMSPublishedApplication.IconContents
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb003faf5e51c9da1f46f23c5f8d6b5ae977987c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341125"
---
# <a name="win32_rdmspublishedapplication-class"></a>\_Класс Win32 рдмспублишедаппликатион

Управляет опубликованным приложением.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSPublishedApplication
{
  string  AppAlias;
  string  PoolName;
  string  DisplayName;
  boolean ShowInPortal;
  string  SecurityDescriptor;
  string  AppPath;
  string  VirtualPath;
  uint32  CommandLineSetting;
  string  RequiredCommandLine;
  string  Folder;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ рдмспублишедаппликатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ рдмспублишедаппликатион** имеет следующие свойства.

<dl> <dt>

**аппалиас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает и задает псевдоним приложения.

</dd> <dt>

**AppPath**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает путь к приложению.

</dd> <dt>

**коммандлинесеттинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает параметр командной строки для приложения.

Это свойство может принимать одно из следующих значений.

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**Доноталлов** (0)


</dt> <dd>

Не разрешать аргументы командной строки.

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Разрешить** (1)


</dt> <dd>

Разрешить аргументы командной строки.

</dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Требовать** (2)


</dt> <dd>

Требовать аргументы командной строки.

</dd> </dl>

</dd> <dt>

**Отображаемое имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает отображаемое имя приложения.

</dd> <dt>

**Папка**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает путь к приложению.

</dd> <dt>

**иконконтентс**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает массив, содержащий значок приложения.

</dd> <dt>

**икониндекс**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает индекс для значка приложения.

</dd> <dt>

**IconPath**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает путь к значку для этого приложения.

</dd> <dt>

**PoolName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает и задает имя пула приложений приложения.

</dd> <dt>

**рекуиредкоммандлине**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает аргументы командной строки, необходимые для приложения.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Возвращает и задает дескриптор безопасности, управляющий доступом к приложению, в формате языка определения дескрипторов безопасности (SDDL).

</dd> <dt>

**шовинпортал**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, следует ли отображать приложение в службах терминалов Веб-доступ (TS Веб-доступ). **Значение true** , чтобы отобразить приложение в службах терминалов веб-доступ; в противном случае — **значение false**.

</dd> <dt>

**VirtualPath**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Возвращает и задает виртуальный путь к приложению.

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

 

