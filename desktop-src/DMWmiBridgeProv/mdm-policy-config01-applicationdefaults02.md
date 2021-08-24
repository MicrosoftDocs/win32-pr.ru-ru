---
title: Класс MDM_Policy_Config01_ApplicationDefaults02
description: '\_Класс политики MDM \_ Config01 \_ ApplicationDefaults02 позволяет администратору задавать тип файла и связи протоколов по умолчанию. Если этот параметр задан, для входа на ПК будут применяться связи по умолчанию.'
ms.assetid: 01a45151-bce3-47a7-bffe-1a3f5a1348ff
keywords:
- Класс MDM_Policy_Config01_ApplicationDefaults02
- MDM_Policy_Config01_ApplicationDefaults02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ApplicationDefaults02
- MDM_Policy_Config01_ApplicationDefaults02.InstanceID
- MDM_Policy_Config01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41273712d3443676e5dfc32d20081b00e9c86a42050e776d3a195a2ec1a90535
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391364"
---
# <a name="mdm_policy_config01_applicationdefaults02-class"></a>\_Класс политики MDM \_ Config01 \_ ApplicationDefaults02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

\_Класс политики MDM \_ Config01 \_ ApplicationDefaults02 позволяет администратору задавать тип файла и связи протоколов по умолчанию. Если этот параметр задан, для входа на ПК будут применяться связи по умолчанию.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a>Члены

Класс **\_ политики MDM \_ Config01 \_ ApplicationDefaults02** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ политики MDM \_ Config01 \_ ApplicationDefaults02** имеет следующие свойства.

<dl> <dt>

[DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

