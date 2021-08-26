---
title: настройка Visual Basic 6,0 для разработки с интерфейсом ADSI
description: в этом разделе описано, как настроить Visual Basic в Visual Studio для разработки приложения ADSI.
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- настройка Visual Basic для adsi разработки adsi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cadc9f74410dcb654a880920a83c20e6af9db1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885200"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a>настройка Visual Basic 6,0 для разработки с интерфейсом ADSI

**настройка среды разработки Microsoft Visual Studio 2010 для Visual Basic**

1.  Запустите Visual Studio 2010.
2.  создайте новый проект Visual Basic.
3.  Добавьте ссылку на **библиотеку типов Active Directory**.
    > [!Note]  
    > Если не требуется ранняя привязка COM-объекта, пропустите этот шаг.

     

    1.  выберите **Project \| добавить ссылку**.
    2.  Перейдите на вкладку **com** .
    3.  Выберите **Библиотека типов Active Directory**.

4.  Начните программировать с помощью ADSI.

прежде чем начать, войдите в домен Windows. Необходимо иметь разрешение на изменение базы данных Active Directory. По умолчанию эта привилегия есть у администратора.

**пример приложения Visual Basic 6,0: изменение FullName и описание пользователя**

1.  выполните описанные выше действия, чтобы создать стандартный исполняемый Visual Basic проект.
2.  Дважды щелкните форму. В поле \_ Загрузка формы введите следующую команду. Необходимо заменить строку "LDAP://кН = жеффсмис, CN = Users, DC = Fabrikam, DC = com" на значение ADsPath существующего пользователя в контейнере в вашем домене. Создайте тестовую учетную запись пользователя, которую можно изменить для этой цели.
    ```VB
    '------------------------------------------------------------
    ' This code example is used to set the FullName and Description
    '------------------------------------------------------------
    Dim usr As IADsUser

    ' Bind to a user object.
    Set usr = GetObject("LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com")

    usr.FullName = "Jeff Smith"
    usr.Description = "A user for fabrikam.com" 
    usr.SetInfo ' Commit the changes to the directory
    ```

    

3.  Нажмите клавишу **&lt; F5 &gt;** , чтобы запустить программу.
4.  Чтобы проверить изменения, используйте средство управления Active Directory пользователи и компьютеры. дополнительные сведения об использовании ADSI и Visual Basic см. в разделе [доступ к Active Directory с помощью Visual Basic](accessing-active-directory-using-visual-basic.md).

 

 




