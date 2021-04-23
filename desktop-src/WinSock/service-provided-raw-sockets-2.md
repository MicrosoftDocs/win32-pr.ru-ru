---
description: Необработанный сокет — это тип сокета, который обеспечивает доступ к базовому поставщику транспорта. Использование необработанных сокетов при переносе приложений в Winsock не рекомендуется по нескольким причинам.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Необработанные сокеты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209c884e85327a7a8c1d21292d9342a0c032747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155870"
---
# <a name="raw-sockets"></a><span data-ttu-id="3778c-104">Необработанные сокеты</span><span class="sxs-lookup"><span data-stu-id="3778c-104">Raw Sockets</span></span>

<span data-ttu-id="3778c-105">Необработанный сокет — это тип сокета, который обеспечивает доступ к базовому поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="3778c-105">A raw socket is a type of socket that allows access to the underlying transport provider.</span></span> <span data-ttu-id="3778c-106">Использование необработанных сокетов при переносе приложений в Winsock не рекомендуется по нескольким причинам.</span><span class="sxs-lookup"><span data-stu-id="3778c-106">The use of raw sockets when porting applications to Winsock is not recommended for several reasons.</span></span>

<span data-ttu-id="3778c-107">Спецификация Windows Sockets не требует, чтобы поставщик службы Winsock поддерживал необработанные сокеты, то есть сокеты типа **Сокк \_ RAW**.</span><span class="sxs-lookup"><span data-stu-id="3778c-107">The Windows Sockets specification does not mandate that a Winsock service provider support raw sockets, that is, sockets of type **SOCK\_RAW**.</span></span> <span data-ttu-id="3778c-108">Однако поставщикам услуг рекомендуется предоставлять поддержку необработанных сокетов.</span><span class="sxs-lookup"><span data-stu-id="3778c-108">However, service providers are encouraged to supply raw socket support.</span></span> <span data-ttu-id="3778c-109">Приложение, совместимое с сокетами Windows и желающее использовать необработанные сокеты, должно попытаться открыть сокет с помощью вызова [**сокета**](/windows/desktop/api/Winsock2/nf-winsock2-socket) , а если не удается использовать другой тип сокета или указать на ошибку пользователя.</span><span class="sxs-lookup"><span data-stu-id="3778c-109">A Windows Sockets-compliant application that wishes to use raw sockets should attempt to open the socket with the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) call, and if it fails either attempt to use another socket type or indicate the failure to the user.</span></span>

<span data-ttu-id="3778c-110">В Windows 7, Windows Server 2008 R2, Windows Vista и Windows XP с пакетом обновления 2 (SP2) возможность отправки трафика через необработанные сокеты ограничена несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="3778c-110">On Windows 7, Windows Server 2008 R2, Windows Vista, and Windows XP with Service Pack 2 (SP2), the ability to send traffic over raw sockets has been restricted in several ways.</span></span> <span data-ttu-id="3778c-111">Дополнительные сведения см. в разделе [необработанные сокеты TCP/IP](tcp-ip-raw-sockets-2.md).</span><span class="sxs-lookup"><span data-stu-id="3778c-111">For more information, see [TCP/IP Raw Sockets](tcp-ip-raw-sockets-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3778c-112">См. также</span><span class="sxs-lookup"><span data-stu-id="3778c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3778c-113">Перенос приложений сокета в Winsock</span><span class="sxs-lookup"><span data-stu-id="3778c-113">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="3778c-114">**фиксатор**</span><span class="sxs-lookup"><span data-stu-id="3778c-114">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="3778c-115">Необработанные сокеты TCP/IP</span><span class="sxs-lookup"><span data-stu-id="3778c-115">TCP/IP Raw Sockets</span></span>](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[<span data-ttu-id="3778c-116">Вопросы программирования Winsock</span><span class="sxs-lookup"><span data-stu-id="3778c-116">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



