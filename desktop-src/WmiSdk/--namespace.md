---
description: Представляет пространство имен WMI.
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: Класс __Namespace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Namespace
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4640570dd834b42652d04262b70ec84fac106d99f463ca22144e28ad388a0937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320772"
---
# <a name="__namespace-class"></a>\_\_Класс Namespace

Класс системы **\_ \_ пространства имен** представляет пространство имен WMI.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ Namespace** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ Namespace** имеет следующие свойства.

<dl> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **ключ**](standard-qualifiers.md)
</dt> </dl>

Имя пространства имен.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **\_ \_ Namespace** является производным от [**\_ \_ системкласс**](--systemclass.md), у которого нет свойств.

**\_ \_ Пространство имен** можно использовать для поиска, создания и удаления дочерних пространств имен в текущем рабочем пространстве, для которого имеется объект [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Создание нового экземпляра **\_ \_ пространства имен** в любом рабочем пространстве имен создает Дочернее пространство имен в рабочем пространстве имен. И наоборот, удаление экземпляра **\_ \_ пространства имен** удаляет Дочернее пространство имен из рабочего пространства имен. Обратите внимание, что при удалении дочернего пространства имен также удаляются все его классы и экземпляры.

Перечисление экземпляров этого класса в любом рабочем пространстве имен предоставляет доступные дочерние пространства имен.

Например, в \\ корневом пространстве имен два экземпляра **\_ \_ пространства имен**. Свойство **Name** имеет значение Default, а другое имеет **имя** "CIMV2". Эти экземпляры представляют \\ корневые \\ пространства имен по умолчанию и \\ корневые \\ CIMV2, соответственно.

## <a name="examples"></a>Примеры

В примере из [списка всех пространств имен WMI](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) в коллекции TechNet используется рекурсивный вызов для перечисления всех экземпляров \_ \_ класса пространства имен в системе.

Следующий пример кода извлекает все пространства имен в PowerShell.


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



Следующий пример кода улучшает предыдущий пример и добавляет дополнительные сведения.


```PowerShell
# Set computer name 
$comp = "." 
 
# Get the name spaces on the local computer, and the local computer name 
$Namespace = get-wmiobject __namespace -namespace 'root' -list -recurse -computer $comp  
$hotsname = hostname 
 
# Display number of and names of the namespaces 
"{0} Namespaces on: {1}" -f $namespace.count, $hostname 
$NameSpace| sort __namespace  | Format-Table @{Expression = "__Namespace"; Label = "Namespace"}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_\_системкласс**](--systemclass.md)
</dt> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> </dl>

 

 




