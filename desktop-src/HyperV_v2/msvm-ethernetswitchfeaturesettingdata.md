---
description: Абстрактный класс, представляющий параметры для данного экземпляра функции коммутатора Ethernet.
ms.assetid: c1720649-585f-45a9-8329-06787bd8b600
title: Класс Msvm_EthernetSwitchFeatureSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchFeatureSettingData
- Msvm_EthernetSwitchFeatureSettingData.InstanceID
- Msvm_EthernetSwitchFeatureSettingData.Caption
- Msvm_EthernetSwitchFeatureSettingData.Description
- Msvm_EthernetSwitchFeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 15ef4b0ce13df4d39cb83167f35124f8a5d6a9939d2b612c167c03fab3e37771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524600"
---
# <a name="msvm_ethernetswitchfeaturesettingdata-class"></a>\_Класс мсвм есернетсвитчфеатуресеттингдата

Абстрактный класс, представляющий параметры для данного экземпляра функции коммутатора Ethernet. Параметры функций коммутатора Ethernet класс управления должны быть производными от этого абстрактного класса.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchFeatureSettingData : Msvm_FeatureSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ есернетсвитчфеатуресеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ есернетсвитчфеатуресеттингдата** имеет следующие свойства.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

