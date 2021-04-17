---
title: Службы удаленных рабочих столов (службы удаленных рабочих столов)
description: Удаленный рабочий стол (Майкрософт) Services — это программное обеспечение удаленного доступа к компьютеру, которое поддерживает удаленный доступ к рабочему столу. Службы удаленных рабочих столов подключает нескольких клиентов к серверу узла сеансов удаленный рабочий стол.
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов службы удаленных рабочих столов
- Службы удаленных рабочих столов службы удаленных рабочих столов, Домашняя страница
- Службы терминалов см. в разделе службы удаленных рабочих столов службы удаленных рабочих столов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f39e176473c98f1e240d58592463df749a95f939
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105681744"
---
# <a name="remote-desktop-services-remote-desktop-services"></a><span data-ttu-id="66b27-107">Службы удаленных рабочих столов (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="66b27-107">Remote Desktop Services (Remote Desktop Services)</span></span>

## <a name="purpose"></a><span data-ttu-id="66b27-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="66b27-108">Purpose</span></span>

<span data-ttu-id="66b27-109">Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 или Windows Server 2008 с службы удаленных рабочих столов (ранее известные как службы терминалов) позволяют серверу размещать несколько одновременных сеансов клиентов.</span><span class="sxs-lookup"><span data-stu-id="66b27-109">Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 with Remote Desktop Services (formerly known as Terminal Services) allow a server to host multiple, simultaneous client sessions.</span></span> <span data-ttu-id="66b27-110">Удаленный рабочий стол использует технологию службы удаленных рабочих столов, чтобы разрешить удаленное выполнение одного сеанса.</span><span class="sxs-lookup"><span data-stu-id="66b27-110">Remote Desktop uses Remote Desktop Services technology to allow a single session to run remotely.</span></span> <span data-ttu-id="66b27-111">Пользователь может подключиться к серверу узла сеансов удаленный рабочий стол (к узлу сеансов удаленных рабочих столов) (ранее известному как сервер терминалов) с помощью клиентского программного обеспечения подключение к удаленному рабочему столу (RDC).</span><span class="sxs-lookup"><span data-stu-id="66b27-111">A user can connect to a Remote Desktop Session Host (RD Session Host) server (formerly known as a terminal server) by using Remote Desktop Connection (RDC) client software.</span></span> <span data-ttu-id="66b27-112">Веб-подключение к удаленному рабочему столу расширяет технологии службы удаленных рабочих столов в Интернете.</span><span class="sxs-lookup"><span data-stu-id="66b27-112">The Remote Desktop Web Connection extends Remote Desktop Services technology to the web.</span></span>

> [!Note]  
> <span data-ttu-id="66b27-113">Этот раздел предназначен для разработчиков программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="66b27-113">This topic is for software developers.</span></span> <span data-ttu-id="66b27-114">Если вы ищете сведения о пользователях удаленный рабочий стол, см. раздел [Подключение к удаленному рабочему столу: часто задаваемые вопросы](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).</span><span class="sxs-lookup"><span data-stu-id="66b27-114">If you are looking for user information for Remote Desktop connections, See [Remote Desktop Connection: frequently asked questions](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="66b27-115">Где применимо</span><span class="sxs-lookup"><span data-stu-id="66b27-115">Where applicable</span></span>

<span data-ttu-id="66b27-116">Клиент подключение к удаленному рабочему столу (RDC) может существовать в различных формах.</span><span class="sxs-lookup"><span data-stu-id="66b27-116">A Remote Desktop Connection (RDC) client can exist in a variety of forms.</span></span> <span data-ttu-id="66b27-117">Устройства с тонким клиентом, которые работают под управлением внедренной операционной системы Windows, могут запускать клиентское программное обеспечение RDC для подключения к серверу узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="66b27-117">Thin-client hardware devices that run an embedded Windows-based operating system can run the RDC client software to connect to an RD Session Host server.</span></span> <span data-ttu-id="66b27-118">Компьютеры под управлением Windows, Macintosh и UNIX могут запускать клиентское программное обеспечение RDC для подключения к серверу узла сеансов удаленных рабочих столов для вывода приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="66b27-118">Windows-, Macintosh-, or UNIX-based computers can run RDC client software to connect to an RD Session Host server to display Windows-based applications.</span></span> <span data-ttu-id="66b27-119">Такое сочетание клиентов RDC обеспечивает доступ к приложениям Windows практически из любой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="66b27-119">This combination of RDC clients provides access to Windows-based applications from virtually any operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="66b27-120">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="66b27-120">Developer audience</span></span>

<span data-ttu-id="66b27-121">Разработчики, использующие службы удаленных рабочих столов, должны быть знакомы с языками программирования C и C++ и средой программирования на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="66b27-121">Developers who use Remote Desktop Services should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span> <span data-ttu-id="66b27-122">Требуется знание архитектуры клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="66b27-122">Familiarity with client/server architecture is required.</span></span> <span data-ttu-id="66b27-123">Веб-подключение к удаленному рабочему столу включает в себя интерфейсы с помощью сценариев для создания и развертывания в веб-каналах, поддерживающих сценарии, в среде службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="66b27-123">The Remote Desktop Web Connection includes scriptable interfaces to create and deploy scriptable virtual channels within Remote Desktop Services web applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="66b27-124">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="66b27-124">Run-time requirements</span></span>

<span data-ttu-id="66b27-125">Для приложений, использующих службы удаленных рабочих столов, требуется Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="66b27-125">Applications that use Remote Desktop Services require Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, or Windows Vista.</span></span> <span data-ttu-id="66b27-126">Чтобы использовать функции веб-подключение к удаленному рабочему столу, клиентскому приложению службы удаленных рабочих столов требуется Internet Explorer и подключение к Интернету в Интернете.</span><span class="sxs-lookup"><span data-stu-id="66b27-126">To use Remote Desktop Web Connection functionality, the Remote Desktop Services client application requires Internet Explorer and a connection to the World Wide Web.</span></span> <span data-ttu-id="66b27-127">Сведения о требованиях времени выполнения для определенного программного элемента см. в разделе "требования" на странице справочника по этому элементу.</span><span class="sxs-lookup"><span data-stu-id="66b27-127">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="66b27-128">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="66b27-128">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="66b27-129">удаленный рабочий стол элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="66b27-129">Remote Desktop ActiveX control</span></span>](remote-desktop-activex-control.md)
</dt> <dd>

<span data-ttu-id="66b27-130">Описывает, как использовать элемент управления ActiveX удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="66b27-130">Describes how to use the Remote Desktop ActiveX control.</span></span>

</dd> <dt>

[<span data-ttu-id="66b27-131">API поставщика протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="66b27-131">Remote Desktop Protocol Provider API</span></span>](custom-remote-desktop-protocols.md)
</dt> <dd>

<span data-ttu-id="66b27-132">API поставщика протокол удаленного рабочего стола используется для создания протокола, обеспечивающего обмен данными между службы удаленных рабочих столовной службой и несколькими клиентами.</span><span class="sxs-lookup"><span data-stu-id="66b27-132">You use the Remote Desktop Protocol Provider API to create a protocol to provide communication between the Remote Desktop Services service and multiple clients.</span></span>

</dd> <dt>

[<span data-ttu-id="66b27-133">Виртуальные каналы службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="66b27-133">Remote Desktop Services virtual channels</span></span>](terminal-services-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="66b27-134">*Виртуальные каналы* — это расширения программного обеспечения, которые можно использовать для добавления функциональных улучшений в службы удаленных рабочих столов приложение.</span><span class="sxs-lookup"><span data-stu-id="66b27-134">*Virtual channels* are software extensions that can be used to add functional enhancements to a Remote Desktop Services application.</span></span>

</dd> <dt>

[<span data-ttu-id="66b27-135">API перенаправления мультимедиа RemoteFX</span><span class="sxs-lookup"><span data-stu-id="66b27-135">RemoteFX Media Redirection API</span></span>](remotefx-api.md)
</dt> <dd>

<span data-ttu-id="66b27-136">API перенаправления мультимедиа RemoteFX используется в сеансе удаленный рабочий стол для обнаружения областей сервера, на которых отображается быстрое изменение содержимого, например видео.</span><span class="sxs-lookup"><span data-stu-id="66b27-136">The RemoteFX Media Redirection API is used in a Remote Desktop session to identify areas of the server that are displaying fast changing content, such as video.</span></span> <span data-ttu-id="66b27-137">Это содержимое может быть закодировано видео и отправлено клиенту в закодированном формате.</span><span class="sxs-lookup"><span data-stu-id="66b27-137">This content can then be video encoded and sent to the client in encoded format.</span></span>

</dd> <dt>

[<span data-ttu-id="66b27-138">API клиента компонента подключение к удаленному рабочему столу Broker</span><span class="sxs-lookup"><span data-stu-id="66b27-138">Remote Desktop Connection Broker client API</span></span>](connection-broker-client-api.md)
</dt> <dd>

<span data-ttu-id="66b27-139">Описывает, как использовать API клиента компонента подключение к удаленному рабочему столу Broker.</span><span class="sxs-lookup"><span data-stu-id="66b27-139">Describes how to use the Remote Desktop Connection Broker client API.</span></span>

</dd> <dt>

[<span data-ttu-id="66b27-140">Справочник по API агента задач персонального рабочего стола</span><span class="sxs-lookup"><span data-stu-id="66b27-140">Personal desktop task agent API reference</span></span>](task-agent-api-reference.md)
</dt> <dd>

<span data-ttu-id="66b27-141">API агента задачи личного рабочего стола используется для управления запланированными обновлениями на личном виртуальном рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="66b27-141">The personal desktop task agent API is used to handle scheduled updates to a personal virtual desktop.</span></span>

</dd> <dt>

[<span data-ttu-id="66b27-142">О службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="66b27-142">About Remote Desktop Services</span></span>](about-terminal-services.md)
</dt> <dd>

<span data-ttu-id="66b27-143">Службы удаленных рабочих столов (ранее назывались службами терминалов) предоставляет функциональные возможности, аналогичные возможностям централизованного узла на основе терминала или мэйнфреймов, в которых несколько терминалов подключаются к главному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="66b27-143">Remote Desktop Services (formerly known as Terminal Services) provides functionality similar to a terminal-based, centralized host, or mainframe, environment in which multiple terminals connect to a host computer.</span></span>

</dd> <dt>

[<span data-ttu-id="66b27-144">Поставщик служб удаленный рабочий стол Management Services</span><span class="sxs-lookup"><span data-stu-id="66b27-144">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> <dd>

<span data-ttu-id="66b27-145">Поставщик служб управления удаленный рабочий стол (RDMS) управляет средами инфраструктуры виртуальных рабочих столов (VDI).</span><span class="sxs-lookup"><span data-stu-id="66b27-145">The Remote Desktop Management Services (RDMS) Provider manages virtual desktop infrastructure (VDI) environments.</span></span>

</dd> <dt>

[<span data-ttu-id="66b27-146">Справочник по службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="66b27-146">Remote Desktop Services reference</span></span>](terminal-services-reference.md)
</dt> <dd>

<span data-ttu-id="66b27-147">Документация по методам свойств, которые можно использовать для проверки и настройки службы удаленных рабочих столов свойств пользователя.</span><span class="sxs-lookup"><span data-stu-id="66b27-147">Documentation of property methods that you can use to examine and configure Remote Desktop Services user properties.</span></span> <span data-ttu-id="66b27-148">Также документированы службы удаленных рабочих столов функций, структур и веб-подключение к удаленному рабочему столу интерфейсов, поддерживающих сценарии.</span><span class="sxs-lookup"><span data-stu-id="66b27-148">Remote Desktop Services functions, structures, and Remote Desktop Web Connection scriptable interfaces are also documented.</span></span>

</dd> <dt>

[<span data-ttu-id="66b27-149">службы удаленных рабочих столов сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="66b27-149">Remote Desktop Services Shortcut Keys</span></span>](terminal-services-shortcut-keys.md)
</dt> <dd>

<span data-ttu-id="66b27-150">Список сочетаний клавиш службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="66b27-150">A list of the Remote Desktop Services shortcut keys.</span></span>

</dd> <dt>

[<span data-ttu-id="66b27-151">Поставщик WMI службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="66b27-151">Remote Desktop Services WMI provider</span></span>](terminal-services-wmi-provider.md)
</dt> <dd>

<span data-ttu-id="66b27-152">Поставщик WMI службы удаленных рабочих столов предоставляет программный доступ к сведениям и параметрам, предоставляемым оснасткой «Настройка службы удаленных рабочих столов/подключения консоли управления Майкрософт (MMC)».</span><span class="sxs-lookup"><span data-stu-id="66b27-152">The Remote Desktop Services WMI provider provides programmatic access to the information and settings that are exposed by the Remote Desktop Services Configuration/Connections Microsoft Management Console (MMC) snap-in.</span></span>

</dd> <dt>

[<span data-ttu-id="66b27-153">Использование службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="66b27-153">Using Remote Desktop Services</span></span>](using-terminal-services.md)
</dt> <dd>

<span data-ttu-id="66b27-154">Как программировать в среде службы удаленных рабочих столов и как расширять службы удаленных рабочих столов (ранее известные как службы терминалов) в Интернете с помощью веб-подключение к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="66b27-154">How to program in the Remote Desktop Services environment and how to extend Remote Desktop Services (formerly known as Terminal Services) technology to the web by using Remote Desktop Web Connection.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="66b27-155">См. также</span><span class="sxs-lookup"><span data-stu-id="66b27-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66b27-156">Службы терминалов теперь службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="66b27-156">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




