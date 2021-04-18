---
description: Представляет точку доступа к службе (SAP), которая может использовать или вызывать службу. SAPs указывает, что служба доступна для использования другими сущностями.
ms.assetid: 09349c95-3f7e-46c5-bea1-c3d14ee16a2a
title: Класс CIM_ServiceAccessPoint (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3e27fc667c55cd101b06a34f9140cb9eed8923f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682806"
---
# <a name="cim_serviceaccesspoint-class-hyper-v-management"></a>Класс CIM_ServiceAccessPoint (Управление Hyper-V)

Представляет точку доступа к службе (SAP), которая может использовать или вызывать службу. SAPs указывает, что служба доступна для использования другими сущностями.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAccessPoint : CIM_EnabledLogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ сервицеакцесспоинт** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ сервицеакцесспоинт** имеет следующие свойства.

<dl> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Имя класса, используемое для создания экземпляра этого класса. **Свойство CreationClassName** объединяется с другими ключевыми свойствами этого класса, чтобы уникальным образом идентифицировать экземпляры этого класса и его подклассов.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Уникальное имя SAP, которое указывает возможности, поддерживаемые SAP.

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**")
</dt> </dl>

Имя класса, используемое для создания экземпляра системы, содержащей SAP. **Системкреатионкласснаме** сочетается с другими ключевыми свойствами этого класса, чтобы уникальным образом идентифицировать экземпляры этого класса и его подклассов.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**")
</dt> </dl>

Имя системы, содержащей SAP.

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

[**\_ЕНАБЛЕДЛОГИКАЛЕЛЕМЕНТ CIM**](cim-enabledlogicalelement.md)
</dt> </dl>

 

