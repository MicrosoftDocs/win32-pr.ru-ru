---
title: Класс MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
description: Класс MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByCount02 используется для получения указанного числа журналов из StartTime.
ms.assetid: 0a581d5a-129b-48c3-a7a1-3947cc1e2ee9
keywords:
- Класс MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 509ab80a8f7b33d3ac7f9d40157152ce5aa693376e4e61edc4581f8d375f1c77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825484"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebycount02-class"></a>\_ \_ Класс EnterpriseDataProtection01 RETRIEVEBYCOUNT02 отчетов MDM \_

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Класс **MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByCount02** используется для получения указанного числа журналов из StartTime. Время начала выражается в формате ISO 8601. Можно задать количество журналов, необходимых для установки Логкаунт и StartTime. Он возвращает указанное число журналов или меньше, если общее число журналов меньше Логкаунт.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
{
  string InstanceID;
  string ParentID;
  string Logs;
  sint32 LogCount;
  string StartTime;
  sint32 Type;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ EnterpriseDataProtection01 \_ RetrieveByCount02 для MDM Reporting** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ EnterpriseDataProtection01 \_ RetrieveByCount02 для MDM Reporting** имеет следующие свойства.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Определяет имя родительского узла. Для этого класса строка имеет значение "Ретриевебикаунт".

</dd> <dt>

[логкаунт](/windows/client-management/mdm/reporting-csp#logcount)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

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
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                            |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>MOF \\DMWmiBridgeProv.dll</dt> </dl> |



 

