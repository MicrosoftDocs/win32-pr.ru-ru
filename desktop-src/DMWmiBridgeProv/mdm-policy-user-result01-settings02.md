---
title: Класс MDM_Policy_User_Result01_Settings02
description: '\_Класс политики MDM \_ user \_ Result01 \_ Settings02 получает параметры для дополнительных календарей на панели задач.'
ms.assetid: 84121b24-590a-4b0b-946f-8a107eaed6c6
keywords:
- Класс MDM_Policy_User_Result01_Settings02
- MDM_Policy_User_Result01_Settings02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Settings02
- MDM_Policy_User_Result01_Settings02.InstanceID
- MDM_Policy_User_Result01_Settings02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b38956121d6391433fd2727048ce95eb0b5646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071161"
---
# <a name="mdm_policy_user_result01_settings02-class"></a>\_Класс политики MDM \_ user \_ Result01 \_ Settings02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

\_Класс политики MDM \_ user \_ Result01 \_ Settings02 получает параметры для дополнительных календарей на панели задач.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Settings02
{
  string InstanceID;
  string ParentID;
  sint32 ConfigureTaskbarCalendar;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ user \_ Result01 \_ Settings02 политики MDM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ user \_ Result01 \_ Settings02 политики MDM** имеет эти свойства.

<dl> <dt>

[ConfigureTaskbarCalendar](/windows/client-management/mdm/policy-csp-settings#settings-configuretaskbarcalendar)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
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

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

