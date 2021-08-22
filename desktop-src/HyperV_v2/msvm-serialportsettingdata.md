---
description: Описание параметров для виртуального последовательного порта.
ms.assetid: 8b257bbf-495a-4eef-86a1-70e31e4a85a5
title: Класс Msvm_SerialPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortSettingData
- Msvm_SerialPortSettingData.DebuggerMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c7365ee67cdcf3f9046ac162f36a909f54da5ab4b9683f801827213d43d0fb79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950563"
---
# <a name="msvm_serialportsettingdata-class"></a>\_Класс мсвм сериалпортсеттингдата

Описание параметров для виртуального последовательного порта.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortSettingData : CIM_ResourceAllocationSettingData
{
  boolean DebuggerMode;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ сериалпортсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ сериалпортсеттингдата** имеет следующие свойства.

<dl> <dt>

**дебугжермоде**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

**значение true** , если режим отладчика включен для виртуального последовательного порта; в противном случае — **значение false**. режим отладчика улучшает использование отладчика ядра Microsoft Windows для виртуального последовательного порта.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




