---
description: Вводный пример с использованием каталога администрирования COM+
ms.assetid: e9ce25aa-4fb1-4357-9f4e-5bf649e29447
title: Вводный пример с использованием каталога администрирования COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db24f3985538b7189534c9fef3ef279ed240e3a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673145"
---
# <a name="introductory-example-using-the-com-administration-catalog"></a>Вводный пример с использованием каталога администрирования COM+

При программном использовании каталога администрирования COM+ обычно выполняются следующие общие действия (не даны в определенном порядке):

-   Откройте сеанс с каталогом COM+ на локальном компьютере. При необходимости подключитесь к каталогу COM+ на удаленном компьютере.
-   Выполнение таких действий, как запуск или остановка служб — действия, которые не относятся к конкретному приложению COM+.
-   Выполнение таких действий, как установка или экспорт приложений COM+ или установка компонентов в приложения — действия, относящиеся к чтению или записи в файлы.
-   Добавление новых элементов в коллекции, например создание нового приложения COM+ путем добавления нового элемента в коллекцию "приложения".
-   Задание или получение свойств элемента в коллекции.
-   Сохранение или Отмена ожидающих изменений в каталоге.
-   Обрабатывайте любые ошибки, которые могут возникнуть.

Чтобы увидеть, как выглядят эти шаги при использовании объектов Комадмин, ниже приведен пример Visual Basic Microsoft. Он кратко иллюстрирует некоторые из типичных действий, описанных выше, таких как поиск коллекций, перечисление коллекции для получения элемента и задание свойств этого элемента.

В приведенном ниже примере выполняются следующие действия.

1.  Создайте новое приложение COM+ «Михомезу».
2.  Установите в приложение некоторые компоненты, Cat и Dog. Оба компонента содержатся в одной библиотеке DLL, которая должна уже существовать: MyZoo.dll.
3.  Настройте безопасность на основе ролей для приложения, определив две роли: ZooKeeper и Аллергиктокатс.
4.  Назначьте роли ZooKeeper доступ ко всему приложению.
5.  Назначьте роли Аллергиктокатс доступ только компоненту Dog.
6.  Включите свойства безопасности, чтобы для приложения была применена проверка ролей.
7.  Экспортируйте приложение Михомезу в файл, чтобы его можно было установить на других компьютерах.

Чтобы использовать этот пример из Visual Basic, добавьте ссылку на библиотеку типов администрирования COM+.


```VB
Function SetupMyZoo() As Boolean  ' Return False if any errors occur.

    '  Initialize error handling for this function.
    SetupMyZoo = False 
    On Error GoTo My_Error_Handler

    '  Open a session with the catalog.
    '  Instantiate a COMAdminCatalog object. 
    Dim objCatalog As COMAdminCatalog
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")

    '  Create a new COM+ application.
    '  First get the "Applications" collection from the catalog.
    Dim objApplicationsColl As COMAdminCatalogCollection
    Set objApplicationsColl = objCatalog.GetCollection("Applications")

    '  Add a new item to this collection. 
    Dim objZooApp As COMAdminCatalogObject
    Set objZooApp = objApplicationsColl.Add

    '  The "Applications" collection determines the available properties.
    '  Set the "Name" property of the new application item. 
    objZooApp.Value("Name") = "MyHomeZoo"

    '  Set the "Description" property of the new application item. 
    objZooApp.Value("Description") = "My pets at home"

    '  Save changes made to the "Applications" collection. 
    objApplicationsColl.SaveChanges

    '  Install components into the application.
    '  Use the InstallComponent method on COMAdminCatalog. 
    '  In this case, the last two parameters are passed as empty strings.
    objCatalog.InstallComponent "MyHomeZoo","MyZoo.DLL","","" 

    '  Define the roles ZooKeeper and AllergicToCats 
    '  by adding them to the "Roles" collection related to MyHomeZoo. 
    '  First get the "Roles" collection related to MyHomeZoo.
    '  Use the GetCollection method on COMAdminCatalogCollection,
    '  passing in the name of the desired collection, "Roles", 
    '  and the Key property value of objZooApp.   
    '  The Key property uniquely identifies the object, serving
    '  here to distinguish the "Roles" collection related 
    '  to MyHomeZoo from that of any other application. 
    Dim objRolesColl As COMAdminCatalogCollection
    Set objRolesColl = objApplicationsColl.GetCollection("Roles", objZooApp.Key)

    '  Add new items to this "Roles" collection. 
    Dim objZooKeeperRole As COMAdminCatalogObject
    Dim objAllergicToCatsRole As COMAdminCatalogObject
    Set objZooKeeperRole = objRolesColl.Add
    Set objAllergicToCatsRole = objRolesColl.Add

    '  Set the "Name" for the new items.
    objZooKeeperRole.Value("Name") = "ZooKeeper" 
    objAllergicToCatsRole.Value("Name") = "AllergicToCats" 

    '  Save changes made to any items in this "Roles" collection. 
    objRolesColl.SaveChanges

    '  Assign the AllergicToCats role to the Dog component to 
    '  restrict its scope of access. (The ZooKeeper role, if assigned
    '  only at the application level, can access the whole application.)
    '  First get the "Components" collection related to MyHomeZoo.
    '  Use the GetCollection method on COMAdminCatalogCollection,
    '  passing in the name of the desired collection, "Components", and
    '  the Key property value of objZooApp. 
    Dim objZooComponentsColl As COMAdminCatalogCollection
    Set objZooComponentsColl = objApplicationsColl.GetCollection("Components", objZooApp.Key) 

    '  Find the Dog component item in this "Components" collection.
    '  First Populate the collection to read in data for all its items. 
    objZooComponentsColl.Populate

    '  Enumerate through the "Components" collection 
    '  until the Dog component item is located. 
    Dim objDog As COMAdminCatalogObject 
    For Each objDog in objZooComponentsColl
        If objDog.Name = "Dog" Then 
            Exit For
        End If
    Next 
    '  Set the role checking property at the component level for Dog.
        objDog.Value("ComponentAccessChecksEnabled") = True 

    '  Save these changes.
        objZooComponentsColl.SaveChanges
    '  Get the "RolesForComponent" collection related to the 
    '  Dog component, using the Key property of objDog. 
    Dim objRolesForDogColl As COMAdminCatalogCollection 
    Set objRolesForDogColl = objZooComponentsColl.GetCollection("RolesForComponent", objDog.Key) 

    '  Add a new item to this "RolesForComponent" collection. 
    Dim objCatSneezerRole As COMAdminCatalogObject
    Set objCatSneezerRole = objRolesForDogColl.Add

    '  Set the "Name" of the new item to be "AllergicToCats". 
    objCatSneezerRole.Value("Name") = "AllergicToCats" 

    '  Save changes made to this "RolesForComponent" collection. 
    objRolesForDogColl.SaveChanges

    '  Now set properties to enforce role-based security. 
    '  First set role-based security at the application level.
    objZooApp.Value("ApplicationAccessChecksEnabled") = True 
    objZooApp.Value("AccessChecksLevel") = COMAdminAccessChecksApplicationComponentLevel 

    '  Save these changes.
    objApplicationsColl.SaveChanges

    '  Finally, export the new configured MyHomeZoo application to an 
    '  MSI file, used to install the application on other machines.
    '  Use the ExportApplication method on COMAdminCatalogObject.
    objCatalog.ExportApplication "MyHomeZoo", "c:\Program Files\COM applications\MyHomeZoo.MSI", 4

    '  Exit the function gracefully.
    SetupMyZoo = True

My_Error_Handler:
    If Not SetupMyZoo Then
        MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) & ")" & vbNewLine & Err.Description
    End If
    objCatSneezerRole = Nothing
    objRolesForDogColl = Nothing
    objDog = Nothing
    objZooComponentsColl = Nothing
    objAllergicToCatsRole = Nothing
    objZooKeeperRole = Nothing
    objRolesColl = Nothing
    objZooApp = Nothing
    objApplicationsColl = Nothing
    objCatalog = Nothing
Exit Function
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Операции администрирования COM+ в транзакциях](com--administration-operations-within-transactions.md)
</dt> <dt>

[Обработка ошибок администрирования COM+](handling-com--administration-errors.md)
</dt> <dt>

[Общие сведения об объектах Комадмин](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Получение коллекций в каталоге COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Установка свойств и сохранение изменений в каталоге COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



