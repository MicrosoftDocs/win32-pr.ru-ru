---
description: Представляет логический элемент, содержащий сведения для представления функциональных возможностей, предоставляемых устройством или программным обеспечением, и управления ими.
ms.assetid: 0b2312da-433b-43d8-8d21-babab12a5b2c
title: Класс CIM_Service (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.PrimaryOwnerName
- CIM_Service.PrimaryOwnerContact
- CIM_Service.StartMode
- CIM_Service.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fc6182ce024b616c49552cf13878d9ec06da97bd0d0b4c7ff3696e7747a943a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899864"
---
# <a name="cim_service-class-hyper-v-management"></a>Класс CIM_Service (Управление Hyper-V)

Представляет логический элемент, содержащий сведения для представления функциональных возможностей, предоставляемых устройством или программным обеспечением, и управления ими. Служба — это объект общего назначения для настройки и управления реализацией функциональности; Это не сама функциональность.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_Service : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  Name;
  string  PrimaryOwnerName;
  string  PrimaryOwnerContact;
  string  StartMode;
  boolean Started;
};
```

## <a name="members"></a>Члены

Класс **\_ службы CIM** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **\_ службы CIM** содержит эти методы.



| Метод                                           | Описание                    |
|:-------------------------------------------------|:-------------------------------|
| [**StartService**](cim-service-startservice.md) | запускает службу.<br/> |
| [**StopService**](cim-service-stopservice.md)   | останавливает службу.<br/>  |



 

### <a name="properties"></a>Свойства

Класс **\_ службы CIM** имеет эти свойства.

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

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Уникальный идентификатор службы, указывающий функциональность службы.

</dd> <dt>

**примарйовнерконтакт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Общие сведения о DMTF \| 001,4 ")
</dt> </dl>

Контактные данные основного владельца службы.

</dd> <dt>

**примарйовнернаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Общие сведения о DMTF \| 001,3 ")
</dt> </dl>

Имя основного владельца службы.

</dd> <dt>

**Запуск**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**значение true** , если служба запущена; в противном случае — **значение false**.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**\_ Служба CIM**".**Енабледдефаулт**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Это свойство использовать не рекомендуется. Вместо этого используйте свойство **енабледдефаулт** , унаследованное от [**CIM \_ енабледлогикалелемент**](cim-enabledlogicalelement.md).

> [!Note]  
> Нерекомендуемое описание: указывает, запускается ли служба автоматически (например, операционная система) или только после запроса.

 

<dt>



 ("Автоматически")


</dt> <dd></dd> <dt>



 ("Вручную")


</dt> <dd></dd> </dl>

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**")
</dt> </dl>

Имя класса, используемое для создания экземпляра системы, содержащей службу. **Системкреатионкласснаме** сочетается с другими ключевыми свойствами этого класса, чтобы уникальным образом идентифицировать экземпляры этого класса и его подклассов.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**")
</dt> </dl>

Имя системы области.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ЕНАБЛЕДЛОГИКАЛЕЛЕМЕНТ CIM**](cim-enabledlogicalelement.md)
</dt> </dl>

 

