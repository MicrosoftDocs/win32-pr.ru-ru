---
title: Атрибуты идентификации пользователя
description: Удостоверение пользователя, запрашивающего проверку подлинности, предоставляется в DLL расширения NPS в различных атрибутах.
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- Атрибуты, идентификация пользователя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527bdffad376ce92fa2fd7c5d5330fb752fea6aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681675"
---
# <a name="user-identification-attributes"></a><span data-ttu-id="af8f4-104">Атрибуты идентификации пользователя</span><span class="sxs-lookup"><span data-stu-id="af8f4-104">User Identification Attributes</span></span>

> [!Note]  
> <span data-ttu-id="af8f4-105">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="af8f4-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="af8f4-106">Содержимое этого раздела относится как к IAS, так и к NPS.</span><span class="sxs-lookup"><span data-stu-id="af8f4-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="af8f4-107">По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.</span><span class="sxs-lookup"><span data-stu-id="af8f4-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="af8f4-108">Удостоверение пользователя, запрашивающего проверку подлинности, предоставляется в DLL расширения NPS в различных атрибутах.</span><span class="sxs-lookup"><span data-stu-id="af8f4-108">The identity of the user requesting authentication is supplied to the NPS Extension DLLs in a number of different attributes.</span></span>

-   <span data-ttu-id="af8f4-109">**ратусернаме**</span><span class="sxs-lookup"><span data-stu-id="af8f4-109">**ratUserName**</span></span>
-   <span data-ttu-id="af8f4-110">**ратстриппедусернаме**</span><span class="sxs-lookup"><span data-stu-id="af8f4-110">**ratStrippedUserName**</span></span>
-   <span data-ttu-id="af8f4-111">**ратфкусернаме**</span><span class="sxs-lookup"><span data-stu-id="af8f4-111">**ratFQUserName**</span></span>

<span data-ttu-id="af8f4-112">Каждый атрибут предоставляет удостоверение пользователя в другом формате.</span><span class="sxs-lookup"><span data-stu-id="af8f4-112">Each attribute provides the user identity in a different format.</span></span> <span data-ttu-id="af8f4-113">Как правило, разработчики должны использовать **ратстриппедусернаме**.</span><span class="sxs-lookup"><span data-stu-id="af8f4-113">In general, developers should use **ratStrippedUserName**.</span></span> <span data-ttu-id="af8f4-114">Использование атрибутов **ратусернаме** и **ратфкусернаме** является более специализированным.</span><span class="sxs-lookup"><span data-stu-id="af8f4-114">The uses of the **ratUserName** and **ratFQUserName** attributes are more specialized.</span></span>

> [!Note]  
> <span data-ttu-id="af8f4-115">Атрибут User-Password **ратусерпассворд** уже был расшифрован при его отправке в библиотеку DLL расширения и может использоваться в этой форме.</span><span class="sxs-lookup"><span data-stu-id="af8f4-115">The User-Password attribute, **ratUserPassword**, has already been decrypted when it is sent to the extension DLL and is usable in that form.</span></span>

 

## <a name="ratusername"></a><span data-ttu-id="af8f4-116">ратусернаме</span><span class="sxs-lookup"><span data-stu-id="af8f4-116">ratUserName</span></span>

<span data-ttu-id="af8f4-117">Атрибут **ратусернаме** содержит имя, которое было фактически Отправлено "по сети".</span><span class="sxs-lookup"><span data-stu-id="af8f4-117">The **ratUserName** attribute contains the name that was actually sent "over the wire."</span></span> <span data-ttu-id="af8f4-118">NPS не может каким либо образом обработать или проверить содержимое этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="af8f4-118">NPS has not, in any way, processed or validated the contents of this attribute.</span></span> <span data-ttu-id="af8f4-119">Этот атрибут может быть недоступен, так как пользователь мог определиться с помощью таких средств, как идентификатор звонящего.</span><span class="sxs-lookup"><span data-stu-id="af8f4-119">This attribute may not be available at all because the user may have been identified through a means such as caller ID.</span></span>

<span data-ttu-id="af8f4-120">При использовании [**радиусекстенсионпроцесс/ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), если этот атрибут доступен, он доступен только в точке подключаемого модуля DLL расширения проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="af8f4-120">When using [**RadiusExtensionProcess/Ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), if this attribute is available, it is available only at the Authentication Extension DLL plug-in point.</span></span> <span data-ttu-id="af8f4-121">Атрибут **ратусернаме** недоступен в точке подключаемого модуля DLL расширения авторизации, так как в библиотеках DLL расширения авторизации функции **радиусекстенсионпроцесс/ex** видят только атрибуты "Outbound".</span><span class="sxs-lookup"><span data-stu-id="af8f4-121">The **ratUserName** attribute is not available at the Authorization Extension DLL plug-in point because in Authorization Extension DLLs the **RadiusExtensionProcess/Ex** functions see only the "outbound" attributes.</span></span>

<span data-ttu-id="af8f4-122">При использовании [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), если этот атрибут доступен, он доступен как в точке подключаемого модуля DLL модуля проверки подлинности, так и в точке подключаемого модуля DLL расширения авторизации.</span><span class="sxs-lookup"><span data-stu-id="af8f4-122">When using [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), if this attribute is available, it is available at both the Authentication Extension DLL plug-in point and the Authorization Extension DLL plug-in point.</span></span>

## <a name="ratstrippedusername"></a><span data-ttu-id="af8f4-123">ратстриппедусернаме</span><span class="sxs-lookup"><span data-stu-id="af8f4-123">ratStrippedUserName</span></span>

<span data-ttu-id="af8f4-124">**Ратстриппедусернаме** — это удостоверение пользователя после удаления области.</span><span class="sxs-lookup"><span data-stu-id="af8f4-124">The **ratStrippedUserName** is the user's identity after "realm stripping."</span></span> <span data-ttu-id="af8f4-125">Дополнительные сведения об отбрасывания сфер см. в разделе " [имена областей](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) " на странице http: \\ \\ technet2.Microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="af8f4-125">For more information on realm stripping, see the [Realm names](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) topic on http:\\\\technet2.microsoft.com.</span></span>

<span data-ttu-id="af8f4-126">Этот атрибут может присутствовать в точке подключаемого модуля DLL расширения проверки подлинности, точке подключаемого модуля DLL расширения авторизации или в обоих случаях.</span><span class="sxs-lookup"><span data-stu-id="af8f4-126">This attribute may be present at the Authentication Extension DLL plug-in point, the Authorization Extension DLL plug-in point, or both.</span></span> <span data-ttu-id="af8f4-127">Этот атрибут гарантированно имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="af8f4-127">This attribute is guaranteed to have the format:</span></span>

<span data-ttu-id="af8f4-128">*Домен ***\\*** имя_пользователя*</span><span class="sxs-lookup"><span data-stu-id="af8f4-128">*Domain ***\\*** UserName*</span></span>

<span data-ttu-id="af8f4-129">Где *domain* — это NetBIOS-имя домена.</span><span class="sxs-lookup"><span data-stu-id="af8f4-129">Where *Domain* is the NetBIOS domain name.</span></span>

## <a name="ratfqusername"></a><span data-ttu-id="af8f4-130">ратфкусернаме</span><span class="sxs-lookup"><span data-stu-id="af8f4-130">ratFQUserName</span></span>

<span data-ttu-id="af8f4-131">Атрибут **ратфкусернаме** — это полное имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="af8f4-131">The **ratFQUserName** attribute is the "fully qualified" user name.</span></span>

<span data-ttu-id="af8f4-132">Этот атрибут может присутствовать в точке подключаемого модуля DLL расширения проверки подлинности, точке подключаемого модуля DLL расширения авторизации или в обоих случаях.</span><span class="sxs-lookup"><span data-stu-id="af8f4-132">This attribute may be present in the Authentication Extension DLL plug-in point, the Authorization Extension DLL plug-in point, or both.</span></span> <span data-ttu-id="af8f4-133">Однако формат атрибута может различаться между двумя точками подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="af8f4-133">However, the format of the attribute may differ between the two plug-in points.</span></span> <span data-ttu-id="af8f4-134">В точке подключаемого модуля DLL расширения проверки подлинности этот атрибут всегда будет иметь вид:</span><span class="sxs-lookup"><span data-stu-id="af8f4-134">At the Authentication Extension DLL plug-in point, this attribute will always be of the form:</span></span>

<span data-ttu-id="af8f4-135">*Домен ***\\*** имя_пользователя*</span><span class="sxs-lookup"><span data-stu-id="af8f4-135">*Domain ***\\*** UserName*</span></span>

<span data-ttu-id="af8f4-136">Формат атрибута **ратфкусернаме** в точке подключаемого модуля DLL расширения авторизации зависит от того, является ли пользователь Active Directory пользователем.</span><span class="sxs-lookup"><span data-stu-id="af8f4-136">The format of the **ratFQUserName** attribute at the Authorization Extension DLL plug-in point depends on whether the user is an Active Directory user.</span></span>

-   <span data-ttu-id="af8f4-137">Если пользователь является локальным пользователем **ратфкусернаме** имеет тот же формат, что и для точки подключаемого модуля DLL расширения проверки подлинности:</span><span class="sxs-lookup"><span data-stu-id="af8f4-137">If the user is a local user **ratFQUserName** has the same format as for the Authentication Extension DLL plug-in point:</span></span>

    <span data-ttu-id="af8f4-138">*Домен ***\\*** имя_пользователя*</span><span class="sxs-lookup"><span data-stu-id="af8f4-138">*Domain ***\\*** UserName*</span></span>

    <span data-ttu-id="af8f4-139">.</span><span class="sxs-lookup"><span data-stu-id="af8f4-139">.</span></span>

-   <span data-ttu-id="af8f4-140">Если пользователь является Active Directory пользователем, **ратфкусернаме** может содержать имя пользователя в "каноническом" формате.</span><span class="sxs-lookup"><span data-stu-id="af8f4-140">If the user is an Active Directory user, **ratFQUserName** may contain the user's name in "canonical" format.</span></span> <span data-ttu-id="af8f4-141">Канонический формат — это формат, используемый Active Directory для определения пользователя.</span><span class="sxs-lookup"><span data-stu-id="af8f4-141">Canonical format is the format used by the Active Directory to identify the user.</span></span> <span data-ttu-id="af8f4-142">Это путь из корня дерева Active Directory и включает подразделение пользователя (OU).</span><span class="sxs-lookup"><span data-stu-id="af8f4-142">It is the path from the root of the Active Directory tree, and includes the user's Organizational Unit (OU).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af8f4-143">См. также</span><span class="sxs-lookup"><span data-stu-id="af8f4-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af8f4-144">Настройка библиотек DLL расширения</span><span class="sxs-lookup"><span data-stu-id="af8f4-144">Setting Up the Extension DLLs</span></span>](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[<span data-ttu-id="af8f4-145">Вызов библиотек DLL расширения</span><span class="sxs-lookup"><span data-stu-id="af8f4-145">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 