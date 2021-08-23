---
description: Этот класс устарел. Вместо этого рекомендуется создавать производные от \_ класса службы CIM.
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: Класс CIM_NetworkService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkService
- CIM_NetworkService.Keywords
- CIM_NetworkService.ServiceURL
- CIM_NetworkService.StartupConditions
- CIM_NetworkService.StartupParameters
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cfb2ea7b122516cc3b62f675684649e22577171f713856638f97985d9713e8d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694694"
---
# <a name="cim_networkservice-class"></a>\_Класс сетевой NetworkService CIM

Этот класс устарел. Вместо этого рекомендуется создавать производные от класса [**\_ службы CIM**](cim-service.md) .

## <a name="syntax"></a>Синтаксис

``` syntax
[Deprecated("CIM_Service"), Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_NetworkService : CIM_Service
{
  string Keywords[];
  string ServiceURL;
  string StartupConditions[];
  string StartupParameters[];
};
```

## <a name="members"></a>Члены

Класс **\_ NetworkService CIM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ NetworkService CIM** имеет эти свойства.

<dl> <dt>

**Ключевые слова**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения")
</dt> </dl>

Это свойство является устаревшим и не должно использоваться.

> [!Note]  
> Нерекомендуемое описание: массив ключевых слов, которые могут использоваться в запросах.

 

</dd> <dt>

**ServiceURL**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ сервицеакцессури")
</dt> </dl>

Это свойство использовать не рекомендуется. Вместо этого рекомендуется использовать класс **CIM \_ сервицеакцессури** .

> [!Note]  
> Нерекомендуемое описание: URL-адрес, предоставляющий протокол, сетевое расположение и другие сведения, относящиеся к службе, необходимые для доступа к службе.

 

</dd> <dt>

**стартупкондитионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения")
</dt> </dl>

Это свойство является устаревшим и не должно использоваться.

> [!Note]  
> Нерекомендуемое описание: предварительные условия, которые должны быть выполнены, чтобы эта служба запускалась правильно.

 

</dd> <dt>

**стартуппараметерс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения")
</dt> </dl>

Это свойство является устаревшим и не должно использоваться.

> [!Note]  
> Нерекомендуемое описание: параметры, которые должны быть передаются методу **StartService** для правильной работы этой службы.

 

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

[**\_Служба CIM**](cim-service.md)
</dt> </dl>

 

