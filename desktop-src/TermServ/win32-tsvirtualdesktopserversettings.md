---
title: Класс Win32_TSVirtualDesktopServerSettings
description: Содержит сведения о конфигурации для сервера Узел виртуализации удаленных рабочих столов (узла виртуализации удаленных рабочих столов).
ms.assetid: 749018aa-a8aa-433e-985b-40b44ef8aa7f
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSVirtualDesktopServerSettings службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSVirtualDesktopServerSettings, описание
topic_type:
- apiref
api_name:
- Win32_TSVirtualDesktopServerSettings
- Win32_TSVirtualDesktopServerSettings.SessionBrokerName
- Win32_TSVirtualDesktopServerSettings.PolicySourceSessionBrokerName
- Win32_TSVirtualDesktopServerSettings.Concurrency
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39635aee7b32430ace0ead0e3b007051a3c049d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803599"
---
# <a name="win32_tsvirtualdesktopserversettings-class"></a>\_Класс Win32 тсвиртуалдесктопсерверсеттингс

Содержит сведения о конфигурации для сервера Узел виртуализации удаленных рабочих столов (узла виртуализации удаленных рабочих столов).

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[singleton, dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVirtualDesktopServerSettings
{
  string SessionBrokerName;
  sint32 PolicySourceSessionBrokerName;
  uint32 Concurrency;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тсвиртуалдесктопсерверсеттингс** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ тсвиртуалдесктопсерверсеттингс** имеет следующие свойства.

<dl> <dt>

**Параллелизм**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Максимально допустимое количество одновременных запросов на подготовку для этого сервера виртуальных рабочих столов.

</dd> <dt>

**полицисаурцесессионброкернаме**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если задано значение 0, указывает, что свойство **сессионброкернаме** настроено сервером. Если задано значение 1, указывает, что свойство **сессионброкернаме** настроено групповой политикой.

</dd> <dt>

**сессионброкернаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Полное различающееся имя посредника сеансов для сервера узла виртуализации удаленных рабочих столов.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                             |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ терминалсервицес<br/>                                                   |
| MOF<br/>                      | <dl> <dt>Тсвмхост. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 





