---
title: Глоссарий служба удаленного управления Windows
description: Страница глоссария
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b6d7411063fbb117c68e211181142ac773f924
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105674573"
---
# <a name="windows-remote-management-glossary"></a><span data-ttu-id="a2847-103">Глоссарий служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="a2847-103">Windows Remote Management Glossary</span></span>


<dl> <dt>

<span data-ttu-id="a2847-104">WSMan: Items \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="a2847-104">\*\*\*\*wsman:Items\*\*\*\*</span></span>
</dt> <dd>

<span data-ttu-id="a2847-105">Элемент протокола WS-Management, возвращаемый в перечислении, который получает экземпляры и [*епрс*](/windows)экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a2847-105">A WS-Management protocol element returned in an enumeration that obtains both the instances and the instance [*EPRs*](/windows).</span></span> <span data-ttu-id="a2847-106">**WSMan: Items** — это контейнер, содержащий экземпляр и его EPR.</span><span class="sxs-lookup"><span data-stu-id="a2847-106">**wsman:Items** is a container that holds an instance and its EPR.</span></span> <span data-ttu-id="a2847-107">Этот тип перечисления инициируется, когда в запросе задан флаг **всманфлагретурнобжектандепр** .</span><span class="sxs-lookup"><span data-stu-id="a2847-107">This type of enumeration is initiated when the **WSManFlagReturnObjectAndEPR** flag is set in the request.</span></span>

</dd> </dl>

## <a name="b"></a><span data-ttu-id="a2847-108">B</span><span class="sxs-lookup"><span data-stu-id="a2847-108">B</span></span>

<dl> <dt>

<span data-ttu-id="a2847-109">**контроллер управления основной платой (BMC)**</span><span class="sxs-lookup"><span data-stu-id="a2847-109">**baseboard management controller (BMC)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-110">Микроконтроллер, подключенный локально к серверу.</span><span class="sxs-lookup"><span data-stu-id="a2847-110">A microcontroller attached locally to a server.</span></span> <span data-ttu-id="a2847-111">Контроллеры BMC имеют датчики, отслеживающие физическое состояние сервера и отдельное сетевое подключение, которое может взаимодействовать по сети, даже если сервер находится в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="a2847-111">BMCs have sensors that monitor the physical state of the server and a separate network connection that can communicate over the network, even if the server is offline.</span></span> <span data-ttu-id="a2847-112">У вас есть доступ к данным BMC через поставщик [*IPMI*](windows-remote-management-glossary.md) WMI.</span><span class="sxs-lookup"><span data-stu-id="a2847-112">You have access to BMC data through the [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md) WMI provider.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-113">**Обычная проверка подлинности**</span><span class="sxs-lookup"><span data-stu-id="a2847-113">**Basic authentication**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-114">Имя пользователя и пароль, отправленные в обмене данными проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a2847-114">The user name and password sent in the authentication exchange.</span></span> <span data-ttu-id="a2847-115">Обычную проверку подлинности можно настроить для использования транспорта HTTP или HTTPS в домене или рабочей группе.</span><span class="sxs-lookup"><span data-stu-id="a2847-115">Basic authentication can be configured to use either HTTP or HTTPS transport in a domain or workgroup.</span></span> <span data-ttu-id="a2847-116">Эта схема является наименее безопасным методом проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a2847-116">This method is the least secure method of authentication.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-117">**Контроллер управления основной платой (BMC)**</span><span class="sxs-lookup"><span data-stu-id="a2847-117">**BMC**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-118">См. раздел [*контроллер управления основной платой (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-118">See [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="a2847-119">C</span><span class="sxs-lookup"><span data-stu-id="a2847-119">C</span></span>

<dl> <dt>

<span data-ttu-id="a2847-120">**ПРОГРАММЕ**</span><span class="sxs-lookup"><span data-stu-id="a2847-120">**CIM**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-121">См. [*модель CIM (CIM)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-121">See [*Common Information Model (CIM)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-122">**компьютера**</span><span class="sxs-lookup"><span data-stu-id="a2847-122">**client**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-123">Клиентское приложение использует протокол WS-Management для доступа к службе управления на локальном или удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a2847-123">The client application using the WS-Management protocol to access the management service on either the local or a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-124">**Модель CIM**</span><span class="sxs-lookup"><span data-stu-id="a2847-124">**Common Information Model (CIM)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-125">Модель применения [*распределенной задачи управления (DMTF)*](windows-remote-management-glossary.md) , описывающая способ представления реальных компьютерных и сетевых объектов.</span><span class="sxs-lookup"><span data-stu-id="a2847-125">The [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md) model that describes how to represent real-world computer and network objects.</span></span> <span data-ttu-id="a2847-126">Модель CIM основана на парадигме объектно-ориентированного программирования, согласно которой объекты моделируются с использованием концепций классов и экземпляров.</span><span class="sxs-lookup"><span data-stu-id="a2847-126">CIM uses an object-oriented paradigm, where managed objects are modeled using the concepts of classes and instances.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="a2847-127">D</span><span class="sxs-lookup"><span data-stu-id="a2847-127">D</span></span>

<dl> <dt>

<span data-ttu-id="a2847-128">**Дайджест-аутентификация**</span><span class="sxs-lookup"><span data-stu-id="a2847-128">**Digest authentication**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-129">Exchange, где сервер получает запрос от клиента и отправляет данные о клиенте серверу проверки подлинности (обычно это контроллер домена).</span><span class="sxs-lookup"><span data-stu-id="a2847-129">An exchange wherein the server receives a request from a client and sends data about the client to an authenticating server, typically a domain controller.</span></span> <span data-ttu-id="a2847-130">При проверке подлинности клиента сервер получает ключ сеанса дайджеста, используемый для проверки подлинности последующих запросов от клиента.</span><span class="sxs-lookup"><span data-stu-id="a2847-130">If the client is authenticated, then the server receives a Digest session key used to authenticate subsequent requests from the client.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-131">**Распределенное управление задачей Force (DMTF)**</span><span class="sxs-lookup"><span data-stu-id="a2847-131">**Distributed Management Task Force (DMTF)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-132">Отраслевые организации разрабатывают стандарты управления и технологию интеграции для корпоративных и Интернет сред.</span><span class="sxs-lookup"><span data-stu-id="a2847-132">The industry organization developing management standards and integration technology for enterprise and Internet environments.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-133">**DMTF**</span><span class="sxs-lookup"><span data-stu-id="a2847-133">**DMTF**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-134">См. раздел [*распределенное управление Task Force (DMTF)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-134">See [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="a2847-135">E</span><span class="sxs-lookup"><span data-stu-id="a2847-135">E</span></span>

<dl> <dt>

<span data-ttu-id="a2847-136">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="a2847-136">**endpoint**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-137">Ресурс, к которому может обращаться [*ссылка на конечную точку (EPR)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-137">A resource that can be addressed by an [*endpoint reference (EPR)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-138">**Ссылка на конечную точку (EPR)**</span><span class="sxs-lookup"><span data-stu-id="a2847-138">**endpoint reference (EPR)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-139">Сочетание WS-Addressing и WS-Management элементов адресации, которые вместе описывают адрес ресурса в заголовке SOAP сообщения.</span><span class="sxs-lookup"><span data-stu-id="a2847-139">A combination of WS-Addressing and WS-Management addressing elements that together describe an address for a resource in the message SOAP header.</span></span> <span data-ttu-id="a2847-140">Это термин веб-службы.</span><span class="sxs-lookup"><span data-stu-id="a2847-140">This is a web service term.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-141">**перечисление**</span><span class="sxs-lookup"><span data-stu-id="a2847-141">**enumeration**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-142">Набор или коллекция экземпляров [*ресурсов*](windows-remote-management-glossary.md) или действие запроса такого набора.</span><span class="sxs-lookup"><span data-stu-id="a2847-142">A set, or collection, of [*resource*](windows-remote-management-glossary.md) instances or the action of requesting such a set.</span></span> <span data-ttu-id="a2847-143">В WS-Management протоколе [*WS-enumeration*](windows-remote-management-glossary.md) используется для получения коллекции.</span><span class="sxs-lookup"><span data-stu-id="a2847-143">In WS-Management protocol, [*WS-Enumeration*](windows-remote-management-glossary.md) is used to obtain the collection.</span></span> <span data-ttu-id="a2847-144">В реализации скриптов службы WinRM используется перечисление, [**Session. Enumerate**](session-enumerate.md) и объект [**перечислителя**](enumerator.md) .</span><span class="sxs-lookup"><span data-stu-id="a2847-144">In the WinRM service scripting implementation of enumeration, [**Session.Enumerate**](session-enumerate.md) and the [**Enumerator**](enumerator.md) object are used.</span></span> <span data-ttu-id="a2847-145">Соответствующий метод и интерфейс C++ — [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) и [**ивсманенумератор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span><span class="sxs-lookup"><span data-stu-id="a2847-145">The corresponding C++ method and interface are [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) and [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-146">**EPR**</span><span class="sxs-lookup"><span data-stu-id="a2847-146">**EPR**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-147">См. [*Справочник по конечной точке (EPR)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-147">See [*endpoint reference (EPR)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-148">**Служба сбора событий**</span><span class="sxs-lookup"><span data-stu-id="a2847-148">**Event Collection Service**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-149">Компонент операционной системы, который получает события от BMC и других компонентов или приложений операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a2847-149">The operating system component that receives events from the BMC and other operating system components or applications.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-150">**Пересылка событий**</span><span class="sxs-lookup"><span data-stu-id="a2847-150">**event forwarding**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-151">Уведомление о событиях, происходящих на удаленных компьютерах, может быть отправлено в приложение-подписчики.</span><span class="sxs-lookup"><span data-stu-id="a2847-151">A notification of events that occur on remote computers can be sent to subscribing applications.</span></span> <span data-ttu-id="a2847-152">Пересылка событий не является компонентом WinRM, а [журналом событий Windows](/windows/desktop/WES/windows-event-log).</span><span class="sxs-lookup"><span data-stu-id="a2847-152">Event forwarding is not a feature of WinRM, but of the [Windows Event Log](/windows/desktop/WES/windows-event-log).</span></span> <span data-ttu-id="a2847-153">Пересылка событий в Windows Vista стала доступной в первый раз.</span><span class="sxs-lookup"><span data-stu-id="a2847-153">Event forwarding becomes available for the first time in Windows Vista.</span></span> <span data-ttu-id="a2847-154">Приложения управления, такие как Microsoft Operations Manager (MOM), используют пересылку событий.</span><span class="sxs-lookup"><span data-stu-id="a2847-154">The Management applications, such as Microsoft Operations Manager (MOM) use event forwarding.</span></span>

</dd> </dl>

## <a name="f"></a><span data-ttu-id="a2847-155">C</span><span class="sxs-lookup"><span data-stu-id="a2847-155">F</span></span>

<dl> <dt>

<span data-ttu-id="a2847-156">**filter**</span><span class="sxs-lookup"><span data-stu-id="a2847-156">**filter**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-157">Механизм запросов для указания ограниченного набора экземпляров в запросе [*ресурса*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-157">A query mechanism for specifying a limited set of instances in the request for a [*resource*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="a2847-158">Параметр *фильтра* можно указать при вызовах метода [**Session. Enumerate**](session-enumerate.md) или [**IWSManSession:: reenumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="a2847-158">You can specify a *filter* parameter on calls to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-159">**Диалект фильтра**</span><span class="sxs-lookup"><span data-stu-id="a2847-159">**filter dialect**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-160">XML-строка, определяющая диалект XML, используемый для указания [*фильтра*](windows-remote-management-glossary.md) в вызове [**Session. Enumerate**](session-enumerate.md) или [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="a2847-160">An XML string that identifies the XML dialect used to specify a [*filter*](windows-remote-management-glossary.md) in a call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span> <span data-ttu-id="a2847-161">Служба WinRM поддерживает [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) в качестве диалекта фильтра при получении запросов.</span><span class="sxs-lookup"><span data-stu-id="a2847-161">The WinRM service supports [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) as a filter dialect when receiving requests.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-162">**экстент**</span><span class="sxs-lookup"><span data-stu-id="a2847-162">**fragment**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-163">XML-строка, идентифицирующая часть экземпляра ресурса, а не весь ресурс.</span><span class="sxs-lookup"><span data-stu-id="a2847-163">An XML string that identifies part of an instance of a resource rather than the entire resource.</span></span> <span data-ttu-id="a2847-164">Поддержка фрагментов находится в объекте [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="a2847-164">Fragment support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-165">**диалект фрагмента**</span><span class="sxs-lookup"><span data-stu-id="a2847-165">**fragment dialect**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-166">XML-строка, определяющая диалект XML, используемый для указания [*фрагмента*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-166">An XML string that identifies the XML dialect used to specify a [*fragment*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="a2847-167">Поддержка фрагментов находится в объекте [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="a2847-167">Fragment support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="a2847-168">Служба удаленного управления Windows поддерживает [*XPath*](windows-remote-management-glossary.md) для диалекта фрагмента при получении запросов.</span><span class="sxs-lookup"><span data-stu-id="a2847-168">The WinRM service supports [*XPath*](windows-remote-management-glossary.md) for fragment dialect when receiving requests.</span></span>

</dd> </dl>

## <a name="i"></a><span data-ttu-id="a2847-169">I</span><span class="sxs-lookup"><span data-stu-id="a2847-169">I</span></span>

<dl> <dt>

<span data-ttu-id="a2847-170">**в основном**</span><span class="sxs-lookup"><span data-stu-id="a2847-170">**in-band**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-171">Клиентское приложение получает данные BMC через [*прослушиватель*](windows-remote-management-glossary.md) WinRM в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="a2847-171">The client application obtains BMC data through the WinRM [*listener*](windows-remote-management-glossary.md) in the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-172">**Интеллектуальный интерфейс управления платформой (IPMI)**</span><span class="sxs-lookup"><span data-stu-id="a2847-172">**Intelligent Platform Management Interface (IPMI)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-173">Промышленный стандарт ИТ для архитектуры [*контроллера управления основной платой (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-173">An IT industry standard for the architecture of [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="a2847-174">Функции управления оборудованием Windows предоставляют [*драйвер IPMI*](windows-remote-management-glossary.md) и [*поставщик IPMI*](windows-remote-management-glossary.md) WMI, позволяющий сценариям управления, средствам командной строки и приложениям получать данные BMC.</span><span class="sxs-lookup"><span data-stu-id="a2847-174">The Windows hardware management features supply an [*IPMI driver*](windows-remote-management-glossary.md) and a WMI [*IPMI provider*](windows-remote-management-glossary.md) that allow management scripts, command-line tools, and applications to obtain BMC data.</span></span> <span data-ttu-id="a2847-175">Поставщик IPMI имеет [классы](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI.</span><span class="sxs-lookup"><span data-stu-id="a2847-175">The IPMI provider has WMI [classes](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-176">**IPMI**</span><span class="sxs-lookup"><span data-stu-id="a2847-176">**IPMI**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-177">См. раздел [*интерфейс интеллектуального управления платформой (ИМПИ)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-177">See [*Intelligent Platform Management Interface (IMPI)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-178">**Драйвер IPMI**</span><span class="sxs-lookup"><span data-stu-id="a2847-178">**IPMI driver**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-179">Драйвер ядра, обеспечивающий доступ к устройствам [*контроллера управления основной платой (BMC)*](windows-remote-management-glossary.md) из компонентов операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a2847-179">The kernel driver that enables access to [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) devices from the operating system components.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-180">**Поставщик IPMI**</span><span class="sxs-lookup"><span data-stu-id="a2847-180">**IPMI provider**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-181">Стандартный поставщик WMI, определяющий классы, моделирующие [*IPMI*](windows-remote-management-glossary.md) и его данные.</span><span class="sxs-lookup"><span data-stu-id="a2847-181">A standard WMI provider that defines classes modeling the [*IPMI*](windows-remote-management-glossary.md) and its data.</span></span> <span data-ttu-id="a2847-182">[Поставщик IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) — это COM-библиотека DLL, которая получает данные из BMC.</span><span class="sxs-lookup"><span data-stu-id="a2847-182">The [IPMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) is a COM DLL that obtains data from the BMC.</span></span>

</dd> </dl>

## <a name="k"></a><span data-ttu-id="a2847-183">K</span><span class="sxs-lookup"><span data-stu-id="a2847-183">K</span></span>

<dl> <dt>

<span data-ttu-id="a2847-184">**ккс**</span><span class="sxs-lookup"><span data-stu-id="a2847-184">**KCS**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-185">См. раздел [*тип контроллера клавиатуры (ККС)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-185">See [*Keyboard Controller Style (KCS)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-186">**Проверка подлинности Kerberos**</span><span class="sxs-lookup"><span data-stu-id="a2847-186">**Kerberos authentication**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-187">Метод взаимной проверки подлинности между клиентом и сервером, который использует зашифрованные ключи.</span><span class="sxs-lookup"><span data-stu-id="a2847-187">A method of mutual authentication between the client and server that uses encrypted keys.</span></span> <span data-ttu-id="a2847-188">Для компьютеров, работающих под управлением операционной системы Windows, учетная запись клиента должна быть учетной записью домена в том же домене, что и сервер.</span><span class="sxs-lookup"><span data-stu-id="a2847-188">For computers running on a Windows-based operating system, the client account must be a domain account in the same domain as the server.</span></span> <span data-ttu-id="a2847-189">Если клиент использует учетные данные по умолчанию, Kerberos является методом проверки подлинности, если строка подключения не является одним из следующих: localhost, 127.0.0.1 или \[ :: 1 \] .</span><span class="sxs-lookup"><span data-stu-id="a2847-189">When a client uses default credentials, Kerberos is the authentication method if the connection string is not one of the following: localhost, 127.0.0.1, or \[::1\].</span></span>

</dd> <dt>

<span data-ttu-id="a2847-190">**Стиль контроллера клавиатуры (ККС)**</span><span class="sxs-lookup"><span data-stu-id="a2847-190">**Keyboard Controller Style (KCS)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-191">Протокол, используемый [*драйвером IPMI*](windows-remote-management-glossary.md) для обмена данными с [*контроллером управления основной платой (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-191">The protocol used by the [*IPMI driver*](windows-remote-management-glossary.md) to communicate with the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="a2847-192">L</span><span class="sxs-lookup"><span data-stu-id="a2847-192">L</span></span>

<dl> <dt>

<span data-ttu-id="a2847-193">**listener**</span><span class="sxs-lookup"><span data-stu-id="a2847-193">**listener**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-194">Служба управления, реализующая протокол WS-Management для отправки и получения сообщений.</span><span class="sxs-lookup"><span data-stu-id="a2847-194">A management service that implements WS-Management protocol to send and receive messages.</span></span> <span data-ttu-id="a2847-195">WinRM — это служба прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="a2847-195">WinRM is a listener service.</span></span> <span data-ttu-id="a2847-196">Прослушиватель определяется транспортом (HTTP или HTTPS) и адресом IPv4 или IPv6.</span><span class="sxs-lookup"><span data-stu-id="a2847-196">A listener is defined by a transport (HTTP or HTTPS) and an IPv4 or IPv6 address.</span></span> <span data-ttu-id="a2847-197">Можно создать несколько экземпляров прослушивателя WinRM на одном компьютере, предоставив им разные TCP/IP-адреса или номера портов.</span><span class="sxs-lookup"><span data-stu-id="a2847-197">You can create more than one WinRM listener instance on a single computer by giving them a different TCP/IP address or port number.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="a2847-198">M</span><span class="sxs-lookup"><span data-stu-id="a2847-198">M</span></span>

<dl> <dt>

<span data-ttu-id="a2847-199">**message**</span><span class="sxs-lookup"><span data-stu-id="a2847-199">**message**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-200">Пакет сведений, передаваемых между компьютерами или отдельными сетями, созданными с помощью протокола [*SOAP*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="a2847-200">A package of information transmitted between computers or separate networks constructed with the [*SOAP*](windows-remote-management-glossary.md) protocol.</span></span> <span data-ttu-id="a2847-201">Пакет содержит заголовок, описывающий цель сообщения и транспорт, а также текст, который содержит содержимое, используемое при поступлении сообщения.</span><span class="sxs-lookup"><span data-stu-id="a2847-201">The package has a header, that describes the message target and transport, and a body that contains the content to be used when the message arrives.</span></span> <span data-ttu-id="a2847-202">Сообщение представляет собой сочетание элементов из таких спецификаций, как [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-*](windows-remote-management-glossary.md)Play и [*WS-Management*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-202">A message is a combination of elements from specifications such as [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md), and [*WS-Management*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="a2847-203">Нет</span><span class="sxs-lookup"><span data-stu-id="a2847-203">N</span></span>

<dl> <dt>

<span data-ttu-id="a2847-204">**namespace**</span><span class="sxs-lookup"><span data-stu-id="a2847-204">**namespace**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-205">Пространство имен [*WMI*](windows-remote-management-glossary.md) , которое является логическим группированием классов и экземпляров WMI для управления областью и доступом.</span><span class="sxs-lookup"><span data-stu-id="a2847-205">A [*WMI*](windows-remote-management-glossary.md) namespace, which is a logical grouping of WMI classes and instances to control scope and access.</span></span> <span data-ttu-id="a2847-206">Наиболее частым источником данных управления для систем под управлением Windows является корневое \\ пространство имен CIMV2, которое содержит классы, такие как [**\_ процесс Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="a2847-206">The most frequent source of management data for systems running Windows is the root\\cimv2 namespace, which contains classes such as [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span> <span data-ttu-id="a2847-207">Пространства имен отображаются в URI ресурса для классов WMI, например https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service .</span><span class="sxs-lookup"><span data-stu-id="a2847-207">Namespaces appear in the resource URI for WMI classes, for example https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-208">**Согласование проверки подлинности**</span><span class="sxs-lookup"><span data-stu-id="a2847-208">**Negotiate authentication**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-209">Согласованный тип проверки подлинности с одним входом, который является реализацией Windows для [*простого и защищенного механизма согласования GSSAPI (SPNEGO)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-209">A negotiated, single sign on type of authentication that is the Windows implementation of [*Simple and Protected GSSAPI Negotiation Mechanism (SPNEGO)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="a2847-210">Согласование SPNEGO определяет, обрабатывается ли проверка подлинности Kerberos или NTLM.</span><span class="sxs-lookup"><span data-stu-id="a2847-210">SPNEGO negotiation determines whether authentication is handled by Kerberos or NTLM.</span></span> <span data-ttu-id="a2847-211">Протокол Kerberos является предпочтительным механизмом.</span><span class="sxs-lookup"><span data-stu-id="a2847-211">Kerberos is the preferred mechanism.</span></span> <span data-ttu-id="a2847-212">Согласование проверки подлинности в системах на основе Windows называется также встроенной проверкой подлинности Windows.</span><span class="sxs-lookup"><span data-stu-id="a2847-212">Negotiate authentication on Windows-based systems is also called Windows Integrated Authentication.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-213">**числовой датчик**</span><span class="sxs-lookup"><span data-stu-id="a2847-213">**numeric sensor**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-214">Числовой тип датчика в [*контроллере управления основной платой (BMC)*](windows-remote-management-glossary.md), например "температура" или "напряжение".</span><span class="sxs-lookup"><span data-stu-id="a2847-214">A numeric type of sensor in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md), for example temperature or voltage.</span></span>

</dd> </dl>

## <a name="o"></a><span data-ttu-id="a2847-215">O</span><span class="sxs-lookup"><span data-stu-id="a2847-215">O</span></span>

<dl> <dt>

<span data-ttu-id="a2847-216">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="a2847-216">**option**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-217">Дополнительные данные, необходимые поставщику ресурсов для обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="a2847-217">The additional data required by the resource provider to process a request.</span></span> <span data-ttu-id="a2847-218">Например, некоторым поставщикам WMI требуются дополнительные данные, предоставляемые в виде объектов [**ивбемконтекст**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) или [**свбемнамедвалуесет**](/windows/desktop/WmiSdk/swbemnamedvalueset) .</span><span class="sxs-lookup"><span data-stu-id="a2847-218">For example, some WMI providers require additional data supplied as [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) or [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) objects.</span></span> <span data-ttu-id="a2847-219">Поддержка параметров находится в объекте [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="a2847-219">Option support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-220">**Внештатный**</span><span class="sxs-lookup"><span data-stu-id="a2847-220">**out-of-band**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-221">Клиентское приложение получает данные непосредственно из [*контроллера управления основной платой (BMC)*](windows-remote-management-glossary.md) другого компьютера, а не с помощью [*прослушивателя*](windows-remote-management-glossary.md) WinRM в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="a2847-221">The client application obtains data directly from the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) of another computer, rather than through the WinRM [*listener*](windows-remote-management-glossary.md) in the operating system.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="a2847-222">С</span><span class="sxs-lookup"><span data-stu-id="a2847-222">P</span></span>

<dl> <dt>

<span data-ttu-id="a2847-223">**собирает**</span><span class="sxs-lookup"><span data-stu-id="a2847-223">**pull**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-224">Для продолжения перечисления, запущенного начальным вызовом WS-enumeration: Enumerate, отправляется сообщение о вытягивание [*WS-enumeration*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="a2847-224">A [*WS-Enumeration*](windows-remote-management-glossary.md) pull message is sent to continue an enumeration started by an initial call to WS-Enumeration:Enumerate.</span></span> <span data-ttu-id="a2847-225">Операция извлечения в службе WinRM выполняется [**перечислителем. ReadItem**](enumerator-readitem.md) или [**Ивсманенумератор:: ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).</span><span class="sxs-lookup"><span data-stu-id="a2847-225">The pull operation in the WinRM service is performed by [**Enumerator.ReadItem**](enumerator-readitem.md) or [**IWSManEnumerator::ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).</span></span>

</dd> </dl>

## <a name="r"></a><span data-ttu-id="a2847-226">R</span><span class="sxs-lookup"><span data-stu-id="a2847-226">R</span></span>

<dl> <dt>

<span data-ttu-id="a2847-227">**ресурсов**</span><span class="sxs-lookup"><span data-stu-id="a2847-227">**resource**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-228">[*Конечная точка*](windows-remote-management-glossary.md) , представляющая отдельный тип операции управления или значение.</span><span class="sxs-lookup"><span data-stu-id="a2847-228">An [*endpoint*](windows-remote-management-glossary.md) that represents a distinct type of management operation or value.</span></span> <span data-ttu-id="a2847-229">Служба предоставляет один или несколько ресурсов, а некоторые ресурсы могут иметь более одного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a2847-229">A service exposes one or more resources and some resources can have more than one instance.</span></span> <span data-ttu-id="a2847-230">Ресурс управления аналогичен классу WMI или таблице базы данных, а экземпляр похож на экземпляр класса или строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="a2847-230">A management resource is similar to a WMI class or a database table, and an instance is similar to an instance of the class or a row in the table.</span></span> <span data-ttu-id="a2847-231">Например, класс [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) представляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="a2847-231">For example, the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class represents a resource.</span></span> <span data-ttu-id="a2847-232">`Win32_LogicalDisk="C:\"` — Это конкретный экземпляр ресурса.</span><span class="sxs-lookup"><span data-stu-id="a2847-232">`Win32_LogicalDisk="C:\"` is a specific instance of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-233">**URI ресурса**</span><span class="sxs-lookup"><span data-stu-id="a2847-233">**resource URI**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-234">[*Универсальный код ресурса (URI)*](windows-remote-management-glossary.md) , используемый для идентификации определенного типа ресурса, например дисков или процессов, в системе.</span><span class="sxs-lookup"><span data-stu-id="a2847-234">The [*uniform resource identifier (URI)*](windows-remote-management-glossary.md) used to identify a specific type of resource, such as disks or processes, on a system.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="a2847-235">S</span><span class="sxs-lookup"><span data-stu-id="a2847-235">S</span></span>

<dl> <dt>

<span data-ttu-id="a2847-236">**SEL**</span><span class="sxs-lookup"><span data-stu-id="a2847-236">**SEL**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-237">См. раздел [*журнал системных событий (SEL)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-237">See [*System Event Log (SEL)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-238">**Адаптер SEL**</span><span class="sxs-lookup"><span data-stu-id="a2847-238">**SEL adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-239">Адаптер, отправляющий данные [*контроллера управления основной платой (BMC)*](windows-remote-management-glossary.md) в [*сборщик событий*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-239">The adapter that sends [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) data to the [*Event Collector*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-240">**selector**</span><span class="sxs-lookup"><span data-stu-id="a2847-240">**selector**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-241">Пара имя и значение, представляющая конкретный экземпляр [*ресурса*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-241">A name and value pair that represents a particular instance of a [*resource*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="a2847-242">По сути, это фильтр или ключ, определяющий нужный экземпляр ресурса.</span><span class="sxs-lookup"><span data-stu-id="a2847-242">This is essentially a filter or "key" that identifies the desired instance of the resource.</span></span> <span data-ttu-id="a2847-243">Поддержка селектора находится в объекте [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="a2847-243">Selector support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-244">**датчика**</span><span class="sxs-lookup"><span data-stu-id="a2847-244">**sensor**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-245">Устройство измерения в [*контроллере управления основной платой (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-245">A measurement device in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-246">**служеб**</span><span class="sxs-lookup"><span data-stu-id="a2847-246">**service**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-247">Приложение, предоставляющее службы управления клиентам через протокол WS-Management и другие [*веб-службы*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-247">An application that provides management services to clients through the WS-Management protocol and other [*web services*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="a2847-248">Служба обычно совпадает с [*прослушивателем*](windows-remote-management-glossary.md) в сети.</span><span class="sxs-lookup"><span data-stu-id="a2847-248">A service is usually the same as the [*listener*](windows-remote-management-glossary.md) on a network.</span></span> <span data-ttu-id="a2847-249">Служба имеет физический адрес транспорта.</span><span class="sxs-lookup"><span data-stu-id="a2847-249">The service has a physical transport address.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-250">**сессии**</span><span class="sxs-lookup"><span data-stu-id="a2847-250">**session**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-251">Подключение между [*клиентом*](windows-remote-management-glossary.md) служба удаленного управления Windows и локальным или удаленным [*прослушивателем*](windows-remote-management-glossary.md)WinRM или службой.</span><span class="sxs-lookup"><span data-stu-id="a2847-251">A connection between a Windows Remote Management [*client*](windows-remote-management-glossary.md) and the local or remote WinRM [*listener*](windows-remote-management-glossary.md), or service.</span></span> <span data-ttu-id="a2847-252">Это соединение аналогично соединению между клиентским скриптом WMI и WMI на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="a2847-252">This connection is similar to the connection between a WMI client script and WMI on a remote server.</span></span> <span data-ttu-id="a2847-253">Операции сеанса, такие как перечисление ресурса (перечисление), получение экземпляра ресурса (Get) или выполнение метода ресурса (Invoke), являются методами объекта **Session** .</span><span class="sxs-lookup"><span data-stu-id="a2847-253">The session operations, such as enumerating a resource (Enumerate), getting an instance of a resource (Get), or running a resource method (Invoke) are methods of the **Session** object.</span></span> <span data-ttu-id="a2847-254">Объект **сеанса** создается с помощью [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-254">A **Session** object is created by [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-255">**Простой и защищенный механизм согласования API GSS (SPNEGO)**</span><span class="sxs-lookup"><span data-stu-id="a2847-255">**Simple and Protected GSS-API Negotiation Mechanism (SPNEGO)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-256">Механизм проверки подлинности, используемый клиентом или сервером для получения запросов данных через службу WinRM в контексте Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a2847-256">An authentication mechanism used by the client or server receiving requests for data through the WinRM in an Active Directory context.</span></span> <span data-ttu-id="a2847-257">Интерфейс SPNEGO основан на протоколе RFC, созданном с помощью IETF.</span><span class="sxs-lookup"><span data-stu-id="a2847-257">SPNEGO is based on an Request For Comments (RFC) protocol produced by the Internet Engineering Task Force (IETF).</span></span> <span data-ttu-id="a2847-258">SPNEGO также называется [*встроенной проверкой подлинности Windows*](windows-remote-management-glossary.md), термином, используемым в разделах справки служба удаленного управления Windows.</span><span class="sxs-lookup"><span data-stu-id="a2847-258">SPNEGO is also known as [*Windows Integrated Authentication*](windows-remote-management-glossary.md), the term used in the Windows Remote Management help topics.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-259">**Simple Object Access Protocol (протокол простого доступа к объектам, SOAP)**</span><span class="sxs-lookup"><span data-stu-id="a2847-259">**Simple Object Access Protocol (SOAP)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-260">Протокол на основе XML, используемый веб-службами.</span><span class="sxs-lookup"><span data-stu-id="a2847-260">An XML-based protocol used by web services.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-261">**Протокол SOAP**</span><span class="sxs-lookup"><span data-stu-id="a2847-261">**SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-262">См. раздел [*протокол протокола SOAP*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-262">See [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-263">**SPNEGO**</span><span class="sxs-lookup"><span data-stu-id="a2847-263">**SPNEGO**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-264">См. раздел [*простой и защищенный механизм согласования API GSS (SPNEGO)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-264">See [*Simple and Protected GSS-API Negotiation Mechanism (SPNEGO)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-265">**Журнал системных событий (SEL)**</span><span class="sxs-lookup"><span data-stu-id="a2847-265">**System Event Log (SEL)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-266">База данных событий на оборудовании [*контроллера управления основной платой (BMC)*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="a2847-266">The database of events in the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) hardware.</span></span> <span data-ttu-id="a2847-267">[*Адаптер SEL*](windows-remote-management-glossary.md) передает эти события в операционную систему.</span><span class="sxs-lookup"><span data-stu-id="a2847-267">The [*SEL adapter*](windows-remote-management-glossary.md) conveys these events to the operating system.</span></span>

</dd> </dl>

## <a name="u"></a><span data-ttu-id="a2847-268">U</span><span class="sxs-lookup"><span data-stu-id="a2847-268">U</span></span>

<dl> <dt>

<span data-ttu-id="a2847-269">**универсальный код ресурса (URI)**</span><span class="sxs-lookup"><span data-stu-id="a2847-269">**uniform resource identifier (URI)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-270">Строка, определяющая ресурс на предприятии, например компьютер, процесс, дисковый накопитель или датчик температуры в [*контроллере управления основной платой (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-270">A string that identifies a resource in the enterprise, such as a computer, a process, a disk drive, or a temperature sensor in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="a2847-271">Универсальный код ресурса (URI) — это механизм адресации веб-службы, определенный в универсальном коде ресурсов (URI) Web Service Task Force (IETF): универсальный синтаксис \[ RFC3986 \] .</span><span class="sxs-lookup"><span data-stu-id="a2847-271">The URI is the web service addressing mechanism defined in Internet Engineering Task Force (IETF) Uniform Resource Identifier (URI): Generic Syntax \[RFC3986\].</span></span>

</dd> <dt>

<span data-ttu-id="a2847-272">**URI**</span><span class="sxs-lookup"><span data-stu-id="a2847-272">**URI**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-273">См. раздел [*универсальный код ресурса (URI)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-273">See [*uniform resource identifier (URI)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="w"></a><span data-ttu-id="a2847-274">W</span><span class="sxs-lookup"><span data-stu-id="a2847-274">W</span></span>

<dl> <dt>

<span data-ttu-id="a2847-275">**веб-служба**</span><span class="sxs-lookup"><span data-stu-id="a2847-275">**web service**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-276">Программное приложение, используемое для взаимодействия между компьютерами через Интернет или сеть.</span><span class="sxs-lookup"><span data-stu-id="a2847-276">A software application used for interaction between computers across the Internet or a network.</span></span> <span data-ttu-id="a2847-277">Веб-службы описаны на [*языке описания веб-служб (WSDL)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-277">Web services are described by the [*Web Service Description Language (WSDL)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="a2847-278">Конкретное описание веб-службы указывает другим службам, как взаимодействовать с веб-службой с помощью сообщений SOAP.</span><span class="sxs-lookup"><span data-stu-id="a2847-278">The specific description of the web service tells other services how to interact with the web service by using SOAP messages.</span></span> <span data-ttu-id="a2847-279">Сообщения передаются между компьютерами транспортом, обычно HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a2847-279">The messages are conveyed between computers by a transport, typically HTTP or HTTPS.</span></span> <span data-ttu-id="a2847-280">В качестве примеров протоколов, используемых приложениями веб-служб для взаимодействия друг с другом, можно использовать [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Eventing*](windows-remote-management-glossary.md)и [*WS-Management*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="a2847-280">[*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Eventing*](windows-remote-management-glossary.md), and [*WS-Management*](windows-remote-management-glossary.md) are examples of protocols used by web service applications to communicate with each other.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-281">**Язык описания веб-служб (WSDL)**</span><span class="sxs-lookup"><span data-stu-id="a2847-281">**Web Service Description Language (WSDL)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-282">Язык на основе XML, используемый для определения способа взаимодействия с веб-службой.</span><span class="sxs-lookup"><span data-stu-id="a2847-282">An XML-based language used to define how to interact with a web service.</span></span> <span data-ttu-id="a2847-283">Как правило, WSDL описывает, какие сообщения SOAP требуются веб-службе для возврата данных или выполнения операций.</span><span class="sxs-lookup"><span data-stu-id="a2847-283">Typically, the WSDL describes what SOAP messages the web service requires to return data or carry out operations.</span></span> <span data-ttu-id="a2847-284">ЯЗЫК WSDL позволяет реализовать взаимодействие одной операционной системы с веб-службой, реализованной в другой операционной системе, при условии, что требования WSDL выполнены.</span><span class="sxs-lookup"><span data-stu-id="a2847-284">The WSDL allows an implementation from one operating system to communicate with the web service implemented on another operating system, as long as the requirements of the WSDL are met.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-285">**Встроенная проверка подлинности Windows**</span><span class="sxs-lookup"><span data-stu-id="a2847-285">**Windows Integrated Authentication**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-286">См. раздел [*согласование проверки подлинности*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-286">See [*Negotiate authentication*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-287">**Инструментарий управления Windows (WMI)**</span><span class="sxs-lookup"><span data-stu-id="a2847-287">**Windows Management Instrumentation (WMI)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-288">Реализация корпорации Майкрософт стандарта управления предприятием Web-Based Enterprise (WBEM), опубликованная [*распределенным управлением Task Force (DMTF)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-288">The Microsoft implementation of the Web-Based Enterprise Management (WBEM) standard published by the [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="a2847-289">Инструментарий WMI позволяет управлять локальными и удаленными компьютерами и моделями компьютеров и сетевых объектов с помощью расширения стандарта [*модель CIM (CIM)*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="a2847-289">WMI allows you to manage local and remote computers and models computer and network objects using an extension of the [*Common Information Model (CIM)*](windows-remote-management-glossary.md) standard.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-290">**Удаленное управление Windows (WinRM)**</span><span class="sxs-lookup"><span data-stu-id="a2847-290">**Windows Remote Management (WinRM)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-291">Реализация веб-службы управления Майкрософт на основе общедоступного стандартного протокола [*WS-Management*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="a2847-291">The Microsoft implementation of a management web service based on the public standard [*WS-Management*](windows-remote-management-glossary.md) protocol.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-292">**Оболочка Windows Remote Shell (WinRS)**</span><span class="sxs-lookup"><span data-stu-id="a2847-292">**Windows Remote Shell (WinRS)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-293">Средство оболочки, использующее [*Служба удаленного управления Windows*](windows-remote-management-glossary.md) для выполнения удаленных команд, особенно для серверов без монитора.</span><span class="sxs-lookup"><span data-stu-id="a2847-293">A shell tool that relies on [*Windows Remote Management*](windows-remote-management-glossary.md) to execute remote commands, especially for headless servers.</span></span> <span data-ttu-id="a2847-294">Программа командной строки — WinRS.</span><span class="sxs-lookup"><span data-stu-id="a2847-294">The command-line tool is Winrs.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-295">**WMI**</span><span class="sxs-lookup"><span data-stu-id="a2847-295">**WMI**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-296">См. раздел [*инструментарий управления Windows (WMI) (WMI)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-296">See [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2847-297">**Подключаемый модуль WMI**</span><span class="sxs-lookup"><span data-stu-id="a2847-297">**WMI plug-in**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-298">Подключаемый модуль WinRM, который делает данные WMI доступными для клиентов WinRM.</span><span class="sxs-lookup"><span data-stu-id="a2847-298">The WinRM plug-in that makes WMI data available to WinRM clients.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-299">**WS-Addressing (WSA)**</span><span class="sxs-lookup"><span data-stu-id="a2847-299">**WS-Addressing (wsa)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-300">Общедоступный стандартный протокол, основанный на SOAP, который создает систему адресации, используемую в заголовках сообщений, отправляемых через Интернет.</span><span class="sxs-lookup"><span data-stu-id="a2847-300">A public standard protocol, which is SOAP-based, that creates an addressing system used in the headers of messages sent across the Internet.</span></span> <span data-ttu-id="a2847-301">Стандарт определяет, как ресурсы могут располагаться в сетях и брандмауэрах.</span><span class="sxs-lookup"><span data-stu-id="a2847-301">The standard defines how resources can be located across networks and firewalls.</span></span> <span data-ttu-id="a2847-302">WS-Addressing является одним из протоколов веб-служб, составляющих протокол WS-Management.</span><span class="sxs-lookup"><span data-stu-id="a2847-302">WS-Addressing is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-303">**WS-enumeration (Всен)**</span><span class="sxs-lookup"><span data-stu-id="a2847-303">**WS-Enumeration (wsen)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-304">Общедоступный стандартный протокол, основанный на SOAP, для перечисления последовательности XML-элементов, которые могут представлять коллекции данных, журналы или другие структуры линейной информации.</span><span class="sxs-lookup"><span data-stu-id="a2847-304">A public standard protocol, which is SOAP-based, for enumerating a sequence of XML elements that may represent data collections, logs, or other linear information structures.</span></span> <span data-ttu-id="a2847-305">WS-Enumeration является одним из протоколов веб-служб, составляющих протокол WS-Management.</span><span class="sxs-lookup"><span data-stu-id="a2847-305">WS-Enumeration is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-306">**WS-Eventing (WSE)**</span><span class="sxs-lookup"><span data-stu-id="a2847-306">**WS-Eventing (wse)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-307">Общедоступный стандартный протокол, основанный на SOAP, который позволяет одной веб-службе (подписчику) подписываться и принимать сообщения уведомления о событиях от другой веб-службы (источника событий).</span><span class="sxs-lookup"><span data-stu-id="a2847-307">A public standard protocol, which is SOAP-based, that allows one web service (the subscriber) to subscribe to and accept event notification messages from another web service (the event source).</span></span> <span data-ttu-id="a2847-308">WS-Eventing является одним из протоколов веб-служб, составляющих протокол WS-Management.</span><span class="sxs-lookup"><span data-stu-id="a2847-308">WS-Eventing is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-309">**WS-Management**</span><span class="sxs-lookup"><span data-stu-id="a2847-309">**WS-Management**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-310">Общедоступный стандартный протокол, основанный на SOAP, для обмена данными управления между всеми операционными системами, компьютерами и устройствами.</span><span class="sxs-lookup"><span data-stu-id="a2847-310">A public standard protocol, which is SOAP-based, for sharing management data among all operating systems, computers, and devices.</span></span> <span data-ttu-id="a2847-311">Этот протокол используется всеми [*сообщениями*](windows-remote-management-glossary.md) , отправляемыми клиентскими или серверными компонентами WinRM.</span><span class="sxs-lookup"><span data-stu-id="a2847-311">All [*messages*](windows-remote-management-glossary.md) sent by the WinRM client or server components use this protocol.</span></span>

</dd> <dt>

<span data-ttu-id="a2847-312">**WS-перенаправление (вксф)**</span><span class="sxs-lookup"><span data-stu-id="a2847-312">**WS-Transfer (wxf)**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-313">Общедоступный стандартный протокол, основанный на SOAP, для доступа к XML-представлениям ресурсов на основе веб-служб через простой набор команд, таких как Get, WHERE, Invoke или DELETE.</span><span class="sxs-lookup"><span data-stu-id="a2847-313">A public standard protocol, which is SOAP-based, for accessing XML representations of web service-based resources through a simple set of verbs such as Get, Put, Invoke, or Delete.</span></span> <span data-ttu-id="a2847-314">WS-Transfer определяет операции для отправки и получения представления определенного ресурса и операций для создания или удаления ресурса и соответствующего представления.</span><span class="sxs-lookup"><span data-stu-id="a2847-314">WS-Transfer defines operations for sending and receiving the representation of a particular resource and operations for creating or deleting a resource and its corresponding representation.</span></span>

</dd> </dl>

## <a name="x"></a><span data-ttu-id="a2847-315">X</span><span class="sxs-lookup"><span data-stu-id="a2847-315">X</span></span>

<dl> <dt>

<span data-ttu-id="a2847-316">**XPath**</span><span class="sxs-lookup"><span data-stu-id="a2847-316">**XPath**</span></span>
</dt> <dd>

<span data-ttu-id="a2847-317">Нотация пути для адресации частей XML-документа, аналогичная URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="a2847-317">A path notation for addressing parts of an XML document, similar to a URL.</span></span> <span data-ttu-id="a2847-318">Выражение XPath — это последовательность фраз, которую необходимо получить из текущего расположения в XML-документе на другой узел или набор узлов.</span><span class="sxs-lookup"><span data-stu-id="a2847-318">An XPath expression is a sequence of phrases to get from the current location in the XML document to another node or set of nodes.</span></span> <span data-ttu-id="a2847-319">Фразы разделяются символами косой черты ("/").</span><span class="sxs-lookup"><span data-stu-id="a2847-319">The phrases are separated by forward-slash ("/") characters.</span></span> <span data-ttu-id="a2847-320">Служба WinRM поддерживает язык [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) для [*диалекта фрагмента*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-320">The WinRM service supports [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) for [*fragment dialect*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

 

 