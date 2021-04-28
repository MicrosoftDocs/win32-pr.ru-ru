---
description: Дополнительные защита ресурсов Windows по разделам реестра
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Дополнительные защита ресурсов Windows по разделам реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1beeea49f06da182b5ebba38d09227134a6d92c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088782"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a><span data-ttu-id="78dba-103">Дополнительные защита ресурсов Windows по разделам реестра</span><span class="sxs-lookup"><span data-stu-id="78dba-103">Additional Windows Resource Protection on Registry Keys</span></span>

## <a name="platform"></a><span data-ttu-id="78dba-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="78dba-104">Platform</span></span>

<span data-ttu-id="78dba-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="78dba-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="78dba-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78dba-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="78dba-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="78dba-107">Feature Impact</span></span>

<span data-ttu-id="78dba-108">**Серьезность** — средний</span><span class="sxs-lookup"><span data-stu-id="78dba-108">**Severity** - Medium</span></span>  
<span data-ttu-id="78dba-109">**Частота** -низкая</span><span class="sxs-lookup"><span data-stu-id="78dba-109">**Frequency** - Low</span></span>  


## <a name="description"></a><span data-ttu-id="78dba-110">Описание</span><span class="sxs-lookup"><span data-stu-id="78dba-110">Description</span></span>

<span data-ttu-id="78dba-111">Дополнительные системные ресурсы добавили параметры защита ресурсов Windows (WRP) в Windows 7, делая их параметрами только для чтения.</span><span class="sxs-lookup"><span data-stu-id="78dba-111">Additional system resources have added Windows Resource Protection (WRP) settings in Windows 7, making them read-only settings.</span></span> <span data-ttu-id="78dba-112">Подавляющее большинство ресурсов, получивших дополнительную защиту, являются системными ключами сервера COM, хотя некоторые функции имеют дополнительную защиту ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78dba-112">The vast majority of resources that received added protection are system COM server keys, although some features have added targeted resource protection.</span></span> <span data-ttu-id="78dba-113">Корпорация Майкрософт изменила эти ресурсы, чтобы защитить систему и другие приложения от нарушения друг друга и обеспечить согласованную, стабильную платформу, на основе которой приложения могут надежно работать.</span><span class="sxs-lookup"><span data-stu-id="78dba-113">Microsoft changed these resources in order to protect the system and other applications from breaking each other and to provide a consistent, stable platform upon which applications can reliably run.</span></span> <span data-ttu-id="78dba-114">В прошлом приложения могли предоставлять пользовательские файлы и использовать незащищенную регистрацию COM для изменения системы.</span><span class="sxs-lookup"><span data-stu-id="78dba-114">In the past, applications could provide custom files and use the unprotected COM registration to change the system.</span></span> <span data-ttu-id="78dba-115">В случае старых приложений это может понизить уровень среды выполнения системы или изменить интерфейс, на котором другие приложения должны работать правильно.</span><span class="sxs-lookup"><span data-stu-id="78dba-115">In the case of older applications, this can downgrade system runtimes or change the interface upon which other applications needed to work properly.</span></span> <span data-ttu-id="78dba-116">В худшем случае такие установки могут привести к сбою системы или ухудшению его производительности с течением времени.</span><span class="sxs-lookup"><span data-stu-id="78dba-116">In the worst case, such installations could cause system failure or degradation over time.</span></span> <span data-ttu-id="78dba-117">Для обеспечения лучшей работы и более стабильной платформы приложений мы заблокировали эти регистрации, чтобы только обновления Майкрософт могли изменять системные компоненты.</span><span class="sxs-lookup"><span data-stu-id="78dba-117">To provide a better experience and a more stable application platform, we locked down these registrations so that only Microsoft updates could change system components.</span></span>

<span data-ttu-id="78dba-118">Так как большинство ресурсов — это ключи COM, используемые системой, это изменение не повлияет на большинство приложений.</span><span class="sxs-lookup"><span data-stu-id="78dba-118">Since most resources changed are COM keys used by the system, this change will not affect the majority of applications.</span></span> <span data-ttu-id="78dba-119">Хотя мы планируем, чтобы большинство приложений имели более высокий опыт работы с Windows 7 в результате этих изменений, это может негативно повлиять на небольшое подмножество приложений.</span><span class="sxs-lookup"><span data-stu-id="78dba-119">While we expect most applications to have a better experience on Windows 7 as a result of these changes, a small subset of applications may be negatively affected.</span></span> <span data-ttu-id="78dba-120">Уровни совместимости приложений автоматически устраняют проблемы установки, всегда указывая приложению, что оно было успешно изменено, даже если оно не прошло из-за того, что он был защищенным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="78dba-120">The system's application compatibility layers will automatically resolve setup problems by always telling the application that it succeeded in changing a setting, even if it failed due to it being a protected resource.</span></span> <span data-ttu-id="78dba-121">Это предотвращает критические установки приложений, но может вызвать проблемы, если необходимо изменить настройку, чтобы приложение работало правильно.</span><span class="sxs-lookup"><span data-stu-id="78dba-121">This prevents application setups from breaking but may cause problems if the setting needed to be changed in order for the application to function properly.</span></span>

## <a name="manifestation"></a><span data-ttu-id="78dba-122">Проявление</span><span class="sxs-lookup"><span data-stu-id="78dba-122">Manifestation</span></span>

<span data-ttu-id="78dba-123">Приложения могли изменить эти параметры до Windows 7.</span><span class="sxs-lookup"><span data-stu-id="78dba-123">Applications may have modified these settings prior to Windows 7.</span></span> <span data-ttu-id="78dba-124">После установки в Windows 7 приложения могут обнаружить, что некоторые функции больше не работают, поскольку параметры не отражали ожидаемое приложение.</span><span class="sxs-lookup"><span data-stu-id="78dba-124">Upon installing on Windows 7, applications may find certain features no longer work because the settings did not reflect what the application expected.</span></span>

<span data-ttu-id="78dba-125">Существуют два сценария, в которых приложения могут столкнуться с проблемами, связанными с этой дополнительной защитой:</span><span class="sxs-lookup"><span data-stu-id="78dba-125">There are two scenarios in which applications may encounter problems related to this added protection:</span></span>

-   <span data-ttu-id="78dba-126">Приложения, которые могли использовать защищенные параметры в качестве хранилища данных или как редкие или непредвиденные точки расширяемости;</span><span class="sxs-lookup"><span data-stu-id="78dba-126">Applications that may have been using the now-protected settings as a data store or as a rare or unintended extensibility point</span></span>
-   <span data-ttu-id="78dba-127">В редких случаях механизм обнаружения, используемый для определения настроек приложений, может не распознать определенную программу установки, поэтому уровень предотвращения совместимости приложений может быть не применен.</span><span class="sxs-lookup"><span data-stu-id="78dba-127">In rare cases, the detection mechanism used to identify application setups may not recognize a particular setup and so the application compatibility mitigation layer may not be applied</span></span>

## <a name="mitigation"></a><span data-ttu-id="78dba-128">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="78dba-128">Mitigation</span></span>

<span data-ttu-id="78dba-129">Основным способом устранения рисков является уровень совместимости приложений системы, который автоматически применяется к программам установки приложений при обнаружении.</span><span class="sxs-lookup"><span data-stu-id="78dba-129">The primary means of mitigation is the system's application compatibility layer, which is automatically applied to application setups when detected.</span></span> <span data-ttu-id="78dba-130">Можно также вручную применить его к любому приложению, используя вкладку Совместимость в свойствах приложения.</span><span class="sxs-lookup"><span data-stu-id="78dba-130">You can also manually apply it to any application using the compatibility tab in the application's properties.</span></span>

<span data-ttu-id="78dba-131">Этот уровень устраняет проблему, перехватывая операции реестра.</span><span class="sxs-lookup"><span data-stu-id="78dba-131">This layer resolves the problem by intercepting registry operations.</span></span> <span data-ttu-id="78dba-132">В случае, когда приложение пытается изменить параметр только для чтения (WRP), слой всегда возвращает значение Success, даже несмотря на то, что настройка фактически не изменилась.</span><span class="sxs-lookup"><span data-stu-id="78dba-132">In the case where the application was attempting to modify a read-only (WRP) setting, the layer always returns success, even though the setting was not really changed.</span></span> <span data-ttu-id="78dba-133">Для большинства приложений это не приведет к возникновению проблем.</span><span class="sxs-lookup"><span data-stu-id="78dba-133">For most applications, this will cause no problems.</span></span> <span data-ttu-id="78dba-134">Тем не менее существует вероятность того, что приложению требовалось изменить настройку, чтобы обеспечить правильную работу, что является первым сценарием, описанным выше.</span><span class="sxs-lookup"><span data-stu-id="78dba-134">However, there is a possibility that the application needed that setting changed in order to function properly, which is the first scenario described above.</span></span>

## <a name="solution"></a><span data-ttu-id="78dba-135">Решение</span><span class="sxs-lookup"><span data-stu-id="78dba-135">Solution</span></span>

<span data-ttu-id="78dba-136">Для двух указанных выше сценариев:</span><span class="sxs-lookup"><span data-stu-id="78dba-136">For the two scenarios identified above:</span></span>

-   <span data-ttu-id="78dba-137">Если приложению требуется, чтобы ключ был доступен для записи, для работы или использования хранилища данных нет решения, отличного от изменения приложения, чтобы оно больше не записывалось в это место.</span><span class="sxs-lookup"><span data-stu-id="78dba-137">If the application requires the key to be writable in order to function or use the data store, there is no solution other than changing the application so that it no longer writes to that location.</span></span>
-   <span data-ttu-id="78dba-138">Если уровень совместимости не был применен к программе установки, то ошибка установки должна быть обнаружена и предложена для применения и повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="78dba-138">If the compatibility layer was not applied to a setup, the setup failure should be detected and offered to be applied and re-run.</span></span> <span data-ttu-id="78dba-139">Приложения также могут работать в режиме совместимости, в этом случае применяется уровень защиты.</span><span class="sxs-lookup"><span data-stu-id="78dba-139">Applications can also run in compatibility mode, in which case the mitigation layer is always applied.</span></span>

## <a name="compatibility-tests"></a><span data-ttu-id="78dba-140">Тесты на совместимость</span><span class="sxs-lookup"><span data-stu-id="78dba-140">Compatibility Tests</span></span>

<span data-ttu-id="78dba-141">Как определить, применено ли приложение к снижению защиты WRP:</span><span class="sxs-lookup"><span data-stu-id="78dba-141">How to detect if an application had WRP mitigation applied to it:</span></span>

-   <span data-ttu-id="78dba-142">Установщик Windows учитывает WRP; он автоматически игнорирует попытки записи или изменения защищенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="78dba-142">Windows Installer is aware of WRP; it automatically and silently ignores attempts to write or modify a protected resource.</span></span> <span data-ttu-id="78dba-143">Если приложение было установлено с установщик Windows и ведение журнала включено, то для каждой операции записи в реестре будет зарегистрировано предупреждение, которое было пропущено из-за того, что он является ресурсом, защищенным WRP.</span><span class="sxs-lookup"><span data-stu-id="78dba-143">If the application was installed with Windows Installer and logging was enabled, then a warning will be logged for each registry key write operation that was ignored due to its being a WRP-protected resource.</span></span>
-   <span data-ttu-id="78dba-144">API WRP включает СфЦискэйпротектед, который может выполнять запросы, если раздел реестра защищен WRP в текущей системе.</span><span class="sxs-lookup"><span data-stu-id="78dba-144">The WRP API incorporates SfCIsKeyProtected, which can query if a registry key is WRP-protected on the current system.</span></span> <span data-ttu-id="78dba-145">Дополнительные сведения об использовании этого API см. в записи WRP в MSDN.</span><span class="sxs-lookup"><span data-stu-id="78dba-145">See the WRP entry in MSDN in the links below for additional information on using this API.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="78dba-146">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="78dba-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="78dba-147">защита ресурсов Windows</span><span class="sxs-lookup"><span data-stu-id="78dba-147">Windows Resource Protection</span></span>](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
