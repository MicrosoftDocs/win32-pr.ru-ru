---
title: О службы удаленных рабочих столов
description: Службы удаленных рабочих столов (ранее назывались службами терминалов) предоставляет функциональные возможности, аналогичные возможностям централизованного узла на основе терминала или мэйнфреймов, в которых несколько терминалов подключаются к главному компьютеру.
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- Службы удаленных рабочих столов службы удаленных рабочих столов, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4644170cfca3b4bacdd6db647e35549d56844e9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681518"
---
# <a name="about-remote-desktop-services"></a><span data-ttu-id="2290e-104">О службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="2290e-104">About Remote Desktop Services</span></span>

<span data-ttu-id="2290e-105">Службы удаленных рабочих столов (ранее назывались службами терминалов) предоставляет функциональные возможности, аналогичные возможностям централизованного узла на основе терминала или мэйнфреймов, в которых несколько терминалов подключаются к главному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="2290e-105">Remote Desktop Services (formerly known as Terminal Services) provides functionality similar to a terminal-based, centralized host, or mainframe, environment in which multiple terminals connect to a host computer.</span></span> <span data-ttu-id="2290e-106">Каждый терминал предоставляет канал для ввода и вывода данных между пользователем и главным компьютером.</span><span class="sxs-lookup"><span data-stu-id="2290e-106">Each terminal provides a conduit for input and output between a user and the host computer.</span></span> <span data-ttu-id="2290e-107">Пользователь может войти в терминал, а затем запускать приложения на главном компьютере, получать доступ к файлам, базам данных, сетевым ресурсам и т. д.</span><span class="sxs-lookup"><span data-stu-id="2290e-107">A user can log on at a terminal, and then run applications on the host computer, accessing files, databases, network resources, and so on.</span></span> <span data-ttu-id="2290e-108">Каждый сеанс терминала является независимым, и операционная система узла управляет конфликтами между несколькими пользователями, которые обычно используются для общих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2290e-108">Each terminal session is independent, with the host operating system managing conflicts between multiple users contending for shared resources.</span></span>

<span data-ttu-id="2290e-109">Основное различие между службы удаленных рабочих столов и традиционной средой мэйнфрейма заключается в том, что терминалы глупы в среде мэйнфрейма обеспечивают только ввод и вывод на основе символов.</span><span class="sxs-lookup"><span data-stu-id="2290e-109">The primary difference between Remote Desktop Services and the traditional mainframe environment is that the dumb terminals in a mainframe environment only provide character-based input and output.</span></span> <span data-ttu-id="2290e-110">Клиент или эмулятор подключение к удаленному рабочему столу (RDC) предоставляет полный графический пользовательский интерфейс, включая рабочий стол операционной системы Windows и поддержку различных устройств ввода, таких как клавиатура и мышь.</span><span class="sxs-lookup"><span data-stu-id="2290e-110">A Remote Desktop Connection (RDC) client or emulator provides a complete graphical user interface including a Windows operating system desktop and support for a variety of input devices, such as a keyboard and mouse.</span></span>

<span data-ttu-id="2290e-111">В среде службы удаленных рабочих столов приложение выполняется полностью на сервере узла сеансов удаленный рабочий стол (который ранее назывался сервером терминалов).</span><span class="sxs-lookup"><span data-stu-id="2290e-111">In the Remote Desktop Services environment, an application runs entirely on the Remote Desktop Session Host (RD Session Host) server (formerly known as a terminal server).</span></span> <span data-ttu-id="2290e-112">Клиент RDC не выполняет локальную обработку программного обеспечения приложения.</span><span class="sxs-lookup"><span data-stu-id="2290e-112">The RDC client performs no local processing of application software.</span></span> <span data-ttu-id="2290e-113">Сервер передает клиенту графический пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2290e-113">The server transmits the graphical user interface to the client.</span></span> <span data-ttu-id="2290e-114">Клиент передает входные данные пользователя обратно на сервер.</span><span class="sxs-lookup"><span data-stu-id="2290e-114">The client transmits the user's input back to the server.</span></span>

<span data-ttu-id="2290e-115">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="2290e-115">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2290e-116">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="2290e-116">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="2290e-117">Изменение перенаправления устройств по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2290e-117">Modify Device Redirection Default</span></span>](modify-device-redirection-default-.md)
</dt> <dd>

<span data-ttu-id="2290e-118">Так как серверы шлюза удаленный рабочий стол пытаются применить безопасные политики перенаправления устройств перед передачей клиентского подключения через сервер узла сеансов удаленный рабочий стол, может потребоваться отключить это значение по умолчанию в некоторых случаях.</span><span class="sxs-lookup"><span data-stu-id="2290e-118">Because Remote Desktop Gateway servers attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server, you may need to disable this default in some cases.</span></span>

</dd> <dt>

[<span data-ttu-id="2290e-119">Протокол удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="2290e-119">Remote Desktop Protocol</span></span>](remote-desktop-protocol.md)
</dt> <dd>

<span data-ttu-id="2290e-120">Протокол Удаленный рабочий стол (Майкрософт) (RDP) предоставляет возможности удаленного просмотра и ввода через сетевые подключения для приложений Windows, работающих на сервере.</span><span class="sxs-lookup"><span data-stu-id="2290e-120">The Microsoft Remote Desktop Protocol (RDP) provides remote display and input capabilities over network connections for Windows-based applications running on a server.</span></span>

</dd> <dt>

[<span data-ttu-id="2290e-121">службы удаленных рабочих столов API</span><span class="sxs-lookup"><span data-stu-id="2290e-121">Remote Desktop Services API</span></span>](terminal-services-api.md)
</dt> <dd>

<span data-ttu-id="2290e-122">Службы удаленных рабочих столов API в основном используется для клиентских и серверных приложений и приложений для службы удаленных рабочих столов администрирования.</span><span class="sxs-lookup"><span data-stu-id="2290e-122">The Remote Desktop Services API is primarily useful to client/server applications and applications for Remote Desktop Services administration.</span></span>

</dd> <dt>

[<span data-ttu-id="2290e-123">Приложения управления службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="2290e-123">Remote Desktop Services management applications</span></span>](terminal-services-management-applications.md)
</dt> <dd>

<span data-ttu-id="2290e-124">Описание приложений управления, которые поддерживает службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="2290e-124">Describes the management applications that Remote Desktop Services supports.</span></span>

</dd> <dt>

[<span data-ttu-id="2290e-125">службы удаленных рабочих столов рекомендации по программированию</span><span class="sxs-lookup"><span data-stu-id="2290e-125">Remote Desktop Services programming guidelines</span></span>](terminal-services-programming-guidelines.md)
</dt> <dd>

<span data-ttu-id="2290e-126">Разделы, содержащие рекомендации по разработке приложений в среде службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="2290e-126">Topics that provide guidelines for developing applications in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="2290e-127">Сеансы удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="2290e-127">Remote Desktop Sessions</span></span>](terminal-services-sessions.md)
</dt> <dd>

<span data-ttu-id="2290e-128">Поскольку каждый вход на клиент подключение к удаленному рабочему столу (RDC) получает отдельный идентификатор сеанса, взаимодействие с пользователем аналогично выполнению одновременного входа на несколько компьютеров. Например, компьютер Office и домашний компьютер.</span><span class="sxs-lookup"><span data-stu-id="2290e-128">Because each logon to a Remote Desktop Connection (RDC) client receives a separate session ID, the user-experience is similar to being logged on to multiple computers at the same time; for example, an office computer and a home computer.</span></span>

</dd> <dt>

[<span data-ttu-id="2290e-129">веб-подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="2290e-129">Remote Desktop Web Connection</span></span>](remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="2290e-130">Описывает, как установить веб-подключение к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="2290e-130">Describes how to install a Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="2290e-131">Ресурсы на сервере узла сеансов удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="2290e-131">Resources on a Remote Desktop Session Host Server</span></span>](resources-on-a-terminal-server.md)
</dt> <dd>

<span data-ttu-id="2290e-132">Несколько пользователей могут одновременно войти в один сервер узла сеансов удаленных рабочих столов, совместно использующий аппаратные и программные ресурсы сервера.</span><span class="sxs-lookup"><span data-stu-id="2290e-132">Multiple users can log on simultaneously to a single RD Session Host server, sharing the hardware and software resources of the server.</span></span>

</dd> <dt>

[<span data-ttu-id="2290e-133">Новые возможности службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="2290e-133">What's New in Remote Desktop Services</span></span>](what-s-new-in-terminal-services.md)
</dt> <dd>

<span data-ttu-id="2290e-134">Разделы, описывающие изменения в каждом выпуске службы удаленных рабочих столов API.</span><span class="sxs-lookup"><span data-stu-id="2290e-134">Topics that describe the changes in each release of the Remote Desktop Services API.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="2290e-135">См. также</span><span class="sxs-lookup"><span data-stu-id="2290e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2290e-136">Подключение к другому компьютеру с помощью подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="2290e-136">Connect to another computer using Remote Desktop Connection</span></span>](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




