---
title: Класс Win32_RDMSDesktopAssignment
description: Описание назначения пользовательского рабочего стола коллекции удаленных рабочих столов.
ms.assetid: d3370cf2-65db-4e01-9ea3-9a71340bf71b
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSDesktopAssignment службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSDesktopAssignment, описание
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment.CollectionAlias
- Win32_RDMSDesktopAssignment.DesktopName
- Win32_RDMSDesktopAssignment.UserName
- Win32_RDMSDesktopAssignment.UserDomain
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72bb252bd2efb71e3192ebd16160cecf18196cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340655"
---
# <a name="win32_rdmsdesktopassignment-class"></a>\_Класс Win32 рдмсдесктопассигнмент

Описание назначения пользовательского рабочего стола коллекции удаленных рабочих столов.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDesktopAssignment
{
  string CollectionAlias;
  string DesktopName;
  string UserName;
  string UserDomain;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ рдмсдесктопассигнмент** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ рдмсдесктопассигнмент** содержит следующие методы.



| Метод                                                                                 | Описание                              |
|:---------------------------------------------------------------------------------------|:-----------------------------------------|
| [**адддесктопассигнмент**](win32-rdmsdesktopassignment-adddesktopassignment.md)       | Добавляет назначение рабочего стола.<br/>    |
| [**ремоведесктопассигнмент**](win32-rdmsdesktopassignment-removedesktopassignment.md) | Удаляет назначение рабочего стола.<br/> |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ рдмсдесктопассигнмент** имеет следующие свойства.

<dl> <dt>

**коллектионалиас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Псевдоним коллекции.

</dd> <dt>

**десктопнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя рабочего стола.

</dd> <dt>

**Доменпользователя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Доменное имя учетной записи пользователя.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя учетной записи пользователя.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMV2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



 

