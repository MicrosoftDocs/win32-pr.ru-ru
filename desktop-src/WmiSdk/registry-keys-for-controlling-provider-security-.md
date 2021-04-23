---
description: Для повышения безопасности wmiprvse.exe процесса узла общего поставщика инструментарий управления Windows (WMI) (WMI) были внесены изменения в платформы Windows, которые защищают хост-процесс поставщика с помощью идентификатора безопасности (SID) службы.
ms.assetid: f93ac155-512c-4efa-8168-ca2d56fe6f01
ms.tgt_platform: multiple
title: Разделы и значения реестра для управления безопасностью поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2c7dd990c1a9ebbc1242af5ce4601ce6eb22a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703181"
---
# <a name="registry-keys-and-values-for-controlling-provider-security"></a><span data-ttu-id="89559-103">Разделы и значения реестра для управления безопасностью поставщика</span><span class="sxs-lookup"><span data-stu-id="89559-103">Registry Keys and Values for Controlling Provider Security</span></span>

<span data-ttu-id="89559-104">Для повышения безопасности wmiprvse.exe процесса узла общего поставщика инструментарий управления Windows (WMI) (WMI) были внесены изменения в платформы Windows, которые защищают хост-процесс поставщика с помощью [*идентификатора безопасности (SID) службы*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="89559-104">To enhance the security of the Windows Management Instrumentation (WMI) shared provider host process (wmiprvse.exe), changes were made to Windows platforms that secure the provider host process with a [*service security identifier (SID)*](gloss-s.md).</span></span> <span data-ttu-id="89559-105">Эти изменения посвящены следующим режимам работы для общего узла WMI: безопасный и совместимый.</span><span class="sxs-lookup"><span data-stu-id="89559-105">These changes introduce the following running modes for the WMI shared host: secure and compatible.</span></span>

<span data-ttu-id="89559-106">В этом разделе рассматриваются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="89559-106">The following sections are covered in this topic:</span></span>

-   [<span data-ttu-id="89559-107">Безопасные и совместимые режимы</span><span class="sxs-lookup"><span data-stu-id="89559-107">Secure and Compatible Modes</span></span>](#secure-and-compatible-modes)
-   [<span data-ttu-id="89559-108">Разделы и значения реестра</span><span class="sxs-lookup"><span data-stu-id="89559-108">Registry Keys and Values</span></span>](#registry-keys-and-values)
-   [<span data-ttu-id="89559-109">Настройка поставщика для работы в безопасном или совместимом режиме</span><span class="sxs-lookup"><span data-stu-id="89559-109">Configuring a Provider to Run in Secure or Compatible Mode</span></span>](#configuring-a-provider-to-run-in-secure-or-compatible-mode)

## <a name="secure-and-compatible-modes"></a><span data-ttu-id="89559-110">Безопасные и совместимые режимы</span><span class="sxs-lookup"><span data-stu-id="89559-110">Secure and Compatible Modes</span></span>

<span data-ttu-id="89559-111">Начиная с Windows 7 были добавлены следующие два режима работы для процесса общего узла WMI:</span><span class="sxs-lookup"><span data-stu-id="89559-111">Starting in Windows 7, the following two running modes for the WMI shared host process were added:</span></span>

<dl> <dt>

<span data-ttu-id="89559-112"><span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Безопасный режим</span><span class="sxs-lookup"><span data-stu-id="89559-112"><span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Secure mode</span></span>
</dt> <dd>

<span data-ttu-id="89559-113">Ресурсы хост-процесса поставщика WMI защищены с помощью [*идентификатора безопасности службы*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="89559-113">WMI provider host process resources are secured with a [*service SID*](gloss-s.md).</span></span> <span data-ttu-id="89559-114">Только *идентификатор безопасности службы* имеет разрешения для этих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89559-114">Only the *service SID* has permissions for these resources.</span></span>

</dd> <dt>

<span data-ttu-id="89559-115"><span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Совместимый режим</span><span class="sxs-lookup"><span data-stu-id="89559-115"><span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Compatible mode</span></span>
</dt> <dd>

<span data-ttu-id="89559-116">Процесс узла общего поставщика WMI не защищен с помощью [*идентификатора безопасности службы*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="89559-116">The WMI shared provider host process is not secured with a [*service SID*](gloss-s.md).</span></span> <span data-ttu-id="89559-117">Ведущий процесс поставщика обеспечивает доступ к учетным записям NetworkService или LocalService в зависимости от модели размещения.</span><span class="sxs-lookup"><span data-stu-id="89559-117">The provider host process allows access to the NetworkService or LocalService accounts depending on the hosting model.</span></span> <span data-ttu-id="89559-118">Дополнительные сведения о моделях размещения см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="89559-118">For more information about hosting models, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

</dd> </dl>

<span data-ttu-id="89559-119">**Windows Vista и Windows Server 2008:** Чтобы получить доступ к разделам реестра и значениям для управления безопасными и совместимыми режимами для хостового процесса поставщика, необходимо установить обновление для системы безопасности в [KB 959454](https://support.microsoft.com/kb/959454).</span><span class="sxs-lookup"><span data-stu-id="89559-119">**Windows Vista and Windows Server 2008:** To access the registry keys and values for controlling secure and compatible modes for the provider host process, you must install the security update in [KB 959454](https://support.microsoft.com/kb/959454).</span></span> <span data-ttu-id="89559-120">Дополнительные сведения см. в [бюллетене по безопасности Microsoft MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).</span><span class="sxs-lookup"><span data-stu-id="89559-120">For more information, see the [Microsoft Security Bulletin MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).</span></span>

## <a name="registry-keys-and-values"></a><span data-ttu-id="89559-121">Разделы и значения реестра</span><span class="sxs-lookup"><span data-stu-id="89559-121">Registry Keys and Values</span></span>

<span data-ttu-id="89559-122">Параметры безопасного и совместимого режимов указываются с помощью разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="89559-122">The secure and compatible mode settings are specified through registry keys.</span></span> <span data-ttu-id="89559-123">Разделы реестра для WMI находятся в реестре в разделе **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .</span><span class="sxs-lookup"><span data-stu-id="89559-123">The registry keys for WMI are located in the registry at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\.</span></span>

<span data-ttu-id="89559-124">Для управления поведением поставщиков WMI были добавлены следующие разделы реестра и значение **DWORD** , описанные в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="89559-124">The following registry keys and **DWORD** value described in the following list were added to control the behavior of WMI providers.</span></span>

<dl> <dt>

<span data-ttu-id="89559-125"><span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**секуредхостпровидерс**</span><span class="sxs-lookup"><span data-stu-id="89559-125"><span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**</span></span>
</dt> <dd>

<span data-ttu-id="89559-126">Этот ключ управляет поведением отдельных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="89559-126">This key controls the behavior of individual providers.</span></span> <span data-ttu-id="89559-127">Все поставщики, перечисленные в этом разделе, всегда выполняются в безопасном режиме.</span><span class="sxs-lookup"><span data-stu-id="89559-127">All of the providers that are listed in this key always run in secure mode.</span></span> <span data-ttu-id="89559-128">Все входящие в состав Windows поставщики входящих сообщений перечислены в этом разделе и по умолчанию запускаются в безопасном режиме.</span><span class="sxs-lookup"><span data-stu-id="89559-128">All inbox providers that are shipped with Windows are listed under this key, and are run in secure mode by default.</span></span>

<span data-ttu-id="89559-129">Этот ключ имеет приоритет над поставщиками, перечисленными в ключе **компатиблехостпровидерс** .</span><span class="sxs-lookup"><span data-stu-id="89559-129">This key takes precedence over providers listed in the **CompatibleHostProviders** key.</span></span>

</dd> <dt>

<span data-ttu-id="89559-130"><span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**компатиблехостпровидерс**</span><span class="sxs-lookup"><span data-stu-id="89559-130"><span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**</span></span>
</dt> <dd>

<span data-ttu-id="89559-131">Этот ключ управляет поведением отдельных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="89559-131">This key controls the behavior of individual providers.</span></span> <span data-ttu-id="89559-132">Все поставщики, перечисленные в этом разделе, всегда выполняются в совместимом режиме.</span><span class="sxs-lookup"><span data-stu-id="89559-132">All providers that are listed in this key always run in compatible mode.</span></span> <span data-ttu-id="89559-133">По умолчанию этот ключ пуст.</span><span class="sxs-lookup"><span data-stu-id="89559-133">This key is empty by default.</span></span>

<span data-ttu-id="89559-134">Если поставщик указан как в разделе **секуредхостпровидерс** , так и в ключе **компатиблехостпровидерс** , то поставщик выполняется в безопасном режиме.</span><span class="sxs-lookup"><span data-stu-id="89559-134">If a provider is listed both in the **SecuredHostProviders** key and in the **CompatibleHostProviders** key, the provider is run in secure mode.</span></span>

> [!Note]  
> <span data-ttu-id="89559-135">Ключ **компатиблехостпровидерс** обеспечивает совместимость приложений для сторонних приложений, если для ключа **дефаултсекуредхост** задано значение 1, а поставщику известно, что он не работает в безопасном режиме.</span><span class="sxs-lookup"><span data-stu-id="89559-135">The **CompatibleHostProviders** key provides application compatibility for third-party applications if the **DefaultSecuredHost** key is set to 1 and the provider is known to not function in secure mode.</span></span>

 

</dd> <dt>

<span data-ttu-id="89559-136"><span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**дефаултсекуредхост**</span><span class="sxs-lookup"><span data-stu-id="89559-136"><span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**</span></span>
</dt> <dd>

<span data-ttu-id="89559-137">Значение **DWORD** глобального реестра, определяющее, работают ли все поставщики, не указанные в ключах **секуредхостпровидерс** или **компатиблехостпровидерс** , в безопасном или совместимом режиме.</span><span class="sxs-lookup"><span data-stu-id="89559-137">A global registry **DWORD** value that determines whether all of the providers, which are not listed in the **SecuredHostProviders** or **CompatibleHostProviders** keys, are run in the secure or compatible mode.</span></span> <span data-ttu-id="89559-138">Это значение **DWORD** позволяет администратору выбрать режим, в котором должен работать сторонний поставщик.</span><span class="sxs-lookup"><span data-stu-id="89559-138">This **DWORD** value lets the administrator decide under which mode a third-party provider must run.</span></span> <span data-ttu-id="89559-139">По умолчанию это значение равно нулю, а все сторонние поставщики работают в совместимом режиме.</span><span class="sxs-lookup"><span data-stu-id="89559-139">By default, this value is set to zero and all third-party providers are run in compatible mode.</span></span> <span data-ttu-id="89559-140">Администраторы могут сделать свой компьютер более безопасным по умолчанию, установив значение **дефаултсекуредхост** равным 1.</span><span class="sxs-lookup"><span data-stu-id="89559-140">Administrators can make their computer more secure by default by setting the **DefaultSecuredHost** value to 1.</span></span>

> [!Note]  
> <span data-ttu-id="89559-141">Значение **дефаултсекуредхост** не влияет на другие разделы реестра.</span><span class="sxs-lookup"><span data-stu-id="89559-141">The **DefaultSecuredHost** value does not affect the other registry keys.</span></span> <span data-ttu-id="89559-142">Поставщики, перечисленные в ключе **секуредхостпровидерс** , остаются в безопасном режиме, а те, которые перечислены в ключе **компатиблехостпровидерс** , остаются в совместимом режиме.</span><span class="sxs-lookup"><span data-stu-id="89559-142">The providers that are listed in the **SecuredHostProviders** key remain in secure mode, and the ones that are listed in the **CompatibleHostProviders** key remain in compatible mode.</span></span>

 

<span data-ttu-id="89559-143">Возможны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="89559-143">The following settings are possible:</span></span>

<dl> <dt>

<span data-ttu-id="89559-144"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="89559-144"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="89559-145">Указывает, что поставщики работают в совместимом режиме.</span><span class="sxs-lookup"><span data-stu-id="89559-145">Specifies that providers run in compatible mode.</span></span>

</dd> <dt>

<span data-ttu-id="89559-146"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="89559-146"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="89559-147">Указывает, что поставщики выполняются в безопасном режиме.</span><span class="sxs-lookup"><span data-stu-id="89559-147">Specifies that providers run in secure mode.</span></span>

</dd> </dl> </dd> </dl>

<span data-ttu-id="89559-148">В следующем списке перечислены возможные параметры реестра и связанные режимы работы для поставщика.</span><span class="sxs-lookup"><span data-stu-id="89559-148">The following list lists the possible registry settings and the associated running modes for a provider.</span></span>



| <span data-ttu-id="89559-149">Перечислены в разделе Секуредхостпровидерс</span><span class="sxs-lookup"><span data-stu-id="89559-149">Listed under SecuredHostProviders</span></span> | <span data-ttu-id="89559-150">Перечислены в разделе Компатиблехостпровидерс</span><span class="sxs-lookup"><span data-stu-id="89559-150">Listed under CompatibleHostProviders</span></span> | <span data-ttu-id="89559-151">Параметр Дефаултсекуредхост</span><span class="sxs-lookup"><span data-stu-id="89559-151">DefaultSecuredHost Setting</span></span> | <span data-ttu-id="89559-152">Режим</span><span class="sxs-lookup"><span data-stu-id="89559-152">Mode</span></span>       |
|-----------------------------------|--------------------------------------|----------------------------|------------|
| <span data-ttu-id="89559-153">Нет</span><span class="sxs-lookup"><span data-stu-id="89559-153">No</span></span>                                | <span data-ttu-id="89559-154">Нет</span><span class="sxs-lookup"><span data-stu-id="89559-154">No</span></span>                                   | <span data-ttu-id="89559-155">0</span><span class="sxs-lookup"><span data-stu-id="89559-155">0</span></span>                          | <span data-ttu-id="89559-156">Совместимые</span><span class="sxs-lookup"><span data-stu-id="89559-156">Compatible</span></span> |
| <span data-ttu-id="89559-157">Нет</span><span class="sxs-lookup"><span data-stu-id="89559-157">No</span></span>                                | <span data-ttu-id="89559-158">Да</span><span class="sxs-lookup"><span data-stu-id="89559-158">Yes</span></span>                                  | <span data-ttu-id="89559-159">0</span><span class="sxs-lookup"><span data-stu-id="89559-159">0</span></span>                          | <span data-ttu-id="89559-160">Совместимые</span><span class="sxs-lookup"><span data-stu-id="89559-160">Compatible</span></span> |
| <span data-ttu-id="89559-161">Да</span><span class="sxs-lookup"><span data-stu-id="89559-161">Yes</span></span>                               | <span data-ttu-id="89559-162">Нет</span><span class="sxs-lookup"><span data-stu-id="89559-162">No</span></span>                                   | <span data-ttu-id="89559-163">0</span><span class="sxs-lookup"><span data-stu-id="89559-163">0</span></span>                          | <span data-ttu-id="89559-164">Безопасность</span><span class="sxs-lookup"><span data-stu-id="89559-164">Secure</span></span>     |
| <span data-ttu-id="89559-165">Да</span><span class="sxs-lookup"><span data-stu-id="89559-165">Yes</span></span>                               | <span data-ttu-id="89559-166">Да</span><span class="sxs-lookup"><span data-stu-id="89559-166">Yes</span></span>                                  | <span data-ttu-id="89559-167">0</span><span class="sxs-lookup"><span data-stu-id="89559-167">0</span></span>                          | <span data-ttu-id="89559-168">Безопасность</span><span class="sxs-lookup"><span data-stu-id="89559-168">Secure</span></span>     |
| <span data-ttu-id="89559-169">Нет</span><span class="sxs-lookup"><span data-stu-id="89559-169">No</span></span>                                | <span data-ttu-id="89559-170">Нет</span><span class="sxs-lookup"><span data-stu-id="89559-170">No</span></span>                                   | <span data-ttu-id="89559-171">1</span><span class="sxs-lookup"><span data-stu-id="89559-171">1</span></span>                          | <span data-ttu-id="89559-172">Безопасность</span><span class="sxs-lookup"><span data-stu-id="89559-172">Secure</span></span>     |
| <span data-ttu-id="89559-173">Нет</span><span class="sxs-lookup"><span data-stu-id="89559-173">No</span></span>                                | <span data-ttu-id="89559-174">Да</span><span class="sxs-lookup"><span data-stu-id="89559-174">Yes</span></span>                                  | <span data-ttu-id="89559-175">1</span><span class="sxs-lookup"><span data-stu-id="89559-175">1</span></span>                          | <span data-ttu-id="89559-176">Совместимые</span><span class="sxs-lookup"><span data-stu-id="89559-176">Compatible</span></span> |
| <span data-ttu-id="89559-177">Да</span><span class="sxs-lookup"><span data-stu-id="89559-177">Yes</span></span>                               | <span data-ttu-id="89559-178">Нет</span><span class="sxs-lookup"><span data-stu-id="89559-178">No</span></span>                                   | <span data-ttu-id="89559-179">1</span><span class="sxs-lookup"><span data-stu-id="89559-179">1</span></span>                          | <span data-ttu-id="89559-180">Безопасность</span><span class="sxs-lookup"><span data-stu-id="89559-180">Secure</span></span>     |
| <span data-ttu-id="89559-181">Да</span><span class="sxs-lookup"><span data-stu-id="89559-181">Yes</span></span>                               | <span data-ttu-id="89559-182">Да</span><span class="sxs-lookup"><span data-stu-id="89559-182">Yes</span></span>                                  | <span data-ttu-id="89559-183">1</span><span class="sxs-lookup"><span data-stu-id="89559-183">1</span></span>                          | <span data-ttu-id="89559-184">Безопасность</span><span class="sxs-lookup"><span data-stu-id="89559-184">Secure</span></span>     |



 

## <a name="configuring-a-provider-to-run-in-secure-or-compatible-mode"></a><span data-ttu-id="89559-185">Настройка поставщика для работы в безопасном или совместимом режиме</span><span class="sxs-lookup"><span data-stu-id="89559-185">Configuring a Provider to Run in Secure or Compatible Mode</span></span>

<span data-ttu-id="89559-186">Разделы реестра можно изменить с помощью консоль управления групповыми политиками (GPMC).</span><span class="sxs-lookup"><span data-stu-id="89559-186">The registry keys can be modified using the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="89559-187">Дополнительные сведения см. в разделе [консоль управления групповыми политиками](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span><span class="sxs-lookup"><span data-stu-id="89559-187">For more information, see [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span></span>

<span data-ttu-id="89559-188">В следующих процедурах показано, как управлять безопасными и совместимыми параметрами режима с помощью предпочтений групповой политики.</span><span class="sxs-lookup"><span data-stu-id="89559-188">The following procedures illustrate how to manage secure and compatible mode settings by using group policy preferences.</span></span> <span data-ttu-id="89559-189">Дополнительные сведения о предпочтениях групповой политики см. в разделе [Общие сведения](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11))о параметрах групповая политика.</span><span class="sxs-lookup"><span data-stu-id="89559-189">For more information about group policy preferences, see the [Group Policy Preferences Overview](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).</span></span>

<span data-ttu-id="89559-190">**Добавление поставщика в безопасный или совместимый режим с помощью групповая политика**</span><span class="sxs-lookup"><span data-stu-id="89559-190">**To add a provider to either the secure or compatible mode by using Group Policy**</span></span>

1.  <span data-ttu-id="89559-191">Откройте консоль управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="89559-191">Open the GPMC.</span></span>
2.  <span data-ttu-id="89559-192">Создайте объект групповая политика (GPO).</span><span class="sxs-lookup"><span data-stu-id="89559-192">Create a Group Policy Object (GPO).</span></span>
3.  <span data-ttu-id="89559-193">Измените объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="89559-193">Edit the GPO.</span></span>
4.  <span data-ttu-id="89559-194">Выберите настройки/параметры Windows/реестр.</span><span class="sxs-lookup"><span data-stu-id="89559-194">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="89559-195">Щелкните правой кнопкой мыши и выберите **создать... Реестр**.</span><span class="sxs-lookup"><span data-stu-id="89559-195">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="89559-196">Это действие представляет пользовательский интерфейс, в котором можно ввести данные реестра.</span><span class="sxs-lookup"><span data-stu-id="89559-196">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="89559-197">Выберите команду **создать** .</span><span class="sxs-lookup"><span data-stu-id="89559-197">Select the **Create** command.</span></span>
7.  <span data-ttu-id="89559-198">Выберите следующий путь к разделу реестра:</span><span class="sxs-lookup"><span data-stu-id="89559-198">Select the following registry key path:</span></span>

    <span data-ttu-id="89559-199">**Безопасный режим: hKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **секуредхостпровидерс**</span><span class="sxs-lookup"><span data-stu-id="89559-199">**Secure Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**SecuredHostProviders**</span></span>

    <span data-ttu-id="89559-200">**Совместимый режим: hKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **компатиблехостпровидерс**</span><span class="sxs-lookup"><span data-stu-id="89559-200">**Compatible Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**CompatibleHostProviders**</span></span>

8.  <span data-ttu-id="89559-201">В поле **имя** введите имя поставщика, который требуется добавить в этот ключ.</span><span class="sxs-lookup"><span data-stu-id="89559-201">In the **name** field, enter the name of the provider you want to add to this key.</span></span> <span data-ttu-id="89559-202">Имя поставщика должно иметь следующий формат: <namespace> : <\_ \_ релпас>.</span><span class="sxs-lookup"><span data-stu-id="89559-202">The provider name must be in the following format: <namespace>:<\_\_RELPATH>.</span></span> <span data-ttu-id="89559-203">Например, root \\ CIMV2: \_ \_ win32provider. Name = "мипровидер".</span><span class="sxs-lookup"><span data-stu-id="89559-203">For example, root\\cimv2:\_\_win32provider.name="MyProvider".</span></span>
9.  <span data-ttu-id="89559-204">В поле **данных** введите 0.</span><span class="sxs-lookup"><span data-stu-id="89559-204">In the **data** field, enter 0.</span></span>
10. <span data-ttu-id="89559-205">Щелкните ОК.</span><span class="sxs-lookup"><span data-stu-id="89559-205">Click OK.</span></span>

<span data-ttu-id="89559-206">**Удаление поставщика из безопасного или совместимого режима с помощью групповая политика**</span><span class="sxs-lookup"><span data-stu-id="89559-206">**To remove a provider from either the secure or compatible mode by using Group Policy**</span></span>

1.  <span data-ttu-id="89559-207">Откройте консоль управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="89559-207">Open the GPMC.</span></span>
2.  <span data-ttu-id="89559-208">Создайте объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="89559-208">Create a GPO.</span></span>
3.  <span data-ttu-id="89559-209">Измените объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="89559-209">Edit the GPO.</span></span>
4.  <span data-ttu-id="89559-210">Выберите настройки/параметры Windows/реестр.</span><span class="sxs-lookup"><span data-stu-id="89559-210">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="89559-211">Щелкните правой кнопкой мыши и выберите **создать... Реестр**.</span><span class="sxs-lookup"><span data-stu-id="89559-211">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="89559-212">Это действие представляет пользовательский интерфейс, в котором можно ввести данные реестра.</span><span class="sxs-lookup"><span data-stu-id="89559-212">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="89559-213">Выберите команду **Удалить** .</span><span class="sxs-lookup"><span data-stu-id="89559-213">Select the **Remove** command.</span></span>
7.  <span data-ttu-id="89559-214">Выберите следующий путь к разделу реестра:</span><span class="sxs-lookup"><span data-stu-id="89559-214">Select the following registry key path:</span></span>

    <span data-ttu-id="89559-215">**Безопасный режим: hKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **секуредхостпровидерс**</span><span class="sxs-lookup"><span data-stu-id="89559-215">**Secure Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**SecuredHostProviders**</span></span>

    <span data-ttu-id="89559-216">**Совместимый режим: hKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **компатиблехостпровидерс**</span><span class="sxs-lookup"><span data-stu-id="89559-216">**Compatible Mode:  HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**CompatibleHostProviders**</span></span>

8.  <span data-ttu-id="89559-217">В поле **имя** введите имя поставщика, который вы хотите удалить из этого ключа.</span><span class="sxs-lookup"><span data-stu-id="89559-217">In the **name** field, enter the name of the provider you want to remove from this key.</span></span>
9.  <span data-ttu-id="89559-218">В поле **данных** введите 0.</span><span class="sxs-lookup"><span data-stu-id="89559-218">In the **data** field, enter 0.</span></span>
10. <span data-ttu-id="89559-219">Щелкните ОК.</span><span class="sxs-lookup"><span data-stu-id="89559-219">Click OK.</span></span>

<span data-ttu-id="89559-220">Следующая процедура предоставляет сведения о том, как изменить поведение поставщиков, не перечисленных в ключах **секуредхостпровидерс** или **компатиблехостпровидерс** .</span><span class="sxs-lookup"><span data-stu-id="89559-220">The following procedure provides details about how to modify the behavior of providers that are not listed in either the **SecuredHostProviders** or **CompatibleHostProviders** keys.</span></span>

<span data-ttu-id="89559-221">**Изменение значения по умолчанию для ключа Дефаултсекуредхост с помощью групповая политика**</span><span class="sxs-lookup"><span data-stu-id="89559-221">**To change the default value of the DefaultSecuredHost key by using Group Policy**</span></span>

1.  <span data-ttu-id="89559-222">Откройте консоль управления групповыми политиками.</span><span class="sxs-lookup"><span data-stu-id="89559-222">Open the GPMC.</span></span>
2.  <span data-ttu-id="89559-223">Создайте объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="89559-223">Create a GPO.</span></span>
3.  <span data-ttu-id="89559-224">Измените объект групповой политики.</span><span class="sxs-lookup"><span data-stu-id="89559-224">Edit the GPO.</span></span>
4.  <span data-ttu-id="89559-225">Выберите настройки/параметры Windows/реестр.</span><span class="sxs-lookup"><span data-stu-id="89559-225">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="89559-226">Щелкните правой кнопкой мыши и выберите **создать... Реестр**.</span><span class="sxs-lookup"><span data-stu-id="89559-226">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="89559-227">Это действие представляет пользовательский интерфейс, в котором можно ввести данные реестра.</span><span class="sxs-lookup"><span data-stu-id="89559-227">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="89559-228">Выберите команду **Обновить** .</span><span class="sxs-lookup"><span data-stu-id="89559-228">Select the **Update** command.</span></span>
7.  <span data-ttu-id="89559-229">Выберите следующий путь к разделу реестра: **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="89559-229">Select the following registry key path: **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**.</span></span>
8.  <span data-ttu-id="89559-230">В поле **имя** введите **дефаултсекуредхост**.</span><span class="sxs-lookup"><span data-stu-id="89559-230">In the **name** field, enter **DefaultSecuredHost**.</span></span>
9.  <span data-ttu-id="89559-231">В поле **данные** введите 0 для совместимого режима или 1 для безопасного режима.</span><span class="sxs-lookup"><span data-stu-id="89559-231">In the **data** field, enter 0 for compatible mode or 1 for secure mode.</span></span>
10. <span data-ttu-id="89559-232">Щелкните ОК.</span><span class="sxs-lookup"><span data-stu-id="89559-232">Click OK.</span></span>

 

 
