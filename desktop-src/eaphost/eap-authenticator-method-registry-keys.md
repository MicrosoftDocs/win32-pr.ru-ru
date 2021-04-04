---
title: Значения реестра для метода средства проверки подлинности EAP
description: Сведения о значениях реестра для методов средства проверки подлинности EAP. Эти конкретные значения реестра необходимы для методов проверки подлинности EAP.
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a710ca6f09914c8d111c42a8323a9c39c51f898
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987896"
---
# <a name="eap-authenticator-method-registry-values"></a><span data-ttu-id="e198f-104">Значения реестра для метода средства проверки подлинности EAP</span><span class="sxs-lookup"><span data-stu-id="e198f-104">EAP Authenticator Method Registry Values</span></span>

<span data-ttu-id="e198f-105">Для методов проверки подлинности EAP требуются определенные значения реестра.</span><span class="sxs-lookup"><span data-stu-id="e198f-105">Specific registry values are required for EAP authenticator methods.</span></span>

## <a name="eap-authenticator-method-dll-paths"></a><span data-ttu-id="e198f-106">Пути DLL метода проверки подлинности EAP</span><span class="sxs-lookup"><span data-stu-id="e198f-106">EAP Authenticator Method DLL Paths</span></span>

<span data-ttu-id="e198f-107">Следующий путь задает расположение реестра для обычных библиотек DLL метода проверки подлинности EAP.</span><span class="sxs-lookup"><span data-stu-id="e198f-107">The following path specifies the registry location for regular EAP authenticator method DLLs.</span></span>

<span data-ttu-id="e198f-108">**HKLM \\ System \\ CCS \\ Services \\ \\ методы EAPHost \\ *&lt; аусорид &gt;* \\ \* &lt; еаптипеид&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="e198f-108">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="e198f-109">Например, путь регистрации установки метода средства проверки подлинности EAP по адресу **аусорид** "311" (указывающий, что "Microsoft" является автором) и **еаптипеид** "40", выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e198f-109">For example, an EAP authenticator method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author) and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="e198f-110">**HKLM \\ System \\ CCS \\ Services \\ \\ методы EAPHost \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="e198f-110">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\40**</span></span>

<span data-ttu-id="e198f-111">Следующий путь задает расположение реестра для расширенных библиотек DLL метода проверки подлинности EAP.</span><span class="sxs-lookup"><span data-stu-id="e198f-111">The following path specifies the registry location for extended EAP authenticator method DLLs.</span></span>

<span data-ttu-id="e198f-112">**HKLM \\ System \\ CCS \\ Services \\ EAPHost \\ Methods \\ *&lt; аусорид &gt;* \\ 254 \\ *&lt; VendorID &gt;* \\ \* &lt; вендортипе&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="e198f-112">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\254\\*&lt;VendorId&gt;*\\*&lt;VendorType&gt;**\*</span></span>

<span data-ttu-id="e198f-113">Например, путь регистрации установки метода средства проверки подлинности EAP по адресу **аусорид** "311" (указывающий на то, что "Microsoft" является автором), **ид поставщика** "311" и **еаптипеид** "40", выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e198f-113">For example, an EAP authenticator method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author), a **VendorId** of "311", and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="e198f-114">**HKLM \\ System \\ CCS \\ Services \\ Eaphost \\ methods \\ 311 \\ 254 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="e198f-114">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\254\\311\\40**</span></span>

> [!Note]  
> <span data-ttu-id="e198f-115">Дополнительные сведения о выделении типов методов EAP см. в разделе 6,2 статьи [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span><span class="sxs-lookup"><span data-stu-id="e198f-115">For more information on the allocation of EAP method types, see section 6.2 of [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span></span>

 

## <a name="registry-values"></a><span data-ttu-id="e198f-116">Значения реестра</span><span class="sxs-lookup"><span data-stu-id="e198f-116">Registry Values</span></span>

<span data-ttu-id="e198f-117">Следующие значения реестра для метода проверки подлинности являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="e198f-117">The following authenticator method registry values are required.</span></span>

-   [<span data-ttu-id="e198f-118">аусентикатордллпас</span><span class="sxs-lookup"><span data-stu-id="e198f-118">AuthenticatorDllPath</span></span>](#authenticatordllpath)
-   [<span data-ttu-id="e198f-119">аусентикаторфриендлинаме</span><span class="sxs-lookup"><span data-stu-id="e198f-119">AuthenticatorFriendlyName</span></span>](#authenticatorfriendlyname)

<span data-ttu-id="e198f-120">Кроме указанных выше значений реестра, рекомендуется использовать следующий параметр реестра для метода проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e198f-120">Besides the above registry values, the following authenticator method registry value is recommended.</span></span>

-   [<span data-ttu-id="e198f-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="e198f-121">Properties</span></span>](#properties)

<span data-ttu-id="e198f-122">Остальные параметры реестра для метода проверки подлинности являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="e198f-122">The remaining authenticator method registry values are optional.</span></span>

-   [<span data-ttu-id="e198f-123">конфигклсид</span><span class="sxs-lookup"><span data-stu-id="e198f-123">ConfigCLSID</span></span>](#configclsid)
-   [<span data-ttu-id="e198f-124">стандалонесуппортед</span><span class="sxs-lookup"><span data-stu-id="e198f-124">StandaloneSupported</span></span>](#standalonesupported)

## <a name="authenticatordllpath"></a><span data-ttu-id="e198f-125">аусентикатордллпас</span><span class="sxs-lookup"><span data-stu-id="e198f-125">AuthenticatorDllPath</span></span>



| <span data-ttu-id="e198f-126">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="e198f-126">Constant Value</span></span> | <span data-ttu-id="e198f-127">аусентикатордллпас</span><span class="sxs-lookup"><span data-stu-id="e198f-127">AuthenticatorDllPath</span></span>                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e198f-128">Тип</span><span class="sxs-lookup"><span data-stu-id="e198f-128">Type</span></span>           | <span data-ttu-id="e198f-129">\_распаковать \_ SZ</span><span class="sxs-lookup"><span data-stu-id="e198f-129">REG\_EXPAND\_SZ</span></span>                                                                                               |
| <span data-ttu-id="e198f-130">Описание</span><span class="sxs-lookup"><span data-stu-id="e198f-130">Description</span></span>    | <span data-ttu-id="e198f-131">Путь к библиотеке DLL метода проверки подлинности EAP.</span><span class="sxs-lookup"><span data-stu-id="e198f-131">The path to the EAP authenticator method DLL.</span></span> <span data-ttu-id="e198f-132">Например,% SystemRoot% \\ system32 \\ &lt; имя \_ DLL. \_ &gt; DLL.</span><span class="sxs-lookup"><span data-stu-id="e198f-132">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

## <a name="authenticatorfriendlyname"></a><span data-ttu-id="e198f-133">аусентикаторфриендлинаме</span><span class="sxs-lookup"><span data-stu-id="e198f-133">AuthenticatorFriendlyName</span></span>



| <span data-ttu-id="e198f-134">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="e198f-134">Constant Value</span></span> | <span data-ttu-id="e198f-135">аусентикаторфриендлинаме</span><span class="sxs-lookup"><span data-stu-id="e198f-135">AuthenticatorFriendlyName</span></span>                                                          |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e198f-136">Тип</span><span class="sxs-lookup"><span data-stu-id="e198f-136">Type</span></span>           | <span data-ttu-id="e198f-137">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="e198f-137">REG\_SZ</span></span>                                                                            |
| <span data-ttu-id="e198f-138">Описание</span><span class="sxs-lookup"><span data-stu-id="e198f-138">Description</span></span>    | <span data-ttu-id="e198f-139">Строка, содержащая понятное (отображаемое) имя метода проверки подлинности EAP.</span><span class="sxs-lookup"><span data-stu-id="e198f-139">String that contains the friendly (display) name for the EAP authenticator method.</span></span> |



 

## <a name="configclsid"></a><span data-ttu-id="e198f-140">конфигклсид</span><span class="sxs-lookup"><span data-stu-id="e198f-140">ConfigCLSID</span></span>



| <span data-ttu-id="e198f-141">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="e198f-141">Constant Value</span></span> | <span data-ttu-id="e198f-142">конфигклсид</span><span class="sxs-lookup"><span data-stu-id="e198f-142">ConfigCLSID</span></span>                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e198f-143">Тип</span><span class="sxs-lookup"><span data-stu-id="e198f-143">Type</span></span>           | <span data-ttu-id="e198f-144">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="e198f-144">REG\_SZ</span></span>                                                                                                                               |
| <span data-ttu-id="e198f-145">Описание</span><span class="sxs-lookup"><span data-stu-id="e198f-145">Description</span></span>    | <span data-ttu-id="e198f-146">Строка, содержащая GUID класса конфигурации для этого метода проверки подлинности в формате {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="e198f-146">String that contains the configuration class GUID for this authenticator method, in the format {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span></span> |



 

## <a name="properties"></a><span data-ttu-id="e198f-147">Свойства</span><span class="sxs-lookup"><span data-stu-id="e198f-147">Properties</span></span>



| <span data-ttu-id="e198f-148">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="e198f-148">Constant Value</span></span> | <span data-ttu-id="e198f-149">Свойства</span><span class="sxs-lookup"><span data-stu-id="e198f-149">Properties</span></span>                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e198f-150">Тип</span><span class="sxs-lookup"><span data-stu-id="e198f-150">Type</span></span>           | <span data-ttu-id="e198f-151">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="e198f-151">REG\_DWORD</span></span>                                                                                                                                                  |
| <span data-ttu-id="e198f-152">Описание</span><span class="sxs-lookup"><span data-stu-id="e198f-152">Description</span></span>    | <span data-ttu-id="e198f-153">Биты в DWORD задаются для указания поддержки свойства.</span><span class="sxs-lookup"><span data-stu-id="e198f-153">Bits in the DWORD are set to indicate support for the property.</span></span> <span data-ttu-id="e198f-154">Список поддерживаемых значений см. в разделе [**Свойства метода EAP**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="e198f-154">For a list of supported values, see [**EAP Method Properties**](eap-method-properties.md).</span></span> |



 

## <a name="standalonesupported"></a><span data-ttu-id="e198f-155">стандалонесуппортед</span><span class="sxs-lookup"><span data-stu-id="e198f-155">StandaloneSupported</span></span>



| <span data-ttu-id="e198f-156">Постоянное значение</span><span class="sxs-lookup"><span data-stu-id="e198f-156">Constant Value</span></span> | <span data-ttu-id="e198f-157">стандалонесуппортед</span><span class="sxs-lookup"><span data-stu-id="e198f-157">StandaloneSupported</span></span>                                             |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="e198f-158">Тип</span><span class="sxs-lookup"><span data-stu-id="e198f-158">Type</span></span>           | <span data-ttu-id="e198f-159">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="e198f-159">REG\_DWORD</span></span>                                                      |
| <span data-ttu-id="e198f-160">Описание</span><span class="sxs-lookup"><span data-stu-id="e198f-160">Description</span></span>    | <span data-ttu-id="e198f-161">0, если это автономный метод проверки подлинности; 1, если это не так.</span><span class="sxs-lookup"><span data-stu-id="e198f-161">0 if this is a standalone authenticator method; 1 if it is not.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e198f-162">См. также</span><span class="sxs-lookup"><span data-stu-id="e198f-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e198f-163">Разделы реестра для метода однорангового узла EAP</span><span class="sxs-lookup"><span data-stu-id="e198f-163">EAP Peer Method Registry Keys</span></span>](eap-peer-method-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="e198f-164">Конфигурация реестра для расширенных типов EAP</span><span class="sxs-lookup"><span data-stu-id="e198f-164">Registry Configuration for Expanded EAP Types</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="e198f-165">Использование EAPHost</span><span class="sxs-lookup"><span data-stu-id="e198f-165">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="e198f-166">RFC 3748</span><span class="sxs-lookup"><span data-stu-id="e198f-166">RFC 3748</span></span>](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




