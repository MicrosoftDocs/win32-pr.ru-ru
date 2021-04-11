---
title: Класс MDM_Policy_Config01_Cellular02
description: '\_Класс политики MDM \_ Config01 \_ Cellular02 настраивает политики сотовой сети.'
ms.assetid: e5926a21-a375-4d1c-8b37-7fe7f7532c50
keywords:
- Класс MDM_Policy_Config01_Cellular02
- MDM_Policy_Config01_Cellular02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Cellular02
- MDM_Policy_Config01_Cellular02.InstanceID
- MDM_Policy_Config01_Cellular02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1b6d9163723299b144368d9d2b73a12ccc7a91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135550"
---
# <a name="mdm_policy_config01_cellular02-class"></a>\_Класс политики MDM \_ Config01 \_ Cellular02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

\_Класс политики MDM \_ Config01 \_ Cellular02 настраивает политики сотовой сети.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Cellular02
{
  string InstanceID;
  string ParentID;
  string LetAppsAccessCellularData_UserInControlOfTheseApps;
  string LetAppsAccessCellularData_ForceDenyTheseApps;
  string LetAppsAccessCellularData_ForceAllowTheseApps;
  sint32 LetAppsAccessCellularData;
  string ShowAppCellularAccessUI;
};
```

## <a name="members"></a>Члены

Класс **\_ политики MDM \_ Config01 \_ Cellular02** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ политики MDM \_ Config01 \_ Cellular02** имеет следующие свойства.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[летаппсакцессцеллулардата](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[Летаппсакцессцеллулардата \_ форцеалловсесеаппс](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forceallowtheseapps)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[Летаппсакцессцеллулардата \_ форцеденисесеаппс](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forcedenytheseapps)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[Летаппсакцессцеллулардата \_ усеринконтролофсесеаппс](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-userincontroloftheseapps)
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

</dd> <dt>

[шоваппцеллуларакцессуи](/windows/client-management/mdm/policy-csp-cellular#cellular-showappcellularaccessui)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
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



 

