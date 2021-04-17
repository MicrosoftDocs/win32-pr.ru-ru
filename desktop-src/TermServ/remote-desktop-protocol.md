---
title: Протокол удаленного рабочего стола
description: Протокол Удаленный рабочий стол (Майкрософт) (RDP) предоставляет возможности удаленного просмотра и ввода через сетевые подключения для приложений Windows, работающих на сервере.
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- Протокол удаленного рабочего стола (RDP) службы удаленных рабочих столов
- RDP (см. протокол удаленного рабочего стола)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7895163a5ee92a6cc756dca9b097db8498d02e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681640"
---
# <a name="remote-desktop-protocol"></a><span data-ttu-id="6d376-105">Протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="6d376-105">Remote Desktop Protocol</span></span>

<span data-ttu-id="6d376-106">Протокол Удаленный рабочий стол (Майкрософт) (RDP) предоставляет возможности удаленного просмотра и ввода через сетевые подключения для приложений Windows, работающих на сервере.</span><span class="sxs-lookup"><span data-stu-id="6d376-106">The Microsoft Remote Desktop Protocol (RDP) provides remote display and input capabilities over network connections for Windows-based applications running on a server.</span></span> <span data-ttu-id="6d376-107">Протокол RDP предназначен для поддержки различных типов сетевых топологий и нескольких протоколов локальной сети.</span><span class="sxs-lookup"><span data-stu-id="6d376-107">RDP is designed to support different types of network topologies and multiple LAN protocols.</span></span>

> [!Note]  
> <span data-ttu-id="6d376-108">Этот раздел предназначен для разработчиков программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="6d376-108">This topic is for software developers.</span></span> <span data-ttu-id="6d376-109">Если вы ищете сведения о пользователе для удаленный рабочий стол, см. раздел [Поддержка Windows](https://windows.microsoft.com/windows/support#1TC=windows-8).</span><span class="sxs-lookup"><span data-stu-id="6d376-109">If you are looking for user information for Remote Desktop, see [Windows Support](https://windows.microsoft.com/windows/support#1TC=windows-8).</span></span> <span data-ttu-id="6d376-110">Если вы ищете сведения о специалистах по информационным технологиям для удаленный рабочий стол, см. статью [службы удаленных рабочих столов на сайте TechNet](/windows/deployment/deploy-whats-new).</span><span class="sxs-lookup"><span data-stu-id="6d376-110">If you are looking for IT professional information for Remote Desktop, see [Remote Desktop Services on TechNet](/windows/deployment/deploy-whats-new).</span></span>

 

## <a name="basic-architecture"></a><span data-ttu-id="6d376-111">Базовая архитектура</span><span class="sxs-lookup"><span data-stu-id="6d376-111">Basic Architecture</span></span>

<span data-ttu-id="6d376-112">Протокол RDP основан на службах и расширении служб семейства ITU T. 120.</span><span class="sxs-lookup"><span data-stu-id="6d376-112">RDP is based on, and an extension of, the ITU T.120 family of protocols.</span></span> <span data-ttu-id="6d376-113">RDP — это протокол с поддержкой нескольких каналов, который позволяет создавать отдельные виртуальные каналы для передачи данных с устройства и представления с сервера, а также зашифрованные клиентские данные мыши и клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="6d376-113">RDP is a multiple-channel capable protocol that allows for separate virtual channels for carrying device communication and presentation data from the server, as well as encrypted client mouse and keyboard data.</span></span> <span data-ttu-id="6d376-114">Протокол RDP предоставляет расширяемый базовый экземпляр и поддерживает до 64 000 отдельных каналов передачи данных и подготавливает их для передачи в MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="6d376-114">RDP provides an extensible base and supports up to 64,000 separate channels for data transmission and provisions for multipoint transmission.</span></span>

<span data-ttu-id="6d376-115">На сервере протокол RDP использует собственный видеодрайвер для отображения выходных данных, создавая данные отрисовки в сетевые пакеты с помощью протокола RDP и отправляя их по сети клиенту.</span><span class="sxs-lookup"><span data-stu-id="6d376-115">On the server, RDP uses its own video driver to render display output by constructing the rendering information into network packets by using RDP protocol and sending them over the network to the client.</span></span> <span data-ttu-id="6d376-116">На клиенте RDP получает данные отрисовки и интерпретирует пакеты в соответствующие вызовы API интерфейса графических устройств (GDI) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6d376-116">On the client, RDP receives rendering data and interprets the packets into corresponding Microsoft Windows graphics device interface (GDI) API calls.</span></span> <span data-ttu-id="6d376-117">Для входного пути события мыши и клавиатуры клиента перенаправляются с клиента на сервер.</span><span class="sxs-lookup"><span data-stu-id="6d376-117">For the input path, client mouse and keyboard events are redirected from the client to the server.</span></span> <span data-ttu-id="6d376-118">На сервере протокол RDP использует собственную клавиатуру и драйвер мыши для получения этих событий клавиатуры и мыши.</span><span class="sxs-lookup"><span data-stu-id="6d376-118">On the server, RDP uses its own keyboard and mouse driver to receive these keyboard and mouse events.</span></span>

<span data-ttu-id="6d376-119">В удаленный рабочий стол сеансе все переменные среды, например переменные, определяющие глубину цвета и фоновый рисунок, определяются параметрами подключения RCP-Tcp.</span><span class="sxs-lookup"><span data-stu-id="6d376-119">In a Remote Desktop session, all environment variables—for example, variables determining color depth and wallpaper enabling and disabling—are determined by the RCP-Tcp connection settings.</span></span> <span data-ttu-id="6d376-120">Это относится ко всем функциям и методам, которые задают переменные среды в [справочнике по веб-подключение к удаленному рабочему столу](remote-desktop-web-connection-reference.md) и [интерфейсе поставщика WMI службы удаленных рабочих столов](terminal-services-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="6d376-120">This applies to all functions and methods that set environment variables in the [Remote Desktop Web Connection Reference](remote-desktop-web-connection-reference.md) and the [Remote Desktop Services WMI Provider interface](terminal-services-wmi-provider-reference.md).</span></span>

## <a name="features"></a><span data-ttu-id="6d376-121">Компоненты</span><span class="sxs-lookup"><span data-stu-id="6d376-121">Features</span></span>

<span data-ttu-id="6d376-122">Microsoft RDP включает следующие функции и возможности:</span><span class="sxs-lookup"><span data-stu-id="6d376-122">Microsoft RDP includes the following features and capabilities:</span></span>

<dl> <dt>

<span data-ttu-id="6d376-123"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Ключ</span><span class="sxs-lookup"><span data-stu-id="6d376-123"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Encryption</span></span>
</dt> <dd>

<span data-ttu-id="6d376-124">Протокол RDP использует Шифр RC4 системы безопасности RSA, потоковый шифр, предназначенный для эффективного шифрования небольших объемов данных.</span><span class="sxs-lookup"><span data-stu-id="6d376-124">RDP uses RSA Security's RC4 cipher, a stream cipher designed to efficiently encrypt small amounts of data.</span></span> <span data-ttu-id="6d376-125">RC4 предназначен для безопасной связи по сетям.</span><span class="sxs-lookup"><span data-stu-id="6d376-125">RC4 is designed for secure communications over networks.</span></span> <span data-ttu-id="6d376-126">Администраторы могут выбрать шифрование данных с помощью 56 или 128-разрядного ключа.</span><span class="sxs-lookup"><span data-stu-id="6d376-126">Administrators can choose to encrypt data by using a 56- or 128-bit key.</span></span>

</dd> <dt>

<span data-ttu-id="6d376-127"><span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Функции уменьшения пропускной способности</span><span class="sxs-lookup"><span data-stu-id="6d376-127"><span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Bandwidth reduction features</span></span>
</dt> <dd>

<span data-ttu-id="6d376-128">Протокол RDP поддерживает различные механизмы уменьшения объема данных, передаваемых через сетевое подключение.</span><span class="sxs-lookup"><span data-stu-id="6d376-128">RDP supports various mechanisms to reduce the amount of data transmitted over a network connection.</span></span> <span data-ttu-id="6d376-129">К механизмам относятся сжатие данных, Постоянное кэширование точечных рисунков и кэширование глифов и фрагментов в ОЗУ.</span><span class="sxs-lookup"><span data-stu-id="6d376-129">Mechanisms include data compression, persistent caching of bitmaps, and caching of glyphs and fragments in RAM.</span></span> <span data-ttu-id="6d376-130">Кэш постоянного растрового изображения может обеспечить значительное повышение производительности при подключениях с низкой пропускной способностью, особенно при работе с приложениями, которые широко используют крупные точечные рисунки.</span><span class="sxs-lookup"><span data-stu-id="6d376-130">The persistent bitmap cache can provide a substantial improvement in performance over low-bandwidth connections, especially when running applications that make extensive use of large bitmaps.</span></span>

</dd> <dt>

<span data-ttu-id="6d376-131"><span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Отключение роуминга</span><span class="sxs-lookup"><span data-stu-id="6d376-131"><span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Roaming disconnect</span></span>
</dt> <dd>

<span data-ttu-id="6d376-132">Пользователь может вручную отключиться от сеанса удаленного рабочего стола, не выходя из системы.</span><span class="sxs-lookup"><span data-stu-id="6d376-132">A user can manually disconnect from a remote desktop session without logging off.</span></span> <span data-ttu-id="6d376-133">Пользователь автоматически повторно подключится к отключенному сеансу при входе в систему с того же устройства или с другого устройства.</span><span class="sxs-lookup"><span data-stu-id="6d376-133">The user is automatically reconnected to their disconnected session when he or she logs back onto the system, either from the same device or a different device.</span></span> <span data-ttu-id="6d376-134">Когда сеанс пользователя неожиданно завершается из-за сбоя сети или клиента, он отключается, но не выключается.</span><span class="sxs-lookup"><span data-stu-id="6d376-134">When a user's session is unexpectedly terminated by a network or client failure, the user is disconnected but not logged off.</span></span>

</dd> <dt>

<span data-ttu-id="6d376-135"><span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Сопоставление буфера обмена</span><span class="sxs-lookup"><span data-stu-id="6d376-135"><span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Clipboard mapping</span></span>
</dt> <dd>

<span data-ttu-id="6d376-136">Пользователи могут удалять, копировать и вставлять текст и графические объекты между приложениями, работающими на локальном компьютере и выполняющимися в сеансе удаленного рабочего стола, а также между сеансами.</span><span class="sxs-lookup"><span data-stu-id="6d376-136">Users can delete, copy, and paste text and graphics between applications running on the local computer and those running in a remote desktop session, and between sessions.</span></span>

</dd> <dt>

<span data-ttu-id="6d376-137"><span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Перенаправление печати</span><span class="sxs-lookup"><span data-stu-id="6d376-137"><span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Print redirection</span></span>
</dt> <dd>

<span data-ttu-id="6d376-138">Приложения, работающие в сеансе удаленного рабочего стола, могут печатать на принтере, подключенном к клиентскому устройству.</span><span class="sxs-lookup"><span data-stu-id="6d376-138">Applications running within a remote desktop session can print to a printer attached to the client device.</span></span>

</dd> <dt>

<span data-ttu-id="6d376-139"><span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Виртуальные каналы</span><span class="sxs-lookup"><span data-stu-id="6d376-139"><span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Virtual channels</span></span>
</dt> <dd>

<span data-ttu-id="6d376-140">Используя архитектуру виртуальных каналов RDP, можно дополнять существующие приложения и разрабатывать новые приложения для добавления функций, требующих обмена данными между клиентским устройством и приложением, выполняемым в сеансе удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="6d376-140">By using RDP virtual channel architecture, existing applications can be augmented and new applications can be developed to add features that require communications between the client device and an application running in a remote desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="6d376-141"><span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Удаленное управление</span><span class="sxs-lookup"><span data-stu-id="6d376-141"><span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Remote control</span></span>
</dt> <dd>

<span data-ttu-id="6d376-142">Сотрудники службы поддержки компьютеров могут просматривать сеанс удаленного рабочего стола и управлять им.</span><span class="sxs-lookup"><span data-stu-id="6d376-142">Computer support staff can view and control a remote desktop session.</span></span> <span data-ttu-id="6d376-143">Совместное использование входных и графических изображений между двумя сеансами удаленного рабочего стола дает возможность специалисту службы поддержки в удаленном режиме диагностировать и устранять проблемы.</span><span class="sxs-lookup"><span data-stu-id="6d376-143">Sharing input and display graphics between two remote desktop sessions gives a support person the ability to diagnose and resolve problems remotely.</span></span>

</dd> <dt>

<span data-ttu-id="6d376-144"><span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Балансировка сетевой нагрузки</span><span class="sxs-lookup"><span data-stu-id="6d376-144"><span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Network load balancing</span></span>
</dt> <dd>

<span data-ttu-id="6d376-145">Протокол RDP использует преимущества балансировки сетевой нагрузки (NLB), где это возможно.</span><span class="sxs-lookup"><span data-stu-id="6d376-145">RDP takes advantage of network load balancing (NLB), where available.</span></span>

</dd> </dl>

<span data-ttu-id="6d376-146">Кроме того, протокол RDP содержит следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="6d376-146">In addition, RDP contains the following features:</span></span>

-   <span data-ttu-id="6d376-147">Поддержка 24-разрядного цвета.</span><span class="sxs-lookup"><span data-stu-id="6d376-147">Support for 24-bit color.</span></span>
-   <span data-ttu-id="6d376-148">Повышенная производительность по сравнению с низкими скоростями коммутируемых подключений благодаря снижению пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="6d376-148">Improved performance over low-speed dial-up connections through reduced bandwidth.</span></span>
-   <span data-ttu-id="6d376-149">Проверка подлинности смарт-карты с помощью службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6d376-149">Smart Card authentication through Remote Desktop Services.</span></span>
-   <span data-ttu-id="6d376-150">Клавиатурный захват.</span><span class="sxs-lookup"><span data-stu-id="6d376-150">Keyboard hooking.</span></span> <span data-ttu-id="6d376-151">Возможность направлять специальные сочетания клавиш Windows в полноэкранном режиме на локальный компьютер или удаленный компьютер.</span><span class="sxs-lookup"><span data-stu-id="6d376-151">The ability to direct special Windows key combinations, in full-screen mode, to the local computer or to a remote computer.</span></span>
-   <span data-ttu-id="6d376-152">Перенаправление звука, диска, порта и сетевого принтера.</span><span class="sxs-lookup"><span data-stu-id="6d376-152">Sound, drive, port, and network printer redirection.</span></span> <span data-ttu-id="6d376-153">Звуки, происходящие на удаленном компьютере, могут быть слышны на клиентском компьютере, на котором работает клиент RDC, а локальные диски клиента будут видны сеансу удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="6d376-153">Sounds that occur on the remote computer can be heard on the client computer running the RDC client, and local client drives will be visible to the remote desktop session.</span></span>

 

 