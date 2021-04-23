---
description: Ниже приведено краткое справочное занятие по обеспечению безопасности при программировании сокетов Windows.
ms.assetid: 70210e86-ead6-4b0c-ae47-66b2ef0a8d11
title: Безопасное программирование Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70d7a0710a4446486835ec14435fa7d7ba1458c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812455"
---
# <a name="secure-winsock-programming"></a><span data-ttu-id="6ab0e-103">Безопасное программирование Winsock</span><span class="sxs-lookup"><span data-stu-id="6ab0e-103">Secure Winsock Programming</span></span>

<span data-ttu-id="6ab0e-104">Ниже приведено краткое справочное занятие по обеспечению безопасности при программировании сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="6ab0e-104">The following is a guide to secure Windows Sockets programming.</span></span> <span data-ttu-id="6ab0e-105">Он предназначен для понимания безопасности Winsock и вариантов, доступных разработчику защищенных сетевых приложений.</span><span class="sxs-lookup"><span data-stu-id="6ab0e-105">It is designed to provide an understanding of Winsock security and the options available to the secure network application developer.</span></span>

-   [<span data-ttu-id="6ab0e-106">Использование \_ реусеаддр и так далее \_ ексклусивеаддрусе</span><span class="sxs-lookup"><span data-stu-id="6ab0e-106">Using SO\_REUSEADDR and SO\_EXCLUSIVEADDRUSE</span></span>](using-so-reuseaddr-and-so-exclusiveaddruse.md)
-   [<span data-ttu-id="6ab0e-107">Расширения безопасных сокетов Winsock</span><span class="sxs-lookup"><span data-stu-id="6ab0e-107">Winsock Secure Socket Extensions</span></span>](winsock-secure-socket-extensions.md)

<span data-ttu-id="6ab0e-108">Связь с помощью сокетов также может быть зашифрована с помощью стандартов SSL/TLS с помощью защищенного канала, также известного как технология SChannel.</span><span class="sxs-lookup"><span data-stu-id="6ab0e-108">Communications using sockets can also be encrypted using the SSL/TLS standards using Secure Channel, also known as Schannel technology.</span></span> <span data-ttu-id="6ab0e-109">Schannel — это поставщик поддержки безопасности (SSP), который содержит набор протоколов безопасности, обеспечивающих проверку подлинности и безопасную закрытую связь с помощью шифрования.</span><span class="sxs-lookup"><span data-stu-id="6ab0e-109">Schannel is a security support provider (SSP) that contains a set of security protocols that provide identity authentication and secure, private communication through encryption.</span></span> <span data-ttu-id="6ab0e-110">Schannel в основном используется для Интернет-приложений, требующих обмена данными по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="6ab0e-110">Schannel is primarily used for Internet applications that require secure Hypertext Transfer Protocol (HTTP) communications.</span></span> <span data-ttu-id="6ab0e-111">Дополнительные сведения см. в разделе [безопасный канал](../secauthn/secure-channel.md).</span><span class="sxs-lookup"><span data-stu-id="6ab0e-111">For more information, please see [Secure Channel](../secauthn/secure-channel.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ab0e-112">См. также</span><span class="sxs-lookup"><span data-stu-id="6ab0e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ab0e-113">Secure Channel</span><span class="sxs-lookup"><span data-stu-id="6ab0e-113">Secure Channel</span></span>](../secauthn/secure-channel.md)
</dt> </dl>

 

 
