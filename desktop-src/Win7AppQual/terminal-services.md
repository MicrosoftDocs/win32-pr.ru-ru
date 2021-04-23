---
description: .
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Службы удаленных рабочих столов (Windows 7 и Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46bd39785526b11ac2e4c0ede26bbb9971aadc9a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105713352"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="e4379-103">Службы удаленных рабочих столов (Windows 7 и Windows Server 2008 R2 Application Quality Cookbook)</span><span class="sxs-lookup"><span data-stu-id="e4379-103">Remote Desktop Services (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="e4379-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="e4379-104">Affected Platforms</span></span>

<span data-ttu-id="e4379-105">**Серверы** — windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e4379-105">**Servers** – Windows Server 2008 \| Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="e4379-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e4379-106">Description</span></span>

<span data-ttu-id="e4379-107">Службы удаленных рабочих столов (прежнее название — службы терминалов) позволяет нескольким пользователям одновременно получить доступ к Windows Server, чтобы предоставить приложениям и службам хостинга данные с помощью технологии виртуализации презентаций Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e4379-107">Remote Desktop Services (formerly known as Terminal Services) allows multiple concurrent users to access Windows Server in order to provide application and data hosting services using Microsoft "Presentation Virtualization" technology.</span></span>

<span data-ttu-id="e4379-108">Хотя большинство 32-разрядных и 64-разрядных приложений работают так же, как в Windows службы удаленных рабочих столов, некоторые другие не выполняются должным образом из-за разницы в платформе (Многопользовательская среда, одновременный доступ нескольких пользователей и т. д.).</span><span class="sxs-lookup"><span data-stu-id="e4379-108">While most 32-bit and 64-bit applications run as is on Windows Remote Desktop Services, several others do not perform as expected due to the difference in the platform (multi-user environment, concurrent access by multiple users, and so on).</span></span>

<span data-ttu-id="e4379-109">Дополнительные сведения о качестве качества приложения см. в техническом документе *готовность приложений для служб терминалов* .</span><span class="sxs-lookup"><span data-stu-id="e4379-109">For further information regarding application quality, please read the *Application Readiness for Terminal Services* white paper.</span></span> <span data-ttu-id="e4379-110">Посетите страницу службы удаленных рабочих столов продукта и веб-сайты TechNet для служб терминалов дополнительные сведения о службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="e4379-110">Visit the Remote Desktop Services product page and the TS TechNet websites learn more about Remote Desktop Services.</span></span> <span data-ttu-id="e4379-111">Чтобы узнать больше о разработке приложений для службы удаленных рабочих столов, ознакомьтесь с *рекомендациями по программированию служб терминалов*.</span><span class="sxs-lookup"><span data-stu-id="e4379-111">To learn more about developing applications for Remote Desktop Services, review the *Terminal Services Programming Guidelines*.</span></span> <span data-ttu-id="e4379-112">(Эти ресурсы могут быть недоступны в некоторых языках и странах или регионах.)</span><span class="sxs-lookup"><span data-stu-id="e4379-112">(These resources may not be available in some languages and countries/regions.)</span></span>

## <a name="manifestation-of-impacts-and-their-mitigations"></a><span data-ttu-id="e4379-113">Проявление последствий и их устранение</span><span class="sxs-lookup"><span data-stu-id="e4379-113">Manifestation of Impacts and Their Mitigations</span></span>

<span data-ttu-id="e4379-114">Три изменения в Windows 7 влияют на работу приложений на службы удаленных рабочих столов:</span><span class="sxs-lookup"><span data-stu-id="e4379-114">Three changes in Windows 7 affect applications on Remote Desktop Services:</span></span>

-   <span data-ttu-id="e4379-115">Windows Server 2008 R2 — только 64-разрядная версия</span><span class="sxs-lookup"><span data-stu-id="e4379-115">Windows Server 2008 R2 is 64-bit only</span></span>
-   <span data-ttu-id="e4379-116">Виртуализация IP для каждого сеанса</span><span class="sxs-lookup"><span data-stu-id="e4379-116">Per-session IP Virtualization</span></span>
-   <span data-ttu-id="e4379-117">Развертывания на основе MSI — пользовательские ключи</span><span class="sxs-lookup"><span data-stu-id="e4379-117">MSI-based deployments – User-specific keys</span></span>

<span data-ttu-id="e4379-118">**64-разрядная версия только Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e4379-118">**64-bit Only Windows Server 2008 R2**</span></span>

<span data-ttu-id="e4379-119">Приложения, написанные для 32-разрядного сервера, работают в режиме WoW, а не изначально на Windows Server 2008 R2 или, следовательно, на службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="e4379-119">Applications written for 32-bit server will run in WoW mode and not natively on the Windows Server 2008 R2 or, hence, on Remote Desktop Services.</span></span> <span data-ttu-id="e4379-120">Дополнительные сведения см. в разделе только Windows 7 64-bit.</span><span class="sxs-lookup"><span data-stu-id="e4379-120">See the Windows 7 64-Bit Only topic for details.</span></span>

<span data-ttu-id="e4379-121">*Устранение рисков для 64-разрядных ОС Windows Server 2008 R2*</span><span class="sxs-lookup"><span data-stu-id="e4379-121">*Mitigations for 64-bit only Windows Server 2008 R2*</span></span>

<span data-ttu-id="e4379-122">Большинство приложений, написанных для 32-разрядной версии, продолжают работать как обычно в режиме WoW.</span><span class="sxs-lookup"><span data-stu-id="e4379-122">Most applications written for 32-bit will continue to work as normal in WoW mode.</span></span> <span data-ttu-id="e4379-123">Все новые приложения, написанные для Windows 7 службы удаленных рабочих столов, должны разрабатываться и тестироваться для развертывания на 64-разрядных платформах.</span><span class="sxs-lookup"><span data-stu-id="e4379-123">Any new applications written for Windows 7 Remote Desktop Services should be developed and tested for deployment on 64-bit platforms.</span></span>

<span data-ttu-id="e4379-124">**Виртуализация IP-адресов**</span><span class="sxs-lookup"><span data-stu-id="e4379-124">**IP Virtualization**</span></span>

<span data-ttu-id="e4379-125">IP-виртуализация удаленных рабочих столов позволяет пользователю назначать IP-адреса подключениям к удаленному рабочему столу отдельно для каждого сеанса или для каждой программы:</span><span class="sxs-lookup"><span data-stu-id="e4379-125">Remote Desktop IP Virtualization allows the user to assign IP addresses to remote desktop connections on a per-session or per-program basis:</span></span>

-   <span data-ttu-id="e4379-126">При назначении IP-адресов отдельно для каждого сеанса все приложения будут использовать IP-адрес сеанса.</span><span class="sxs-lookup"><span data-stu-id="e4379-126">If you assign IP addresses on a per-session basis, all of the applications will use the session IP address.</span></span>
-   <span data-ttu-id="e4379-127">Если IP-адреса назначаются отдельно для каждой программы, то только указанные приложения будут использовать IP-адрес сеанса, а остальные приложения в этом сеансе не будут затронуты.</span><span class="sxs-lookup"><span data-stu-id="e4379-127">If you assign IP addresses on a per-program basis, only the specified applications will use the session IP address and the remaining applications in the session will not be affected.</span></span>
-   <span data-ttu-id="e4379-128">При назначении IP-адресов нескольким программам они будут совместно использовать IP-адрес сеанса.</span><span class="sxs-lookup"><span data-stu-id="e4379-128">If you assign IP addresses for multiple programs, they will share a session IP address.</span></span>
-   <span data-ttu-id="e4379-129">Если на компьютере установлено несколько сетевых адаптеров, необходимо также выбрать один из них для IP-виртуализация удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="e4379-129">If you have more than one network adapter on the computer, you must also choose one of them for Remote Desktop IP Virtualization.</span></span>

<span data-ttu-id="e4379-130">*Устранение рисков для виртуализации IP*</span><span class="sxs-lookup"><span data-stu-id="e4379-130">*Mitigations for IP Virtualization*</span></span>

<span data-ttu-id="e4379-131">Некоторым программам требуется уникальный IP-адрес для каждого экземпляра приложения.</span><span class="sxs-lookup"><span data-stu-id="e4379-131">Some programs require a unique IP address for each instance of the application.</span></span> <span data-ttu-id="e4379-132">До выхода Windows Server 2008 R2 каждый сеанс на сервере удаленных рабочих столов совместно с одним и тем же IP-адресом, что приводит к проблемам совместимости этих приложений.</span><span class="sxs-lookup"><span data-stu-id="e4379-132">Prior to Windows Server 2008 R2, every session on a remote desktop server shared the same IP address, resulting in compatibility issues for these applications.</span></span> <span data-ttu-id="e4379-133">IP-виртуализация удаленных рабочих столов позволяет запускать эти приложения на сервере удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="e4379-133">Remote Desktop IP Virtualization allows these applications to run on a Remote Desktop Server.</span></span>

<span data-ttu-id="e4379-134">**Развертывания на основе MSI**</span><span class="sxs-lookup"><span data-stu-id="e4379-134">**MSI-based Deployments**</span></span>

<span data-ttu-id="e4379-135">Совместимость служб удаленных рабочих столов Microsoft Installer — это новая функция, входящая в состав службы удаленных рабочих столов в Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="e4379-135">Microsoft Installer RDS Compatibility is a new feature included with Remote Desktop Services in Windows Server 2008 R2.</span></span> <span data-ttu-id="e4379-136">При использовании службы удаленных рабочих столов в Windows Server 2008 R2 установки приложений на уровне пользователей помещаются в очередь сервера удаленный рабочий стол и затем обрабатываются установщиком Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e4379-136">With Remote Desktop Services in Windows Server 2008 R2, per-user application installations are queued by the Remote Desktop Server and then handled by the Microsoft Installer.</span></span>

<span data-ttu-id="e4379-137">В Windows Server 2008 R2 можно установить программу на удаленный рабочий стол сервере точно так же, как при установке программы на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e4379-137">In Windows Server 2008 R2, you can install a program on the Remote Desktop Server just as you would install the program on a local desktop.</span></span> <span data-ttu-id="e4379-138">Однако обязательно установите программу для всех пользователей и установите все компоненты программы локально на удаленный рабочий стол сервере.</span><span class="sxs-lookup"><span data-stu-id="e4379-138">Ensure, however, that you install the program for all users and install all components of the program locally on the Remote Desktop Server.</span></span>

<span data-ttu-id="e4379-139">*Устранение рисков для развертываний на основе MSI*</span><span class="sxs-lookup"><span data-stu-id="e4379-139">*Mitigations for MSI based Deployments*</span></span>

<span data-ttu-id="e4379-140">До выхода версии Windows Server 2008 R2 службы удаленных рабочих столов Windows поддерживала только одну установщик Windowsную установку за раз.</span><span class="sxs-lookup"><span data-stu-id="e4379-140">Prior to the Windows Server 2008 R2 version of Remote Desktop Services, Windows supported only one Windows Installer installation at a time.</span></span> <span data-ttu-id="e4379-141">Для приложений, требующих конфигурации для каждого пользователя, например Microsoft Office слово, администратору необходимо предварительно установить приложение, а разработчикам приложений требовалось протестировать эти приложения как на клиенте удаленного рабочего стола, так и на узле сеансов удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="e4379-141">For applications that required per-user configurations, such as Microsoft Office Word, an administrator needed to pre-install the application, and application developers needed to test these applications on both the remote desktop client and the Remote Desktop Session Host.</span></span> <span data-ttu-id="e4379-142">Установщик Windows Совместимость RDS позволяет идентифицировать и устанавливать недостающие конфигурации для каждого пользователя одновременно для нескольких пользователей и делает установку приложения на удаленный рабочий стол сервере, аналогичном на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e4379-142">Windows Installer RDS Compatibility feature allows identifying and installing missing per-user configurations for multiple users simultaneously and makes the application installation experience on Remote Desktop Server similar to that on a local desktop.</span></span>

<span data-ttu-id="e4379-143">**Windows Server 2008 R2 с включенной ролью [службы удаленных рабочих столов](../termserv/terminal-services-portal.md) :** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e4379-143">**Windows Server 2008 R2 with the [Remote Desktop Services](../termserv/terminal-services-portal.md) role enabled:** Not supported.</span></span> <span data-ttu-id="e4379-144">Если роль [службы удаленных рабочих столов](../termserv/terminal-services-portal.md) включена, то установка нескольких пакетов с помощью [таблицы мсиембеддедчаинер](../msi/msiembeddedchainer-table.md) завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e4379-144">A multiple package installation using the [MsiEmbeddedChainer table](../msi/msiembeddedchainer-table.md) fails if the [Remote Desktop Services](../termserv/terminal-services-portal.md) role is enabled.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="e4379-145">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="e4379-145">Links to Other Resources</span></span>

-   [<span data-ttu-id="e4379-146">Рекомендации по программированию служб терминалов</span><span class="sxs-lookup"><span data-stu-id="e4379-146">Terminal Services Programming Guidelines</span></span>](../termserv/terminal-services-programming-guidelines.md)
-   [<span data-ttu-id="e4379-147">Домашняя страница продукта служб терминалов</span><span class="sxs-lookup"><span data-stu-id="e4379-147">Terminal Services product home page</span></span>](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [<span data-ttu-id="e4379-148">Технический документ «готовность приложений для служб терминалов»</span><span class="sxs-lookup"><span data-stu-id="e4379-148">Application Readiness for Terminal Services white paper</span></span>](/collaborate/connect-redirect)

> [!Note]  
> <span data-ttu-id="e4379-149">Эти ресурсы могут быть недоступны в некоторых языках и странах или регионах.</span><span class="sxs-lookup"><span data-stu-id="e4379-149">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
