---
title: Bluetooth и сетсоккопт
description: Bluetooth использует функцию сетсоккопт для установки различных параметров, связанных с каналом сервера или соединением.
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- сетсоккопт
- Bluetooth и сетсоккопт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943839a49788b76e597596aee9cba65fa4b8d30d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337753"
---
# <a name="bluetooth-and-setsockopt"></a><span data-ttu-id="02818-106">Bluetooth и сетсоккопт</span><span class="sxs-lookup"><span data-stu-id="02818-106">Bluetooth and setsockopt</span></span>

<span data-ttu-id="02818-107">Bluetooth использует функцию [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) для установки различных параметров, связанных с каналом сервера или соединением.</span><span class="sxs-lookup"><span data-stu-id="02818-107">Bluetooth uses the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to set various parameters associated with the server channel or the connection.</span></span> <span data-ttu-id="02818-108">Использование **сетсоккопт** с Bluetooth имеет следующие требования.</span><span class="sxs-lookup"><span data-stu-id="02818-108">Use of **setsockopt** with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="02818-109">Параметр *s* параметра [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) должен быть допустимым сокетом Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="02818-109">The *s* parameter of [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) must be a valid Bluetooth socket.</span></span>
-   <span data-ttu-id="02818-110">Параметр *Level* параметра [**СЕТСОККОПТ**](/windows/desktop/api/winsock/nf-winsock-setsockopt) должен быть Sol \_ RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="02818-110">The *level* parameter of [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) must be SOL\_RFCOMM.</span></span>

<span data-ttu-id="02818-111">Список доступных параметров сокетов Bluetooth см. в разделе [Параметры Bluetooth и сокета](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="02818-111">For a listing of available Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02818-112">См. также</span><span class="sxs-lookup"><span data-stu-id="02818-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02818-113">Сокеты Windows</span><span class="sxs-lookup"><span data-stu-id="02818-113">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="02818-114">**сетсоккопт**</span><span class="sxs-lookup"><span data-stu-id="02818-114">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 