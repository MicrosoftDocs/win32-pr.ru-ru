---
title: Bluetooth и жетсоккопт
description: Bluetooth использует функцию жетсоккопт для запроса различных параметров, связанных с каналом сервера или соединением.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- жетсоккопт
- Bluetooth и жетсоккопт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dede19b27eea39b7d1e778b3e92312a5e148c0ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792421"
---
# <a name="bluetooth-and-getsockopt"></a><span data-ttu-id="da58e-106">Bluetooth и жетсоккопт</span><span class="sxs-lookup"><span data-stu-id="da58e-106">Bluetooth and getsockopt</span></span>

<span data-ttu-id="da58e-107">Bluetooth использует функцию [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) для запроса различных параметров, связанных с каналом сервера или соединением.</span><span class="sxs-lookup"><span data-stu-id="da58e-107">Bluetooth uses the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function to query various parameters associated with the server channel or the connection.</span></span> <span data-ttu-id="da58e-108">Использование **жетсоккопт** с Bluetooth имеет следующие требования.</span><span class="sxs-lookup"><span data-stu-id="da58e-108">Use of **getsockopt** with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="da58e-109">Параметр *s* параметра [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) должен быть допустимым сокетом Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="da58e-109">The *s* parameter of [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) must be a valid Bluetooth socket.</span></span>
-   <span data-ttu-id="da58e-110">Параметр *Level* параметра [**ЖЕТСОККОПТ**](/windows/desktop/api/winsock/nf-winsock-getsockopt) должен быть Sol \_ RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="da58e-110">The *level* parameter of [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) must be SOL\_RFCOMM.</span></span>

<span data-ttu-id="da58e-111">Список доступных параметров сокетов Bluetooth см. в разделе [Параметры Bluetooth и сокета](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="da58e-111">For a listing of available Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="da58e-112">См. также</span><span class="sxs-lookup"><span data-stu-id="da58e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da58e-113">Сокеты Windows</span><span class="sxs-lookup"><span data-stu-id="da58e-113">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="da58e-114">**жетсоккопт**</span><span class="sxs-lookup"><span data-stu-id="da58e-114">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 