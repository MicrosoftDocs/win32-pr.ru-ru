---
description: Когда WUA обнаруживает, что вызывающий объект не имеет разрешения на доступ к интерфейсу, методу или свойству, возвращается значение HRESULT E \_ ACCESSDENIED.
ms.assetid: 4535ce8d-c329-4335-8b0a-8f63c22f111d
title: Защита интерфейсов, методов и свойств в API-интерфейсе WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6680f616e1ca0596aba04edf4f7ddf7615e0c7f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692472"
---
# <a name="securing-interfaces-methods-and-properties-in-the-wua-api"></a><span data-ttu-id="4f984-103">Защита интерфейсов, методов и свойств в API-интерфейсе WUA</span><span class="sxs-lookup"><span data-stu-id="4f984-103">Securing Interfaces, Methods, and Properties in the WUA API</span></span>

<span data-ttu-id="4f984-104">Некоторые интерфейсы, методы и свойства агента Центр обновления Windows (WUA) доступны только вызывающим объектам, принадлежащим следующим группам безопасности Windows:</span><span class="sxs-lookup"><span data-stu-id="4f984-104">Some interfaces, methods, and properties of Windows Update Agent (WUA) are accessible only to callers who belong to the following Windows security groups:</span></span>

-   <span data-ttu-id="4f984-105">Администратор</span><span class="sxs-lookup"><span data-stu-id="4f984-105">Administrator</span></span>
-   <span data-ttu-id="4f984-106">Пользователь</span><span class="sxs-lookup"><span data-stu-id="4f984-106">User</span></span>
-   <span data-ttu-id="4f984-107">Опытный пользователь</span><span class="sxs-lookup"><span data-stu-id="4f984-107">Power User</span></span>

<span data-ttu-id="4f984-108">Когда WUA обнаруживает, что вызывающий объект не имеет разрешения на доступ к интерфейсу, методу или свойству, возвращается значение **HRESULT** E \_ ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="4f984-108">When WUA detects that a caller does not have permission to access an interface, method, or property, the **HRESULT** E\_ACCESSDENIED is returned.</span></span>

<span data-ttu-id="4f984-109">Для групп безопасности администратора, пользователя и опытного пользователя доступны следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="4f984-109">The following interfaces are available to the Administrator, User, and Power User security groups:</span></span>

-   [<span data-ttu-id="4f984-110">**иаутоматикупдатес**</span><span class="sxs-lookup"><span data-stu-id="4f984-110">**IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [<span data-ttu-id="4f984-111">**иаутоматикупдатессеттингс**</span><span class="sxs-lookup"><span data-stu-id="4f984-111">**IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)
-   [<span data-ttu-id="4f984-112">**IAutomaticUpdatesSettings2**</span><span class="sxs-lookup"><span data-stu-id="4f984-112">**IAutomaticUpdatesSettings2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings2)
-   [<span data-ttu-id="4f984-113">**исистеминформатион**</span><span class="sxs-lookup"><span data-stu-id="4f984-113">**ISystemInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)
-   [<span data-ttu-id="4f984-114">**иупдатесеарчер**</span><span class="sxs-lookup"><span data-stu-id="4f984-114">**IUpdateSearcher**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   <span data-ttu-id="4f984-115">[**Иупдатесессион**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) и [ **IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)</span><span class="sxs-lookup"><span data-stu-id="4f984-115">[**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) and [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)</span></span>

> [!Note]  
> <span data-ttu-id="4f984-116">Если выполняются следующие условия, поиск завершается ошибкой:</span><span class="sxs-lookup"><span data-stu-id="4f984-116">If the following conditions are true, a search fails:</span></span>
>
> -   <span data-ttu-id="4f984-117">Пользователь, не являющийся администратором, задает для [**Свойства UserLocale интерфейса IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) языковой стандарт, соответствующий языку, который не установлен на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4f984-117">A user who is not an administrator sets the [**UserLocale property of the IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) interface to a locale that corresponds to a language that is not installed on the computer.</span></span>
> -   <span data-ttu-id="4f984-118">Поиск использует объект Упдатесеарч, созданный из объекта UpdateSession.</span><span class="sxs-lookup"><span data-stu-id="4f984-118">The search uses an UpdateSearch object created from the UpdateSession object.</span></span>

 

<span data-ttu-id="4f984-119">Следующие интерфейсы и методы загрузки доступны для групп "Администраторы" и "Опытные пользователи":</span><span class="sxs-lookup"><span data-stu-id="4f984-119">The following download interfaces and methods are available to the Administrator and Power User groups:</span></span>

-   [<span data-ttu-id="4f984-120">**иупдатедовнлоадер**</span><span class="sxs-lookup"><span data-stu-id="4f984-120">**IUpdateDownloader**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)
-   [<span data-ttu-id="4f984-121">**Иупдате:: Копифромкаче**</span><span class="sxs-lookup"><span data-stu-id="4f984-121">**IUpdate::CopyFromCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [<span data-ttu-id="4f984-122">**IAutomaticUpdatesSettings2:: Чеккпермиссион**</span><span class="sxs-lookup"><span data-stu-id="4f984-122">**IAutomaticUpdatesSettings2::CheckPermission**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)
    > [!Note]  
    > <span data-ttu-id="4f984-123">Администраторы, пользователи и опытные пользователи могут вызывать [**IAutomaticUpdatesSettings2:: чеккпермиссион**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).</span><span class="sxs-lookup"><span data-stu-id="4f984-123">Administrators, users, and power users can call [**IAutomaticUpdatesSettings2::CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).</span></span>

     

<span data-ttu-id="4f984-124">Следующие интерфейсы, методы и свойства установки доступны для групп администраторов:</span><span class="sxs-lookup"><span data-stu-id="4f984-124">The following installation interfaces, methods, and properties are available to the Administrator groups:</span></span>

-   [<span data-ttu-id="4f984-125">**Иаутоматикупдатес::P Аусе**</span><span class="sxs-lookup"><span data-stu-id="4f984-125">**IAutomaticUpdates::Pause**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [<span data-ttu-id="4f984-126">**Иаутоматикупдатес:: Resume**</span><span class="sxs-lookup"><span data-stu-id="4f984-126">**IAutomaticUpdates::Resume**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [<span data-ttu-id="4f984-127">**Иаутоматикупдатес:: Енаблесервице**</span><span class="sxs-lookup"><span data-stu-id="4f984-127">**IAutomaticUpdates::EnableService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [<span data-ttu-id="4f984-128">**иупдатеинсталлер**</span><span class="sxs-lookup"><span data-stu-id="4f984-128">**IUpdateInstaller**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)
-   [<span data-ttu-id="4f984-129">**Свойство Hidden объекта Иупдате**</span><span class="sxs-lookup"><span data-stu-id="4f984-129">**IsHidden Property of IUpdate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)
    > [!Note]  
    > <span data-ttu-id="4f984-130">Администраторы, пользователи и опытные пользователи могут извлекать значения [**свойства Hidden объекта иупдате**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden).</span><span class="sxs-lookup"><span data-stu-id="4f984-130">Administrators, users, and power users can retrieve the values of the [**IsHidden Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden).</span></span> <span data-ttu-id="4f984-131">Тем не менее, значения могут быть заданы только администраторам и опытным пользователям.</span><span class="sxs-lookup"><span data-stu-id="4f984-131">However, only administrators and power users can set the values.</span></span>

     

-   [<span data-ttu-id="4f984-132">**Иупдате:: AcceptEula**</span><span class="sxs-lookup"><span data-stu-id="4f984-132">**IUpdate::AcceptEula**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
    > [!Note]  
    > <span data-ttu-id="4f984-133">Администраторы и опытные пользователи могут вызывать [**метод AcceptEula иупдате**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).</span><span class="sxs-lookup"><span data-stu-id="4f984-133">Administrators and power users can call the [**AcceptEula method of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).</span></span>

     

-   [<span data-ttu-id="4f984-134">**Иаутоматикупдатессеттингс:: Save**</span><span class="sxs-lookup"><span data-stu-id="4f984-134">**IAutomaticUpdatesSettings::Save**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)
-   [<span data-ttu-id="4f984-135">**Свойство Нотификатионлевел объекта Иаутоматикупдатессеттингс**</span><span class="sxs-lookup"><span data-stu-id="4f984-135">**NotificationLevel Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)
    > [!Note]  
    > <span data-ttu-id="4f984-136">Администраторы, пользователи и опытные пользователи могут извлекать значения [**Свойства нотификатионлевел объекта иаутоматикупдатессеттингс**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel).</span><span class="sxs-lookup"><span data-stu-id="4f984-136">Administrators, users, and power users can retrieve the values of the [**NotificationLevel Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel).</span></span> <span data-ttu-id="4f984-137">Однако значения могут быть заданы только администраторами.</span><span class="sxs-lookup"><span data-stu-id="4f984-137">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="4f984-138">**Свойство Счедулединсталлатиондай объекта Иаутоматикупдатессеттингс**</span><span class="sxs-lookup"><span data-stu-id="4f984-138">**ScheduledInstallationDay Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)
    > [!Note]  
    > <span data-ttu-id="4f984-139">Администраторы, пользователи и опытные пользователи могут извлекать значения [**Свойства счедулединсталлатиондай объекта иаутоматикупдатессеттингс**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday).</span><span class="sxs-lookup"><span data-stu-id="4f984-139">Administrators, users, and power users can retrieve the values of the [**ScheduledInstallationDay Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday).</span></span> <span data-ttu-id="4f984-140">Однако значения могут быть заданы только администраторами.</span><span class="sxs-lookup"><span data-stu-id="4f984-140">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="4f984-141">**Свойство Счедулединсталлатионтиме объекта Иаутоматикупдатессеттингс**</span><span class="sxs-lookup"><span data-stu-id="4f984-141">**ScheduledInstallationTime Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)
    > [!Note]  
    > <span data-ttu-id="4f984-142">Администраторы, пользователи и опытные пользователи могут извлекать значения [**Свойства счедулединсталлатионтиме объекта иаутоматикупдатессеттингс**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span><span class="sxs-lookup"><span data-stu-id="4f984-142">Administrators, users, and power users can retrieve the values of the [**ScheduledInstallationTime Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span></span> <span data-ttu-id="4f984-143">Однако значения могут быть заданы только администраторами.</span><span class="sxs-lookup"><span data-stu-id="4f984-143">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="4f984-144">**Свойство Инклудерекоммендедупдатес объекта IAutomaticUpdatesSettings2**</span><span class="sxs-lookup"><span data-stu-id="4f984-144">**IncludeRecommendedUpdates Property of IAutomaticUpdatesSettings2**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)
    > [!Note]  
    > <span data-ttu-id="4f984-145">Администраторы, пользователи и опытные пользователи могут извлекать значения [**Свойства инклудерекоммендедупдатес объекта IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates).</span><span class="sxs-lookup"><span data-stu-id="4f984-145">Administrators, users, and power users can retrieve the values of the [**IncludeRecommendedUpdates Property of IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates).</span></span> <span data-ttu-id="4f984-146">Однако значения могут быть заданы только администраторами.</span><span class="sxs-lookup"><span data-stu-id="4f984-146">However, only administrators can set the values.</span></span>

     

 

 



