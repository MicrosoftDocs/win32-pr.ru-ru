---
description: При попытке удалить несколько элементов в коллекции некоторые элементы могут быть не удалены.
ms.assetid: 7c82321e-059f-497c-8561-33c3e9306d41
ms.tgt_platform: multiple
title: Удаление нескольких элементов из коллекции WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17795378f5215977e5e7c2d0afd745c5d02fe6b294d062fcdbcf82f7ccc15351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992444"
---
# <a name="removing-multiple-items-from-a-wmi-collection"></a>Удаление нескольких элементов из коллекции WMI

При попытке удалить несколько элементов в коллекции некоторые элементы могут быть не удалены. Невозможно выполнить итерацию коллекции при удалении элементов, поскольку при удалении элемента из коллекции указатель коллекции перемещается к следующему элементу. Например, попытка удалить все элементы из коллекции приводит к удалению всех остальных элементов. Эта проблема может появиться при удалении элементов с помощью методов [**свбемкуалифиерсет. Remove**](swbemqualifierset-remove.md) или [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) . Эту проблему можно избежать, пройдите по коллекции и поместив имена элементов, которые нужно удалить в массиве. Затем можно перебрать массив и удалить элементы с именем в массиве. Такие коллекции, как [**свбемнамедвалуесет**](swbemnamedvalueset.md), [**свбемпривилежесет**](swbemprivilegeset.md)и [**свбемрефрешер**](swbemrefresher.md), также имеют метод, который удаляет все элементы в контейнере обновитель.

В следующем скрипте показано, как удалить несколько элементов из коллекции.


```VB
Const WBEM_CIMTYPE_STRING = 8    ' Value for string data type
Dim names()
Redim names (0)
set objSWbemService = GetObject("winmgmts:root\default")
set objClass = ObjSWbemService.Get()

Wscript.Echo "Creating class NewClass"
objClass.Path_.Class = "NewClass"
For i = 1 to 5
    objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
Next
objClass.Put_
Getprops()

' Get all the property names in an array
For Each oprop in objClass.properties_
    Redim Preserve names(Ubound(names)+1)
    names(Ubound(names)-1) = oprop.name
Next
Wscript.Echo "Remove first 3 properties using array of names:"

For i = Lbound(names) to Ubound(names)-1
    If (i < 3) Then
       Wscript.Echo "Removing " & names(i)
       objClass.Properties_.Remove names(i)
    End If
Next

objClass.Put_
Wscript.Echo "Result:"
Getprops()

Sub Getprops()
    Wscript.Echo "Number of properties = " _
        & objClass.Properties_.Count
    For Each oprop in objClass.Properties_
        Wscript.Echo oprop.name
    Next
End Sub
```



Нельзя удалить свойства и квалификаторы в экземпляре класса или в производном классе, который имеет унаследованные свойства. Такая операция удаления вызывает ошибку, а свойство или квалификатор не удаляется; Вместо этого инструментарий WMI сбрасывает свойство или квалификатор в значение по умолчанию. В случае производного класса с унаследованными свойствами Инструментарий WMI сбрасывает унаследованное свойство в значение по умолчанию свойства в родительском классе.

Дополнительные сведения см. в статьях [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md), [доступ к коллекции](accessing-a-collection.md)и [Удаление одного элемента из коллекции](removing-a-single-item-from-a-collection.md).

 

 



