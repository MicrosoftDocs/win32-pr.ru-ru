---
title: Постоянные виртуальные каналы удаленного управления
description: Постоянный виртуальный канал удаленного управления не закрывается при подключении или отключении удаленного управления для сеанса, подключенного к клиенту. Данные по-прежнему будут передаваться и приниматься через этот канал.
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d87054a79863df5816b30fced648ab40251a80e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411335"
---
# <a name="remote-control-persistent-virtual-channels"></a><span data-ttu-id="d78a5-104">Постоянные виртуальные каналы удаленного управления</span><span class="sxs-lookup"><span data-stu-id="d78a5-104">Remote Control Persistent Virtual Channels</span></span>

<span data-ttu-id="d78a5-105">В Windows XP библиотека DLL может указывать один или несколько виртуальных каналов в качестве *постоянного удаленного управления*.</span><span class="sxs-lookup"><span data-stu-id="d78a5-105">On Windows XP, a DLL can specify one or more virtual channels as *remote control persistent*.</span></span> <span data-ttu-id="d78a5-106">Постоянный виртуальный канал удаленного управления не закрывается при подключении или отключении удаленного управления для сеанса, подключенного к клиенту.</span><span class="sxs-lookup"><span data-stu-id="d78a5-106">A remote control persistent virtual channel is not closed when a remote control connects or disconnects for the session connected to the client.</span></span> <span data-ttu-id="d78a5-107">Данные по-прежнему будут передаваться и приниматься через этот канал.</span><span class="sxs-lookup"><span data-stu-id="d78a5-107">Data will continue to be transmitted and received through this channel.</span></span> <span data-ttu-id="d78a5-108">Виртуальные каналы, не указанные библиотекой DLL в качестве постоянного удаленного управления, будут закрыты в этом сценарии.</span><span class="sxs-lookup"><span data-stu-id="d78a5-108">Virtual channels that the DLL does not specify as remote control persistent will close in this scenario.</span></span>

<span data-ttu-id="d78a5-109">Постоянные виртуальные каналы удаленного управления указываются во время вызова **виртуалчаннелинит**.</span><span class="sxs-lookup"><span data-stu-id="d78a5-109">Remote control persistent virtual channels are specified during the call to **VirtualChannelInit**.</span></span> <span data-ttu-id="d78a5-110">Конкретные сведения об этом см. на странице справочника по [**виртуалчаннелинит**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) .</span><span class="sxs-lookup"><span data-stu-id="d78a5-110">Refer to the reference page for [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) for specific information about this.</span></span>

 

 




