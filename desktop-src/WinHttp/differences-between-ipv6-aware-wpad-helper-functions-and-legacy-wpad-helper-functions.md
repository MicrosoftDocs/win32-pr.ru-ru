---
title: IPv6-Aware и устаревшие вспомогательные функции WPAD
description: Различия между вспомогательными функциями IPv6-Aware WPAD и устаревшими вспомогательными функциями WPAD
ms.assetid: ea4b1c0d-ce02-477b-85c8-44e1beef90c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511b7f04aa0a2abe04b99562c15aeb3a53bdaadf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712553"
---
# <a name="ipv6-aware-and-legacy-wpad-helper-functions"></a><span data-ttu-id="c7d30-103">IPv6-Aware и устаревшие вспомогательные функции WPAD</span><span class="sxs-lookup"><span data-stu-id="c7d30-103">IPv6-Aware and Legacy WPAD helper functions</span></span>

<span data-ttu-id="c7d30-104">В следующих таблицах объясняются различия между новыми вспомогательными функциями WPAD и устаревшими вспомогательными функциями WPAD.</span><span class="sxs-lookup"><span data-stu-id="c7d30-104">The following tables explain the differences between the new WPAD helper functions and the legacy WPAD helper functions.</span></span> <span data-ttu-id="c7d30-105">Новые функции помечаются звездочкой.</span><span class="sxs-lookup"><span data-stu-id="c7d30-105">The new functions are marked with an asterisk.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c7d30-106">Функции</span><span class="sxs-lookup"><span data-stu-id="c7d30-106">Functions</span></span></th>
<th><span data-ttu-id="c7d30-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c7d30-107">Input</span></span></th>
<th><span data-ttu-id="c7d30-108">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="c7d30-108">Output</span></span></th>
<th><span data-ttu-id="c7d30-109">Причина изменения</span><span class="sxs-lookup"><span data-stu-id="c7d30-109">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c7d30-110">: dnsResolve</span><span class="sxs-lookup"><span data-stu-id="c7d30-110">dnsResolve</span></span></td>
<td><span data-ttu-id="c7d30-111">Узел</span><span class="sxs-lookup"><span data-stu-id="c7d30-111">Host</span></span></td>
<td><span data-ttu-id="c7d30-112">IPv4-адрес</span><span class="sxs-lookup"><span data-stu-id="c7d30-112">IPv4 address</span></span></td>
<td rowspan="2"><span data-ttu-id="c7d30-113">Функция ex вернет список IPv6/IPv4.</span><span class="sxs-lookup"><span data-stu-id="c7d30-113">Ex function will return a list of IPv6/IPv4.</span></span> <span data-ttu-id="c7d30-114">Требуется, так как адреса IPv6 или IPv4 могут иметь несколько адресов одноадресной рассылки для одного интерфейса. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c7d30-114">Necessary since IPv6 or IPv4 addresses can have multiple unicast addresses for a single interface.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7d30-115">Днсресолвикс \*</span><span class="sxs-lookup"><span data-stu-id="c7d30-115">dnsResolveEx\*</span></span></td>
<td><span data-ttu-id="c7d30-116">Узел</span><span class="sxs-lookup"><span data-stu-id="c7d30-116">Host</span></span></td>
<td><span data-ttu-id="c7d30-117">Список адресов IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="c7d30-117">List of IPv6/IPv4 addresses</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c7d30-118">Функции</span><span class="sxs-lookup"><span data-stu-id="c7d30-118">Functions</span></span></th>
<th><span data-ttu-id="c7d30-119">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c7d30-119">Input</span></span></th>
<th><span data-ttu-id="c7d30-120">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="c7d30-120">Output</span></span></th>
<th><span data-ttu-id="c7d30-121">Причина изменения</span><span class="sxs-lookup"><span data-stu-id="c7d30-121">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c7d30-122">Разрешено</span><span class="sxs-lookup"><span data-stu-id="c7d30-122">isResolveable</span></span></td>
<td><span data-ttu-id="c7d30-123">Узел IPv4</span><span class="sxs-lookup"><span data-stu-id="c7d30-123">IPv4 host</span></span></td>
<td><span data-ttu-id="c7d30-124">TRUE / FALSE</span><span class="sxs-lookup"><span data-stu-id="c7d30-124">TRUE / FALSE</span></span></td>
<td rowspan="2"><span data-ttu-id="c7d30-125">Функция ex возвращает значение TRUE, если узел может разрешаться в адрес IPv6 или IPv4.</span><span class="sxs-lookup"><span data-stu-id="c7d30-125">The Ex function will return TRUE if a host can resolve to an IPv6 or IPv4 address.</span></span> <span data-ttu-id="c7d30-126">Функция Legacy Возвращает значение TRUE только в том случае, если узел разрешается в IPv4-адрес. $ {Resolve} $</span><span class="sxs-lookup"><span data-stu-id="c7d30-126">The legacy function only returns TRUE if the host resolves to an IPv4 address.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7d30-127">Исресолвеабликс \*</span><span class="sxs-lookup"><span data-stu-id="c7d30-127">isResolveableEx\*</span></span></td>
<td><span data-ttu-id="c7d30-128">Узел IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="c7d30-128">IPv6/IPv4 host</span></span></td>
<td><span data-ttu-id="c7d30-129">TRUE / FALSE</span><span class="sxs-lookup"><span data-stu-id="c7d30-129">TRUE / FALSE</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c7d30-130">Функции</span><span class="sxs-lookup"><span data-stu-id="c7d30-130">Functions</span></span></th>
<th><span data-ttu-id="c7d30-131">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c7d30-131">Input</span></span></th>
<th><span data-ttu-id="c7d30-132">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="c7d30-132">Output</span></span></th>
<th><span data-ttu-id="c7d30-133">Причина изменения</span><span class="sxs-lookup"><span data-stu-id="c7d30-133">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c7d30-134">myIPAddress</span><span class="sxs-lookup"><span data-stu-id="c7d30-134">myIPAddress</span></span></td>
<td><span data-ttu-id="c7d30-135">нет</span><span class="sxs-lookup"><span data-stu-id="c7d30-135">none</span></span></td>
<td><span data-ttu-id="c7d30-136">IPv4-адрес</span><span class="sxs-lookup"><span data-stu-id="c7d30-136">IPv4 address</span></span></td>
<td rowspan="2"><span data-ttu-id="c7d30-137">Функция ex вернет список IPv6/IPv4.</span><span class="sxs-lookup"><span data-stu-id="c7d30-137">Ex function will return a list of IPv6/IPv4.</span></span> <span data-ttu-id="c7d30-138">Требуется, так как адреса IPv6 или IPv4 могут иметь несколько адресов одноадресной рассылки для одного интерфейса $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c7d30-138">Necessary since IPv6 or IPv4 addresses can have multiple unicast addresses for a single interface ${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7d30-139">Мипаддрессекс \*</span><span class="sxs-lookup"><span data-stu-id="c7d30-139">myIPAddressEx\*</span></span></td>
<td><span data-ttu-id="c7d30-140">нет</span><span class="sxs-lookup"><span data-stu-id="c7d30-140">none</span></span></td>
<td><span data-ttu-id="c7d30-141">Список адресов IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="c7d30-141">List of IPv6/IPv4 addresses</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c7d30-142">Функции</span><span class="sxs-lookup"><span data-stu-id="c7d30-142">Functions</span></span></th>
<th><span data-ttu-id="c7d30-143">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c7d30-143">Input</span></span></th>
<th><span data-ttu-id="c7d30-144">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="c7d30-144">Output</span></span></th>
<th><span data-ttu-id="c7d30-145">Причина изменения</span><span class="sxs-lookup"><span data-stu-id="c7d30-145">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c7d30-146">isInNet</span><span class="sxs-lookup"><span data-stu-id="c7d30-146">isInNet</span></span></td>
<td><span data-ttu-id="c7d30-147">Узел, шаблон IP-адреса, разделенного точками, маска IP-адреса</span><span class="sxs-lookup"><span data-stu-id="c7d30-147">Host, Dot separated IP address pattern, IP address Mask</span></span></td>
<td><span data-ttu-id="c7d30-148">TRUE / FALSE</span><span class="sxs-lookup"><span data-stu-id="c7d30-148">TRUE / FALSE</span></span></td>
<td rowspan="2"><span data-ttu-id="c7d30-149">Предоставить версию IP-адреса независимым образом, чтобы найти IP-адрес в данной подсети.</span><span class="sxs-lookup"><span data-stu-id="c7d30-149">Provide an IP version agnostic way to find if an IP address is in a given subnet.</span></span> <span data-ttu-id="c7d30-150">Кроме того, нотация маски в IPv4 является устаревшей. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="c7d30-150">Also, the mask notation in IPv4 is deprecated.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7d30-151">Исиннетекс \*</span><span class="sxs-lookup"><span data-stu-id="c7d30-151">isInNetEx\*</span></span></td>
<td><span data-ttu-id="c7d30-152">Префикс IP-адреса IP</span><span class="sxs-lookup"><span data-stu-id="c7d30-152">IP Address IP Prefix</span></span></td>
<td><span data-ttu-id="c7d30-153">TRUE / FALSE</span><span class="sxs-lookup"><span data-stu-id="c7d30-153">TRUE / FALSE</span></span></td>

</tr>
</tbody>
</table>



 



| <span data-ttu-id="c7d30-154">Функции</span><span class="sxs-lookup"><span data-stu-id="c7d30-154">Functions</span></span>           | <span data-ttu-id="c7d30-155">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c7d30-155">Input</span></span>                       | <span data-ttu-id="c7d30-156">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="c7d30-156">Output</span></span>                             | <span data-ttu-id="c7d30-157">Причина изменения</span><span class="sxs-lookup"><span data-stu-id="c7d30-157">Reason for Change</span></span>                                                                                                                           |
|---------------------|-----------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d30-158">сортипаддресслист\*</span><span class="sxs-lookup"><span data-stu-id="c7d30-158">sortIPAddressList\*</span></span> | <span data-ttu-id="c7d30-159">Список адресов IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="c7d30-159">List of IPv6/IPv4 addresses</span></span> | <span data-ttu-id="c7d30-160">Отсортированный список адресов IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="c7d30-160">Sorted List of IPv6/IPv4 addresses</span></span> | <span data-ttu-id="c7d30-161">Нет аналоговой функции Legacy, так как устаревшие функции возвращают только один IPv4-адрес, поэтому сортировка не требуется.</span><span class="sxs-lookup"><span data-stu-id="c7d30-161">There is no counterpart legacy function because legacy functions only returned a single IPv4 address, therefore there was no need to sort .</span></span> |



 



| <span data-ttu-id="c7d30-162">Функции</span><span class="sxs-lookup"><span data-stu-id="c7d30-162">Functions</span></span>          | <span data-ttu-id="c7d30-163">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c7d30-163">Input</span></span> | <span data-ttu-id="c7d30-164">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="c7d30-164">Output</span></span>                     | <span data-ttu-id="c7d30-165">Причина изменения</span><span class="sxs-lookup"><span data-stu-id="c7d30-165">Reason for Change</span></span>                                                                                                                                                                                                           |
|--------------------|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d30-166">жетклиентверсион\*</span><span class="sxs-lookup"><span data-stu-id="c7d30-166">getClientVersion\*</span></span> | <span data-ttu-id="c7d30-167">нет</span><span class="sxs-lookup"><span data-stu-id="c7d30-167">none</span></span>  | <span data-ttu-id="c7d30-168">Номер версии модуля WPAD</span><span class="sxs-lookup"><span data-stu-id="c7d30-168">WPAD engine version number</span></span> | <span data-ttu-id="c7d30-169">В настоящее время эта функция возвращает версию 1,0.</span><span class="sxs-lookup"><span data-stu-id="c7d30-169">Currently this function returns version 1.0.</span></span> <span data-ttu-id="c7d30-170">Мы добавили эту функцию, чтобы позволить ИТ-администраторам обновить свой WPAD для работы с разными версиями модуля WPAD, не нарушая их существующее развертывание.</span><span class="sxs-lookup"><span data-stu-id="c7d30-170">We added this function to allow IT administrators to update their WPAD to work with different versions of the WPAD engine without causing breaks to their existent deployment.</span></span> |



 

> [!Note]  
> <span data-ttu-id="c7d30-171">Для этой функции требуется Windows Internet Explorer 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="c7d30-171">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



