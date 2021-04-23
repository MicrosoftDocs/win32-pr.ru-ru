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
# <a name="setting-up-visual-basic-60-for-adsi-development"></a><span data-ttu-id="26cea-104">Настройка Visual Basic 6,0 для разработки с интерфейсом ADSI</span><span class="sxs-lookup"><span data-stu-id="26cea-104">Setting Up Visual Basic 6.0 for ADSI Development</span></span>

<span data-ttu-id="26cea-105">**Настройка среды разработки Microsoft Visual Studio 2010 для Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="26cea-105">**Setting Up the Microsoft Visual Studio 2010 Development Environment For Visual Basic**</span></span>

1.  <span data-ttu-id="26cea-106">Запустите Visual Studio 2010.</span><span class="sxs-lookup"><span data-stu-id="26cea-106">Start Visual Studio 2010.</span></span>
2.  <span data-ttu-id="26cea-107">Создайте новый проект Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="26cea-107">Create a new Visual Basic project.</span></span>
3.  <span data-ttu-id="26cea-108">Добавьте ссылку на **библиотеку типов Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="26cea-108">Add a reference to the **Active DS Type Library**.</span></span>
    > [!Note]  
    > <span data-ttu-id="26cea-109">Если не требуется ранняя привязка COM-объекта, пропустите этот шаг.</span><span class="sxs-lookup"><span data-stu-id="26cea-109">If you do not require early COM object binding, ignore this step.</span></span>

     

    1.  <span data-ttu-id="26cea-110">Выберите **проект \| Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="26cea-110">Select **Project \| Add Reference**.</span></span>
    2.  <span data-ttu-id="26cea-111">Перейдите на вкладку **com** .</span><span class="sxs-lookup"><span data-stu-id="26cea-111">Select the **COM** tab.</span></span>
    3.  <span data-ttu-id="26cea-112">Выберите **Библиотека типов Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="26cea-112">Select **Active DS Type Library**.</span></span>

4.  <span data-ttu-id="26cea-113">Начните программировать с помощью ADSI.</span><span class="sxs-lookup"><span data-stu-id="26cea-113">Begin programming with ADSI.</span></span>

<span data-ttu-id="26cea-114">Прежде чем начать, войдите в домен Windows.</span><span class="sxs-lookup"><span data-stu-id="26cea-114">Before you begin, log on to a Windows domain.</span></span> <span data-ttu-id="26cea-115">Необходимо иметь разрешение на изменение базы данных Active Directory.</span><span class="sxs-lookup"><span data-stu-id="26cea-115">You must have permission to modify the Active Directory database.</span></span> <span data-ttu-id="26cea-116">По умолчанию эта привилегия есть у администратора.</span><span class="sxs-lookup"><span data-stu-id="26cea-116">By default, the Administrator has this privilege.</span></span>

<span data-ttu-id="26cea-117">**Пример приложения Visual Basic 6,0: изменение FullName и описание пользователя**</span><span class="sxs-lookup"><span data-stu-id="26cea-117">**A Sample Visual Basic 6.0 Application: Modifying FullName and Description for a User**</span></span>

1.  <span data-ttu-id="26cea-118">Выполните описанные выше действия, чтобы создать стандартный исполняемый Visual Basic проект.</span><span class="sxs-lookup"><span data-stu-id="26cea-118">Follow the previous steps to create a standard executable Visual Basic project.</span></span>
2.  <span data-ttu-id="26cea-119">Дважды щелкните форму.</span><span class="sxs-lookup"><span data-stu-id="26cea-119">Double-click the Form.</span></span> <span data-ttu-id="26cea-120">В поле \_ Загрузка формы введите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="26cea-120">In Form\_Load, type the following.</span></span> <span data-ttu-id="26cea-121">Необходимо заменить строку "LDAP://кН = жеффсмис, CN = Users, DC = Fabrikam, DC = com" на значение ADsPath существующего пользователя в контейнере в вашем домене.</span><span class="sxs-lookup"><span data-stu-id="26cea-121">You must replace the "LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com" string with the ADsPath of an existing user in a container in your domain.</span></span> <span data-ttu-id="26cea-122">Создайте тестовую учетную запись пользователя, которую можно изменить для этой цели.</span><span class="sxs-lookup"><span data-stu-id="26cea-122">Create a test user account that can be modified for this purpose.</span></span>
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

    

3.  <span data-ttu-id="26cea-123">Нажмите клавишу **<F5>** , чтобы запустить программу.</span><span class="sxs-lookup"><span data-stu-id="26cea-123">Press **<F5>** to run the program.</span></span>
4.  <span data-ttu-id="26cea-124">Чтобы проверить изменения, используйте средство управления Active Directory пользователи и компьютеры.</span><span class="sxs-lookup"><span data-stu-id="26cea-124">To verify changes, use the Active Directory Users and Computers management tool.</span></span> <span data-ttu-id="26cea-125">Дополнительные сведения об использовании ADSI и Visual Basic см. в разделе [доступ к Active Directory с помощью Visual Basic](accessing-active-directory-using-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="26cea-125">For more information about using ADSI and Visual Basic, see [Accessing Active Directory Using Visual Basic](accessing-active-directory-using-visual-basic.md).</span></span>

 

 




