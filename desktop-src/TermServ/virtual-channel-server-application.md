---
title: Серверное приложение виртуального канала
description: Серверный модуль приложения, использующего виртуальные каналы, должен быть приложением пользовательского режима, выполняющимся в сеансе клиента на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов). Обратите внимание, что необходимо предоставить метод для запуска серверного приложения.
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377732b91d6f93645e23b0f0b93cc203a65ef471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776949"
---
# <a name="virtual-channel-server-application"></a><span data-ttu-id="3acb2-104">Серверное приложение виртуального канала</span><span class="sxs-lookup"><span data-stu-id="3acb2-104">Virtual Channel Server Application</span></span>

<span data-ttu-id="3acb2-105">Серверный модуль приложения, использующего виртуальные каналы, должен быть приложением пользовательского режима, выполняющимся в сеансе клиента на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="3acb2-105">The server module of an application that uses virtual channels must be a user-mode application running in a client session on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="3acb2-106">Обратите внимание, что необходимо предоставить метод для запуска серверного приложения.</span><span class="sxs-lookup"><span data-stu-id="3acb2-106">Note that you must provide a method to start the server application.</span></span> <span data-ttu-id="3acb2-107">Это можно сделать несколькими способами. Например, можно использовать сценарий входа в систему или программу или сценарий в папке Startup.</span><span class="sxs-lookup"><span data-stu-id="3acb2-107">You can accomplish this in multiple ways; for example, you can use a logon script, or a program or script in the Startup folder.</span></span> <span data-ttu-id="3acb2-108">Пользователи также могут запустить приложение.</span><span class="sxs-lookup"><span data-stu-id="3acb2-108">Users could also launch the application.</span></span>

<span data-ttu-id="3acb2-109">Необходимо сохранить имя серверного приложения виртуального канала в реестре, добавив подраздел в следующем расположении:</span><span class="sxs-lookup"><span data-stu-id="3acb2-109">You must store the name of the virtual channel server application in the registry by adding a subkey under the following location:</span></span>

<span data-ttu-id="3acb2-110">**HKey \_ \_** \\  \\  \\ **Управление** \\  \\ **надстройками** сервера терминалов в системе локального компьютера CurrentControlSet</span><span class="sxs-lookup"><span data-stu-id="3acb2-110">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Terminal Server**\\**Addins**</span></span>

<span data-ttu-id="3acb2-111">Дополнительные сведения о подразделе см. в разделе [наблюдение за подключениями и отсоединениями сеансов](monitoring-session-connections-and-disconnections.md).</span><span class="sxs-lookup"><span data-stu-id="3acb2-111">For more information about the subkey, see [Monitoring Session Connections and Disconnections](monitoring-session-connections-and-disconnections.md).</span></span>

<span data-ttu-id="3acb2-112">Серверное приложение может вызвать функцию [**втсвиртуалчаннелопен**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) , чтобы открыть маркер для виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="3acb2-112">The server application can call the [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) function to open a handle to a virtual channel.</span></span> <span data-ttu-id="3acb2-113">Затем приложение может использовать этот обработчик в любой из следующих функций.</span><span class="sxs-lookup"><span data-stu-id="3acb2-113">The application can then use the handle in any of the following functions.</span></span>

<dl> <dt>

[<span data-ttu-id="3acb2-114">**втсвиртуалчаннелклосе**</span><span class="sxs-lookup"><span data-stu-id="3acb2-114">**WTSVirtualChannelClose**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

<span data-ttu-id="3acb2-115">Закрывает открытый маркер виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="3acb2-115">Closes an open virtual channel handle.</span></span>

</dd> <dt>

[<span data-ttu-id="3acb2-116">**втсвиртуалчаннелпуржеинпут**</span><span class="sxs-lookup"><span data-stu-id="3acb2-116">**WTSVirtualChannelPurgeInput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

<span data-ttu-id="3acb2-117">Удаляет все входные данные из очереди, отправленные клиентом на сервер в определенном виртуальном канале.</span><span class="sxs-lookup"><span data-stu-id="3acb2-117">Deletes all queued input data sent from the client to the server on a specific virtual channel.</span></span>

> [!Note]  
> <span data-ttu-id="3acb2-118">В настоящее время эта функция не используется службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3acb2-118">This function currently is not used by Remote Desktop Services.</span></span>

 

</dd> <dt>

[<span data-ttu-id="3acb2-119">**втсвиртуалчаннелпуржеаутпут**</span><span class="sxs-lookup"><span data-stu-id="3acb2-119">**WTSVirtualChannelPurgeOutput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

<span data-ttu-id="3acb2-120">Удаляет все выходные данные в очереди, отправленные с сервера клиенту по определенному виртуальному каналу.</span><span class="sxs-lookup"><span data-stu-id="3acb2-120">Deletes all queued output data sent from the server to the client on a specific virtual channel.</span></span>

> [!Note]  
> <span data-ttu-id="3acb2-121">В настоящее время эта функция не используется службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3acb2-121">This function currently is not used by Remote Desktop Services.</span></span>

 

</dd> <dt>

[<span data-ttu-id="3acb2-122">**втсвиртуалчаннелкуери**</span><span class="sxs-lookup"><span data-stu-id="3acb2-122">**WTSVirtualChannelQuery**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

<span data-ttu-id="3acb2-123">Возвращает сведения об указанном виртуальном канале.</span><span class="sxs-lookup"><span data-stu-id="3acb2-123">Returns information about a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="3acb2-124">**втсвиртуалчаннелреад**</span><span class="sxs-lookup"><span data-stu-id="3acb2-124">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

<span data-ttu-id="3acb2-125">Считывает данные с конца виртуального канала на сервере.</span><span class="sxs-lookup"><span data-stu-id="3acb2-125">Reads data from the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="3acb2-126">**втсвиртуалчаннелврите**</span><span class="sxs-lookup"><span data-stu-id="3acb2-126">**WTSVirtualChannelWrite**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

<span data-ttu-id="3acb2-127">Записывает данные на серверный конец виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="3acb2-127">Writes data to the server end of a virtual channel.</span></span>

</dd> </dl>

 

 




