---
description: Представляет конфигурацию и операционные параметры для \_ экземпляров МАНАЖЕДЕЛЕМЕНТ CIM.
ms.assetid: a9ee0eb6-dc48-43f2-bdb5-f84fe7bbc1f2
title: Класс CIM_SettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingData
- CIM_SettingData.InstanceID
- CIM_SettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 934aaaf694a79537f5761717f91db398141c33d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265059"
---
# <a name="cim_settingdata-class"></a>\_Класс SETTINGDATA CIM

Представляет конфигурацию и операционные параметры для экземпляров [**\_ манажеделемент CIM**](cim-managedelement.md) .

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingData : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a>Члены

Класс **\_ SettingData CIM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ SettingData CIM** имеет эти свойства.

<dl> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**обязательный**](/windows/desktop/WmiSdk/standard-qualifiers), [**переопределенный**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Понятное имя для экземпляра этого класса. Кроме того, понятное имя может использоваться в качестве индекса для поиска или запроса. Имя не обязательно должно быть уникальным в пределах пространства имен.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")
</dt> </dl>

Уникально идентифицирует экземпляр этого класса в области содержащего его пространства имен.

> [!IMPORTANT]
>
> Чтобы обеспечить уникальность в пространстве имен, значение свойства **InstanceId** должно быть создано в следующем шаблоне: *OrgID*:*LocalId*
>
> -   *OrgID* должен включать уникальное имя, присвоенное товару или иным способом, которое принадлежит бизнес-сущности, определяющей свойство **InstanceId** , или быть зарегистрированным идентификатором, назначенным распознанным глобальным центром сертификации.
> -   *OrgID* не должно содержать двоеточие. Первое двоеточие в **InstanceId** должно находиться между *OrgID* и *LocalId*.
> -   *LocalId* выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых реальных элементов.
> -   Если приведенный выше шаблон не используется, определяющая сущность должна гарантировать, что результирующее значение **InstanceId** не будет повторно использоваться во всех свойствах **InstanceId** , созданных этим поставщиком или другими поставщиками для этого пространства имен.
> -   Для экземпляров, определенных DMTF, шаблон должен использоваться с *OrgID* , для которого задано значение "CIM".

 

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_МАНАЖЕДЕЛЕМЕНТ CIM**](cim-managedelement.md)
</dt> </dl>

 

