---
title: Класс MDM_PassportForWork_ExcludeSecurityDevices03
description: класс MDM \_ пасспортфорворк \_ ExcludeSecurityDevices03 определяет модули доверенной платформы, которые разрешено использовать с Windows Hello для бизнеса.
ms.assetid: ca8fba3a-736b-4bd3-ac93-e0d44d54798d
keywords:
- Класс MDM_PassportForWork_ExcludeSecurityDevices03
- MDM_PassportForWork_ExcludeSecurityDevices03 класс, описание
topic_type:
- apiref
api_name:
- MDM_PassportForWork_ExcludeSecurityDevices03
- MDM_PassportForWork_ExcludeSecurityDevices03.InstanceID
- MDM_PassportForWork_ExcludeSecurityDevices03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5957e42d8df1a6c41ad8c27067119503f9a40034d6133081bc9460afc5c72f23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391374"
---
# <a name="mdm_passportforwork_excludesecuritydevices03-class"></a>\_Класс MDM пасспортфорворк \_ ExcludeSecurityDevices03

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

класс MDM \_ пасспортфорворк \_ ExcludeSecurityDevices03 определяет модули доверенной платформы, которые разрешено использовать с Windows Hello для бизнеса.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_ExcludeSecurityDevices03
{
  string  InstanceID;
  string  ParentID;
  boolean TPM12;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ пасспортфорворк \_ ExcludeSecurityDevices03** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **MDM \_ пасспортфорворк \_ ExcludeSecurityDevices03** имеет следующие свойства.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Корневой узел.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Дополнительные сведения см. в статье [ПАССПОРТФОРВОРК CSP](/windows/client-management/mdm/passportforwork-csp).

</dd> <dt>

[TPM12](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
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



 

