---
description: Предоставляет функции доступа семисинчронаус и пример кода для выполнения вызова метода семисинчронаус.
ms.assetid: 3eae38e8-6a63-45c0-99b0-94e25ddbc5a8
ms.tgt_platform: multiple
title: Вызов Семисинчронаус с помощью VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e875a269d2cf1cd4e3b40d5c84d42ffb97dc35a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693323"
---
# <a name="making-a-semisynchronous-call-with-vbscript"></a>Вызов Семисинчронаус с помощью VBScript

Некоторые методы WMI могут возвращать большие коллекции, что приводит к зависанию сценариев. В скрипте по умолчанию используется семисинчронаус Access, а инструментарий управления Windows (WMI) (WMI) задает **вбемфлагретурниммедиатели** для вызовов, которые могут возвращать коллекции больших объектов, такие как следующие методы [**SwbemServices**](swbemservices.md) : [**инстанцесоф**](swbemservices-instancesof.md), [**субклассесоф**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**ассоЦиаторсоф**](swbemservices-associatorsof.md)и [**ReferencesTo**](swbemservices-referencesto.md).

Семисинчронаус Access, использующий **вбемфлагретурниммедиатели** , заданный в параметре *ифлагс* , также является значением по умолчанию для вызовов, которые могут возвращать наборы больших объектов для следующих методов [**SWbemObject**](swbemobject.md) : [**\_ экземпляров**](swbemobject-instances-.md), [**подклассов \_**](swbemobject-subclasses-.md), [**соединителей \_**](swbemobject-associators-.md)и [**ссылок \_**](swbemobject-references-.md).

Чтобы уменьшить использование ресурсов памяти инструментария WMI при обработке большой коллекции объектов, включите значение **вбемфлагфорвардонли** в параметр *ифлагс* . Использование **вбемфлагфорвардонли** заставляет Инструментарий WMI создать перечислитель только для перенаправления, который не допускает повторного поворота коллекции и доступа к элементам.

Инструментарий WMI исключает память для каждого объекта, так как оператор **for each** обрабатывает объект. Нельзя вызвать метод **Count** для коллекции, если установлен флаг **вбемфлагфорвардонли** для вызова, который получил коллекцию. Обратите внимание, что параметр *ифлагс* имеет значение **вбемфлагретурниммедиатели** и **вбемфлагфорвардонли** по умолчанию для метода [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md) .

Следующая процедура описывает, как использовать VBScript для выполнения вызова семисинчронаус.

**Создание вызова семисинчронаус в VBScript**

1.  Задайте для параметра *ифлагс* значение [вбемфлагретурниммедиатели](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).
2.  Сделайте нормальный синхронный вызов для [**SWbemServices.Exeккуери**](swbemservices-execquery.md) или [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md) с помощью значения *ифлагс* .
3.  Если требуется обрабатывать объекты, возвращаемые вызовом в виде коллекции, используйте синтаксис перечисления, такой как VBScript **для каждого из них**. При возвращении каждого объекта он обрабатывается как следующий элемент в коллекции.
4.  Создайте однопроходный перечислитель, объединив значение **вбемфлагретурниммедиатели** со значением **вбемфлагфорвардонли**. Десятичное значение этой операции или равно 48. Эти константы определены в библиотеке типов wbemdisp. tlb для Visual Basic. Большинство языков сценариев используют числовое значение или определяют константу. Дополнительные сведения см. в разделе [вбемфлаженум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).

В следующем примере кода показано, как выполнить вызов метода семисинчронаус. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).


```VB
wbemFlagReturnImmediately = 16
wbemFlagForwardOnly = 32
IFlags = wbemFlagReturnImmediately + wbemFlagForwardOnly
WScript.Echo IFlags
Set objWMIService = GetObject("winmgmts:root\cimv2")
' Query for all the Win32_Process objects on the 
'     local computer and use forward-only enumerator
Set colProcesses = objWMIService.ExecQuery("SELECT Name FROM Win32_Process",,IFlags)
' Receive each object as it arrives
For Each objProcess in colProcesses
    WScript.Echo objProcess.Name
Next
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Вызов метода](calling-a-method.md)
</dt> </dl>

 

 



