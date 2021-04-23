---
description: Интерфейс Иаутоматикупдатессеттингс определяет следующие свойства.
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: Свойства Иаутоматикупдатессеттингс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2463fdc69fc93960ee45c0003a65894eaaf7399
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991179"
---
# <a name="iautomaticupdatessettings-properties"></a><span data-ttu-id="3fb39-103">Свойства Иаутоматикупдатессеттингс</span><span class="sxs-lookup"><span data-stu-id="3fb39-103">IAutomaticUpdatesSettings Properties</span></span>

<span data-ttu-id="3fb39-104">Интерфейс [**иаутоматикупдатессеттингс**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3fb39-104">The [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) interface defines the following properties.</span></span>



| <span data-ttu-id="3fb39-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="3fb39-105">Property</span></span>                                                                                 | <span data-ttu-id="3fb39-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3fb39-106">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fb39-107">**нотификатионлевел**</span><span class="sxs-lookup"><span data-stu-id="3fb39-107">**NotificationLevel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | <span data-ttu-id="3fb39-108">Возвращает и задает, как пользователи получают уведомления о событиях автоматического обновления.</span><span class="sxs-lookup"><span data-stu-id="3fb39-108">Gets and sets how users are notified about Automatic Update events.</span></span>                              |
| [<span data-ttu-id="3fb39-109">**Доступно**</span><span class="sxs-lookup"><span data-stu-id="3fb39-109">**ReadOnly**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | <span data-ttu-id="3fb39-110">Возвращает логическое значение, указывающее, доступны ли параметры автоматического обновления только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3fb39-110">Gets a Boolean value that indicates whether the Automatic Update settings are read-only.</span></span>         |
| [<span data-ttu-id="3fb39-111">**Обязательно**</span><span class="sxs-lookup"><span data-stu-id="3fb39-111">**Required**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | <span data-ttu-id="3fb39-112">Возвращает логическое значение, указывающее, требует ли групповая политика службы автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="3fb39-112">Gets a Boolean value that indicates whether Group Policy requires the Automatic Updates service.</span></span> |
| [<span data-ttu-id="3fb39-113">**счедулединсталлатиондай**</span><span class="sxs-lookup"><span data-stu-id="3fb39-113">**ScheduledInstallationDay**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | <span data-ttu-id="3fb39-114">Возвращает и задает дни недели, в которые автоматическое обновление устанавливает или удаляет обновления.</span><span class="sxs-lookup"><span data-stu-id="3fb39-114">Gets and sets the days of the week on which Automatic Updates installs or uninstalls updates.</span></span>    |
| [<span data-ttu-id="3fb39-115">**счедулединсталлатионтиме**</span><span class="sxs-lookup"><span data-stu-id="3fb39-115">**ScheduledInstallationTime**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | <span data-ttu-id="3fb39-116">Возвращает и задает время, когда автоматическое обновление устанавливает или удаляет обновления.</span><span class="sxs-lookup"><span data-stu-id="3fb39-116">Gets and sets the time at which Automatic Updates installs or uninstalls updates.</span></span>                |



 

> [!Note]  
> <span data-ttu-id="3fb39-117">Windows 8, Windows 8.1, Windows Server 2012 и Windows Server 2012 R2 предоставляют только ограниченную поддержку [**счедулединсталлатиондай**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) и [**счедулединсталлатионтиме**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span><span class="sxs-lookup"><span data-stu-id="3fb39-117">Windows 8, Windows 8.1, Windows Server 2012, and Windows Server 2012 R2 provide only limited support for [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) and [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span></span> <span data-ttu-id="3fb39-118">Если компьютер был настроен с помощью групповая политика для использования запланированного дня установки и времени, свойства **счедулединсталлатиондай** и **счедулединсталлатионтиме** возвращают этот запланированный день и время.</span><span class="sxs-lookup"><span data-stu-id="3fb39-118">If the computer has been configured through Group Policy to use a scheduled installation day and time, the **ScheduledInstallationDay** and **ScheduledInstallationTime** properties return this scheduled day and time.</span></span> <span data-ttu-id="3fb39-119">Если компьютер не был настроен с помощью групповая политика таким образом, свойства **счедулединсталлатиондай** и **счедулединсталлатионтиме** возвращают значения по умолчанию и ненадежные.</span><span class="sxs-lookup"><span data-stu-id="3fb39-119">If the computer hasn't been configured through Group Policy in this way, the **ScheduledInstallationDay** and **ScheduledInstallationTime** properties return default and unreliable values.</span></span> <span data-ttu-id="3fb39-120">Если вы попытаетесь изменить запланированный день установки и время для этих операционных систем, то **счедулединсталлатиондай** и **счедулединсталлатионтиме** будут успешно работать, но не будут действовать.</span><span class="sxs-lookup"><span data-stu-id="3fb39-120">If you try to modify the scheduled installation day and time on these operating systems, **ScheduledInstallationDay** and **ScheduledInstallationTime** appear to succeed but have no effect.</span></span>

 

 

 



