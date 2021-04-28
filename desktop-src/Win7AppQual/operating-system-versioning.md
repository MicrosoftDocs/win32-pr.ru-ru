---
description: Управление версиями операционной системы
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Управление версиями операционной системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2b8c60994eaee7a3becfa9acc03fe2c61fb12
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088042"
---
# <a name="operating-system-versioning"></a><span data-ttu-id="fed2b-103">Управление версиями операционной системы</span><span class="sxs-lookup"><span data-stu-id="fed2b-103">Operating System Versioning</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="fed2b-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="fed2b-104">Affected Platforms</span></span>

<span data-ttu-id="fed2b-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="fed2b-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="fed2b-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fed2b-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="fed2b-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="fed2b-107">Feature Impact</span></span>

<span data-ttu-id="fed2b-108">**Серьезность** — высокая</span><span class="sxs-lookup"><span data-stu-id="fed2b-108">**Severity** - High</span></span>  
<span data-ttu-id="fed2b-109">**Частота** — высокая</span><span class="sxs-lookup"><span data-stu-id="fed2b-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="fed2b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="fed2b-110">Description</span></span>

<span data-ttu-id="fed2b-111">Внутренний номер версии для Windows 7 и Windows Server 2008 R2 — 6,1.</span><span class="sxs-lookup"><span data-stu-id="fed2b-111">The internal version number for Windows 7 and Windows Server 2008 R2 is 6.1.</span></span> <span data-ttu-id="fed2b-112">Функция noreturn теперь будет возвращать этот номер версии приложениям при запросе.</span><span class="sxs-lookup"><span data-stu-id="fed2b-112">The GetVersion function will now return this version number to applications when queried.</span></span> <span data-ttu-id="fed2b-113">Это особенно важно для антивирусной программы, резервного копирования, служебных приложений и защиты от копирования.</span><span class="sxs-lookup"><span data-stu-id="fed2b-113">This is especially important for AntiVirus, backup, utility applications, and copy protection.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="fed2b-114">Влияние на манифесты</span><span class="sxs-lookup"><span data-stu-id="fed2b-114">Manifestation of Impact</span></span>

<span data-ttu-id="fed2b-115">Это изменение зависит от конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="fed2b-115">The manifestation of this change is application-specific.</span></span> <span data-ttu-id="fed2b-116">Это означает, что все приложения, специально проверяющие версию операционной системы, получат более высокий номер версии, что может привести к одной или нескольким из следующих ситуаций:</span><span class="sxs-lookup"><span data-stu-id="fed2b-116">This means that any application that specifically checks for the operating system version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="fed2b-117">Возможно, установщики приложений не смогут установить приложение, и приложения могут не запуститься</span><span class="sxs-lookup"><span data-stu-id="fed2b-117">Application installers might be unable to install the application, and applications might be unable to start</span></span>
-   <span data-ttu-id="fed2b-118">Приложения могут стать нестабильными или аварийными</span><span class="sxs-lookup"><span data-stu-id="fed2b-118">Applications might become unstable or crash</span></span>
-   <span data-ttu-id="fed2b-119">Приложения могут создавать сообщения об ошибках, но продолжать работать правильно</span><span class="sxs-lookup"><span data-stu-id="fed2b-119">Applications might generate error messages, but continue to function properly</span></span>

## <a name="mitigation"></a><span data-ttu-id="fed2b-120">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="fed2b-120">Mitigation</span></span>

<span data-ttu-id="fed2b-121">Большинство приложений будут правильно работать в Windows 7 и Windows Server 2008 R2, так как совместимость приложений в Windows 7 и Windows Server 2008 R2 очень высока.</span><span class="sxs-lookup"><span data-stu-id="fed2b-121">Most applications will function properly on Windows 7 and Windows Server 2008 R2 because the application compatibility in Windows 7 and Windows Server 2008 R2 is very high.</span></span> <span data-ttu-id="fed2b-122">Однако Windows 7 и Windows Server 2008 R2 включают представление совместимости для установщиков и приложений, которые проверяют версию операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fed2b-122">However, Windows 7 and Windows Server 2008 R2 include a Compatibility View for installers and applications that check for operating system version.</span></span>

<span data-ttu-id="fed2b-123">Чтобы включить представление "совместимость", пользователи могут щелкнуть правой кнопкой мыши ярлык или исполняемый файл, а затем применить представление совместимости Windows XP с пакетом обновления 2 (SP2) или Windows Vista на вкладке "совместимость". В большинстве случаев это должно обеспечить правильную работу приложения без каких бы то ни было изменений в приложении.</span><span class="sxs-lookup"><span data-stu-id="fed2b-123">To enable the compatibility view, users can right-click the shortcut or the executable file, and then apply the Windows XP SP2 or Windows Vista Compatibility View from the Compatibility tab. In most cases, this should enable the application to operate properly without the need for any changes to the application.</span></span>

<span data-ttu-id="fed2b-124">ИТ-специалисты также могут применить любые исправления совместимости Версионлие с помощью средства администрирования совместимости, которое устанавливается вместе с набором средств для обеспечения совместимости приложений (ACT).</span><span class="sxs-lookup"><span data-stu-id="fed2b-124">IT Professionals can also apply any of the applicable VersionLie compatibility fixes, by using the Compatibility Administrator tool, which installs with the Application Compatibility Toolkit (ACT).</span></span> <span data-ttu-id="fed2b-125">Например, если приложение не работает из-за проверки, но не обнаруживается в Windows XP® с пакетом обновления 2 (SP2), можно применить WinXPSP2VersionLie, чтобы вернуть в приложение соответствующие сведения о номере версии, независимо от фактической версии операционной системы, установленной на компьютере.</span><span class="sxs-lookup"><span data-stu-id="fed2b-125">For example, if an application fails to function because it is checking for, but not finding, the Windows XP® with Service Pack 2 (SP2) version information, the WinXPSP2VersionLie can be applied to return the proper version number information to the application, regardless of the actual operating system version that is running on the computer.</span></span> <span data-ttu-id="fed2b-126">Доступны следующие исправления совместимости Версионлие:</span><span class="sxs-lookup"><span data-stu-id="fed2b-126">The available VersionLie compatibility fixes are:</span></span>

-   <span data-ttu-id="fed2b-127">Win95VersionLie</span><span class="sxs-lookup"><span data-stu-id="fed2b-127">Win95VersionLie</span></span>
-   <span data-ttu-id="fed2b-128">Win98VersionLie</span><span class="sxs-lookup"><span data-stu-id="fed2b-128">Win98VersionLie</span></span>
-   <span data-ttu-id="fed2b-129">WinNT4SP5VersionLie</span><span class="sxs-lookup"><span data-stu-id="fed2b-129">WinNT4SP5VersionLie</span></span>
-   <span data-ttu-id="fed2b-130">Win2000VersionLie</span><span class="sxs-lookup"><span data-stu-id="fed2b-130">Win2000VersionLie</span></span>
-   <span data-ttu-id="fed2b-131">Win2000SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="fed2b-131">Win2000SP1VersionLie</span></span>
-   <span data-ttu-id="fed2b-132">Win2000SP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="fed2b-132">Win2000SP2VersionLie</span></span>
-   <span data-ttu-id="fed2b-133">Win2000SP3VersionLie</span><span class="sxs-lookup"><span data-stu-id="fed2b-133">Win2000SP3VersionLie</span></span>
-   <span data-ttu-id="fed2b-134">винкспверсионлие</span><span class="sxs-lookup"><span data-stu-id="fed2b-134">WinXPVersionLie</span></span>
-   <span data-ttu-id="fed2b-135">WinXPSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="fed2b-135">WinXPSP1VersionLie</span></span>
-   <span data-ttu-id="fed2b-136">WinXPSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="fed2b-136">WinXPSP2VersionLie</span></span>
-   <span data-ttu-id="fed2b-137">вистартмверсионлие</span><span class="sxs-lookup"><span data-stu-id="fed2b-137">VistaRTMVersionLie</span></span>
-   <span data-ttu-id="fed2b-138">VistaSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="fed2b-138">VistaSP1VersionLie</span></span>
-   <span data-ttu-id="fed2b-139">VistaSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="fed2b-139">VistaSP2VersionLie</span></span>
-   <span data-ttu-id="fed2b-140">Win2K3RTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="fed2b-140">Win2K3RTMVersionLie</span></span>
-   <span data-ttu-id="fed2b-141">Win2K3SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="fed2b-141">Win2K3SP1VersionLie</span></span>

## <a name="solution"></a><span data-ttu-id="fed2b-142">Решение</span><span class="sxs-lookup"><span data-stu-id="fed2b-142">Solution</span></span>

<span data-ttu-id="fed2b-143">Как правило, приложения не должны выполнять проверки версий операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fed2b-143">Generally, applications should not perform operating system version checks.</span></span> <span data-ttu-id="fed2b-144">Если приложению требуется определенная функция, предпочтительнее попробовать найти эту функцию и завершить ее только в том случае, если нужная функция отсутствует.</span><span class="sxs-lookup"><span data-stu-id="fed2b-144">If an application needs a specific feature, it is preferable to try to find the feature, and fail only if the needed feature is missing.</span></span> <span data-ttu-id="fed2b-145">Как минимум, приложения должны всегда принимать номера версий, которые больше или равны минимальной поддерживаемой версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fed2b-145">At a minimum, applications should always accept version numbers greater than or equal to the lowest supported version of the operating system.</span></span> <span data-ttu-id="fed2b-146">Исключения должны происходить только при наличии конкретных юридических, бизнес-или системных компонентов.</span><span class="sxs-lookup"><span data-stu-id="fed2b-146">Exceptions should occur only if there is a specific legal, business, or system-component requirement.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="fed2b-147">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="fed2b-147">Links to Other Resources</span></span>

-   [<span data-ttu-id="fed2b-148">Загрузка набора средств для обеспечения совместимости приложений</span><span class="sxs-lookup"><span data-stu-id="fed2b-148">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="fed2b-149">[Известные исправления совместимости, режимы совместимости и сообщения AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="fed2b-149">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>

 

 
