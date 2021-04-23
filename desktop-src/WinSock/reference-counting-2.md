---
description: Процесс может вызвать Вспклосесоккет на повторяющемся сокете, и дескриптор будет освобожден. Однако базовый сокет остается открытым до тех пор, пока не будет вызван Вспклосесоккет для последнего оставшегося дескриптора.
ms.assetid: dff1e932-5e87-4ec5-995d-686d20ba6236
title: Подсчет ссылок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72d9ef7b3e5e31cc7941d30c47f107fc068489ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692714"
---
# <a name="reference-counting"></a><span data-ttu-id="315ca-104">Подсчет ссылок</span><span class="sxs-lookup"><span data-stu-id="315ca-104">Reference Counting</span></span>

<span data-ttu-id="315ca-105">Процесс может вызвать [**вспклосесоккет**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) на повторяющемся сокете, и дескриптор будет освобожден.</span><span class="sxs-lookup"><span data-stu-id="315ca-105">A process may call [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) on a duplicated socket and the descriptor will become deallocated.</span></span> <span data-ttu-id="315ca-106">Однако базовый сокет остается открытым до тех пор, пока не будет вызван **вспклосесоккет** для последнего оставшегося дескриптора.</span><span class="sxs-lookup"><span data-stu-id="315ca-106">The underlying socket, however, will remain open until **WSPCloseSocket** is called on the last remaining descriptor.</span></span>

 

 
