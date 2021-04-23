---
description: Прежде чем сокет можно будет использовать для настройки соединения или получения запроса на подключение, он должен быть привязан к локальному адресу.
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: Привязка к локальному адресу
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa022d17a8862e6092c52b18edd1539f2d95ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711044"
---
# <a name="binding-to-a-local-address"></a><span data-ttu-id="c2a0b-103">Привязка к локальному адресу</span><span class="sxs-lookup"><span data-stu-id="c2a0b-103">Binding to a Local Address</span></span>

<span data-ttu-id="c2a0b-104">Прежде чем сокет можно будет использовать для настройки соединения или получения запроса на подключение, он должен быть привязан к локальному адресу.</span><span class="sxs-lookup"><span data-stu-id="c2a0b-104">Before a socket can be used to set up a connection or receive a connection request, it needs to be bound to a local address.</span></span> <span data-ttu-id="c2a0b-105">Это можно сделать явным образом, вызвав [**вспбинд**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))или неявно [**вспконнект**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) , если сокет не привязан при вызове этой функции.</span><span class="sxs-lookup"><span data-stu-id="c2a0b-105">This could be done explicitly by calling [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)), or implicitly by [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) if the socket is unbound when this function is called.</span></span>

 

 
