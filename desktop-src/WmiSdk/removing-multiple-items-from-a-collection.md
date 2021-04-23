---
description: При попытке удалить несколько элементов в коллекции некоторые элементы могут быть не удалены.
ms.assetid: 7c82321e-059f-497c-8561-33c3e9306d41
ms.tgt_platform: multiple
title: Удаление нескольких элементов из коллекции WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c44203f3279163a1de595cac8a00270dccd31c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712953"
---
# <a name="removing-multiple-items-from-a-wmi-collection"></a><span data-ttu-id="c81d0-103">Удаление нескольких элементов из коллекции WMI</span><span class="sxs-lookup"><span data-stu-id="c81d0-103">Removing Multiple Items from a WMI Collection</span></span>

<span data-ttu-id="c81d0-104">При попытке удалить несколько элементов в коллекции некоторые элементы могут быть не удалены.</span><span class="sxs-lookup"><span data-stu-id="c81d0-104">If you attempt to remove more than one item in a collection, you may find that some items are not removed.</span></span> <span data-ttu-id="c81d0-105">Невозможно выполнить итерацию коллекции при удалении элементов, поскольку при удалении элемента из коллекции указатель коллекции перемещается к следующему элементу.</span><span class="sxs-lookup"><span data-stu-id="c81d0-105">You cannot iterate a collection while removing items, because when you remove an element from a collection, the collection pointer is moved on to the next element.</span></span> <span data-ttu-id="c81d0-106">Например, попытка удалить все элементы из коллекции приводит к удалению всех остальных элементов.</span><span class="sxs-lookup"><span data-stu-id="c81d0-106">For example, an attempt to remove all of the items from a collection results in the removal of every other item.</span></span> <span data-ttu-id="c81d0-107">Эта проблема может появиться при удалении элементов с помощью методов [**свбемкуалифиерсет. Remove**](swbemqualifierset-remove.md) или [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="c81d0-107">You may see this problem when you are removing items with the [**SWbemQualifierSet.Remove**](swbemqualifierset-remove.md) or [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) methods.</span></span> <span data-ttu-id="c81d0-108">Эту проблему можно избежать, пройдите по коллекции и поместив имена элементов, которые нужно удалить в массиве.</span><span class="sxs-lookup"><span data-stu-id="c81d0-108">You can avoid this problem by looping through the collection and putting the names of the items to remove in an array.</span></span> <span data-ttu-id="c81d0-109">Затем можно перебрать массив и удалить элементы с именем в массиве.</span><span class="sxs-lookup"><span data-stu-id="c81d0-109">You then can loop through the array and delete the items named in the array.</span></span> <span data-ttu-id="c81d0-110">Такие коллекции, как [**свбемнамедвалуесет**](swbemnamedvalueset.md), [**свбемпривилежесет**](swbemprivilegeset.md)и [**свбемрефрешер**](swbemrefresher.md), также имеют метод, который удаляет все элементы в контейнере обновитель.</span><span class="sxs-lookup"><span data-stu-id="c81d0-110">The collections, such as [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), and [**SWbemRefresher**](swbemrefresher.md), also have a method that deletes all items in the refresher container.</span></span>

<span data-ttu-id="c81d0-111">В следующем скрипте показано, как удалить несколько элементов из коллекции.</span><span class="sxs-lookup"><span data-stu-id="c81d0-111">The following script illustrates how to remove several items from a collection.</span></span>


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



Нельзя удалить свойства и квалификаторы в экземпляре класса или в производном классе, который имеет унаследованные свойства. Такая операция удаления вызывает ошибку, а свойство или квалификатор не удаляется; Вместо этого инструментарий WMI сбрасывает свойство или квалификатор в значение по умолчанию. <span data-ttu-id="c81d0-114">В случае производного класса с унаследованными свойствами Инструментарий WMI сбрасывает унаследованное свойство в значение по умолчанию свойства в родительском классе.</span><span class="sxs-lookup"><span data-stu-id="c81d0-114">In the case of a derived class with inherited properties, WMI resets the inherited property to the default value of the property in the parent class.</span></span>

<span data-ttu-id="c81d0-115">Дополнительные сведения см. в статьях [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md), [доступ к коллекции](accessing-a-collection.md)и [Удаление одного элемента из коллекции](removing-a-single-item-from-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="c81d0-115">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Accessing a Collection](accessing-a-collection.md), and [Removing a Single Item from a Collection](removing-a-single-item-from-a-collection.md).</span></span>

 

 



