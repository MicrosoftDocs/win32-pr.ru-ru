---
description: API Центр обновления Windows Agent (WUA) может использоваться пользователем на удаленном компьютере или приложением, которое работает на удаленном компьютере. Однако у удаленного пользователя или приложения должны быть права администратора.
ms.assetid: 15f86590-bed8-4506-916d-43b0bac5db2a
title: Использование агента WUA с удаленного компьютера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb14c019e48d6c36b210633ab9d57dcd157585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692144"
---
# <a name="using-wua-from-a-remote-computer"></a><span data-ttu-id="37046-104">Использование агента WUA с удаленного компьютера</span><span class="sxs-lookup"><span data-stu-id="37046-104">Using WUA From a Remote Computer</span></span>

<span data-ttu-id="37046-105">API Центр обновления Windows Agent (WUA) может использоваться пользователем на удаленном компьютере или приложением, которое работает на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="37046-105">The Windows Update Agent (WUA) API can be used by a user on a remote computer or by an application that is running on a remote computer.</span></span> <span data-ttu-id="37046-106">Однако у удаленного пользователя или приложения должны быть права администратора.</span><span class="sxs-lookup"><span data-stu-id="37046-106">However, the remote user or application must have administrator privileges.</span></span>

<span data-ttu-id="37046-107">В следующем списке содержатся интерфейсы, доступные для удаленных пользователей и приложений.</span><span class="sxs-lookup"><span data-stu-id="37046-107">The following list contains interfaces that are available to remote users and applications:</span></span>

-   [<span data-ttu-id="37046-108">**иупдатесессион**</span><span class="sxs-lookup"><span data-stu-id="37046-108">**IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)
-   [<span data-ttu-id="37046-109">**IUpdateSession2**</span><span class="sxs-lookup"><span data-stu-id="37046-109">**IUpdateSession2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [<span data-ttu-id="37046-110">**иупдатесеарчер**</span><span class="sxs-lookup"><span data-stu-id="37046-110">**IUpdateSearcher**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [<span data-ttu-id="37046-111">**иаутоматикупдатес**</span><span class="sxs-lookup"><span data-stu-id="37046-111">**IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [<span data-ttu-id="37046-112">**исеарчресулт**</span><span class="sxs-lookup"><span data-stu-id="37046-112">**ISearchResult**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)
-   [<span data-ttu-id="37046-113">**иупдатеколлектион**</span><span class="sxs-lookup"><span data-stu-id="37046-113">**IUpdateCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)
-   [<span data-ttu-id="37046-114">**иупдате**</span><span class="sxs-lookup"><span data-stu-id="37046-114">**IUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)
-   [<span data-ttu-id="37046-115">**IUpdate2**</span><span class="sxs-lookup"><span data-stu-id="37046-115">**IUpdate2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdate2)
-   [<span data-ttu-id="37046-116">**ивиндовсдриверупдате**</span><span class="sxs-lookup"><span data-stu-id="37046-116">**IWindowsDriverUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)
-   [<span data-ttu-id="37046-117">**IWindowsDriverUpdate2**</span><span class="sxs-lookup"><span data-stu-id="37046-117">**IWindowsDriverUpdate2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate2)
-   [<span data-ttu-id="37046-118">**иупдатеидентити**</span><span class="sxs-lookup"><span data-stu-id="37046-118">**IUpdateIdentity**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateidentity)
-   [<span data-ttu-id="37046-119">**иимажеинформатион**</span><span class="sxs-lookup"><span data-stu-id="37046-119">**IImageInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iimageinformation)
-   [<span data-ttu-id="37046-120">**иинсталлатионбехавиор**</span><span class="sxs-lookup"><span data-stu-id="37046-120">**IInstallationBehavior**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior)
-   [<span data-ttu-id="37046-121">**истрингколлектион**</span><span class="sxs-lookup"><span data-stu-id="37046-121">**IStringCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection)
-   [<span data-ttu-id="37046-122">**иупдатехисторентриколлектион**</span><span class="sxs-lookup"><span data-stu-id="37046-122">**IUpdateHistoryEntryCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection)
-   [<span data-ttu-id="37046-123">**иупдатехисторентри**</span><span class="sxs-lookup"><span data-stu-id="37046-123">**IUpdateHistoryEntry**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)
-   [<span data-ttu-id="37046-124">**икатегориколлектион**</span><span class="sxs-lookup"><span data-stu-id="37046-124">**ICategoryCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)
-   [<span data-ttu-id="37046-125">**икатегори**</span><span class="sxs-lookup"><span data-stu-id="37046-125">**ICategory**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-icategory)
-   [<span data-ttu-id="37046-126">**иупдатиксцептионколлектион**</span><span class="sxs-lookup"><span data-stu-id="37046-126">**IUpdateExceptionCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)
-   [<span data-ttu-id="37046-127">**иупдатиксцептион**</span><span class="sxs-lookup"><span data-stu-id="37046-127">**IUpdateException**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)
-   [<span data-ttu-id="37046-128">**иупдатедовнлоадконтентколлектион**</span><span class="sxs-lookup"><span data-stu-id="37046-128">**IUpdateDownloadContentCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontentcollection)
-   [<span data-ttu-id="37046-129">**иупдатедовнлоадконтент**</span><span class="sxs-lookup"><span data-stu-id="37046-129">**IUpdateDownloadContent**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontent)
-   [<span data-ttu-id="37046-130">**иупдатесервицеманажер**</span><span class="sxs-lookup"><span data-stu-id="37046-130">**IUpdateServiceManager**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)
-   [<span data-ttu-id="37046-131">**иупдатесервицеколлектион**</span><span class="sxs-lookup"><span data-stu-id="37046-131">**IUpdateServiceCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection)
-   [<span data-ttu-id="37046-132">**иупдатесервице**</span><span class="sxs-lookup"><span data-stu-id="37046-132">**IUpdateService**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)
-   [<span data-ttu-id="37046-133">**ивиндовсупдатеажентинфо**</span><span class="sxs-lookup"><span data-stu-id="37046-133">**IWindowsUpdateAgentInfo**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo)

<span data-ttu-id="37046-134">В следующем списке содержатся интерфейсы и свойства, недоступные для удаленных пользователей и приложений.</span><span class="sxs-lookup"><span data-stu-id="37046-134">The following list contains interfaces and properties that are not available to remote users and applications:</span></span>

-   [<span data-ttu-id="37046-135">**Иупдатесессион:: Креатеупдатедовнлоадер**</span><span class="sxs-lookup"><span data-stu-id="37046-135">**IUpdateSession::CreateUpdateDownloader**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdatedownloader)
-   [<span data-ttu-id="37046-136">**Иупдатесессион:: Креатеупдатеинсталлер**</span><span class="sxs-lookup"><span data-stu-id="37046-136">**IUpdateSession::CreateUpdateInstaller**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdateinstaller)
-   [<span data-ttu-id="37046-137">**Свойство WebProxy объекта Иупдатесессион**</span><span class="sxs-lookup"><span data-stu-id="37046-137">**WebProxy Property of IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-get_webproxy)
-   [<span data-ttu-id="37046-138">**Иупдатесеарчер:: Бегинсеарч**</span><span class="sxs-lookup"><span data-stu-id="37046-138">**IUpdateSearcher::BeginSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)
-   [<span data-ttu-id="37046-139">**Иупдатесеарчер:: Ендсеарч**</span><span class="sxs-lookup"><span data-stu-id="37046-139">**IUpdateSearcher::EndSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)
-   <span data-ttu-id="37046-140">[**Свойство иупдате**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**Hidden** доступно только для чтения, если оно вызывается удаленно.)</span><span class="sxs-lookup"><span data-stu-id="37046-140">[**IsHidden Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**IsHidden** is read-only when it is called remotely.)</span></span>
-   [<span data-ttu-id="37046-141">**Иупдате:: AcceptEula**</span><span class="sxs-lookup"><span data-stu-id="37046-141">**IUpdate::AcceptEula**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
-   [<span data-ttu-id="37046-142">**Иупдате:: Копифромкаче**</span><span class="sxs-lookup"><span data-stu-id="37046-142">**IUpdate::CopyFromCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [<span data-ttu-id="37046-143">**IUpdate2:: Копитокаче**</span><span class="sxs-lookup"><span data-stu-id="37046-143">**IUpdate2::CopyToCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate2-copytocache)
-   [<span data-ttu-id="37046-144">**IWindowsDriverUpdate2:: Копитокаче**</span><span class="sxs-lookup"><span data-stu-id="37046-144">**IWindowsDriverUpdate2::CopyToCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-copytocache)
-   [<span data-ttu-id="37046-145">**Иупдатесервицеманажер:: AddService**</span><span class="sxs-lookup"><span data-stu-id="37046-145">**IUpdateServiceManager::AddService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)
-   [<span data-ttu-id="37046-146">**Иупдатесервицеманажер:: Регистерсервицевисау**</span><span class="sxs-lookup"><span data-stu-id="37046-146">**IUpdateServiceManager::RegisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)
-   [<span data-ttu-id="37046-147">**Иупдатесервицеманажер:: Унрегистерсервицевисау**</span><span class="sxs-lookup"><span data-stu-id="37046-147">**IUpdateServiceManager::UnregisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau)
-   [<span data-ttu-id="37046-148">**Иаутоматикупдате::P Аусе**</span><span class="sxs-lookup"><span data-stu-id="37046-148">**IAutomaticUpdate::Pause**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [<span data-ttu-id="37046-149">**Иаутоматикупдатес:: Resume**</span><span class="sxs-lookup"><span data-stu-id="37046-149">**IAutomaticUpdates::Resume**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [<span data-ttu-id="37046-150">**Иаутоматикупдатес:: Шовсеттингсдиалог**</span><span class="sxs-lookup"><span data-stu-id="37046-150">**IAutomaticUpdates::ShowSettingsDialog**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-showsettingsdialog)
-   [<span data-ttu-id="37046-151">**Свойство Settings объекта Иаутоматикупдатес**</span><span class="sxs-lookup"><span data-stu-id="37046-151">**Settings Property of IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_settings)
-   [<span data-ttu-id="37046-152">**Свойство Сервицеенаблед объекта Иаутоматикупдатес**</span><span class="sxs-lookup"><span data-stu-id="37046-152">**ServiceEnabled Property of IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_serviceenabled)
-   [<span data-ttu-id="37046-153">**Иаутоматикупдатес:: Енаблесервице**</span><span class="sxs-lookup"><span data-stu-id="37046-153">**IAutomaticUpdates::EnableService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [<span data-ttu-id="37046-154">**исистеминформатион**</span><span class="sxs-lookup"><span data-stu-id="37046-154">**ISystemInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)

<span data-ttu-id="37046-155">Следующие порты и исключения должны быть добавлены в параметры брандмауэра Windows для Windows Vista и Windows Server 2008 для удаленного вызова API WUA.</span><span class="sxs-lookup"><span data-stu-id="37046-155">The following ports and exceptions must be added to the Windows firewall settings for Windows Vista and Windows Server 2008 for the WUA API to be called remotely.</span></span>

<dl> <dt>

<span data-ttu-id="37046-156"><span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Исключение 1</span><span class="sxs-lookup"><span data-stu-id="37046-156"><span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Exception 1</span></span>
</dt> <dd> <dl> <dd><span data-ttu-id="37046-157">Локальный порт: 135</span><span class="sxs-lookup"><span data-stu-id="37046-157">Local port: 135</span></span></dd> <dd><span data-ttu-id="37046-158">Удаленный порт: все</span><span class="sxs-lookup"><span data-stu-id="37046-158">Remote port: ALL</span></span></dd> <dd><span data-ttu-id="37046-159">Номер протокола: 6</span><span class="sxs-lookup"><span data-stu-id="37046-159">Protocol number: 6</span></span></dd> <dd><span data-ttu-id="37046-160">Исполняемый файл:% WINDIR% \\ system32 \\svchost.exe</span><span class="sxs-lookup"><span data-stu-id="37046-160">Executable: %windir%\\system32\\svchost.exe</span></span></dd> <dd><span data-ttu-id="37046-161">Служба: RPCSS</span><span class="sxs-lookup"><span data-stu-id="37046-161">Service: rpcss</span></span></dd> <dd><span data-ttu-id="37046-162">Удаленное право: администратор</span><span class="sxs-lookup"><span data-stu-id="37046-162">Remote privilege: Administrator</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="37046-163"><span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Исключение 2</span><span class="sxs-lookup"><span data-stu-id="37046-163"><span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Exception 2</span></span>
</dt> <dd> <dl> <dd><span data-ttu-id="37046-164">Локальный порт: динамический RPC</span><span class="sxs-lookup"><span data-stu-id="37046-164">Local port: Dynamic RPC</span></span></dd> <dd><span data-ttu-id="37046-165">Удаленный порт: все</span><span class="sxs-lookup"><span data-stu-id="37046-165">Remote port: ALL</span></span></dd> <dd><span data-ttu-id="37046-166">Номер протокола: 6</span><span class="sxs-lookup"><span data-stu-id="37046-166">Protocol number: 6</span></span></dd> <dd><span data-ttu-id="37046-167">Исполняемый файл:% WINDIR% \\ system32 \\dllhost.exe</span><span class="sxs-lookup"><span data-stu-id="37046-167">Executable: %windir%\\system32\\dllhost.exe</span></span></dd> <dd><span data-ttu-id="37046-168">Удаленное право: администратор</span><span class="sxs-lookup"><span data-stu-id="37046-168">Remote privilege: Administrator</span></span></dd> </dl> </dd> </dl>

<span data-ttu-id="37046-169">В следующем списке содержатся средства, которые можно использовать для настройки параметров брандмауэра Windows.</span><span class="sxs-lookup"><span data-stu-id="37046-169">The following list contains tools that can be used to configure Windows Firewall settings:</span></span>

-   <span data-ttu-id="37046-170">Брандмауэр Windows с оснасткой «Повышенная безопасность».</span><span class="sxs-lookup"><span data-stu-id="37046-170">Windows Firewall with Advanced Security snap-in</span></span>
-   <span data-ttu-id="37046-171">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="37046-171">Group Policy</span></span>
-   <span data-ttu-id="37046-172">Программа командной строки netsh advfirewall</span><span class="sxs-lookup"><span data-stu-id="37046-172">Netsh advfirewall command-line tool</span></span>

<span data-ttu-id="37046-173">Дополнительные сведения об использовании средств для настройки параметров брандмауэра Windows см. в разделе [Начало работы с брандмауэром Windows в расширенной безопасности](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="37046-173">For more information about how to use tools to configure Windows Firewall settings, see [Getting Started with Windows Firewall with Advanced Security](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).</span></span>

 

 
