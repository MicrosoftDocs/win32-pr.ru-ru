---
title: Класс MDM_Policy_Config01_SmartScreen02
description: '\_Класс политики MDM \_ Config01 \_ SmartScreen02 настраивает политики интеллектуального экрана.'
ms.assetid: e5ad04a1-afa9-4887-a4c1-c92c574a5398
keywords:
- Класс MDM_Policy_Config01_SmartScreen02
- MDM_Policy_Config01_SmartScreen02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_SmartScreen02
- MDM_Policy_Config01_SmartScreen02.InstanceID
- MDM_Policy_Config01_SmartScreen02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49624cd014c71a1f459530cc889733a945d92603b0a539fce6c496988e302dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017822"
---
# <a name="mdm_policy_config01_smartscreen02-class"></a>\_Класс политики MDM \_ Config01 \_ SmartScreen02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

\_Класс политики MDM \_ Config01 \_ SmartScreen02 настраивает политики интеллектуального экрана.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_SmartScreen02
{
  string InstanceID;
  string ParentID;
  sint32 EnableAppInstallControl;
  sint32 EnableSmartScreenInShell;
  sint32 PreventOverrideForFilesInShell;
};
```

## <a name="members"></a>Члены

Класс **\_ политики MDM \_ Config01 \_ SmartScreen02** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ политики MDM \_ Config01 \_ SmartScreen02** имеет следующие свойства.

<dl> <dt>

[EnableAppInstallControl](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enableappinstallcontrol)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[EnableSmartScreenInShell](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enablesmartscreeninshell)
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

</dd> <dt>

[PreventOverrideForFilesInShell](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-preventoverrideforfilesinshell)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

