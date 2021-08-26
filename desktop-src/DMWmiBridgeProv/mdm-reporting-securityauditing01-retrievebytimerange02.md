---
title: Класс MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
description: Класс MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02 используется для получения журналов, существующих в параметрах StartTime и StopTime.
ms.assetid: e360bc76-f006-45e1-b78a-29125fbcd5ae
keywords:
- Класс MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c307f2b5ddcad1631cd5981a0ea25d8b9fb43566a482de20a2d050a0f3e8db57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913580"
---
# <a name="mdm_reporting_securityauditing01_retrievebytimerange02-class"></a>\_ \_ Класс SecurityAuditing01 RETRIEVEBYTIMERANGE02 отчетов MDM \_

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Класс **MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02** используется для получения журналов, существующих в параметре StartTime и StopTime. значение StartTime и StopTime выражается в формате ISO 8601. Если параметры StartTime и StopTime не указаны, то значения будут интерпретированы как первое существующее или последнее существующее время.

Ниже приведены другие возможные сценарии.

-   Если параметр StartTime и StopTime не указаны, то возвращаются все существующие журналы.
-   Если указан параметр StopTime, но параметр StartTime не указан, то возвращаются все журналы, которые существовали до StopTime.
-   Если задан параметр StartTime, но StopTime не указан, возвращаются все журналы, существующие из StartTime.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02 для MDM Reporting** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02 для MDM Reporting** имеет следующие свойства.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Определяет имя родительского узла. Для этого класса строка имеет значение "Ретриевебитимеранже".

</dd> <dt>

[Журналы](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/секуритяудитинг"

</dd> <dt>

[StartTime](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[StopTime](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                            |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>MOF \\DMWmiBridgeProv.dll</dt> </dl> |



 

