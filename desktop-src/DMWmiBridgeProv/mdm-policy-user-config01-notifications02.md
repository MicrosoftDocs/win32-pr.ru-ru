---
title: Класс MDM_Policy_User_Config01_Notifications02
description: '\_Класс политики MDM \_ user \_ Config01 \_ Notifications02 представляет доступные политики уведомлений.'
ms.assetid: da70b3b4-e8ed-4784-ad6b-52e152a8b78f
keywords:
- Класс MDM_Policy_User_Config01_Notifications02
- MDM_Policy_User_Config01_Notifications02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Notifications02
- MDM_Policy_User_Config01_Notifications02.InstanceID
- MDM_Policy_User_Config01_Notifications02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbe0fcfae252730b346a54186569c423f459fd8c518c45e1bc78240e3fe69dce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077068"
---
# <a name="mdm_policy_user_config01_notifications02-class"></a>\_Класс политики MDM \_ user \_ Config01 \_ Notifications02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Класс **\_ политики MDM \_ user \_ Config01 \_ Notifications02** представляет доступные политики уведомлений.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Notifications02
{
  string InstanceID;
  string ParentID;
  sint32 DisallowNotificationMirroring;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ user \_ Config01 \_ Notifications02 политики MDM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ user \_ Config01 \_ Notifications02 политики MDM** имеет эти свойства.

<dl> <dt>

[дисалловнотификатионмирроринг](/windows/client-management/mdm/policy-csp-notifications#notifications-disallownotificationmirroring)
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

Определяет имя родительского узла. Для этого класса строка имеет значение "Notifications".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./Усер/вендор/мсфт/Полици/конфиг"

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                            |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MOF \\DMWmiBridgeProv.dll</dt> </dl> |



 

