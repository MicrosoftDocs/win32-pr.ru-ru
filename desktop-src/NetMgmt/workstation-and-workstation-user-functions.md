---
title: Пользовательские функции рабочих станций и рабочих станций
description: Функции рабочей станции управления сетью выполняют задачи администрирования на локальной или удаленной рабочей станции.
ms.assetid: cc400f43-297b-4ff4-8353-b268839c48b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd445746bca51abaa0cd72877bdf03dd4d00d338
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105661771"
---
# <a name="workstation-and-workstation-user-functions"></a><span data-ttu-id="d9c0d-103">Пользовательские функции рабочих станций и рабочих станций</span><span class="sxs-lookup"><span data-stu-id="d9c0d-103">Workstation and Workstation User Functions</span></span>

<span data-ttu-id="d9c0d-104">Функции рабочей станции управления сетью выполняют задачи администрирования на локальной или удаленной рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="d9c0d-104">The network management workstation functions perform administrative tasks on a local or remote workstation.</span></span> <span data-ttu-id="d9c0d-105">Только пользователь или приложение с членством в административной группе на локальном или удаленном сервере может выполнять административные задачи на рабочей станции, чтобы управлять ее работой, доступом пользователей и предоставлением общего доступа к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="d9c0d-105">Only a user or application with admin group membership, on a local or remote server, can perform administrative tasks on a workstation to control its operation, user access, and resource sharing.</span></span> <span data-ttu-id="d9c0d-106">Дополнительные сведения о вызове функций, требующих прав администратора, см. [в разделе Запуск с особыми привилегиями](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="d9c0d-106">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="d9c0d-107">Ниже перечислены функции рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="d9c0d-107">The workstation functions are listed following.</span></span>



| <span data-ttu-id="d9c0d-108">Функция</span><span class="sxs-lookup"><span data-stu-id="d9c0d-108">Function</span></span>                                   | <span data-ttu-id="d9c0d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d9c0d-109">Description</span></span>                                                             |
|--------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="d9c0d-110">**нетвкстажетинфо**</span><span class="sxs-lookup"><span data-stu-id="d9c0d-110">**NetWkstaGetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) | <span data-ttu-id="d9c0d-111">Возвращает сведения об элементах конфигурации для рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="d9c0d-111">Returns information about the configuration elements for a workstation.</span></span> |
| [<span data-ttu-id="d9c0d-112">**нетвкстасетинфо**</span><span class="sxs-lookup"><span data-stu-id="d9c0d-112">**NetWkstaSetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo) | <span data-ttu-id="d9c0d-113">Настраивает рабочую станцию.</span><span class="sxs-lookup"><span data-stu-id="d9c0d-113">Configures a workstation.</span></span>                                               |



 

<span data-ttu-id="d9c0d-114">Функции рабочей станции разрешают доступ к двум дискретным типам сведений о рабочих станциях:</span><span class="sxs-lookup"><span data-stu-id="d9c0d-114">The workstation functions allow access to two discrete types of workstation information:</span></span>

-   <span data-ttu-id="d9c0d-115">Сведения о системе</span><span class="sxs-lookup"><span data-stu-id="d9c0d-115">System information</span></span>
-   <span data-ttu-id="d9c0d-116">Сведения о конкретной платформе</span><span class="sxs-lookup"><span data-stu-id="d9c0d-116">Platform-specific information</span></span>

<span data-ttu-id="d9c0d-117">В каждом типе данные классифицируются по доступу безопасности.</span><span class="sxs-lookup"><span data-stu-id="d9c0d-117">Within each type the data is categorized by security access.</span></span> <span data-ttu-id="d9c0d-118">Доступ к данным, доступным для гостей, является подмножеством данных, доступных пользователю, которые в свою очередь представляют собой подмножество данных, доступных для администрирования.</span><span class="sxs-lookup"><span data-stu-id="d9c0d-118">Data that is guest-accessible is a subset of the data that is user-accessible, which is in turn a subset of the admin-accessible data.</span></span>

<span data-ttu-id="d9c0d-119">Сведения о рабочей станции доступны на следующих уровнях:</span><span class="sxs-lookup"><span data-stu-id="d9c0d-119">Workstation information is available at the following levels:</span></span>

-   [<span data-ttu-id="d9c0d-120">**\_Сведения о вкста \_ 100**</span><span class="sxs-lookup"><span data-stu-id="d9c0d-120">**WKSTA\_INFO\_100**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_100)
-   [<span data-ttu-id="d9c0d-121">**\_Сведения о вкста \_ 101**</span><span class="sxs-lookup"><span data-stu-id="d9c0d-121">**WKSTA\_INFO\_101**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_101)
-   [<span data-ttu-id="d9c0d-122">**\_Сведения о вкста \_ 102**</span><span class="sxs-lookup"><span data-stu-id="d9c0d-122">**WKSTA\_INFO\_102**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_102)

<span data-ttu-id="d9c0d-123">Пользовательские функции рабочей станции управления сетью разрешают доступ к сведениям, относящимся к конкретному пользователю.</span><span class="sxs-lookup"><span data-stu-id="d9c0d-123">The network management workstation user functions allow access to user-specific information.</span></span> <span data-ttu-id="d9c0d-124">Сведения, относящиеся к пользователю, отделены от сведений о рабочей станции, так как на рабочей станции может быть несколько пользователей.</span><span class="sxs-lookup"><span data-stu-id="d9c0d-124">The user-specific information is separated from the workstation information because there can be more than one user on a workstation.</span></span>

<span data-ttu-id="d9c0d-125">Пользовательские функции рабочей станции перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="d9c0d-125">The workstation user functions are listed following.</span></span>



| <span data-ttu-id="d9c0d-126">Функция</span><span class="sxs-lookup"><span data-stu-id="d9c0d-126">Function</span></span>                                           | <span data-ttu-id="d9c0d-127">Описание</span><span class="sxs-lookup"><span data-stu-id="d9c0d-127">Description</span></span>                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9c0d-128">**нетвкстаусеренум**</span><span class="sxs-lookup"><span data-stu-id="d9c0d-128">**NetWkstaUserEnum**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | <span data-ttu-id="d9c0d-129">Выводит сведения обо всех пользователях, которые в данный момент вошли на рабочую станцию.</span><span class="sxs-lookup"><span data-stu-id="d9c0d-129">Lists information about all users currently logged on to the workstation.</span></span>           |
| [<span data-ttu-id="d9c0d-130">**нетвкстаусержетинфо**</span><span class="sxs-lookup"><span data-stu-id="d9c0d-130">**NetWkstaUserGetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | <span data-ttu-id="d9c0d-131">Возвращает сведения об одном пользователе, вошедшем в систему.</span><span class="sxs-lookup"><span data-stu-id="d9c0d-131">Returns information about one currently logged-on user.</span></span>                             |
| [<span data-ttu-id="d9c0d-132">**нетвкстаусерсетинфо**</span><span class="sxs-lookup"><span data-stu-id="d9c0d-132">**NetWkstaUserSetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | <span data-ttu-id="d9c0d-133">Задает сведения об отдельных пользователях для элементов конфигурации рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="d9c0d-133">Sets the user-specific information for the configuration elements of a workstation.</span></span> |



 

<span data-ttu-id="d9c0d-134">Сведения о пользователе рабочей станции доступны на следующих уровнях:</span><span class="sxs-lookup"><span data-stu-id="d9c0d-134">Workstation user information is available at the following levels:</span></span>

-   [<span data-ttu-id="d9c0d-135">**\_ \_ Сведения о пользователе вкста \_ 0**</span><span class="sxs-lookup"><span data-stu-id="d9c0d-135">**WKSTA\_USER\_INFO\_0**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_0)
-   [<span data-ttu-id="d9c0d-136">**\_ \_ Сведения о пользователе вкста \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d9c0d-136">**WKSTA\_USER\_INFO\_1**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1)
-   [<span data-ttu-id="d9c0d-137">**ВКСТА \_ \_ сведения о пользователе \_ 1101**</span><span class="sxs-lookup"><span data-stu-id="d9c0d-137">**WKSTA\_USER\_INFO\_1101**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1101)

 

 