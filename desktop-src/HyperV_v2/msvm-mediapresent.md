---
description: Связывает диск хранилища с носителем, вставленным в диск.
ms.assetid: C0B2D604-0B55-4EA0-A46E-2450D89A5B22
title: Класс Msvm_MediaPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MediaPresent
- Msvm_MediaPresent.Antecedent
- Msvm_MediaPresent.Dependent
- Msvm_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7044cfed5a4affd628ea8008c89b4aabeee3499d65f03abf815e68d73d06a773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521724"
---
# <a name="msvm_mediapresent-class"></a>\_Класс мсвм медиапресент

Связывает диск хранилища с носителем, вставленным в диск. Эта ассоциация используется для всех объектов дисков хранилища.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MediaPresent : CIM_MediaPresent
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ медиапресент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ медиапресент** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на устройство доступа к носителю. Это свойство наследуется от [**CIM \_ медиапресент**](/windows/desktop/CIMWin32Prov/cim-mediapresent).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экстент хранилища, к которому осуществляется доступ с помощью устройства доступа к носителю. Это свойство наследуется от [**CIM \_ медиапресент**](/windows/desktop/CIMWin32Prov/cim-mediapresent).

</dd> <dt>

**фикседмедиа**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, является ли доступная область хранилища фиксированной и не может быть извлечена. Значение **true** для жестких дисков и **false** в противном случае. Это свойство наследуется от [**CIM \_ медиапресент**](/windows/desktop/CIMWin32Prov/cim-mediapresent).

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ медиапресент мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_МЕДИАПРЕСЕНТ CIM**](cim-mediapresent.md)
</dt> <dt>

[**\_МЕДИАПРЕСЕНТ CIM**](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[служба хранилища Класса](storage-classes.md)
</dt> </dl>

 

