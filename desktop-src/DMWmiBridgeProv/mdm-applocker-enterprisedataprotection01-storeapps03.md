---
title: Класс MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
description: класс MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03 фиксирует список приложений Windows, которым разрешено работать с корпоративными данными. Следует использовать в сочетании с параметрами в./вендор/мсфт/Полици/конфигсаурце/датапротектион.
ms.assetid: f37fe52d-dbe1-45b7-acd5-5047c46d9bd0
keywords:
- Класс MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03 класс, описание
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5b0c3af455e501695cb7a2093b841159f5755ac54e1de97a370c7dc7f2d6fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077417"
---
# <a name="mdm_applocker_enterprisedataprotection01_storeapps03-class"></a>\_Класс MDM AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

класс **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** фиксирует список приложений Windows, которым разрешено работать с корпоративными данными. Следует использовать в сочетании с параметрами в./вендор/мсфт/Полици/конфигсаурце/датапротектион.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** имеет следующие свойства.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

определяет ограничения для запуска приложений из хранилища Windows.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/апплоккер/ентерприседатапротектион/*GROUPING*"

</dd> <dt>

[**Политика**](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование сценариев PowerShell с WMI Bridge Provider](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

