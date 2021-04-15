---
description: Одной из основных целей доступа к коллекции является удаление элемента из коллекции. Элемент из коллекции можно удалить с помощью вызова метода SWbemPropertySet. Remove. Этот метод недоступен для SWbemObjectSet или Свбеммесодсет.
ms.assetid: 4a71029c-9fe1-4348-9f78-daa345728e8d
ms.tgt_platform: multiple
title: Удаление одного элемента из коллекции WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dabeb3ff2e7e70cf6fe25f1ddfb0b14032119d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683146"
---
# <a name="removing-a-single-item-from-a-wmi-collection"></a><span data-ttu-id="32257-105">Удаление одного элемента из коллекции WMI</span><span class="sxs-lookup"><span data-stu-id="32257-105">Removing a Single Item from a WMI Collection</span></span>

<span data-ttu-id="32257-106">Одной из основных целей доступа к коллекции является удаление элемента из коллекции.</span><span class="sxs-lookup"><span data-stu-id="32257-106">One of the main purposes of accessing a collection is to remove an item from the collection.</span></span> <span data-ttu-id="32257-107">Элемент из коллекции можно удалить с помощью вызова метода [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="32257-107">You can remove an item from a collection with a call to the [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) method.</span></span> <span data-ttu-id="32257-108">Этот метод недоступен для [**SWbemObjectSet**](swbemobjectset.md) или [**свбеммесодсет**](swbemmethodset.md).</span><span class="sxs-lookup"><span data-stu-id="32257-108">This method is not available for [**SWbemObjectSet**](swbemobjectset.md) or [**SWbemMethodSet**](swbemmethodset.md).</span></span>

<span data-ttu-id="32257-109">Элементы удаляются по имени из [**SWbemPropertySet**](swbempropertyset.md), [**свбемкуалифиерсет**](swbemqualifierset.md)и [**свбемнамедвалуесет**](swbemnamedvalueset.md).</span><span class="sxs-lookup"><span data-stu-id="32257-109">Items are removed by name from [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md), and [**SWbemNamedValueSet**](swbemnamedvalueset.md).</span></span> <span data-ttu-id="32257-110">Однако элементы в [**свбемрефрешер**](swbemrefresher.md) удаляются по индексу, а из [**свбемпривилежесет**](swbemprivilegeset.md) — константой, представляющей имя привилегии.</span><span class="sxs-lookup"><span data-stu-id="32257-110">However, items in [**SWbemRefresher**](swbemrefresher.md) are removed by index and from [**SWbemPrivilegeSet**](swbemprivilegeset.md) by the constant that represents the privilege name.</span></span>

<span data-ttu-id="32257-111">**Удаление элемента из коллекции**</span><span class="sxs-lookup"><span data-stu-id="32257-111">**To remove an item from a collection**</span></span>

-   <span data-ttu-id="32257-112">В следующем примере кода показано, как удалить элемент с помощью вызова метода [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="32257-112">The following code example shows how to remove the item with a call to the [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) method.</span></span>

    ```VB
    oclass.Properties_.Remove "Prop2"
    ```

    

    <span data-ttu-id="32257-113">В следующем примере создается новый класс с именем «Невкласс» в корневом \\ пространстве имен по умолчанию и в него добавляются три свойства.</span><span class="sxs-lookup"><span data-stu-id="32257-113">The following example creates a new class named "NewClass" in the root\\default namespace and adds three properties to it.</span></span> <span data-ttu-id="32257-114">Затем скрипт использует код из предыдущего примера, чтобы удалить второе свойство.</span><span class="sxs-lookup"><span data-stu-id="32257-114">The script then uses the code from the previous example to delete the second property.</span></span>

    ```VB
    ' Obtain an empty class and name it
    Const WBEM_CIMTYPE_STRING = 8
    Set objSWbemService = GetObject("winmgmts:root\default")
    Set objClass = objSWbemService.get()
    Wscript.Echo "Creating class NewClass"
    objClass.Path_.Class = "NewClass"

    ' Add three properties 
    For i = 1 to 3
        objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
    Next
    Getprops()

    ' Remove the Prop2 property
    objClass.Properties_.Remove "Prop2"
    Wscript.Echo "Second property removed "
    Getprops()

    ' Write the changes to the class back
    objClass.Put_

    Sub Getprops()
        Wscript.Echo "Number of Properties = " _
            & objClass.Properties_.Count
        For Each prop in objClass.Properties_
            Wscript.Echo prop.name
        Next
    End Sub
    ```

    

<span data-ttu-id="32257-115">Дополнительные сведения см. в статьях [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md), [доступ к коллекции](accessing-a-collection.md)и [Удаление нескольких элементов из коллекции](removing-multiple-items-from-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="32257-115">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Accessing a Collection](accessing-a-collection.md), and [Removing Multiple Items from a Collection](removing-multiple-items-from-a-collection.md).</span></span>

 

 



