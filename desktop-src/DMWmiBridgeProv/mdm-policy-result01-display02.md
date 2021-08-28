---
title: Класс MDM_Policy_Result01_Display02
description: '\_Класс политики MDM \_ Result01 \_ Display02 представляет политики экрана.'
ms.assetid: 9f8675d6-1fd7-4269-8059-9159622f03cb
keywords:
- Класс MDM_Policy_Result01_Display02
- MDM_Policy_Result01_Display02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Display02
- MDM_Policy_Result01_Display02.InstanceID
- MDM_Policy_Result01_Display02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a2e93b61e50b73240e8283695c6b7893d2963cae31aea2bd04fb0baef1c642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118164388"
---
# <a name="mdm_policy_result01_display02-class"></a>\_Класс политики MDM \_ Result01 \_ Display02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

\_Класс политики MDM \_ Result01 \_ Display02 представляет политики экрана.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Display02
{
  string InstanceID;
  string ParentID;
  string TurnOffGdiDPIScalingForApps;
  string TurnOnGdiDPIScalingForApps;
};
```

## <a name="members"></a>Члены

Класс **\_ политики MDM \_ Result01 \_ Display02** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ политики MDM \_ Result01 \_ Display02** имеет следующие свойства.

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

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[турноффгдидпискалингфораппс](/windows/client-management/mdm/policy-csp-display#display-turnoffgdidpiscalingforapps)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[турнонгдидпискалингфораппс](/windows/client-management/mdm/policy-csp-display#display-turnongdidpiscalingforapps)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
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



 

