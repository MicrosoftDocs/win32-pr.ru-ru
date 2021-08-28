---
title: Класс MDM_Policy_Config01_ApplicationManagement02
description: '\_Класс политики MDM \_ Config01 \_ ApplicationManagement02 представляет доступные политики управления приложениями.'
ms.assetid: f05c4852-e694-4e0d-94e1-07531c879613
keywords:
- Класс MDM_Policy_Config01_ApplicationManagement02
- MDM_Policy_Config01_ApplicationManagement02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ApplicationManagement02
- MDM_Policy_Config01_ApplicationManagement02.InstanceID
- MDM_Policy_Config01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1ecff562e5e51c2e998c1708afbd2a3460b77e5315050475327d8165540f953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118165736"
---
# <a name="mdm_policy_config01_applicationmanagement02-class"></a>\_Класс политики MDM \_ Config01 \_ ApplicationManagement02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Класс **\_ политики MDM \_ Config01 \_ ApplicationManagement02** представляет доступные политики управления приложениями.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAllTrustedApps;
  sint32 AllowAppStoreAutoUpdate;
  sint32 AllowDeveloperUnlock;
  sint32 AllowGameDVR;
  sint32 AllowSharedUserAppData;
  sint32 DisableStoreOriginatedApps;
  sint32 RestrictAppDataToSystemVolume;
  sint32 RestrictAppToSystemVolume;
};
```

## <a name="members"></a>Члены

Класс **\_ политики MDM \_ Config01 \_ ApplicationManagement02** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ политики MDM \_ Config01 \_ ApplicationManagement02** имеет следующие свойства.

<dl> <dt>

[AllowAllTrustedApps](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[AllowAppStoreAutoUpdate](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowappstoreautoupdate)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[AllowDeveloperUnlock](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowdeveloperunlock)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[AllowGameDVR](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowgamedvr)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[AllowSharedUserAppData](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowshareduserappdata)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[дисаблестореоригинатедаппс](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-disablestoreoriginatedapps)
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

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"

</dd> <dt>

[RestrictAppDataToSystemVolume](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictappdatatosystemvolume)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[RestrictAppToSystemVolume](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictapptosystemvolume)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Использование сценариев PowerShell с WMI Bridge Provider](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

