---
description: Агент сетевого DDE запускает сетевой DDE, если обнаруживает активность DDE по локальной сети.
ms.assetid: bc1e6a06-be07-4ae8-94da-9603a885b3a5
title: Агент сетевого DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a6259b512782102936f54f65646454509c6b37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682430"
---
# <a name="network-dde-agent"></a><span data-ttu-id="8fbeb-103">Агент сетевого DDE</span><span class="sxs-lookup"><span data-stu-id="8fbeb-103">Network DDE Agent</span></span>

<span data-ttu-id="8fbeb-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8fbeb-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="8fbeb-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="8fbeb-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="8fbeb-106">Агент сетевого DDE запускает сетевой DDE, если обнаруживает активность DDE по локальной сети.</span><span class="sxs-lookup"><span data-stu-id="8fbeb-106">The network DDE agent starts network DDE if it detects local network DDE activity.</span></span> <span data-ttu-id="8fbeb-107">Он не обнаруживает удаленный клиент, пытающийся подключиться.</span><span class="sxs-lookup"><span data-stu-id="8fbeb-107">It does not detect a remote client trying to connect.</span></span> <span data-ttu-id="8fbeb-108">Поэтому, прежде чем клиент сможет успешно подключиться, необходимо запустить сетевой DDE на компьютере сервера.</span><span class="sxs-lookup"><span data-stu-id="8fbeb-108">Therefore, before any client can successfully connect, network DDE must be started on the server computer.</span></span> <span data-ttu-id="8fbeb-109">Обратите внимание, что по умолчанию сетевой DDE не запускается.</span><span class="sxs-lookup"><span data-stu-id="8fbeb-109">Note that network DDE is not started by default.</span></span> <span data-ttu-id="8fbeb-110">Чтобы запустить сетевой DDE, запустите NETDDE.EXE.</span><span class="sxs-lookup"><span data-stu-id="8fbeb-110">To start network DDE, run NETDDE.EXE.</span></span> <span data-ttu-id="8fbeb-111">Этот файл находится в каталоге Windows.</span><span class="sxs-lookup"><span data-stu-id="8fbeb-111">This file is located in your Windows directory.</span></span>

<span data-ttu-id="8fbeb-112">Агент сетевого DDE также запускает приложения, необходимые для сетевого DDE.</span><span class="sxs-lookup"><span data-stu-id="8fbeb-112">The network DDE agent also starts the applications necessary for network DDE.</span></span> <span data-ttu-id="8fbeb-113">После запуска сетевого DDE сеансы DDE контролируются через окно сетевого DDE, связанное с одним из приложений сетевого DDE.</span><span class="sxs-lookup"><span data-stu-id="8fbeb-113">After network DDE is started, DDE conversations are controlled through a network DDE window associated with one of the network DDE applications.</span></span> <span data-ttu-id="8fbeb-114">Это приложение выступает в качестве прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="8fbeb-114">This application acts as a proxy.</span></span> <span data-ttu-id="8fbeb-115">Он взаимодействует со всеми локальными и удаленными приложениями DDE.</span><span class="sxs-lookup"><span data-stu-id="8fbeb-115">It communicates with all local and remote DDE applications.</span></span>

 

 



