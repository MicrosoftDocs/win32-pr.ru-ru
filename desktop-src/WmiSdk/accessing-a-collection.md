---
description: Коллекция — это стандартная концепция автоматизации, которая предоставляет единообразный интерфейс для набора объектов, для которого можно выполнить итерацию.
ms.assetid: c1ebe529-33cb-4158-923d-124d6328fc60
ms.tgt_platform: multiple
title: Доступ к коллекции WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da563830b742b47a138c106b21efe197108bbdddf7ad7f86b90984a04431aa0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860519"
---
# <a name="accessing-a-wmi-collection"></a>Доступ к коллекции WMI

Коллекция — это стандартная концепция автоматизации, которая предоставляет единообразный интерфейс для набора объектов, для которого можно выполнить итерацию. API скриптов для WMI предоставляет ряд интерфейсов, которые соответствуют парадигме коллекции. В каждом случае используйте метод **Item** для обнаружения элементов с помощью строки, содержащей значение.

Коллекции [**SWbemPropertySet**](swbempropertyset.md), [**свбемкуалифиерсет**](swbemqualifierset.md)и [**свбеммесодсет**](swbemmethodset.md) в основном используются для изменения схемы. Объект [**SWbemObjectSet**](swbemobjectset.md) содержит объекты WMI, такие как экземпляр [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , которые были получены с помощью вызовов, таких как [**SwbemServices. инстанцесоф**](swbemservices-instancesof.md) или [**SWbemObject. \_**](swbemobject-associators-.md)Calls. Объект [**свбемрефрешер**](swbemrefresher.md) может содержать только экземпляры классов WMI. Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) может содержать объекты WMI или любые другие типы данных, которые требуются поставщику для вызова метода.

> [!Note]  
> Следующие разделы были написаны в основном для VBScript. В C# для сортировки и перечисления объектов используется стандартный интерфейс [IEnumerable](/dotnet/api/system.collections.ienumerable) . В отличие от этого, PowerShell обычно использует неявную коллекцию объектов всякий раз, когда возвращаемое значение содержит более одного результата.

 

В следующей таблице перечислены коллекции в API скриптов для WMI, а также элементы и параметры для каждой коллекции.



| Коллекция                                       | Элемент                                              | Параметр Item ()                                                         |
|--------------------------------------------------|------------------------------------------------------|--------------------------------------------------------------------------|
| [**SWbemObjectSet**](swbemobjectset.md)         | [**SWbemObject**](swbemobject.md)                   | Путь объекта                                                              |
| [**SWbemPropertySet**](swbempropertyset.md)     | [**SWbemProperty**](swbemproperty.md)               | Имя свойства                                                            |
| [**свбемкуалифиерсет**](swbemqualifierset.md)   | [**свбемкуалифиер**](swbemqualifier.md)             | Имя квалификатора                                                           |
| [**свбеммесодсет**](swbemmethodset.md)         | [**свбеммесод**](swbemmethod.md)                   | Имя метода                                                              |
| [**свбемнамедвалуесет**](swbemnamedvalueset.md) | [**свбемнамедвалуе**](swbemnamedvalue.md)           | Имя значения                                                               |
| [**свбемпривилежесет**](swbemprivilegeset.md)   | [**свбемпривилеже**](swbemprivilege.md)             | Имя права                                                           |
| [**свбемрефрешер**](swbemrefresher.md)         | [**свбемрефрешаблеитем**](swbemrefreshableitem.md) | Индекс элемента в объекте [**свбемрефрешер**](swbemrefresher.md) |



 

Дополнительные сведения и примеры добавления и удаления элементов из коллекции см. в разделе [Удаление одного элемента](removing-a-single-item-from-a-collection.md) из коллекции и [Удаление нескольких элементов из коллекции](removing-multiple-items-from-a-collection.md). Дополнительные сведения о работе с классами см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).

 

 
