---
title: Bluetooth и прослушивание, выбор и функции closesocket
description: Bluetooth использует функции прослушивания, выбора и функции closesocket без каких бы то ни было изменений в стандартном программировании Windows Sockets.
ms.assetid: b64440de-bc63-4e3b-bfd9-5cf783f36c23
keywords:
- Bluetooth
- функции closesocket
- прослушивание
- select
- Bluetooth и прослушивание
- Bluetooth и прослушивать, выберите
- Bluetooth и прослушивание, выбор и функции closesocket
- прослушивание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e442cfc0593ab5be297902487c7c3ccdf056b4e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487913"
---
# <a name="bluetooth-and-listen-select-and-closesocket"></a><span data-ttu-id="7a923-111">Bluetooth и прослушивание, выбор и функции closesocket</span><span class="sxs-lookup"><span data-stu-id="7a923-111">Bluetooth and listen, select, and closesocket</span></span>

<span data-ttu-id="7a923-112">Bluetooth использует функции [**прослушивания**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**выбора**](/windows/desktop/api/winsock2/nf-winsock2-select)и [**функции closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) без каких бы то ни было изменений в стандартном программировании Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="7a923-112">Bluetooth uses the [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**select**](/windows/desktop/api/winsock2/nf-winsock2-select), and [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) functions without any modification from standard Windows Sockets programming.</span></span>

<span data-ttu-id="7a923-113">Как и в случае с сокетами Windows, функция [**функции closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) освобождает ресурсы, связанные с сокетом.</span><span class="sxs-lookup"><span data-stu-id="7a923-113">As with Windows Sockets, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function frees resources associated with the socket.</span></span>

<span data-ttu-id="7a923-114">При вызове функции [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) настоятельно рекомендуется использовать низкое значение для параметра *невыполненной работы* (обычно от 2 до 4), поскольку принимаются только несколько клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="7a923-114">When calling the [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) function, it is strongly recommended that a low value is used for the *backlog* parameter (typically 2 to 4), since only a few client connections are accepted.</span></span> <span data-ttu-id="7a923-115">Это сокращает количество системных ресурсов, выделенных для использования сокетом прослушивания.</span><span class="sxs-lookup"><span data-stu-id="7a923-115">This reduces the system resources that are allocated for use by the listening socket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a923-116">См. также</span><span class="sxs-lookup"><span data-stu-id="7a923-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a923-117">Сокеты Windows</span><span class="sxs-lookup"><span data-stu-id="7a923-117">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="7a923-118">**функции closesocket**</span><span class="sxs-lookup"><span data-stu-id="7a923-118">**closesocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[<span data-ttu-id="7a923-119">**слушивают**</span><span class="sxs-lookup"><span data-stu-id="7a923-119">**listen**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-listen)
</dt> <dt>

[<span data-ttu-id="7a923-120">**метьте**</span><span class="sxs-lookup"><span data-stu-id="7a923-120">**select**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-select)
</dt> </dl>

 

 