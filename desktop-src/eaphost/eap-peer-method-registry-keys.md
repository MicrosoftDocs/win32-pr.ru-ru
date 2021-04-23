---
title: Значения реестра для метода однорангового узла EAP
description: Сведения о конкретных значениях реестра, необходимых для методов соединения EAP. Просмотрите список значений реестра и просмотрите дополнительные доступные ресурсы.
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796260a25f824ffe52ada7cdfadfb7a25f05d491
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339284"
---
# <a name="eap-peer-method-registry-values"></a><span data-ttu-id="3903a-104">Значения реестра для метода однорангового узла EAP</span><span class="sxs-lookup"><span data-stu-id="3903a-104">EAP Peer Method Registry Values</span></span>

<span data-ttu-id="3903a-105">Для методов соединения EAP требуются определенные значения реестра.</span><span class="sxs-lookup"><span data-stu-id="3903a-105">Specific registry values are required for EAP peer methods.</span></span>

## <a name="eap-peer-method-dll-paths"></a><span data-ttu-id="3903a-106">Пути к библиотеке DLL однорангового метода EAP</span><span class="sxs-lookup"><span data-stu-id="3903a-106">EAP Peer Method DLL Paths</span></span>

<span data-ttu-id="3903a-107">Следующий путь задает расположение реестра для обычных библиотек DLL метода однорангового узла EAP.</span><span class="sxs-lookup"><span data-stu-id="3903a-107">The following path specifies the registry location for regular EAP peer method DLLs.</span></span>

<span data-ttu-id="3903a-108">**HKLM \\ System \\ CCS \\ Services \\ \\ методы EAPHost \\ *&lt; аусорид &gt;* \\ \* &lt; еаптипеид&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="3903a-108">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="3903a-109">Например, путь регистрации установки метода EAP по адресу **аусорид** "311" (указывающий, что "Microsoft" является автором) и **еаптипеид** "40", выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="3903a-109">For example, an EAP method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author) and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="3903a-110">**HKLM \\ System \\ CCS \\ Services \\ \\ методы EAPHost \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="3903a-110">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\40**</span></span>

<span data-ttu-id="3903a-111">Следующий путь задает расположение реестра для расширенных библиотек DLL методов EAP.</span><span class="sxs-lookup"><span data-stu-id="3903a-111">The following path specifies the registry location for extended EAP method DLLs.</span></span>

> [!Note]  
> <span data-ttu-id="3903a-112">Расширенные библиотеки DLL методов EAP поддерживаются в Windows Vista с пакетом обновления 1 (SP1) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="3903a-112">Extended EAP method DLLs are supported in Windows Vista with Service Pack 1 (SP1) or later.</span></span>

 

<span data-ttu-id="3903a-113">**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ Methods \\ *&lt; аусорид &gt;* \\ 254 \\ *&lt; VendorID &gt;* \\ \* &lt; еаптипеид&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="3903a-113">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\254\\*&lt;VendorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="3903a-114">Например, путь регистрации установки метода EAP по адресу **аусорид** "311" (указывающий на то, что "Microsoft" является автором), **ид поставщика** "311" и **еаптипеид** "40", выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="3903a-114">For example, an EAP method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author), a **VendorId** of "311", and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="3903a-115">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ methods \\ 311 \\ 254 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="3903a-115">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\254\\311\\40**</span></span>

> [!Note]  
> <span data-ttu-id="3903a-116">Дополнительные сведения о выделении типов методов EAP см. в разделе 6,2 статьи [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span><span class="sxs-lookup"><span data-stu-id="3903a-116">For more information on the allocation of EAP method types, see section 6.2 of [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span></span>

 

## <a name="registry-values"></a><span data-ttu-id="3903a-117">Значения реестра</span><span class="sxs-lookup"><span data-stu-id="3903a-117">Registry Values</span></span>

<span data-ttu-id="3903a-118">Требуются следующие значения реестра однорангового метода EAPHost.</span><span class="sxs-lookup"><span data-stu-id="3903a-118">The following EAPHost peer method registry values are required.</span></span>

-   [<span data-ttu-id="3903a-119">пирдллпас</span><span class="sxs-lookup"><span data-stu-id="3903a-119">PeerDllPath</span></span>](#peerdllpath)
-   [<span data-ttu-id="3903a-120">пирфриендлинаме</span><span class="sxs-lookup"><span data-stu-id="3903a-120">PeerFriendlyName</span></span>](#peerfriendlyname)
-   [<span data-ttu-id="3903a-121">пиринвокепассворддиалог</span><span class="sxs-lookup"><span data-stu-id="3903a-121">PeerInvokePasswordDialog</span></span>](#peerinvokepassworddialog)
-   [<span data-ttu-id="3903a-122">пиринвокеусернамедиалог</span><span class="sxs-lookup"><span data-stu-id="3903a-122">PeerInvokeUsernameDialog</span></span>](#peerinvokeusernamedialog)

<span data-ttu-id="3903a-123">Рекомендуется использовать следующие значения реестра однорангового метода AP.</span><span class="sxs-lookup"><span data-stu-id="3903a-123">The following AP peer method registry values are recommended.</span></span>

-   [<span data-ttu-id="3903a-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="3903a-124">Properties</span></span>](#properties)

<span data-ttu-id="3903a-125">Следующие значения реестра однорангового метода AP являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="3903a-125">The following AP peer method registry values are optional.</span></span>

-   [<span data-ttu-id="3903a-126">пирконфигуипас</span><span class="sxs-lookup"><span data-stu-id="3903a-126">PeerConfigUIPath</span></span>](#peerconfiguipath)
-   [<span data-ttu-id="3903a-127">пиридентитипас</span><span class="sxs-lookup"><span data-stu-id="3903a-127">PeerIdentityPath</span></span>](#peeridentitypath)
-   [<span data-ttu-id="3903a-128">пиринтерактивеуипас</span><span class="sxs-lookup"><span data-stu-id="3903a-128">PeerInteractiveUIPath</span></span>](#peerinteractiveuipath)
-   [<span data-ttu-id="3903a-129">пиррекуиреконфигуи</span><span class="sxs-lookup"><span data-stu-id="3903a-129">PeerRequireConfigUI</span></span>](#peerrequireconfigui)

### <a name="peerconfiguipath"></a><span data-ttu-id="3903a-130">пирконфигуипас</span><span class="sxs-lookup"><span data-stu-id="3903a-130">PeerConfigUIPath</span></span>



| <span data-ttu-id="3903a-131">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="3903a-131">Constant Value</span></span> | <span data-ttu-id="3903a-132">пирконфигуипас</span><span class="sxs-lookup"><span data-stu-id="3903a-132">PeerConfigUIPath</span></span>                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3903a-133">Тип</span><span class="sxs-lookup"><span data-stu-id="3903a-133">Type</span></span>           | <span data-ttu-id="3903a-134">\_распаковать \_ SZ</span><span class="sxs-lookup"><span data-stu-id="3903a-134">REG\_EXPAND\_SZ</span></span>                                                                                                                                        |
| <span data-ttu-id="3903a-135">Описание</span><span class="sxs-lookup"><span data-stu-id="3903a-135">Description</span></span>    | <span data-ttu-id="3903a-136">Путь к библиотеке DLL, содержащей реализацию диалогового окна настройки пользователя.</span><span class="sxs-lookup"><span data-stu-id="3903a-136">The path to the DLL that contains the implementation of the user configuration dialog.</span></span> <span data-ttu-id="3903a-137">Например,% SystemRoot% \\ system32 \\ &lt; имя \_ DLL. \_ &gt; DLL.</span><span class="sxs-lookup"><span data-stu-id="3903a-137">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerdllpath"></a><span data-ttu-id="3903a-138">пирдллпас</span><span class="sxs-lookup"><span data-stu-id="3903a-138">PeerDllPath</span></span>



| <span data-ttu-id="3903a-139">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="3903a-139">Constant Value</span></span> | <span data-ttu-id="3903a-140">пирдллпас</span><span class="sxs-lookup"><span data-stu-id="3903a-140">PeerDllPath</span></span>                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3903a-141">Тип</span><span class="sxs-lookup"><span data-stu-id="3903a-141">Type</span></span>           | <span data-ttu-id="3903a-142">\_распаковать \_ SZ</span><span class="sxs-lookup"><span data-stu-id="3903a-142">REG\_EXPAND\_SZ</span></span>                                                                                 |
| <span data-ttu-id="3903a-143">Описание</span><span class="sxs-lookup"><span data-stu-id="3903a-143">Description</span></span>    | <span data-ttu-id="3903a-144">Путь к DLL метода EAP.</span><span class="sxs-lookup"><span data-stu-id="3903a-144">The path to the EAP method DLL.</span></span> <span data-ttu-id="3903a-145">Например,% SystemRoot% \\ system32 \\ &lt; имя \_ DLL. \_ &gt; DLL.</span><span class="sxs-lookup"><span data-stu-id="3903a-145">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerfriendlyname"></a><span data-ttu-id="3903a-146">пирфриендлинаме</span><span class="sxs-lookup"><span data-stu-id="3903a-146">PeerFriendlyName</span></span>



| <span data-ttu-id="3903a-147">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="3903a-147">Constant Value</span></span> | <span data-ttu-id="3903a-148">пирфриендлинаме</span><span class="sxs-lookup"><span data-stu-id="3903a-148">PeerFriendlyName</span></span>                                                     |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="3903a-149">Тип</span><span class="sxs-lookup"><span data-stu-id="3903a-149">Type</span></span>           | <span data-ttu-id="3903a-150">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="3903a-150">REG\_SZ</span></span>                                                              |
| <span data-ttu-id="3903a-151">Описание</span><span class="sxs-lookup"><span data-stu-id="3903a-151">Description</span></span>    | <span data-ttu-id="3903a-152">Строка, содержащая понятное (отображаемое) имя метода EAP.</span><span class="sxs-lookup"><span data-stu-id="3903a-152">String that contains the friendly (display) name for the EAP method.</span></span> |



 

### <a name="peeridentitypath"></a><span data-ttu-id="3903a-153">пиридентитипас</span><span class="sxs-lookup"><span data-stu-id="3903a-153">PeerIdentityPath</span></span>



| <span data-ttu-id="3903a-154">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="3903a-154">Constant Value</span></span> | <span data-ttu-id="3903a-155">пиридентитипас</span><span class="sxs-lookup"><span data-stu-id="3903a-155">PeerIdentityPath</span></span>                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3903a-156">Тип</span><span class="sxs-lookup"><span data-stu-id="3903a-156">Type</span></span>           | <span data-ttu-id="3903a-157">\_распаковать \_ SZ</span><span class="sxs-lookup"><span data-stu-id="3903a-157">REG\_EXPAND\_SZ</span></span>                                                                                                                                      |
| <span data-ttu-id="3903a-158">Описание</span><span class="sxs-lookup"><span data-stu-id="3903a-158">Description</span></span>    | <span data-ttu-id="3903a-159">Путь к библиотеке DLL, содержащей реализацию функций идентификации пользователя.</span><span class="sxs-lookup"><span data-stu-id="3903a-159">The path to the DLL that contains the implementation of the user identity functions.</span></span> <span data-ttu-id="3903a-160">Например,% SystemRoot% \\ system32 \\ &lt; имя \_ DLL. \_ &gt; DLL.</span><span class="sxs-lookup"><span data-stu-id="3903a-160">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerinteractiveuipath"></a><span data-ttu-id="3903a-161">пиринтерактивеуипас</span><span class="sxs-lookup"><span data-stu-id="3903a-161">PeerInteractiveUIPath</span></span>



| <span data-ttu-id="3903a-162">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="3903a-162">Constant Value</span></span> | <span data-ttu-id="3903a-163">пиринтерактивеуипас</span><span class="sxs-lookup"><span data-stu-id="3903a-163">PeerInteractiveUIPath</span></span>                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3903a-164">Тип</span><span class="sxs-lookup"><span data-stu-id="3903a-164">Type</span></span>           | <span data-ttu-id="3903a-165">\_распаковать \_ SZ</span><span class="sxs-lookup"><span data-stu-id="3903a-165">REG\_EXPAND\_SZ</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="3903a-166">Описание</span><span class="sxs-lookup"><span data-stu-id="3903a-166">Description</span></span>    | <span data-ttu-id="3903a-167">Путь к библиотеке DLL, содержащей реализацию интерактивного пользовательского интерфейса, используемого для получения сведений о пользователе во время выполнения метода EAP.</span><span class="sxs-lookup"><span data-stu-id="3903a-167">The path to the DLL that contains the implementation of the interactive user interface used to obtain user information during execution of the EAP method.</span></span> <span data-ttu-id="3903a-168">Например,% SystemRoot% \\ system32 \\ &lt; имя \_ DLL. \_ &gt; DLL.</span><span class="sxs-lookup"><span data-stu-id="3903a-168">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerinvokepassworddialog"></a><span data-ttu-id="3903a-169">пиринвокепассворддиалог</span><span class="sxs-lookup"><span data-stu-id="3903a-169">PeerInvokePasswordDialog</span></span>



| <span data-ttu-id="3903a-170">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="3903a-170">Constant Value</span></span> | <span data-ttu-id="3903a-171">пиринвокепассворддиалог</span><span class="sxs-lookup"><span data-stu-id="3903a-171">PeerInvokePasswordDialog</span></span>                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3903a-172">Тип</span><span class="sxs-lookup"><span data-stu-id="3903a-172">Type</span></span>           | <span data-ttu-id="3903a-173">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="3903a-173">REG\_DWORD</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="3903a-174">Описание</span><span class="sxs-lookup"><span data-stu-id="3903a-174">Description</span></span>    | <span data-ttu-id="3903a-175">1 — для получения учетных данных с помощью универсального пароля EAPHost и диалогового окна домен.</span><span class="sxs-lookup"><span data-stu-id="3903a-175">1- to get credentials using the generic EAPHost password and domain dialog box.</span></span> <span data-ttu-id="3903a-176">0 — использовать пользовательское диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3903a-176">0 - to use a custom dialog box.</span></span> <span data-ttu-id="3903a-177">Если используется универсальное диалоговое окно, учетные данные задаются методом [**еаппирсеткредентиалс**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) .</span><span class="sxs-lookup"><span data-stu-id="3903a-177">If the generic dialog box is used, credentials are set by the [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) method.</span></span> |



 

### <a name="peerinvokeusernamedialog"></a><span data-ttu-id="3903a-178">пиринвокеусернамедиалог</span><span class="sxs-lookup"><span data-stu-id="3903a-178">PeerInvokeUsernameDialog</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3903a-179">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="3903a-179">Constant Value</span></span></th>
<th><span data-ttu-id="3903a-180">пиринвокеусернамедиалог</span><span class="sxs-lookup"><span data-stu-id="3903a-180">PeerInvokeUsernameDialog</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3903a-181">Тип</span><span class="sxs-lookup"><span data-stu-id="3903a-181">Type</span></span></td>
<td><span data-ttu-id="3903a-182">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="3903a-182">REG_DWORD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3903a-183">Описание</span><span class="sxs-lookup"><span data-stu-id="3903a-183">Description</span></span></td>
<td><ul>
<li><span data-ttu-id="3903a-184">1 — для получения учетных данных используется диалоговое окно универсальное имя пользователя EAPHost.</span><span class="sxs-lookup"><span data-stu-id="3903a-184">1 - to get credentials using the generic EAPHost user name dialog box.</span></span></li>
<li><span data-ttu-id="3903a-185">0 — использовать пользовательское диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3903a-185">0- to use a custom dialog box.</span></span></li>
</ul>
<span data-ttu-id="3903a-186">Если используется универсальное диалоговое окно, учетные данные задаются методом [<strong>еаппирсеткредентиалс</strong>] (/превиаус-версионс/Виндовс/десктоп/АПИ/еапмесодпирапис/НФ-еапмесодпирапис-еаппирсеткредентиалс).</span><span class="sxs-lookup"><span data-stu-id="3903a-186">If the generic dialog box is used, credentials are set by the [<strong>EapPeerSetCredentials</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) method.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="peerrequireconfigui"></a><span data-ttu-id="3903a-187">пиррекуиреконфигуи</span><span class="sxs-lookup"><span data-stu-id="3903a-187">PeerRequireConfigUI</span></span>



| <span data-ttu-id="3903a-188">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="3903a-188">Constant Value</span></span> | <span data-ttu-id="3903a-189">пиррекуиреконфигуи</span><span class="sxs-lookup"><span data-stu-id="3903a-189">PeerRequireConfigUI</span></span>                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3903a-190">Тип</span><span class="sxs-lookup"><span data-stu-id="3903a-190">Type</span></span>           | <span data-ttu-id="3903a-191">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="3903a-191">REG\_DWORD</span></span>                                                                                 |
| <span data-ttu-id="3903a-192">Описание</span><span class="sxs-lookup"><span data-stu-id="3903a-192">Description</span></span>    | <span data-ttu-id="3903a-193">0, если диалоговое окно пользовательского интерфейса конфигурации реализовано для этого метода; 1, если это не так.</span><span class="sxs-lookup"><span data-stu-id="3903a-193">0 if a configuration user interface dialog is implemented for this method; 1 if it is not.</span></span> |



 

### <a name="properties"></a><span data-ttu-id="3903a-194">Свойства</span><span class="sxs-lookup"><span data-stu-id="3903a-194">Properties</span></span>



| <span data-ttu-id="3903a-195">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="3903a-195">Constant Value</span></span> | <span data-ttu-id="3903a-196">Свойства</span><span class="sxs-lookup"><span data-stu-id="3903a-196">Properties</span></span>                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3903a-197">Тип</span><span class="sxs-lookup"><span data-stu-id="3903a-197">Type</span></span>           | <span data-ttu-id="3903a-198">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="3903a-198">REG\_DWORD</span></span>                                                                                                                                                  |
| <span data-ttu-id="3903a-199">Описание</span><span class="sxs-lookup"><span data-stu-id="3903a-199">Description</span></span>    | <span data-ttu-id="3903a-200">Биты в DWORD задаются для указания поддержки свойства.</span><span class="sxs-lookup"><span data-stu-id="3903a-200">Bits in the DWORD are set to indicate support for the property.</span></span> <span data-ttu-id="3903a-201">Список поддерживаемых значений см. в разделе [**Свойства метода EAP**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="3903a-201">For a list of supported values, see [**EAP Method Properties**](eap-method-properties.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3903a-202">См. также</span><span class="sxs-lookup"><span data-stu-id="3903a-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3903a-203">Разделы реестра для методов средства проверки подлинности EAP</span><span class="sxs-lookup"><span data-stu-id="3903a-203">EAP Authenticator Method Registry Keys</span></span>](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="3903a-204">Конфигурация реестра для расширенных типов EAP</span><span class="sxs-lookup"><span data-stu-id="3903a-204">Registry Configuration for Expanded EAP Types</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="3903a-205">Использование EAPHost</span><span class="sxs-lookup"><span data-stu-id="3903a-205">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="3903a-206">RFC 3748</span><span class="sxs-lookup"><span data-stu-id="3903a-206">RFC 3748</span></span>](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 