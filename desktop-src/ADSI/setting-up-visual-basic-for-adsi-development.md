---
title: Настройка Visual Basic 6,0 для разработки с интерфейсом ADSI
description: В этом разделе описано, как настроить Visual Basic в Visual Studio для разработки приложения ADSI.
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- Настройка Visual Basic для ADSI разработки ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e6b1f39ec06d3716beab750dbf2a522d4c18cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887483"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a>Настройка Visual Basic 6,0 для разработки с интерфейсом ADSI

**Настройка среды разработки Microsoft Visual Studio 2010 для Visual Basic**

1.  Запустите Visual Studio 2010.
2.  Создайте новый проект Visual Basic.
3.  Добавьте ссылку на **библиотеку типов Active Directory**.
    > [!Note]  
    > Если не требуется ранняя привязка COM-объекта, пропустите этот шаг.

     

    1.  Выберите **проект \| Добавить ссылку**.
    2.  Перейдите на вкладку **com** .
    3.  Выберите **Библиотека типов Active Directory**.

4.  Начните программировать с помощью ADSI.

Прежде чем начать, войдите в домен Windows. Необходимо иметь разрешение на изменение базы данных Active Directory. По умолчанию эта привилегия есть у администратора.

**Пример приложения Visual Basic 6,0: изменение FullName и описание пользователя**

1.  Выполните описанные выше действия, чтобы создать стандартный исполняемый Visual Basic проект.
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

    

3.  Нажмите клавишу **<F5>** , чтобы запустить программу.
4.  Чтобы проверить изменения, используйте средство управления Active Directory пользователи и компьютеры. Дополнительные сведения об использовании ADSI и Visual Basic см. в разделе [доступ к Active Directory с помощью Visual Basic](accessing-active-directory-using-visual-basic.md).

 

 




