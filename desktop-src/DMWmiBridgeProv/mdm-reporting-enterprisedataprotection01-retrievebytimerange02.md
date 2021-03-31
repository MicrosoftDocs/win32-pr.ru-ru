---
title: Класс MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
description: Класс MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02 используется для получения журналов, существующих в параметрах StartTime и StopTime.
ms.assetid: 6abec00e-901f-4f79-840d-a4ef3a4d392d
keywords:
- Класс MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec266e68bbaaafb1f1e3a78fba7ea6b91805096a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071155"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebytimerange02-class"></a>\_ \_ Класс EnterpriseDataProtection01 RETRIEVEBYTIMERANGE02 отчетов MDM \_

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** используется для получения журналов, существующих в параметрах StartTime и StopTime. Время StartTime и StopTime выражаются в формате ISO 8601. Если параметры StartTime и StopTime не указаны, то значения будут интерпретированы как первое существующее или последнее существующее время.

Ниже приведены другие возможные сценарии.

-   Если параметр StartTime и StopTime не указаны, то возвращаются все существующие журналы.
-   Если указан параметр StopTime, но параметр StartTime не указан, то возвращаются все журналы, которые существовали до StopTime.
-   Если задан параметр StartTime, но StopTime не указан, возвращаются все журналы, существующие из StartTime.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
  sint32 Type;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02 для MDM Reporting** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02 для MDM Reporting** имеет следующие свойства.

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

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/ентерприседатапротектион"

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

</dd> <dt>

[Тип](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                            |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>MOF \\DMWmiBridgeProv.dll</dt> </dl> |



 

