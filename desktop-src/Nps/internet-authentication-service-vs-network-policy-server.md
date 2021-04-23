---
title: Служба проверки подлинности в Интернете & сервер политики сети
description: Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS).
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca657da17e823caa51e8401905a8a0a3e307e975
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104070771"
---
# <a name="internet-authentication-service--network-policy-server"></a><span data-ttu-id="2f02c-103">Служба проверки подлинности в Интернете & сервер политики сети</span><span class="sxs-lookup"><span data-stu-id="2f02c-103">Internet Authentication Service & Network Policy Server</span></span>

<span data-ttu-id="2f02c-104">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS).</span><span class="sxs-lookup"><span data-stu-id="2f02c-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span>

## <a name="internet-authentication-service"></a><span data-ttu-id="2f02c-105">Служба проверки подлинности в Интернете</span><span class="sxs-lookup"><span data-stu-id="2f02c-105">Internet Authentication Service</span></span>

<span data-ttu-id="2f02c-106">Служба проверки подлинности через Интернет является реализацией сервера RADIUS и прокси-сервером корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2f02c-106">Internet Authentication Service is the Microsoft implementation of a RADIUS server and proxy.</span></span>

<span data-ttu-id="2f02c-107">Служба проверки подлинности в Интернете поддерживает два набора API: [API расширений сервера политики сети](ias-extensions.md) и [API объектов данных сервера](server-data-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2f02c-107">Internet Authentication Service supports two API sets: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="2f02c-108">Дополнительные сведения о службе IAS см. в статье [TechNet: служба проверки подлинности в Интернете](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="2f02c-108">See [TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on IAS.</span></span>

## <a name="network-policy-server"></a><span data-ttu-id="2f02c-109">Сервер политики сети</span><span class="sxs-lookup"><span data-stu-id="2f02c-109">Network Policy Server</span></span>

<span data-ttu-id="2f02c-110">Сервер политики сети является реализацией корпорации Майкрософт сервера и прокси-сервера RADIUS и доступен на серверах Windows, начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2f02c-110">Network Policy Server is the Microsoft implementation of a RADIUS server and proxy and it is available on Windows servers starting with Windows Server 2008.</span></span>

<span data-ttu-id="2f02c-111">Сервер политики сети поддерживает те же два набора API, что и IAS: API [расширений сервера политики сети](ias-extensions.md) и [API объектов данных сервера](server-data-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2f02c-111">NPS supports the same two API sets as IAS: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="2f02c-112">Кроме того, NPS содержит набор новых функций, расширяющих возможности IAS.</span><span class="sxs-lookup"><span data-stu-id="2f02c-112">In addition, NPS contains a set of new features that expand the IAS capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2f02c-113">Функция</span><span class="sxs-lookup"><span data-stu-id="2f02c-113">Feature</span></span></th>
<th><span data-ttu-id="2f02c-114">Новые возможности NPS</span><span class="sxs-lookup"><span data-stu-id="2f02c-114">What's new for NPS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2f02c-115"><a href="/windows/desktop/NAP/network-access-protection-start-page">Защита доступа к сети (NAP)</a></span><span class="sxs-lookup"><span data-stu-id="2f02c-115"><a href="/windows/desktop/NAP/network-access-protection-start-page">Network Access Protection (NAP)</a></span></span><br/></td>
<td><span data-ttu-id="2f02c-116">NPS является центральным сервером защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="2f02c-116">NPS is the central server of Network Access Protection.</span></span><br/> <span data-ttu-id="2f02c-117">Сервер политики сети поддерживает создание политик с помощью следующих дополнительных условий.</span><span class="sxs-lookup"><span data-stu-id="2f02c-117">NPS supports policy authoring using the following additional conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="2f02c-118">Истечение срока действия политики.</span><span class="sxs-lookup"><span data-stu-id="2f02c-118">Policy expiration.</span></span></li>
<li><span data-ttu-id="2f02c-119">Версия операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2f02c-119">Operating system version.</span></span></li>
<li><span data-ttu-id="2f02c-120">Доступ к IP-адресу клиента.</span><span class="sxs-lookup"><span data-stu-id="2f02c-120">Access client IP address.</span></span></li>
<li><span data-ttu-id="2f02c-121">Политики работоспособности.</span><span class="sxs-lookup"><span data-stu-id="2f02c-121">Health policies.</span></span></li>
<li><span data-ttu-id="2f02c-122">Разрешенные типы EAP.</span><span class="sxs-lookup"><span data-stu-id="2f02c-122">Allowed EAP types.</span></span></li>
<li><span data-ttu-id="2f02c-123">Протокола.</span><span class="sxs-lookup"><span data-stu-id="2f02c-123">HCAP.</span></span></li>
</ul>
<span data-ttu-id="2f02c-124">Сервер политики сети поддерживает создание политик с помощью следующих дополнительных параметров:</span><span class="sxs-lookup"><span data-stu-id="2f02c-124">NPS supports policy authoring using the following additional settings:</span></span><br/>
<ul>
<li><span data-ttu-id="2f02c-125">Надзора.</span><span class="sxs-lookup"><span data-stu-id="2f02c-125">Probation.</span></span></li>
<li><span data-ttu-id="2f02c-126">Ограниченный доступ.</span><span class="sxs-lookup"><span data-stu-id="2f02c-126">Limited access.</span></span></li>
<li><span data-ttu-id="2f02c-127">Расширенное состояние для ограниченного доступа.</span><span class="sxs-lookup"><span data-stu-id="2f02c-127">Extended state for limited access.</span></span></li>
</ul>
<span data-ttu-id="2f02c-128">Сервер политики сети через NAP взаимодействует с CISCO NAC.</span><span class="sxs-lookup"><span data-stu-id="2f02c-128">NPS, through NAP, interoperates with CISCO NAC.</span></span><br/> <span data-ttu-id="2f02c-129">IAS не поддерживает NAP.</span><span class="sxs-lookup"><span data-stu-id="2f02c-129">IAS does not support NAP.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f02c-130"><a href="/windows/win32/eap/eap-start-page">Протокол EAP</a> Поддержка политик и <a href="/windows/win32/eaphost/portal">EAPHost</a></span><span class="sxs-lookup"><span data-stu-id="2f02c-130"><a href="/windows/win32/eap/eap-start-page">EAP</a> Policy and <a href="/windows/win32/eaphost/portal">EAPHost</a> Support</span></span><br/></td>
<td><span data-ttu-id="2f02c-131">NPS использует EAPHost для расширяемости методов EAP.</span><span class="sxs-lookup"><span data-stu-id="2f02c-131">NPS uses EAPHost for EAP method extensibility.</span></span> <span data-ttu-id="2f02c-132">Кроме того, администраторы могут настроить политику доступа к сети для EAP.</span><span class="sxs-lookup"><span data-stu-id="2f02c-132">Additionally, administrators may configure network access policy for EAP.</span></span><br/> <span data-ttu-id="2f02c-133">IAS не поддерживает интеграцию EAPHost или условия фильтра типа EAP для политик.</span><span class="sxs-lookup"><span data-stu-id="2f02c-133">IAS does not support EAPHost integration, or EAP type filter conditions for policies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f02c-134">Поддержка IPv6</span><span class="sxs-lookup"><span data-stu-id="2f02c-134">IPv6 Support</span></span><br/></td>
<td><span data-ttu-id="2f02c-135">Сервер политики сети поддерживает развертывание в средах IPv6.</span><span class="sxs-lookup"><span data-stu-id="2f02c-135">NPS supports deployment in IPv6 environments.</span></span><br/> <span data-ttu-id="2f02c-136">Служба IAS не поддерживает сетевые адреса IPv6.</span><span class="sxs-lookup"><span data-stu-id="2f02c-136">IAS does not support IPv6 network addresses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f02c-137">Конфигурация XML</span><span class="sxs-lookup"><span data-stu-id="2f02c-137">XML Configuration</span></span><br/></td>
<td><span data-ttu-id="2f02c-138">Конфигурацию NPS можно импортировать и экспортировать в формате XML.</span><span class="sxs-lookup"><span data-stu-id="2f02c-138">NPS configuration can be imported and exported in XML format.</span></span><br/> <span data-ttu-id="2f02c-139">Служба IAS использует базу данных Jet для хранения конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="2f02c-139">IAS is using a Jet database for storing service configuration.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f02c-140"><a href="https://www.niap-ccevs.org/cc-scheme/">Общие критерии</a> Технической</span><span class="sxs-lookup"><span data-stu-id="2f02c-140"><a href="https://www.niap-ccevs.org/cc-scheme/">Common Criteria</a> Support</span></span><br/></td>
<td><span data-ttu-id="2f02c-141">Сервер политики сети был обновлен для поддержки развертывания в средах, которые должны соответствовать стандартам безопасности общего критерия.</span><span class="sxs-lookup"><span data-stu-id="2f02c-141">NPS has been updated to support its deployment in environments that must meet the Common Criteria security standards.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f02c-142"><a href="ias-extensions.md">API расширений NPS</a></span><span class="sxs-lookup"><span data-stu-id="2f02c-142"><a href="ias-extensions.md">NPS Extensions API</a></span></span><br/></td>
<td><span data-ttu-id="2f02c-143">Библиотеки DLL расширения NPS выполняются в отдельном процессе из службы NPS.</span><span class="sxs-lookup"><span data-stu-id="2f02c-143">The NPS extension DLLs run in a separate process from the NPS service.</span></span> <span data-ttu-id="2f02c-144">Если произошел сбой DLL расширения, NPS продолжит работу и будущие запросы будут отклонены.</span><span class="sxs-lookup"><span data-stu-id="2f02c-144">Should an extension DLL crash, NPS will keep running and future requests will be rejected.</span></span><br/> <span data-ttu-id="2f02c-145">Библиотеки DLL расширения IAS выполняются в том же процессе, что и служба IAS, и могут негативно повлиять на работу службы.</span><span class="sxs-lookup"><span data-stu-id="2f02c-145">The IAS extension DLLs run in the same process as the IAS service and may adversely affect the service.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f02c-146">Пользовательский интерфейс управления</span><span class="sxs-lookup"><span data-stu-id="2f02c-146">Management User Interface</span></span><br/></td>
<td><span data-ttu-id="2f02c-147">Консоль управления NPS (NPS. msc) имеет новый вид, улучшенный способ использования и охватывает все новые функции, добавленные в NPS.</span><span class="sxs-lookup"><span data-stu-id="2f02c-147">The NPS management console (nps.msc) has a new look, improved usability, and covers all the new functionality added to NPS.</span></span><br/> <span data-ttu-id="2f02c-148">IAS использует консоль управления IAS. msc.</span><span class="sxs-lookup"><span data-stu-id="2f02c-148">IAS uses the ias.msc management console.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f02c-149">Интеграция средств управления ролями и диспетчер сервера</span><span class="sxs-lookup"><span data-stu-id="2f02c-149">Role Management Tool and Server Manager Integration</span></span><br/></td>
<td><span data-ttu-id="2f02c-150">Сервер политики сети интегрирован с диспетчер сервера и средством управления ролями.</span><span class="sxs-lookup"><span data-stu-id="2f02c-150">NPS is integrated with the Server Manager and the Role Management Tool.</span></span> <span data-ttu-id="2f02c-151">Такая интеграция упрощает настройку и управление NPS и связанными сценариями.</span><span class="sxs-lookup"><span data-stu-id="2f02c-151">This integration facilitates the configuration and management of NPS and related scenarios.</span></span><br/> <span data-ttu-id="2f02c-152">Диспетчер сервера недоступна на компьютерах, работающих под управлением службы IAS.</span><span class="sxs-lookup"><span data-stu-id="2f02c-152">Server Manager is not available on computers running IAS.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f02c-153">Обновлены сценарии командной строки с помощью команды <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">netsh</a>.</span><span class="sxs-lookup"><span data-stu-id="2f02c-153">Updated Command Line Scripting with <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">Netsh</a>.</span></span><br/></td>
<td><span data-ttu-id="2f02c-154">NPS поддерживает &quot; &quot; интерфейс командной строки netsh nps.</span><span class="sxs-lookup"><span data-stu-id="2f02c-154">NPS supports the &quot;Netsh nps&quot; command line interface.</span></span> <span data-ttu-id="2f02c-155">&quot;Netsh nps &quot; содержит новые команды, позволяющие полностью настроить NPS, включая функции защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="2f02c-155">&quot;Netsh nps&quot; contains new commands that permit to fully configure NPS, including NAP features.</span></span><br/> <span data-ttu-id="2f02c-156">Служба IAS поддерживает &quot; &quot; интерфейс командной строки Netsh AAAA.</span><span class="sxs-lookup"><span data-stu-id="2f02c-156">IAS supports the &quot;Netsh aaaa&quot; command line interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f02c-157">Изоляция политик</span><span class="sxs-lookup"><span data-stu-id="2f02c-157">Policy Isolation</span></span><br/></td>
<td><span data-ttu-id="2f02c-158">СЕРВЕР политики сети позволяет реализовать изоляцию политики, задавая источник политики сети.</span><span class="sxs-lookup"><span data-stu-id="2f02c-158">NPS enables the implementation of policy isolation by setting the Network Policy Source.</span></span> <span data-ttu-id="2f02c-159">Можно настроить политики, применимые только к предварительно определенному типу NAS.</span><span class="sxs-lookup"><span data-stu-id="2f02c-159">Policies can be configured that are applicable only to a predetermined NAS type.</span></span><br/> <span data-ttu-id="2f02c-160">IAS не поддерживает изоляцию политики.</span><span class="sxs-lookup"><span data-stu-id="2f02c-160">IAS does not support policy isolation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2f02c-161">Дополнительные сведения о NPS см. в статье [TechNet: сервер политики сети](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="2f02c-161">See [TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on NPS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f02c-162">См. также</span><span class="sxs-lookup"><span data-stu-id="2f02c-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f02c-163">Проверка подлинности, авторизация и учет RADIUS</span><span class="sxs-lookup"><span data-stu-id="2f02c-163">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="2f02c-164">Ведение журнала с помощью сервера политики сети</span><span class="sxs-lookup"><span data-stu-id="2f02c-164">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="2f02c-165">Работа с сервером состояний</span><span class="sxs-lookup"><span data-stu-id="2f02c-165">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

