---
title: Класс MDM_WindowsAdvancedThreatProtection_DeviceTagging01
description: Класс MDM \_ виндовсадванцедсреатпротектион \_ DeviceTagging01 используется для подключения, определения состояния конфигурации и работоспособности, а также конечных точек отключение для Advanced Threat Protection в Защитнике Windows.
ms.assetid: b56d5d46-e994-404a-865a-c59bb948f2b3
keywords:
- Класс MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01 класс, описание
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.InstanceID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.ParentID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.IdMethod
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 12cf3863ba67f422b42572a6934807d86abbc0e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136742"
---
# <a name="mdm_windowsadvancedthreatprotection_devicetagging01-class"></a>\_Класс MDM виндовсадванцедсреатпротектион \_ DeviceTagging01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс MDM \_ виндовсадванцедсреатпротектион \_ DeviceTagging01 используется для подключения, определения состояния конфигурации и работоспособности, а также конечных точек отключение для Advanced Threat Protection в Защитнике Windows.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_DeviceTagging01
{
  string InstanceID;
  string ParentID;
  string Group;
  sint32 Criticality;
  sint32 IdMethod;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ виндовсадванцедсреатпротектион \_ DeviceTagging01** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **MDM \_ виндовсадванцедсреатпротектион \_ DeviceTagging01** имеет следующие свойства.

<dl> <dt>

[Степень важности](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#criticality)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[Группа](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#group)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

**идмесод**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

TBD

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
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                     |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                       |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



 

