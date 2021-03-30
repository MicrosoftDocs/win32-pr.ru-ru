---
title: Настройка Visual C++ 6,0 для разработки с интерфейсом ADSI
description: В этом разделе показано, как настроить C++ в Visual Studio, чтобы можно было разрабатывать приложения ADSI.
ms.assetid: 6f1ab3eb-2e0b-4f3e-b93c-e24c8b3b1a27
ms.tgt_platform: multiple
keywords:
- Настройка C++ для разработки с интерфейсом ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f2350b88402c921d014b0c93756759a1d0f744
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067314"
---
# <a name="setting-up-visual-c-60-for-adsi-development"></a><span data-ttu-id="6629e-104">Настройка Visual C++ 6,0 для разработки с интерфейсом ADSI</span><span class="sxs-lookup"><span data-stu-id="6629e-104">Setting Up Visual C++ 6.0 for ADSI Development</span></span>

<span data-ttu-id="6629e-105">Систему разработки Microsoft Visual C++ 6,0 можно использовать для разработки корпоративных приложений.</span><span class="sxs-lookup"><span data-stu-id="6629e-105">The Microsoft Visual C++ 6.0 development system can be used to develop enterprise applications.</span></span> <span data-ttu-id="6629e-106">Чтобы настроить среду Visual C++ 6,0 для разработки приложения ADSI, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6629e-106">To set up your Visual C++ 6.0 environment to develop an ADSI application, perform the following steps:</span></span>

<span data-ttu-id="6629e-107">**Настройка среды разработки Microsoft Visual C++ 6,0**</span><span class="sxs-lookup"><span data-stu-id="6629e-107">**Setting Up the Microsoft Visual C++ 6.0 Development Environment**</span></span>

1.  <span data-ttu-id="6629e-108">Укажите каталог include и Library.</span><span class="sxs-lookup"><span data-stu-id="6629e-108">Point to the include and library directory.</span></span> <span data-ttu-id="6629e-109">Выберите **Сервис \| Параметры**.</span><span class="sxs-lookup"><span data-stu-id="6629e-109">Select **Tools \| Options**.</span></span> <span data-ttu-id="6629e-110">Перейдите на вкладку **Каталог** и укажите путь к ФАЙЛАМ заголовка ADSI.</span><span class="sxs-lookup"><span data-stu-id="6629e-110">Click the **Directory** tab, and specify the path to the ADSI header files.</span></span>
2.  <span data-ttu-id="6629e-111">Включите в проект файл Активедс. h.</span><span class="sxs-lookup"><span data-stu-id="6629e-111">Include the Activeds.h file in your project.</span></span>
3.  <span data-ttu-id="6629e-112">Добавьте файлы Активедс. lib и Адсиид. lib в входные данные компоновщика для вашего проекта.</span><span class="sxs-lookup"><span data-stu-id="6629e-112">Add the Activeds.lib and Adsiid.lib files to the linker input for your project.</span></span>
4.  <span data-ttu-id="6629e-113">Начните программировать с помощью ADSI.</span><span class="sxs-lookup"><span data-stu-id="6629e-113">Begin programming with ADSI.</span></span>

<span data-ttu-id="6629e-114">Войдите в домен Windows.</span><span class="sxs-lookup"><span data-stu-id="6629e-114">Log on to a Windows domain.</span></span> <span data-ttu-id="6629e-115">Кроме того, необходимо иметь разрешение на изменение данных в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6629e-115">You must also have permission to modify data in Active Directory.</span></span> <span data-ttu-id="6629e-116">По умолчанию эта привилегия есть у администратора.</span><span class="sxs-lookup"><span data-stu-id="6629e-116">By default, the Administrator has this privilege.</span></span> <span data-ttu-id="6629e-117">Чтобы ввести этот пример кода, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="6629e-117">To enter this code example:</span></span>

<span data-ttu-id="6629e-118">**Пример Visual C++ приложения: создание пользователя в домене**</span><span class="sxs-lookup"><span data-stu-id="6629e-118">**A Sample Visual C++ Application: Creating a User in a Domain**</span></span>

1.  <span data-ttu-id="6629e-119">Запустите Visual C++ 6,0.</span><span class="sxs-lookup"><span data-stu-id="6629e-119">Start Visual C++ 6.0.</span></span>
2.  <span data-ttu-id="6629e-120">Создайте автономный исполняемый проект.</span><span class="sxs-lookup"><span data-stu-id="6629e-120">Create a standalone executable project.</span></span> <span data-ttu-id="6629e-121">Это может быть либо MFC, ATL, либо консольное приложение.</span><span class="sxs-lookup"><span data-stu-id="6629e-121">It can be either an MFC, ATL, or Console Application.</span></span>
3.  <span data-ttu-id="6629e-122">Выполните описанные выше действия, чтобы настроить проект.</span><span class="sxs-lookup"><span data-stu-id="6629e-122">Follow the previous steps to set up your project.</span></span>
4.  <span data-ttu-id="6629e-123">Введите следующий пример кода.</span><span class="sxs-lookup"><span data-stu-id="6629e-123">Enter the following code example.</span></span> <span data-ttu-id="6629e-124">Замените строку "LDAP://кН = Users, DC = Fabrikam, DC = com" на значение ADsPath контейнера в вашем домене.</span><span class="sxs-lookup"><span data-stu-id="6629e-124">Replace the "LDAP://CN=users,DC=fabrikam,DC=com" string with the ADsPath of a container in your domain.</span></span> <span data-ttu-id="6629e-125">Необходимо также заменить имя пользователя "жеффсмис" уникальным именем пользователя в домене.</span><span class="sxs-lookup"><span data-stu-id="6629e-125">You should also replace the user name "jeffsmith" with a user name that is unique in your domain.</span></span>

    ```C++
    #include "stdafx.h"
    #include "activeds.h"

    int main(int argc, char* argv[])
    {
        HRESULT hr;
        IADsContainer *pCont;
        IDispatch *pDisp=NULL;
        IADs *pUser;

         // Initialize COM before calling any ADSI functions or interfaces.
         CoInitialize(NULL);

        hr = ADsGetObject( L"LDAP://CN=users,DC=fabrikam,DC=com", 
                                   IID_IADsContainer, 
                                   (void**) &pCont );
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        //-----------------
        // Create a user
        //-----------------
        
        hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=jeffsmith"), &pDisp );
        
        // Release the container object.    
        pCont->Release();
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        hr = pDisp->QueryInterface( IID_IADs, (void**) &pUser );

        // Release the dispatch interface.
        pDisp->Release();

        if ( !SUCCEEDED(hr) )
        {    
            return 0;
        }

        // Commit the object data to the directory.
        pUser->SetInfo();

        // Release the object.
        pUser->Release();

        CoUninitialize();
    }
    ```

    

5.  <span data-ttu-id="6629e-126">Выполните сборку и запуск приложения.</span><span class="sxs-lookup"><span data-stu-id="6629e-126">Build and run the application.</span></span> <span data-ttu-id="6629e-127">Чтобы убедиться, что пользователь создан, используйте средство управления Active Directory пользователи и компьютеры.</span><span class="sxs-lookup"><span data-stu-id="6629e-127">To verify that the user has been created, use the Active Directory Users and Computers management tool.</span></span>

 

 




