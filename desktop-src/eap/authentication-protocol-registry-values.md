---
title: Значения реестра протокола проверки подлинности
description: Программа установки для DLL-библиотеки EAP может создать следующие значения реестра, приведенные ниже еаптипеид.
ms.assetid: a5f6674d-77c8-4b88-af0e-bb62f84d8a2b
keywords:
- RAS_EAP_VALUENAME_PATH
- RAS_EAP_VALUENAME_FRIENDLY_NAME
- RAS_EAP_VALUENAME_CONFIGUI
- RAS_EAP_VALUENAME_DEFAULT_DATA
- RAS_EAP_VALUENAME_REQUIRE_CONFIGUI
- RAS_EAP_VALUENAME_CONFIG_CLSID
- RAS_EAP_VALUENAME_IDENTITY
- RAS_EAP_VALUENAME_INTERACTIVEUI
- RAS_EAP_VALUENAME_INVOKE_NAMEDLG
- RAS_EAP_VALUENAME_INVOKE_PWDDLG
- RAS_EAP_VALUENAME_ENCRYPTION
- RAS_EAP_VALUENAME_STANDALONE_SUPPORTED
- RAS_EAP_VALUENAME_ROLES_SUPPORTED
- RAS_EAP_VALUENAME_PER_POLICY_CONFIG
- RAS_EAP_VALUENAME_ISTUNNEL_METHOD
- RAS_EAP_VALUENAME_FILTER_INNERMETHODS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8091197c7b0d5c5a208bf3658bbc15284a29ac9e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104069414"
---
# <a name="authentication-protocol-registry-values"></a><span data-ttu-id="ea3b0-119">Значения реестра протокола проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="ea3b0-119">Authentication Protocol Registry Values</span></span>

<span data-ttu-id="ea3b0-120">Программа установки для DLL-библиотеки EAP может создать следующие значения реестра, приведенные ниже **&lt; еаптипеид &gt;**.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-120">The setup software for the EAP DLL may create the following registry values below **&lt;eaptypeid&gt;**.</span></span> <span data-ttu-id="ea3b0-121">Эти значения реестра определены в файле заголовка Расеапиф. h.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-121">These registry values are defined in the Raseapif.h header file.</span></span> <span data-ttu-id="ea3b0-122">Значения **RAS_EAP_VALUENAME_PATH** и **RAS_EAP_VALUENAME_FRIENDLY_NAME** являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-122">The **RAS_EAP_VALUENAME_PATH** and **RAS_EAP_VALUENAME_FRIENDLY_NAME** values are required.</span></span> <span data-ttu-id="ea3b0-123">Программа установки может также создавать и другие ключи и значения.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-123">The setup software may create other keys and values as well.</span></span> <span data-ttu-id="ea3b0-124">Они могут использоваться самим протоколом проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-124">These could be used by the authentication protocol itself.</span></span> <span data-ttu-id="ea3b0-125">Дополнительные сведения и пример настройки реестра см. в разделе [Пример значений реестра](registry-values-example.md).</span><span class="sxs-lookup"><span data-stu-id="ea3b0-125">For more information and an example of registry configuration, see [Registry Values Example](registry-values-example.md).</span></span>

[<span data-ttu-id="ea3b0-126">RAS_EAP_VALUENAME_PATH</span><span class="sxs-lookup"><span data-stu-id="ea3b0-126">RAS_EAP_VALUENAME_PATH</span></span>](#ras_eap_valuename_path)

[<span data-ttu-id="ea3b0-127">RAS_EAP_VALUENAME_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="ea3b0-127">RAS_EAP_VALUENAME_FRIENDLY_NAME</span></span>](#ras_eap_valuename_friendly_name)

[<span data-ttu-id="ea3b0-128">RAS_EAP_VALUENAME_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="ea3b0-128">RAS_EAP_VALUENAME_CONFIGUI</span></span>](#ras_eap_valuename_configui)

[<span data-ttu-id="ea3b0-129">RAS_EAP_VALUENAME_DEFAULT_DATA</span><span class="sxs-lookup"><span data-stu-id="ea3b0-129">RAS_EAP_VALUENAME_DEFAULT_DATA</span></span>](#ras_eap_valuename_default_data)

[<span data-ttu-id="ea3b0-130">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="ea3b0-130">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span></span>](#ras_eap_valuename_require_configui)

[<span data-ttu-id="ea3b0-131">RAS_EAP_VALUENAME_CONFIG_CLSID</span><span class="sxs-lookup"><span data-stu-id="ea3b0-131">RAS_EAP_VALUENAME_CONFIG_CLSID</span></span>](#ras_eap_valuename_config_clsid)

[<span data-ttu-id="ea3b0-132">RAS_EAP_VALUENAME_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="ea3b0-132">RAS_EAP_VALUENAME_IDENTITY</span></span>](#ras_eap_valuename_identity)

<span data-ttu-id="ea3b0-133">[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui) Сохранении</span><span class="sxs-lookup"><span data-stu-id="ea3b0-133">[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui)I</span></span>

[<span data-ttu-id="ea3b0-134">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span><span class="sxs-lookup"><span data-stu-id="ea3b0-134">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span></span>](#ras_eap_valuename_invoke_namedlg)

[<span data-ttu-id="ea3b0-135">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span><span class="sxs-lookup"><span data-stu-id="ea3b0-135">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span></span>](#ras_eap_valuename_invoke_pwddlg)

[<span data-ttu-id="ea3b0-136">RAS_EAP_VALUENAME_ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="ea3b0-136">RAS_EAP_VALUENAME_ENCRYPTION</span></span>](#ras_eap_valuename_encryption)

[<span data-ttu-id="ea3b0-137">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="ea3b0-137">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span></span>](#ras_eap_valuename_standalone_supported)

[<span data-ttu-id="ea3b0-138">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="ea3b0-138">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span></span>](#ras_eap_valuename_roles_supported)

[<span data-ttu-id="ea3b0-139">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="ea3b0-139">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span></span>](#ras_eap_valuename_per_policy_config)

[<span data-ttu-id="ea3b0-140">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span><span class="sxs-lookup"><span data-stu-id="ea3b0-140">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span></span>](#ras_eap_valuename_istunnel_method)

[<span data-ttu-id="ea3b0-141">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span><span class="sxs-lookup"><span data-stu-id="ea3b0-141">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span></span>](#ras_eap_valuename_filter_innermethods)

## <a name="ras_eap_valuename_path"></a><span data-ttu-id="ea3b0-142">RAS_EAP_VALUENAME_PATH</span><span class="sxs-lookup"><span data-stu-id="ea3b0-142">RAS_EAP_VALUENAME_PATH</span></span>

| <span data-ttu-id="ea3b0-143">Константа</span><span class="sxs-lookup"><span data-stu-id="ea3b0-143">Constant value</span></span> | <span data-ttu-id="ea3b0-144">Путь</span><span class="sxs-lookup"><span data-stu-id="ea3b0-144">Path</span></span>                               |
|----------------|------------------------------------|
| <span data-ttu-id="ea3b0-145">Тип</span><span class="sxs-lookup"><span data-stu-id="ea3b0-145">Type</span></span>           | <span data-ttu-id="ea3b0-146">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="ea3b0-146">REG_EXPAND_SZ</span></span>                    |
| <span data-ttu-id="ea3b0-147">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3b0-147">Description</span></span>    | <span data-ttu-id="ea3b0-148">Указывает путь к DLL-библиотеке EAP.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-148">Specifies the path to the EAP DLL.</span></span> |

## <a name="ras_eap_valuename_friendly_name"></a><span data-ttu-id="ea3b0-149">RAS_EAP_VALUENAME_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="ea3b0-149">RAS_EAP_VALUENAME_FRIENDLY_NAME</span></span>

| <span data-ttu-id="ea3b0-150">Константа</span><span class="sxs-lookup"><span data-stu-id="ea3b0-150">Constant value</span></span> | <span data-ttu-id="ea3b0-151">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ea3b0-151">FriendlyName</span></span>                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3b0-152">Тип</span><span class="sxs-lookup"><span data-stu-id="ea3b0-152">Type</span></span>           | <span data-ttu-id="ea3b0-153">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ea3b0-153">REG_SZ</span></span>                                                                                                                                                           |
| <span data-ttu-id="ea3b0-154">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3b0-154">Description</span></span>    | <span data-ttu-id="ea3b0-155">Указывает понятное имя для протокола проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-155">Specifies a friendly name for the authentication protocol.</span></span> <span data-ttu-id="ea3b0-156">Это имя отображается в пользовательском интерфейсе приложения EAP для реализаций удаленного доступа и беспроводной связи.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-156">This name appears in the EAP application user interface for both dial-up and wireless implementations.</span></span> |

## <a name="ras_eap_valuename_configui"></a><span data-ttu-id="ea3b0-157">RAS_EAP_VALUENAME_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="ea3b0-157">RAS_EAP_VALUENAME_CONFIGUI</span></span>

| <span data-ttu-id="ea3b0-158">Константа</span><span class="sxs-lookup"><span data-stu-id="ea3b0-158">Constant value</span></span> | <span data-ttu-id="ea3b0-159">конфигуипас</span><span class="sxs-lookup"><span data-stu-id="ea3b0-159">ConfigUIPath</span></span>                                                                                                                      |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3b0-160">Тип</span><span class="sxs-lookup"><span data-stu-id="ea3b0-160">Type</span></span>           | <span data-ttu-id="ea3b0-161">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="ea3b0-161">REG_EXPAND_SZ</span></span>                                                                                                                   |
| <span data-ttu-id="ea3b0-162">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3b0-162">Description</span></span>    | <span data-ttu-id="ea3b0-163">Указывает путь к библиотеке DLL, реализующей пользовательский интерфейс конфигурации на клиенте, так как этот пользовательский интерфейс предназначен только для клиента.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-163">Specifies the path to the DLL that implements the configuration user interface on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_default_data"></a><span data-ttu-id="ea3b0-164">RAS_EAP_VALUENAME_DEFAULT_DATA</span><span class="sxs-lookup"><span data-stu-id="ea3b0-164">RAS_EAP_VALUENAME_DEFAULT_DATA</span></span>

| <span data-ttu-id="ea3b0-165">Константа</span><span class="sxs-lookup"><span data-stu-id="ea3b0-165">Constant value</span></span> | <span data-ttu-id="ea3b0-166">конфигдата</span><span class="sxs-lookup"><span data-stu-id="ea3b0-166">ConfigData</span></span>                                                            |
|----------------|-----------------------------------------------------------------------|
| <span data-ttu-id="ea3b0-167">Тип</span><span class="sxs-lookup"><span data-stu-id="ea3b0-167">Type</span></span>           | <span data-ttu-id="ea3b0-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="ea3b0-168">REG_BINARY</span></span>                                                           |
| <span data-ttu-id="ea3b0-169">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3b0-169">Description</span></span>    | <span data-ttu-id="ea3b0-170">Указывает данные конфигурации по умолчанию для протокола проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-170">Specifies default configuration data for the authentication protocol.</span></span> |

## <a name="ras_eap_valuename_require_configui"></a><span data-ttu-id="ea3b0-171">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="ea3b0-171">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span></span>

| <span data-ttu-id="ea3b0-172">Константа</span><span class="sxs-lookup"><span data-stu-id="ea3b0-172">Constant value</span></span> | <span data-ttu-id="ea3b0-173">рекуиреконфигуи</span><span class="sxs-lookup"><span data-stu-id="ea3b0-173">RequireConfigUI</span></span>                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3b0-174">Тип</span><span class="sxs-lookup"><span data-stu-id="ea3b0-174">Type</span></span>           | <span data-ttu-id="ea3b0-175">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ea3b0-175">REG_DWORD</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="ea3b0-176">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3b0-176">Description</span></span>    | <span data-ttu-id="ea3b0-177">Указывает, должен ли пользователь предоставлять данные конфигурации в пользовательском интерфейсе клиентского приложения EAP.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-177">Specifies whether the user must provide configuration data in the EAP client application user interface.</span></span> <span data-ttu-id="ea3b0-178">Если это значение равно 1, пользователь не может выйти из пользовательского интерфейса клиентского приложения EAP без предоставления данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-178">If this value is 1, the user is not allowed to exit the EAP client application UI without providing configuration data.</span></span> <span data-ttu-id="ea3b0-179">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-179">The default value is 0.</span></span> |

## <a name="ras_eap_valuename_config_clsid"></a><span data-ttu-id="ea3b0-180">RAS_EAP_VALUENAME_CONFIG_CLSID</span><span class="sxs-lookup"><span data-stu-id="ea3b0-180">RAS_EAP_VALUENAME_CONFIG_CLSID</span></span>

| <span data-ttu-id="ea3b0-181">Константа</span><span class="sxs-lookup"><span data-stu-id="ea3b0-181">Constant value</span></span> | <span data-ttu-id="ea3b0-182">конфигклсид</span><span class="sxs-lookup"><span data-stu-id="ea3b0-182">ConfigCLSID</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="ea3b0-183">Тип</span><span class="sxs-lookup"><span data-stu-id="ea3b0-183">Type</span></span>           | <span data-ttu-id="ea3b0-184">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ea3b0-184">REG_SZ</span></span>                                                       |
| <span data-ttu-id="ea3b0-185">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3b0-185">Description</span></span>    | <span data-ttu-id="ea3b0-186">Указывает идентификатор класса пользовательского интерфейса конфигурации на сервере.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-186">Specifies the class ID of the configuration UI on the server.</span></span> |

## <a name="ras_eap_valuename_identity"></a><span data-ttu-id="ea3b0-187">RAS_EAP_VALUENAME_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="ea3b0-187">RAS_EAP_VALUENAME_IDENTITY</span></span>

| <span data-ttu-id="ea3b0-188">Константа</span><span class="sxs-lookup"><span data-stu-id="ea3b0-188">Constant value</span></span> | <span data-ttu-id="ea3b0-189">идентитипас</span><span class="sxs-lookup"><span data-stu-id="ea3b0-189">IdentityPath</span></span>                                                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3b0-190">Тип</span><span class="sxs-lookup"><span data-stu-id="ea3b0-190">Type</span></span>           | <span data-ttu-id="ea3b0-191">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="ea3b0-191">REG_EXPAND_SZ</span></span>                                                                                                                        |
| <span data-ttu-id="ea3b0-192">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3b0-192">Description</span></span>    | <span data-ttu-id="ea3b0-193">Указывает путь к библиотеке DLL, которая реализует функции для получения удостоверения пользователя на клиенте, так как этот пользовательский интерфейс предназначен только для клиента.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-193">Specifies the path to the DLL that implements functions to obtain the user identity on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_interactiveui"></a><span data-ttu-id="ea3b0-194">RAS_EAP_VALUENAME_INTERACTIVEUI</span><span class="sxs-lookup"><span data-stu-id="ea3b0-194">RAS_EAP_VALUENAME_INTERACTIVEUI</span></span>

| <span data-ttu-id="ea3b0-195">Константа</span><span class="sxs-lookup"><span data-stu-id="ea3b0-195">Constant value</span></span> | <span data-ttu-id="ea3b0-196">интерактивеуипас</span><span class="sxs-lookup"><span data-stu-id="ea3b0-196">InteractiveUIPath</span></span>                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3b0-197">Тип</span><span class="sxs-lookup"><span data-stu-id="ea3b0-197">Type</span></span>           | <span data-ttu-id="ea3b0-198">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="ea3b0-198">REG_EXPAND_SZ</span></span>                                                                                                                 |
| <span data-ttu-id="ea3b0-199">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3b0-199">Description</span></span>    | <span data-ttu-id="ea3b0-200">Указывает путь к библиотеке DLL, которая реализует интерактивный пользовательский интерфейс на клиенте, так как этот пользовательский интерфейс предназначен только для клиента.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-200">Specifies the path to the DLL that implements the interactive user interface on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_invoke_namedlg"></a><span data-ttu-id="ea3b0-201">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span><span class="sxs-lookup"><span data-stu-id="ea3b0-201">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span></span>

| <span data-ttu-id="ea3b0-202">Константа</span><span class="sxs-lookup"><span data-stu-id="ea3b0-202">Constant value</span></span> | <span data-ttu-id="ea3b0-203">инвокеусернамедиалог</span><span class="sxs-lookup"><span data-stu-id="ea3b0-203">InvokeUsernameDialog</span></span>                                                                                                                                                                                   |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3b0-204">Тип</span><span class="sxs-lookup"><span data-stu-id="ea3b0-204">Type</span></span>           | <span data-ttu-id="ea3b0-205">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ea3b0-205">REG_DWORD</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="ea3b0-206">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3b0-206">Description</span></span>    | <span data-ttu-id="ea3b0-207">Указывает, должен ли RAS отображать стандартное диалоговое окно имени пользователя Windows NT или Windows 2000 (значение 1) или вызывать [**расеапжетидентити**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (значение 0).</span><span class="sxs-lookup"><span data-stu-id="ea3b0-207">Specifies whether RAS should display the standard Windows NT/Windows 2000 user name dialog (value of 1) or invoke [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (value of 0).</span></span> <span data-ttu-id="ea3b0-208">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-208">The default value is 1.</span></span> |

## <a name="ras_eap_valuename_invoke_pwddlg"></a><span data-ttu-id="ea3b0-209">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span><span class="sxs-lookup"><span data-stu-id="ea3b0-209">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span></span>

| <span data-ttu-id="ea3b0-210">Константа</span><span class="sxs-lookup"><span data-stu-id="ea3b0-210">Constant value</span></span> | <span data-ttu-id="ea3b0-211">инвокепассворддиалог</span><span class="sxs-lookup"><span data-stu-id="ea3b0-211">InvokePasswordDialog</span></span>                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3b0-212">Тип</span><span class="sxs-lookup"><span data-stu-id="ea3b0-212">Type</span></span>           | <span data-ttu-id="ea3b0-213">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ea3b0-213">REG_DWORD</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="ea3b0-214">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3b0-214">Description</span></span>    | <span data-ttu-id="ea3b0-215">Указывает, должен ли RAS отображать стандартное диалоговое окно пароля Windows NT или Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-215">Specifies whether RAS should display the standard Windows NT/Windows 2000 password dialog.</span></span> <span data-ttu-id="ea3b0-216">Если это значение существует и равно 0, служба RAS не будет отображать диалоговое окно пароля.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-216">If this value exists and is 0, RAS will not display the password dialog.</span></span> <span data-ttu-id="ea3b0-217">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-217">The default value is 1.</span></span> |


## <a name="ras_eap_valuename_encryption"></a><span data-ttu-id="ea3b0-218">RAS_EAP_VALUENAME_ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="ea3b0-218">RAS_EAP_VALUENAME_ENCRYPTION</span></span>

| <span data-ttu-id="ea3b0-219">Константа</span><span class="sxs-lookup"><span data-stu-id="ea3b0-219">Constant value</span></span> | <span data-ttu-id="ea3b0-220">мппинкриптионсуппортед</span><span class="sxs-lookup"><span data-stu-id="ea3b0-220">MPPEEncryptionSupported</span></span>                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3b0-221">Тип</span><span class="sxs-lookup"><span data-stu-id="ea3b0-221">Type</span></span>           | <span data-ttu-id="ea3b0-222">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ea3b0-222">REG_DWORD</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="ea3b0-223">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3b0-223">Description</span></span>    | <span data-ttu-id="ea3b0-224">Если это значение равно 1, протокол проверки подлинности может создавать ключи для шифрования с шифрованием типа "точка — точка" (MPPE).</span><span class="sxs-lookup"><span data-stu-id="ea3b0-224">If this value is 1, the authentication protocol can generate keys for the Microsoft Point-to-Point Encryption (MPPE) style of encryption.</span></span> <span data-ttu-id="ea3b0-225">Возможные значения: 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-225">Possible values are 0 or 1.</span></span> <span data-ttu-id="ea3b0-226">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-226">The default value is 0.</span></span> |

## <a name="ras_eap_valuename_standalone_supported"></a><span data-ttu-id="ea3b0-227">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="ea3b0-227">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span></span>

| <span data-ttu-id="ea3b0-228">Константа</span><span class="sxs-lookup"><span data-stu-id="ea3b0-228">Constant value</span></span> | <span data-ttu-id="ea3b0-229">стандалонесуппортед</span><span class="sxs-lookup"><span data-stu-id="ea3b0-229">StandaloneSupported</span></span>                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3b0-230">Тип</span><span class="sxs-lookup"><span data-stu-id="ea3b0-230">Type</span></span>           | <span data-ttu-id="ea3b0-231">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ea3b0-231">REG_DWORD</span></span>                                                                                                                                                                     |
| <span data-ttu-id="ea3b0-232">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3b0-232">Description</span></span>    | <span data-ttu-id="ea3b0-233">Указывает, поддерживается ли этот протокол проверки подлинности на автономном сервере Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-233">Specifies whether this authentication protocol is supported on a standalone Windows 2000 Server.</span></span> <span data-ttu-id="ea3b0-234">Значение 0 указывает, что протокол EAP не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-234">A value of 0 indicates that the EAP is not supported.</span></span> <span data-ttu-id="ea3b0-235">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-235">The default value is 1.</span></span> |

## <a name="ras_eap_valuename_roles_supported"></a><span data-ttu-id="ea3b0-236">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="ea3b0-236">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span></span>

| <span data-ttu-id="ea3b0-237">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="ea3b0-237">Constant Value</span></span> | <span data-ttu-id="ea3b0-238">ролессуппортед</span><span class="sxs-lookup"><span data-stu-id="ea3b0-238">RolesSupported</span></span>                                                                                                                                                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3b0-239">Тип</span><span class="sxs-lookup"><span data-stu-id="ea3b0-239">Type</span></span>           | <span data-ttu-id="ea3b0-240">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ea3b0-240">REG_DWORD</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="ea3b0-241">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3b0-241">Description</span></span>    | <span data-ttu-id="ea3b0-242">Указывает различные роли, поддерживаемые EAP.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-242">Specifies the various roles the EAP supports.</span></span> <span data-ttu-id="ea3b0-243">Указывает, можно ли использовать на сервере или клиенте, поддерживается ли он для подключений RAS (VPN) или PEAP.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-243">This indicates whether it can be used on a server or a client, whether it is supported for RAS connections (VPN) or PEAP.</span></span> <span data-ttu-id="ea3b0-244">Поведение по умолчанию — отображение метода EAP в протоколе PEAP и в протоколе EAP.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-244">The default behavior is to show the EAP method in PEAP and in EAP.</span></span> |

## <a name="ras_eap_valuename_per_policy_config"></a><span data-ttu-id="ea3b0-245">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="ea3b0-245">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span></span>

| <span data-ttu-id="ea3b0-246">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="ea3b0-246">Constant Value</span></span> | <span data-ttu-id="ea3b0-247">перполициконфиг</span><span class="sxs-lookup"><span data-stu-id="ea3b0-247">PerPolicyConfig</span></span> |
|----------------|-----------------|
| <span data-ttu-id="ea3b0-248">Тип</span><span class="sxs-lookup"><span data-stu-id="ea3b0-248">Type</span></span>           | <span data-ttu-id="ea3b0-249">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ea3b0-249">REG_DWORD</span></span>      |
| <span data-ttu-id="ea3b0-250">Описание</span><span class="sxs-lookup"><span data-stu-id="ea3b0-250">Description</span></span>    |                 |

## <a name="ras_eap_valuename_istunnel_method"></a><span data-ttu-id="ea3b0-251">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span><span class="sxs-lookup"><span data-stu-id="ea3b0-251">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span></span>

<span data-ttu-id="ea3b0-252">Это значение реестра не используется.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-252">This registry value is not in use.</span></span>

## <a name="ras_eap_valuename_filter_innermethods"></a><span data-ttu-id="ea3b0-253">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span><span class="sxs-lookup"><span data-stu-id="ea3b0-253">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span></span>

<span data-ttu-id="ea3b0-254">Это значение реестра не используется.</span><span class="sxs-lookup"><span data-stu-id="ea3b0-254">This registry value is not in use.</span></span>

