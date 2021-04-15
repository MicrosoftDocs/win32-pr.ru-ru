---
description: Подключает порт коммутатора к конечной точке Fibre Channel, к которой подключен порт.
ms.assetid: e2762e0c-2f78-4159-a67c-31213e311072
title: Класс Msvm_FcActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcActiveConnection
- Msvm_FcActiveConnection.Antecedent
- Msvm_FcActiveConnection.Dependent
- Msvm_FcActiveConnection.TrafficType
- Msvm_FcActiveConnection.OtherTrafficDescription
- Msvm_FcActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e29330e073266f2f2a8749ec3c70d9e26b35ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682866"
---
# <a name="msvm_fcactiveconnection-class"></a>\_Класс мсвм фкактивеконнектион

Подключает порт коммутатора к конечной точке Fibre Channel, к которой подключен порт. Существование этого объекта означает, что порт коммутатора и конечная точка Fibre Channel активно подключены, а Fibre Channelный порт, связанный с конечной точкой Fibre Channel, может взаимодействовать с сетью через порт коммутатора.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcActiveConnection : CIM_ActiveConnection
{
  Msvm_FcEndpoint REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
  uint16              TrafficType;
  string              OtherTrafficDescription;
  boolean             IsUnidirectional;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ фкактивеконнектион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ фкактивеконнектион** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ фцендпоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ фцендпоинт**](msvm-fcendpoint.md) , представляющий точку доступа к службе (SAP), настроенную для обмена данными или активно взаимодействующая с зависимым SAP. В однонаправленном соединении это SAP является передающим.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ фцендпоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ фцендпоинт**](msvm-fcendpoint.md) , представляющий SAP, настроенный для обмена данными или активно взаимодействующий с предшествующей SAP. В однонаправленном соединении этот SAP является получаемым.

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

