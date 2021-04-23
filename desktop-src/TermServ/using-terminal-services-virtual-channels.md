---
title: Использование виртуальных каналов службы удаленных рабочих столов
description: Для реализации виртуального канала необходимо предоставить серверные и клиентские модули приложения виртуального канала.
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eafca38c19855fdb057ceeb6e79cb4613773a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774288"
---
# <a name="using-remote-desktop-services-virtual-channels"></a><span data-ttu-id="7c2ab-103">Использование виртуальных каналов службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="7c2ab-103">Using Remote Desktop Services virtual channels</span></span>

<span data-ttu-id="7c2ab-104">Для реализации виртуального канала необходимо предоставить серверные и клиентские модули приложения виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-104">To implement a virtual channel, you provide the server and client modules of a virtual channel's application.</span></span> <span data-ttu-id="7c2ab-105">Серверный модуль может быть приложением пользовательского режима или драйвером режима ядра.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-105">The server module can be a user-mode application or a kernel-mode driver.</span></span> <span data-ttu-id="7c2ab-106">Клиентский модуль должен быть библиотекой DLL.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-106">The client module must be a DLL.</span></span>

<span data-ttu-id="7c2ab-107">Описание этих модулей см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-107">For descriptions of these modules, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7c2ab-108">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="7c2ab-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="7c2ab-109">Серверное приложение виртуального канала</span><span class="sxs-lookup"><span data-stu-id="7c2ab-109">Virtual Channel Server Application</span></span>](virtual-channel-server-application.md)
</dt> <dd>

<span data-ttu-id="7c2ab-110">Серверный модуль приложения, использующего виртуальные каналы, должен быть приложением пользовательского режима, выполняющимся в сеансе клиента на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="7c2ab-110">The server module of an application that uses virtual channels must be a user-mode application running in a client session on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="7c2ab-111">Обратите внимание, что необходимо предоставить метод для запуска серверного приложения.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-111">Note that you must provide a method to start the server application.</span></span>

</dd> <dt>

[<span data-ttu-id="7c2ab-112">Клиентская библиотека виртуальных каналов</span><span class="sxs-lookup"><span data-stu-id="7c2ab-112">Virtual Channel Client DLL</span></span>](virtual-channel-client-dll.md)
</dt> <dd>

<span data-ttu-id="7c2ab-113">Клиент приложения виртуальных каналов — это библиотека DLL, которая загружается во время инициализации службы удаленных рабочих столов на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-113">The client of a virtual channels application is a DLL that is loaded during the Remote Desktop Services initialization on the client computer.</span></span> <span data-ttu-id="7c2ab-114">Библиотека DLL должна быть зарегистрирована на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-114">The DLL must be registered on the client computer.</span></span>

</dd> <dt>

[<span data-ttu-id="7c2ab-115">Регистрация клиента виртуального канала</span><span class="sxs-lookup"><span data-stu-id="7c2ab-115">Virtual Channel Client Registration</span></span>](virtual-channel-client-registration.md)
</dt> <dd>

<span data-ttu-id="7c2ab-116">Необходимо сохранить имя библиотеки DLL клиента в реестре.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-116">You must store the name of the client DLL in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="7c2ab-117">Постоянные виртуальные каналы удаленного управления</span><span class="sxs-lookup"><span data-stu-id="7c2ab-117">Remote Control Persistent Virtual Channels</span></span>](remote-control-persistent-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="7c2ab-118">Постоянный виртуальный канал удаленного управления не закрывается при подключении или отключении удаленного управления для сеанса, подключенного к клиенту.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-118">A remote control persistent virtual channel is not closed when a remote control connects or disconnects for the session connected to the client.</span></span> <span data-ttu-id="7c2ab-119">Данные по-прежнему будут передаваться и приниматься через этот канал.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-119">Data will continue to be transmitted and received through this channel.</span></span>

</dd> <dt>

[<span data-ttu-id="7c2ab-120">Динамические виртуальные каналы</span><span class="sxs-lookup"><span data-stu-id="7c2ab-120">Dynamic Virtual Channels</span></span>](dynamic-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="7c2ab-121">Динамические API виртуальных каналов (DVC) расширяют существующие API виртуальных каналов для службы удаленных рабочих столов, называемых статическими интерфейсами API виртуального канала (SVC).</span><span class="sxs-lookup"><span data-stu-id="7c2ab-121">Dynamic virtual channel (DVC) APIs extend the existing virtual channel APIs for Remote Desktop Services, known as static virtual channel (SVC) APIs.</span></span>

</dd> </dl>

<span data-ttu-id="7c2ab-122">Если вы включили приложение виртуального канала в развертывание службы удаленных рабочих столов, можно также сделать приложение доступным для клиентских компьютеров, обращающихся к серверу узла сеансов удаленных рабочих столов с помощью элемента управления ActiveX удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-122">If you have enabled a virtual channel's application in your Remote Desktop Services deployment, you can also make the application available to client computers that access the RD Session Host server by means of the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="7c2ab-123">Дополнительные сведения см. [в статье Использование элемента управления ActiveX удаленный рабочий стол с виртуальными каналами](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="7c2ab-123">For more information, see [Using the Remote Desktop ActiveX Control with Virtual Channels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span></span>

 

 




