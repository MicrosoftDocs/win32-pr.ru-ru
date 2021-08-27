---
description: Навигация по иерархии коллекции COM+
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Навигация по иерархии коллекции COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef6f23cd9f584b6cbe496fe7122abfa9978cd25cb28d81a5c89782b718138be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070454"
---
# <a name="navigating-the-com-collection-hierarchy"></a>Навигация по иерархии коллекции COM+

Некоторые коллекции можно легко получить с помощью метода [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) объекта [**комадминкаталог**](comadmincatalog.md) . Этот метод получает коллекцию "верхнего уровня"; Это означает, что коллекция, например [**приложения**](applications.md), является собственной и является уникальной и не относящиеся в другую коллекцию.

Однако многие коллекции логически относящиеся под другой коллекцией, поскольку они содержат элементы, которые являются частью некоторой большой структуры. Например, коллекция [**Components**](components.md) относящиеся или связана с коллекцией [**приложений**](applications.md) , так как она содержит компоненты, установленные в определенном приложении COM+, которое само соответствует элементу в коллекции **приложений** . Связанные коллекции, такие как, не являются уникальными; существует коллекция **компонентов** для каждого отдельного приложения.

Поэтому коллекции упорядочиваются в иерархическую структуру, которая естественным образом соответствует логическим связям между элементами, которые они содержат. Схему иерархии коллекции можно найти в [коллекции администрирования com+](com--administration-collections.md). Для многих элементов, которые необходимо настроить с помощью объектов Комадмин, необходимо перемещаться по некоторой части иерархии коллекции, чтобы получить соответствующий элемент.

На практике это означает, что если требуется получить элемент в связанной коллекции, необходимо сначала пройти все необходимые более высокие уровни, субсуминг коллекции. Чтобы получить связанную коллекцию, необходимо получить конкретный элемент в родительской коллекции, с которой связана Дочерняя коллекция. Например, если требуется настроить элемент, соответствующий компоненту в определенном приложении COM+, необходимо выполнить следующие действия.

1.  Получите коллекцию [**приложений**](applications.md) и заполните ее.
2.  Перечислите содержимое коллекции [**приложений**](applications.md) , чтобы перейти к элементу, соответствующему нужному приложению COM+.
3.  Получите и заполните коллекцию [**компонентов**](components.md) для конкретного приложения COM+.
4.  Перечислите содержимое коллекции [**Components**](components.md) , пока не будет получен элемент, соответствующий нужному компоненту.

в следующем примере Microsoft Visual Basic показано, как выполнить описанные выше действия.


```VB
On Error GoTo My_Error_Handler

Dim Catalog As COMAdminCatalog 
Set Catalog = CreateObject("COMAdmin.COMAdminCatalog")

' Get the Applications collection and populate it.
Dim Applications As COMAdminCatalogCollection 
Set Applications = Catalog.GetCollection("Applications") 
Applications.Populate

' Get the correct application, "My Application".
Dim AppObject As COMAdminCatalogObject 
For Each AppObject in Applications 
    If AppObject.Name = "My Application" Then 
        Exit For 
    End If
Next 

' Get and populate the Components collection for "My Application".
Dim Components As COMAdminCatalogCollection 
Set Components = Applications.GetCollection("Components", AppObject.Key) 
Components.Populate

' Get the correct component, "My Component".
Dim CompObject As COMAdminCatalogObject 
For Each CompObject in Components 
    If CompObject.Name = "My Component" Then 
        Exit For 
    End If
Next 

```



В предыдущем примере используются два различных метода **IsCollection** . Первый объект предоставляется [**комадминкаталог**](comadmincatalog.md) и используется для получения коллекции верхнего уровня — в данном случае — «Applications». Второй объект предоставляется [**комадминкаталогколлектион**](comadmincatalogcollection.md) и используется для получения коллекции, связанной с текущей коллекцией. точно указывается, какая коллекция нужна, передав имя "Components" и значение свойства ключа родительского объекта. Значение ключевого свойства часто является именем или идентификатором GUID, уникальным образом определяющим объект. Это значение определяется в документации по каждой коллекции.

В общем случае необходимо получить связанные коллекции итеративно вниз по иерархии коллекции, пока вы не получите нужную коллекцию. Действия, которые необходимо выполнить в одной и той же общей модели, повторяются повторно. Полный список коллекций см. в разделе [com+ Administration Collections](com--administration-collections.md).

В некоторых случаях может потребоваться использовать метод ярлыка во второй раз после пути через иерархию коллекции. Этот метод можно использовать только после кэширования всех промежуточных значений ключей. Дополнительные сведения см. в разделе [**икомадминкаталог:: жетколлектионбикуери**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Заполнение коллекций COM+](populating-com--collections.md)
</dt> <dt>

[Запросы к доступным связанным коллекциям](querying-for-available-related-collections.md)
</dt> <dt>

[Получение коллекций в каталоге COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



