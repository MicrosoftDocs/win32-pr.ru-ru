---
description: Подключает порт коммутатора к конечной точке локальной сети, к которой подключен порт.
ms.assetid: 963EC004-6A67-4F75-BD93-1BCD17F32490
title: Класс Msvm_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ActiveConnection
- Msvm_ActiveConnection.Antecedent
- Msvm_ActiveConnection.Dependent
- Msvm_ActiveConnection.TrafficType
- Msvm_ActiveConnection.OtherTrafficDescription
- Msvm_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2f8326fe50d3fef4e7776fa865afdd730416cb38fccd6347b4b27f0079966501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693614"
---
# <a name="msvm_activeconnection-class"></a>\_Класс мсвм ActiveConnection

Подключает порт коммутатора к конечной точке локальной сети, к которой подключен порт. Наличие этого объекта означает, что порт коммутатора и конечная точка локальной сети активно подключены, а порт Ethernet, связанный с конечной точкой локальной сети, может взаимодействовать с сетью через порт коммутатора.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ActiveConnection : CIM_ActiveConnection
{
  Msvm_LANEndpoint REF Antecedent;
  CIM_LANEndpoint  REF Dependent;
  uint16               TrafficType;
  string               OtherTrafficDescription;
  boolean              IsUnidirectional;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ ActiveConnection** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ ActiveConnection** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ ланендпоинт**](msvm-lanendpoint.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ ланендпоинт**](msvm-lanendpoint.md) , представляющий точку доступа к службе (SAP), настроенную для обмена данными или активно взаимодействующая с зависимым SAP. В однонаправленном соединении это SAP является передающим.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ ланендпоинт**](cim-lanendpoint.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ ланендпоинт**](cim-lanendpoint.md) , представляющий SAP, настроенный для обмена данными или активно взаимодействующий с предшествующей SAP. В однонаправленном соединении этот SAP является получаемым.

</dd> <dt>

**По поднаправлению**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если это свойство имеет **значение true**, это соединение является однонаправленным; в противном случае это соединение является двунаправленным. При однонаправленном соединении «докладчик» должен быть определен как ссылка **Antecedent** . В двунаправленном соединении не имеет значения, является ли выбранная точка доступа **предшествующей** или **зависимой**. Это свойство наследуется от [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)).

</dd> <dt>

**осертраффикдескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), но не используется.

</dd> <dt>

**ТипТрафика**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), но не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ ActiveConnection мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Примеры

См. раздел [запросы к сетевым объектам](querying-networking-objects.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ACTIVECONNECTION CIM**](cim-activeconnection.md)
</dt> <dt>

[**\_ACTIVECONNECTION CIM**](/previous-versions//cc136779(v=vs.85))
</dt> </dl>

 

