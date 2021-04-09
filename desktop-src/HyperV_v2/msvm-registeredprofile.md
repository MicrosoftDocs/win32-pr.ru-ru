---
description: Описывает набор классов с обязательными свойствами и методами, необходимые для управления реальной сущностью или для поддержки сценария использования в среде с возможностью взаимодействия.
ms.assetid: 75644856-3B47-43B8-835C-783A6BEE7251
title: Класс Msvm_RegisteredProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredProfile
- Msvm_RegisteredProfile.InstanceID
- Msvm_RegisteredProfile.Caption
- Msvm_RegisteredProfile.Description
- Msvm_RegisteredProfile.ElementName
- Msvm_RegisteredProfile.RegisteredOrganization
- Msvm_RegisteredProfile.OtherRegisteredOrganization
- Msvm_RegisteredProfile.RegisteredName
- Msvm_RegisteredProfile.RegisteredVersion
- Msvm_RegisteredProfile.AdvertiseTypes
- Msvm_RegisteredProfile.AdvertiseTypeDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a7014687355524fbe10ff01869cac6c3fd35a894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080855"
---
# <a name="msvm_registeredprofile-class"></a>\_Класс мсвм регистередпрофиле

Описывает набор классов с обязательными свойствами и методами, необходимые для управления реальной сущностью или для поддержки сценария использования в среде с возможностью взаимодействия.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class Msvm_RegisteredProfile : CIM_RegisteredProfile
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 RegisteredOrganization;
  string OtherRegisteredOrganization;
  string RegisteredName;
  string RegisteredVersion;
  uint16 AdvertiseTypes[];
  string AdvertiseTypeDescriptions[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ регистередпрофиле** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ регистередпрофиле** имеет следующие свойства.

<dl> <dt>

**адвертисетипедескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив строк, предоставляющий дополнительные сведения, связанные со свойством **адвертисетипе** . Необходимо указать описание, если **адвертисетипе** имеет значение 1 (другое). Запись в этом массиве соответствует тому же индексу в массиве **адвертисетипес** . Это свойство наследуется от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)).

</dd> <dt>

**адвертисетипес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает объявление для сведений о профиле. Он используется службами рекламы инфраструктуры WBEM для определения того, что следует объявить, с помощью каких механизмов. Свойство является массивом, чтобы можно было объявить профиль с помощью нескольких механизмов. Если это свойство имеет **значение NULL**, это эквивалентно указанию значения 2 (не объявлено). Это свойство наследуется от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)).

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)
</dt> <dt>

<span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Не объявлено** (2)
</dt> <dt>

<span id="SLP_"></span><span id="slp_"></span>**SLP** (3)
</dt> </dl>

</dd> <dt>

**Заголовок**
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

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**, **Переопределение**
</dt> </dl>

Строка, уникально идентифицирующая экземпляр этого класса. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**осеррегистередорганизатион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (256)
</dt> </dl>

Строка, которая предоставляет описание организации, если **RegisteredOrganization** содержит значение 1 (другое). Это свойство наследуется от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)).

</dd> <dt>

**регистереднаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (256)
</dt> </dl>

Имя этого зарегистрированного профиля. Так как для одного **регистереднаме** могут существовать несколько версий, сочетание **регистереднаме**, **RegisteredOrganization** и **регистередверсион** должно однозначно идентифицировать зарегистрированный профиль в области организации. Это свойство наследуется от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)).

</dd> <dt>

**RegisteredOrganization**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Организация, которая определяет этот профиль. Это свойство наследуется от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)).

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)
</dt> <dt>

<span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)
</dt> <dt>

<span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**КомпТИА** (3)
</dt> <dt>

<span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Консорциум для инноваций в сфере обслуживания** (4)
</dt> <dt>

<span id="FAST"></span><span id="fast"></span>**Быстрое** (5)
</dt> <dt>

<span id="GGF"></span><span id="ggf"></span>**ГГФ** (6)
</dt> <dt>

<span id="INTAP"></span><span id="intap"></span>**Интап** (7)
</dt> <dt>

<span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**итсмф** (8)
</dt> <dt>

<span id="NAC"></span><span id="nac"></span>**NAC** (9)
</dt> <dt>

<span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**10-я экономичный энергетическый союз** (10)
</dt> <dt>

<span id="SNIA"></span><span id="snia"></span>**Сниа** (11)
</dt> <dt>

<span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**Форум TM** (12)
</dt> <dt>

<span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**Открытая группа** (13)
</dt> <dt>

<span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)
</dt> <dt>

<span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)
</dt> <dt>

<span id="IETF"></span><span id="ietf"></span>**IETF** (16)
</dt> <dt>

<span id="INCITS"></span><span id="incits"></span>**ИнЦитс** (17)
</dt> <dt>

<span id="ISO"></span><span id="iso"></span>**ISO** (18)
</dt> <dt>

<span id="W3C"></span><span id="w3c"></span>**W3C** (19)
</dt> <dt>

<span id="__20___________OGF"></span><span id="__20___________ogf"></span>**20 ОГФ** (20)
</dt> <dt>

<span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**Зеленая сетка** (21)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (.. )
</dt> </dl>

</dd> <dt>

**регистередверсион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Версия этого профиля. Строка должна иметь вид: "*M*. *N*. *U*"где:

-   *M* — основной номер версии (в числовом формате), описывающий создание или Последнее изменение профиля.
-   *N* — это дополнительный номер версии (в числовом формате), описывающий создание или Последнее изменение профиля.
-   *U* — это обновление (в числовом формате), описывающее создание или Последнее изменение профиля.

Это свойство наследуется от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                                 |
| Пространство имен<br/>                | Корневое \\ взаимодействие<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

