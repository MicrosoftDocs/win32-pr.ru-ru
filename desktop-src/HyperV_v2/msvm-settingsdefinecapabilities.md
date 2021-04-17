---
description: Предоставляет связь между экземпляром возможностей и минимальными, максимальными, добавочными и параметрами по умолчанию для ресурса.
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Класс Msvm_SettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineCapabilities
- Msvm_SettingsDefineCapabilities.SupportStatement
- Msvm_SettingsDefineCapabilities.GroupComponent
- Msvm_SettingsDefineCapabilities.PartComponent
- Msvm_SettingsDefineCapabilities.PropertyPolicy
- Msvm_SettingsDefineCapabilities.ValueRole
- Msvm_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7a312d3453b783c3d72f909ec6cb0b37d83feb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682911"
---
# <a name="msvm_settingsdefinecapabilities-class"></a>\_Класс мсвм сеттингсдефинекапабилитиес

Предоставляет связь между экземпляром возможностей и минимальными, максимальными, добавочными и параметрами по умолчанию для ресурса.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  uint16               SupportStatement;
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ сеттингсдефинекапабилитиес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ сеттингсдефинекапабилитиес** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **[ **\_ возможности CIM**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Экземпляр возможностей. Это свойство наследуется от [**CIM \_ сеттингсдефинекапабилитиес**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **[ **\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85))**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Параметр, используемый для определения связанного экземпляра возможностей. Это свойство наследуется от [**CIM \_ сеттингсдефинекапабилитиес**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**пропертиполици**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, обрабатываются ли непустые, ненулевые свойства экземпляра данных связанных параметров, независимо друг от друга или как коррелированный набор. Это свойство наследуется от [**CIM \_ сеттингсдефинекапабилитиес**](/previous-versions//cc136913(v=vs.85)) и всегда имеет значение 0 (независимо от него).

</dd> <dt>

**суппортстатемент**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентифицирует инструкцию поддержки.

> [!Note]  
> Это свойство было добавлено в Windows 10 версии 1703.

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Рабочая среда** (0)


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Предварительный выпуск** (1)


</dt> <dd>

> [!Note]  
> Было **Непроизводствым** в Windows 10, версия 1703.

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Зарезервировано** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**валуеранже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Любая дальнейшая семантика для интерпретации всех ненулевых неключевых свойств данных параметров. Это свойство наследуется от [**CIM \_ сеттингсдефинекапабилитиес**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**валуероле**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Любая дальнейшая семантика интерпретации ненулевых неключевых свойств данных параметров. Это свойство наследуется от [**CIM \_ сеттингсдефинекапабилитиес**](/previous-versions//cc136913(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Значения для свойств **валуероле** и **валуеранже** используются в следующих парах:

-   Точка или значение по умолчанию (0/0)
-   Минимум/поддерживается (1/3)
-   Максимум/поддерживается (2/3)
-   Инкременты и поддерживаются (3/3).

"Точка" означает, что каждое из свойств объекта **PartComponent** представляет платформу по умолчанию.

"Минимум" и "максимум" означают, что каждое из свойств объекта **PartComponent** представляет наименьшее и наибольшее возможное значение для этих свойств, поддерживаемое платформой на основе текущей конфигурации компьютера.

«Приращения» обозначает гранулярность, с которой можно увеличить или уменьшить параметры.

Доступ к классу **\_ сеттингсдефинекапабилитиес мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СЕТТИНГСДЕФИНЕКАПАБИЛИТИЕС CIM**](cim-settingsdefinecapabilities.md)
</dt> <dt>

[**\_СЕТТИНГСДЕФИНЕКАПАБИЛИТИЕС CIM**](/previous-versions//cc136913(v=vs.85))
</dt> <dt>

[**Мсвм \_ сеттингсдефинекапабилитиес (v1)**](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[Классы управления ресурсами](resource-management-classes.md)
</dt> </dl>

 

