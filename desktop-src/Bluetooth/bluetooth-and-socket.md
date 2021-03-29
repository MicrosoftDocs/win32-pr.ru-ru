---
title: Bluetooth и сокет
description: Создает сокет для входящих или исходящих соединений.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth Bluetooth
- сокет Bluetooth
- Bluetooth и сокет Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2c2085ee0c61941bab93ed25dd86f5c102d0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791887"
---
# <a name="bluetooth-and-socket"></a><span data-ttu-id="b680e-106">Bluetooth и сокет</span><span class="sxs-lookup"><span data-stu-id="b680e-106">Bluetooth and socket</span></span>

<span data-ttu-id="b680e-107">Функция [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) создает сокет для входящих или исходящих соединений.</span><span class="sxs-lookup"><span data-stu-id="b680e-107">The [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) function creates a socket for incoming or outgoing connections.:</span></span>

<span data-ttu-id="b680e-108">Чтобы создать сокет с помощью Bluetooth, используйте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="b680e-108">To create a socket using Bluetooth, use the following settings:</span></span>

-   <span data-ttu-id="b680e-109">Параметр *AF* функции [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) всегда имеет значение **AF \_ БС** для сокетов Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="b680e-109">The *af* parameter of the [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) function is always set to **AF\_BTH** for Bluetooth sockets.</span></span>
-   <span data-ttu-id="b680e-110">Параметр *типа* функции [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) всегда **Сокк \_ Stream**; **Сокк \_** Сокеты дграм не поддерживаются Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="b680e-110">The *type* parameter of the [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) function is always **SOCK\_STREAM**; **SOCK\_DGRAM** sockets are not supported by Bluetooth.</span></span>
-   <span data-ttu-id="b680e-111">Для параметра *протокола* **бспрото \_ RFCOMM** является поддерживаемым протоколом.</span><span class="sxs-lookup"><span data-stu-id="b680e-111">For the *protocol* parameter, **BTHPROTO\_RFCOMM** is the supported protocol.</span></span>

<span data-ttu-id="b680e-112">Дополнительные сведения см. в разделе [сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2).</span><span class="sxs-lookup"><span data-stu-id="b680e-112">For more information, see [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b680e-113">См. также</span><span class="sxs-lookup"><span data-stu-id="b680e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b680e-114">Сокеты Windows</span><span class="sxs-lookup"><span data-stu-id="b680e-114">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="b680e-115">**фиксатор**</span><span class="sxs-lookup"><span data-stu-id="b680e-115">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 