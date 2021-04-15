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
# <a name="removing-a-single-item-from-a-wmi-collection"></a>Удаление одного элемента из коллекции WMI

Одной из основных целей доступа к коллекции является удаление элемента из коллекции. Элемент из коллекции можно удалить с помощью вызова метода [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) . Этот метод недоступен для [**SWbemObjectSet**](swbemobjectset.md) или [**свбеммесодсет**](swbemmethodset.md).

Элементы удаляются по имени из [**SWbemPropertySet**](swbempropertyset.md), [**свбемкуалифиерсет**](swbemqualifierset.md)и [**свбемнамедвалуесет**](swbemnamedvalueset.md). Однако элементы в [**свбемрефрешер**](swbemrefresher.md) удаляются по индексу, а из [**свбемпривилежесет**](swbemprivilegeset.md) — константой, представляющей имя привилегии.

**Удаление элемента из коллекции**

-   В следующем примере кода показано, как удалить элемент с помощью вызова метода [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .

    ```VB
    oclass.Properties_.Remove "Prop2"
    ```

    

    В следующем примере создается новый класс с именем «Невкласс» в корневом \\ пространстве имен по умолчанию и в него добавляются три свойства. Затем скрипт использует код из предыдущего примера, чтобы удалить второе свойство.

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

    

Дополнительные сведения см. в статьях [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md), [доступ к коллекции](accessing-a-collection.md)и [Удаление нескольких элементов из коллекции](removing-multiple-items-from-a-collection.md).

 

 



