---
title: Класс MDM_AppLocker_EnterpriseDataProtection01_EXE03
description: Класс MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03 фиксирует список исполняемых приложений, которым разрешено работать с корпоративными данными.
ms.assetid: 43f253d4-3f9d-4651-91b4-b7460706e8b4
keywords:
- Класс MDM_AppLocker_EnterpriseDataProtection01_EXE03
- MDM_AppLocker_EnterpriseDataProtection01_EXE03 класс, описание
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_EXE03
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b21cc2acfc316744138536cb08d6fe5a21f49f7f4417249180d5aaf7b80dda7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797124"
---
# <a name="mdm_applocker_enterprisedataprotection01_exe03-class"></a>\_Класс MDM AppLocker \_ EnterpriseDataProtection01 \_ EXE03

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Класс **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** фиксирует список исполняемых приложений, которым разрешено работать с корпоративными данными. Следует использовать в сочетании с параметрами в./вендор/мсфт/Полици/конфигсаурце/датапротектион.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** имеет следующие свойства.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Определяет ограничения для запуска исполняемых приложений.

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

 

