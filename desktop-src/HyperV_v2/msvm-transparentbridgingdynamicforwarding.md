---
description: Подключает службу прозрачного моста к динамической пересылке (известному MAC-адресу).
ms.assetid: CA083F15-1E75-4EB9-BE56-95742181FDAC
title: Класс Msvm_TransparentBridgingDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingDynamicForwarding
- Msvm_TransparentBridgingDynamicForwarding.Antecedent
- Msvm_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dd768b458ffed82f82b682b6f121baf67c6a909e142a9e9efdf7f63e29573671
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811764"
---
# <a name="msvm_transparentbridgingdynamicforwarding-class"></a>\_Класс мсвм транспарентбридгингдинамикфорвардинг

Подключает службу прозрачного моста к динамической пересылке (известному MAC-адресу).

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingDynamicForwarding : CIM_TransparentBridgingDynamicForwarding
{
  Msvm_TransparentBridgingService REF Antecedent;
  Msvm_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ транспарентбридгингдинамикфорвардинг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ транспарентбридгингдинамикфорвардинг** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ транспарентбридгингсервице**](msvm-transparentbridgingservice.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ транспарентбридгингсервице**](msvm-transparentbridgingservice.md) , представляющий прозрачную службу моста.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ динамикфорвардинжентри**](msvm-dynamicforwardingentry.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ динамикфорвардинжентри**](msvm-dynamicforwardingentry.md) , представляющий динамическую запись пересылки базы данных пересылки.

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ транспарентбридгингдинамикфорвардинг мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_ТРАНСПАРЕНТБРИДГИНГДИНАМИКФОРВАРДИНГ CIM**](cim-transparentbridgingdynamicforwarding.md)
</dt> <dt>

[**\_ТРАНСПАРЕНТБРИДГИНГДИНАМИКФОРВАРДИНГ CIM**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingdynamicforwarding)
</dt> </dl>

 

