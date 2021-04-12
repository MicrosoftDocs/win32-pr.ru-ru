---
title: Класс MDM_Policy_User_Result01_ApplicationManagement02
description: '\_ \_ \_ Класс User RESULT01 ApplicationManagement02 политики MDM \_ представляет доступные политики запуска, заданные для каждого пользователя.'
ms.assetid: 62545af1-9c26-481e-9668-cd253cf592e7
keywords:
- Класс MDM_Policy_User_Result01_ApplicationManagement02
- MDM_Policy_User_Result01_ApplicationManagement02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_ApplicationManagement02
- MDM_Policy_User_Result01_ApplicationManagement02.InstanceID
- MDM_Policy_User_Result01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18177046691e5c9fe5ca8cb61ee0518a41533c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136018"
---
# <a name="mdm_policy_user_result01_applicationmanagement02-class"></a>\_Класс политики MDM \_ user \_ Result01 \_ ApplicationManagement02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **\_ \_ user \_ Result01 \_ ApplicationManagement02 политики MDM** представляет доступные политики запуска, заданные для каждого пользователя.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 RequirePrivateStoreOnly;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ user \_ Result01 \_ ApplicationManagement02 политики MDM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ user \_ Result01 \_ ApplicationManagement02 политики MDM** имеет эти свойства.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Определяет имя родительского узла. Для этого класса строка имеет значение "Аппликатионманажемент".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./Усер/вендор/мсфт/Полици/ресулт"

</dd> <dt>

[рекуиреприватестореонли](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-requireprivatestoreonly)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование сценариев PowerShell с WMI Bridge Provider](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

