---
title: Сравнение функций Windows 2000 и распространяемого компонента RRAS
description: API RAS распространяется как компонент Windows 2000 и более поздних операционных систем и доступен в качестве распространяемого пакета для Windows NT 4,0 с пакетом обновления 3 (SP3) и более ранних версий.
ms.assetid: fd6c76b9-52e2-405e-b62e-055cfbdb5ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 745ad0c50654c8269c3e62b03629a7ae12a17476
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105650300"
---
# <a name="function-comparison-windows-2000-vs-rras-redistributable"></a><span data-ttu-id="509ea-103">Сравнение функций: Windows 2000 и распространяемый компонент RRAS</span><span class="sxs-lookup"><span data-stu-id="509ea-103">Function Comparison: Windows 2000 vs. RRAS Redistributable</span></span>

<span data-ttu-id="509ea-104">API RAS распространяется как компонент Windows 2000 и более поздних операционных систем и доступен в качестве распространяемого пакета для Windows NT 4,0 с пакетом обновления 3 (SP3) и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="509ea-104">The RAS API is distributed as a feature of Windows 2000 and later operating systems and is available as a redistributable for Windows NT 4.0 with Service Pack 3 (SP3) and earlier.</span></span> <span data-ttu-id="509ea-105">Служба RAS предоставляет те же функциональные возможности, что и в обеих формах, но используемое соглашение об именовании отличается для элементов ссылок в каждой версии API службы RAS.</span><span class="sxs-lookup"><span data-stu-id="509ea-105">RAS provides the same functionality in both of these forms but the naming convention that is used is different for the reference elements in each version of the RAS API.</span></span>

<span data-ttu-id="509ea-106">Функции RAS для Windows NT 4,0 с пакетом обновления 3 (SP3) и более ранних версий обычно начинаются с префикса "Расадмин".</span><span class="sxs-lookup"><span data-stu-id="509ea-106">The RAS functions for Windows NT 4.0 with SP3 and earlier typically begin with the "RasAdmin" prefix.</span></span> <span data-ttu-id="509ea-107">Аналогичные функции службы маршрутизации и удаленного доступа (RRAS) начинаются с префикса "Мпрадмин".</span><span class="sxs-lookup"><span data-stu-id="509ea-107">The analogous functions for Routing and Remote Access Service (RRAS) begin with the "MprAdmin" prefix.</span></span> <span data-ttu-id="509ea-108">Например, служба RAS предоставляет функцию с именем [**расадминпортжетинфо**](rasadminportgetinfo.md).</span><span class="sxs-lookup"><span data-stu-id="509ea-108">For example, RAS provides a function called [**RasAdminPortGetInfo**](rasadminportgetinfo.md).</span></span> <span data-ttu-id="509ea-109">Аналогичная функция в RRAS называется [**мпрадминпортжетинфо**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo).</span><span class="sxs-lookup"><span data-stu-id="509ea-109">The analogous function in RRAS is called [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo).</span></span> <span data-ttu-id="509ea-110">Как и тот же пример, служба RAS предоставляет функцию обратного вызова [**расадминжетипаддрессфорусер**](rasadmingetipaddressforuser.md).</span><span class="sxs-lookup"><span data-stu-id="509ea-110">As a similar example, RAS provides the callback function [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span></span> <span data-ttu-id="509ea-111">RRAS предоставляет аналогичную функцию обратного вызова с именем [**мпрадминжетипаддрессфорусер**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser).</span><span class="sxs-lookup"><span data-stu-id="509ea-111">RRAS provides a similar callback function called [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser).</span></span> <span data-ttu-id="509ea-112">Исключениями из этого правила являются [**расадминпортклеарстатистикс**](rasadminportclearstatistics.md), для которых в качестве RRAS используется [**Мпрадминпортклеарстатс**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats), а [**расадминфрибуффер**](rasadminfreebuffer.md)— [**мпрадминбуфферфри**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).</span><span class="sxs-lookup"><span data-stu-id="509ea-112">Exceptions to this rule are [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md), which under RRAS is [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats), and [**RasAdminFreeBuffer**](rasadminfreebuffer.md), which under RRAS is [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).</span></span>

<span data-ttu-id="509ea-113">В следующей таблице перечислены функции RAS Windows NT 4,0 SP3 и соответствующие функции RRAS.</span><span class="sxs-lookup"><span data-stu-id="509ea-113">The following table lists the Windows NT 4.0 SP3 RAS functions and the corresponding RRAS functions.</span></span>



| <span data-ttu-id="509ea-114">Служба RAS Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="509ea-114">Windows NT 4.0 RAS</span></span>                                                                   | <span data-ttu-id="509ea-115">УДАЛЕННОГО</span><span class="sxs-lookup"><span data-stu-id="509ea-115">RRAS</span></span>                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="509ea-116">**расадминакцептневконнектион**</span><span class="sxs-lookup"><span data-stu-id="509ea-116">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)                   | [<span data-ttu-id="509ea-117">**мпрадминакцептневконнектион**</span><span class="sxs-lookup"><span data-stu-id="509ea-117">**MprAdminAcceptNewConnection**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)                   |
| [<span data-ttu-id="509ea-118">**расадминконнектионхангупнотификатион**</span><span class="sxs-lookup"><span data-stu-id="509ea-118">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md) | [<span data-ttu-id="509ea-119">**мпрадминконнектионхангупнотификатион**</span><span class="sxs-lookup"><span data-stu-id="509ea-119">**MprAdminConnectionHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) |
| [<span data-ttu-id="509ea-120">**расадминфрибуффер**</span><span class="sxs-lookup"><span data-stu-id="509ea-120">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)                                     | [<span data-ttu-id="509ea-121">**мпрадминбуфферфри**</span><span class="sxs-lookup"><span data-stu-id="509ea-121">**MprAdminBufferFree**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)                                     |
| [<span data-ttu-id="509ea-122">**расадминжетеррорстринг**</span><span class="sxs-lookup"><span data-stu-id="509ea-122">**RasAdminGetErrorString**</span></span>](rasadmingeterrorstring.md)                             | [<span data-ttu-id="509ea-123">**мпрадминжетеррорстринг**</span><span class="sxs-lookup"><span data-stu-id="509ea-123">**MprAdminGetErrorString**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)                             |
| [<span data-ttu-id="509ea-124">**расадминжетипаддрессфорусер**</span><span class="sxs-lookup"><span data-stu-id="509ea-124">**RasAdminGetIpAddressForUser**</span></span>](rasadmingetipaddressforuser.md)                   | [<span data-ttu-id="509ea-125">**мпрадминжетипаддрессфорусер**</span><span class="sxs-lookup"><span data-stu-id="509ea-125">**MprAdminGetIpAddressForUser**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)                   |
| [<span data-ttu-id="509ea-126">**расадминпортклеарстатистикс**</span><span class="sxs-lookup"><span data-stu-id="509ea-126">**RasAdminPortClearStatistics**</span></span>](rasadminportclearstatistics.md)                   | [<span data-ttu-id="509ea-127">**мпрадминпортклеарстатс**</span><span class="sxs-lookup"><span data-stu-id="509ea-127">**MprAdminPortClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)                             |
| [<span data-ttu-id="509ea-128">**расадминпортдисконнект**</span><span class="sxs-lookup"><span data-stu-id="509ea-128">**RasAdminPortDisconnect**</span></span>](rasadminportdisconnect.md)                             | [<span data-ttu-id="509ea-129">**мпрадминпортдисконнект**</span><span class="sxs-lookup"><span data-stu-id="509ea-129">**MprAdminPortDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)                             |
| [<span data-ttu-id="509ea-130">**расадминпортенум**</span><span class="sxs-lookup"><span data-stu-id="509ea-130">**RasAdminPortEnum**</span></span>](rasadminportenum.md)                                         | [<span data-ttu-id="509ea-131">**мпрадминпортенум**</span><span class="sxs-lookup"><span data-stu-id="509ea-131">**MprAdminPortEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)                                         |
| [<span data-ttu-id="509ea-132">**расадминпортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="509ea-132">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)                                   | [<span data-ttu-id="509ea-133">**мпрадминпортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="509ea-133">**MprAdminPortGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)                                   |
| [<span data-ttu-id="509ea-134">**расадминрелеасеипаддресс**</span><span class="sxs-lookup"><span data-stu-id="509ea-134">**RasAdminReleaseIpAddress**</span></span>](rasadminreleaseipaddress.md)                         | [<span data-ttu-id="509ea-135">**мпрадминрелеасеипаддресс**</span><span class="sxs-lookup"><span data-stu-id="509ea-135">**MprAdminReleaseIpAddress**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)                         |
| [<span data-ttu-id="509ea-136">**расадминусержетинфо**</span><span class="sxs-lookup"><span data-stu-id="509ea-136">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)                                   | [<span data-ttu-id="509ea-137">**мпрадминусержетинфо**</span><span class="sxs-lookup"><span data-stu-id="509ea-137">**MprAdminUserGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)                                   |
| [<span data-ttu-id="509ea-138">**расадминусерсетинфо**</span><span class="sxs-lookup"><span data-stu-id="509ea-138">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)                                   | [<span data-ttu-id="509ea-139">**мпрадминусерсетинфо**</span><span class="sxs-lookup"><span data-stu-id="509ea-139">**MprAdminUserSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)                                   |



 

<span data-ttu-id="509ea-140">Хотя функции RRAS аналогичны функциям Windows NT 4,0 с пакетом обновления 3 (SP3) и более ранним аналогам службы удаленного доступа, функции RRAS часто используют разные наборы параметров.</span><span class="sxs-lookup"><span data-stu-id="509ea-140">Although the RRAS functions are similar to their Windows NT 4.0 with SP3 and earlier RAS counterparts in functionality, RRAS functions often take a different set of parameters.</span></span> <span data-ttu-id="509ea-141">Полные сведения о списке параметров этой функции см. на странице справки по определенной функции.</span><span class="sxs-lookup"><span data-stu-id="509ea-141">See the reference page for a particular function for complete information on that function's parameter list.</span></span>

<span data-ttu-id="509ea-142">Распространяемый компонент RRAS для Windows NT 4,0 с пакетом обновления 3 (SP3) и более ранних версий добавляет следующие функции, которые не имеют аналогов для RAS:</span><span class="sxs-lookup"><span data-stu-id="509ea-142">The RRAS redistributable for Windows NT 4.0 with SP3 and earlier adds the following functions, which have no RAS counterparts:</span></span>

[<span data-ttu-id="509ea-143">**мпрадминакцептневлинк**</span><span class="sxs-lookup"><span data-stu-id="509ea-143">**MprAdminAcceptNewLink**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[<span data-ttu-id="509ea-144">**мпрадминконнектионклеарстатс**</span><span class="sxs-lookup"><span data-stu-id="509ea-144">**MprAdminConnectionClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)

[<span data-ttu-id="509ea-145">**мпрадминконнектионенум**</span><span class="sxs-lookup"><span data-stu-id="509ea-145">**MprAdminConnectionEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)

[<span data-ttu-id="509ea-146">**мпрадминконнектионжетинфо**</span><span class="sxs-lookup"><span data-stu-id="509ea-146">**MprAdminConnectionGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)

[<span data-ttu-id="509ea-147">**мпрадминжетпдксервер**</span><span class="sxs-lookup"><span data-stu-id="509ea-147">**MprAdminGetPDCServer**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)

[<span data-ttu-id="509ea-148">**мпрадминиссервицеруннинг**</span><span class="sxs-lookup"><span data-stu-id="509ea-148">**MprAdminIsServiceRunning**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)

[<span data-ttu-id="509ea-149">**мпрадминлинкхангупнотификатион**</span><span class="sxs-lookup"><span data-stu-id="509ea-149">**MprAdminLinkHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[<span data-ttu-id="509ea-150">**мпрадминпортресет**</span><span class="sxs-lookup"><span data-stu-id="509ea-150">**MprAdminPortReset**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

[<span data-ttu-id="509ea-151">**мпрадминсерверконнект**</span><span class="sxs-lookup"><span data-stu-id="509ea-151">**MprAdminServerConnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)

[<span data-ttu-id="509ea-152">**мпрадминсервердисконнект**</span><span class="sxs-lookup"><span data-stu-id="509ea-152">**MprAdminServerDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

<span data-ttu-id="509ea-153">Помимо описанных выше функций, Windows 2000 и более поздних операционных систем добавляют следующие функции:</span><span class="sxs-lookup"><span data-stu-id="509ea-153">In addition to the preceding functions, Windows 2000 and later operating systems add the following functions:</span></span>

[<span data-ttu-id="509ea-154">**мпрадминсендусермессаже**</span><span class="sxs-lookup"><span data-stu-id="509ea-154">**MprAdminSendUserMessage**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)

[<span data-ttu-id="509ea-155">**MprAdminAcceptNewConnection2**</span><span class="sxs-lookup"><span data-stu-id="509ea-155">**MprAdminAcceptNewConnection2**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)

[<span data-ttu-id="509ea-156">**MprAdminConnectionHangupNotification2**</span><span class="sxs-lookup"><span data-stu-id="509ea-156">**MprAdminConnectionHangupNotification2**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

 

 




