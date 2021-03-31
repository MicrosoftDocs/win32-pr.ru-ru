---
description: Связывает экземпляр виртуальной машины со службой управления, которая управляет ее состоянием.
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Класс Msvm_ServiceAffectsElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceAffectsElement
- Msvm_ServiceAffectsElement.AffectedElement
- Msvm_ServiceAffectsElement.AffectingElement
- Msvm_ServiceAffectsElement.ElementEffects
- Msvm_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eadb9f33015091999776b73c83d792ccd29396b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154846"
---
# <a name="msvm_serviceaffectselement-class"></a>\_Класс мсвм сервицеаффектселемент

Связывает экземпляр виртуальной машины со службой управления, которая управляет ее состоянием.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceAffectsElement : CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[] = 5;
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ сервицеаффектселемент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ сервицеаффектселемент** имеет следующие свойства.

<dl> <dt>

**аффектеделемент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на виртуальную машину. Это свойство наследуется от [**CIM \_ сервицеаффектселемент**](/previous-versions//cc136907(v=vs.85)).

</dd> <dt>

**аффектинжелемент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **\_ Служба CIM**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на службу, которая управляет виртуальной машиной. Это свойство наследуется от [**CIM \_ сервицеаффектселемент**](/previous-versions//cc136907(v=vs.85)).

</dd> <dt>

**елементеффектс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает тип элемента управления, который представляет Ассоциация. Это свойство наследуется от [**CIM \_ сервицеаффектселемент**](/previous-versions//cc136907(v=vs.85)), и для него всегда устанавливается следующее значение.



| Значение                                                                        | Значение            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>5</dt> </dl> | Управление<br/> |



 

</dd> <dt>

**осерелементеффектсдескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Сведения о типе ассоциации в соответствующей позиции массива в массиве свойств **елементаффектс** . Эта информация необходима, если для **елементаффектс** задано значение 1 (другое). Это свойство наследуется от [**CIM \_ сервицеаффектселемент**](/previous-versions//cc136907(v=vs.85))и всегда имеет значение **null**.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ сервицеаффектселемент мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_СЕРВИЦЕАФФЕКТСЕЛЕМЕНТ CIM**](cim-serviceaffectselement.md)
</dt> <dt>

[**\_СЕРВИЦЕАФФЕКТСЕЛЕМЕНТ CIM**](/previous-versions//cc136907(v=vs.85))
</dt> </dl>

 

