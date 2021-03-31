---
title: Виртуальные каналы службы удаленных рабочих столов
description: Виртуальные каналы — это расширения программного обеспечения, которые можно использовать для добавления функциональных улучшений в службы удаленных рабочих столов приложение.
ms.assetid: f7bdebec-ecc3-4f28-9327-f0d2f169c142
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce78331841a41502aa337de19e9879d42d85fe1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329699"
---
# <a name="remote-desktop-services-virtual-channels"></a><span data-ttu-id="9857d-103">Виртуальные каналы службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="9857d-103">Remote Desktop Services virtual channels</span></span>

<span data-ttu-id="9857d-104">*Виртуальные каналы* — это расширения программного обеспечения, которые можно использовать для добавления функциональных улучшений в службы удаленных рабочих столов приложение.</span><span class="sxs-lookup"><span data-stu-id="9857d-104">*Virtual channels* are software extensions that can be used to add functional enhancements to a Remote Desktop Services application.</span></span> <span data-ttu-id="9857d-105">Примеры функциональных улучшений могут включать в себя поддержку специальных типов оборудования, аудио или других дополнений к основным функциям, предоставляемым службы удаленных рабочих столов [протокол удаленного рабочего стола](remote-desktop-protocol.md) (RDP).</span><span class="sxs-lookup"><span data-stu-id="9857d-105">Examples of functional enhancements might include: support for special types of hardware, audio, or other additions to the core functionality provided by the Remote Desktop Services [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP).</span></span> <span data-ttu-id="9857d-106">Протокол RDP обеспечивает мультиплексированное Управление несколькими виртуальными каналами.</span><span class="sxs-lookup"><span data-stu-id="9857d-106">The RDP protocol provides multiplexed management of multiple virtual channels.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9857d-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="9857d-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="9857d-108">Использование виртуальных каналов службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="9857d-108">Using Remote Desktop Services virtual channels</span></span>](using-terminal-services-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="9857d-109">Для реализации виртуального канала необходимо предоставить серверные и клиентские модули приложения виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="9857d-109">To implement a virtual channel, you provide the server and client modules of a virtual channel's application.</span></span>

</dd> <dt>

[<span data-ttu-id="9857d-110">Справочник по динамическим виртуальным каналам</span><span class="sxs-lookup"><span data-stu-id="9857d-110">Dynamic virtual channels reference</span></span>](dynamic-virtual-channels-reference.md)
</dt> <dd>

<span data-ttu-id="9857d-111">Клиентские интерфейсы динамического виртуального канала (DVC) поддерживаются службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="9857d-111">Dynamic virtual channel (DVC) client interfaces are supported by Remote Desktop Services.</span></span>

</dd> <dt>

[<span data-ttu-id="9857d-112">Справочник по виртуальным каналам графики</span><span class="sxs-lookup"><span data-stu-id="9857d-112">Graphics virtual channels reference</span></span>](graphics-virtual-channels-reference.md)
</dt> <dd>

<span data-ttu-id="9857d-113">В справочнике по виртуальным каналам графики содержатся программные элементы, позволяющие создавать виртуальные графические каналы.</span><span class="sxs-lookup"><span data-stu-id="9857d-113">The graphics virtual channels reference contains programming elements that enable you to create a virtual graphics channel.</span></span>

</dd> </dl>

<span data-ttu-id="9857d-114">Приложение виртуального канала состоит из двух частей: клиентского модуля и серверного модуля.</span><span class="sxs-lookup"><span data-stu-id="9857d-114">A virtual channel application has two parts, a client module and a server module.</span></span> <span data-ttu-id="9857d-115">Серверный модуль — это исполняемая программа, выполняемая на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="9857d-115">The server module is an executable program running on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="9857d-116">Клиентский модуль — это библиотека DLL, которая должна быть загружена в память клиентского компьютера при запуске клиентской программы подключение к удаленному рабочему столу (RDC).</span><span class="sxs-lookup"><span data-stu-id="9857d-116">The client module is a DLL that must be loaded into memory on the client computer when the Remote Desktop Connection (RDC) client program runs.</span></span>

<span data-ttu-id="9857d-117">Виртуальные каналы могут добавлять функциональные улучшения в клиент подключение к удаленному рабочему столу (RDC) независимо от протокола RDP.</span><span class="sxs-lookup"><span data-stu-id="9857d-117">Virtual channels can add functional enhancements to a Remote Desktop Connection (RDC) client, independent of the RDP protocol.</span></span> <span data-ttu-id="9857d-118">Благодаря поддержке виртуальных каналов новые функции можно добавлять без необходимости обновления клиентского или серверного программного обеспечения или протокола RDP.</span><span class="sxs-lookup"><span data-stu-id="9857d-118">With virtual channel support, new features can be added without having to update the client or server software, or the RDP protocol.</span></span>

<span data-ttu-id="9857d-119">Определены четыре основных класса пользователей виртуальных каналов:</span><span class="sxs-lookup"><span data-stu-id="9857d-119">Four major classes of users of virtual channels have been identified:</span></span>

-   <span data-ttu-id="9857d-120">Общие драйверы режима ядра, например драйверы последовательного порта или принтера.</span><span class="sxs-lookup"><span data-stu-id="9857d-120">General kernel-mode drivers, such as serial or printer drivers.</span></span>
-   <span data-ttu-id="9857d-121">Перенаправление файловой системы (это лишь особый случай общего драйвера режима ядра).</span><span class="sxs-lookup"><span data-stu-id="9857d-121">File system redirection (this is just a special case of a general kernel-mode driver).</span></span>
-   <span data-ttu-id="9857d-122">Приложения пользовательского режима, например Удаленная Вырезание и вставка.</span><span class="sxs-lookup"><span data-stu-id="9857d-122">User mode applications, for example remote cut-and-paste.</span></span>
-   <span data-ttu-id="9857d-123">Звуковые устройства.</span><span class="sxs-lookup"><span data-stu-id="9857d-123">Audio devices.</span></span>

<span data-ttu-id="9857d-124">Дополнительные сведения см. [в статье использование службы удаленных рабочих столов виртуальных каналов](using-terminal-services-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="9857d-124">For more information, see [Using Remote Desktop Services Virtual Channels](using-terminal-services-virtual-channels.md).</span></span>

<span data-ttu-id="9857d-125">Если вы включили приложение виртуальных каналов в развертывание службы удаленных рабочих столов, можно сделать приложение доступным для клиентских компьютеров, обращающихся к серверу узла сеансов удаленных рабочих столов с помощью удаленный рабочий стол элемента управления Microsoft ActiveX.</span><span class="sxs-lookup"><span data-stu-id="9857d-125">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make the application available to client computers that access the RD Session Host server by means of the Remote Desktop Microsoft ActiveX control.</span></span> <span data-ttu-id="9857d-126">Дополнительные сведения см. в статьях [виртуальные каналы с поддержкой скриптов](scriptable-virtual-channels.md) и [использование элемента управления ActiveX удаленный рабочий стол с виртуальными каналами](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="9857d-126">For more information, see [Scriptable Virtual Channels](scriptable-virtual-channels.md) and [Using the Remote Desktop ActiveX Control with Virtual Channels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span></span>

 

 




