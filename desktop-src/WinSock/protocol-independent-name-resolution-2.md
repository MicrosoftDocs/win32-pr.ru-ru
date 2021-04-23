---
description: Независимое от протокола разрешение имен и сокеты Windows (Winsock).
ms.assetid: f55219b9-1518-4b49-a0da-6a3fa025cca3
title: Разрешение имен Protocol-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cafed9759a4ca5431dafb230e7f09578ff1c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343475"
---
# <a name="protocol-independent-name-resolution"></a><span data-ttu-id="05475-103">Разрешение имен Protocol-Independent</span><span class="sxs-lookup"><span data-stu-id="05475-103">Protocol-Independent Name Resolution</span></span>

<span data-ttu-id="05475-104">При разработке независимого от протокола клиентского или серверного приложения существует два основных требования, которые связаны с разрешением имен и регистрацией:</span><span class="sxs-lookup"><span data-stu-id="05475-104">In developing a protocol-independent client/server application, there are two basic requirements that exist with respect to name resolution and registration:</span></span>

-   <span data-ttu-id="05475-105">Возможность серверной части приложения (службы) регистрировать свое существование в одном или нескольких пространствах имен (или стать доступным).</span><span class="sxs-lookup"><span data-stu-id="05475-105">The ability of the server half of the application ( service) to register its existence within (or become accessible to) one or more namespaces.</span></span>
-   <span data-ttu-id="05475-106">Способность клиентского приложения находить службу в пространстве имен и получать требуемый транспортный протокол и сведения об адресации.</span><span class="sxs-lookup"><span data-stu-id="05475-106">The ability of the client application to find the service within a namespace and obtain the required transport protocol and addressing information.</span></span>

<span data-ttu-id="05475-107">Для тех, которые привыкли к разработке приложений на основе TCP/IP, может показаться, что требуется немного больше, чем поиск адреса узла и использование согласованного по номеру порта.</span><span class="sxs-lookup"><span data-stu-id="05475-107">For those accustomed to developing TCP/IP-based applications, this may seem to involve little more than looking up a host address and then using an agreed upon port number.</span></span> <span data-ttu-id="05475-108">Другие схемы сети, тем не менее, разрешают расположение службы, протокол, используемый для службы, и другие атрибуты, которые обнаруживаются во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="05475-108">Other networking schemes however, allow the location of the service, the protocol used for the service, and other attributes to be discovered at run time.</span></span> <span data-ttu-id="05475-109">Для поддержки широкого спектра возможностей, имеющихся в существующих службах имен, интерфейс Windows Sockets 2 использует модель, описанную в подразделах этого раздела.</span><span class="sxs-lookup"><span data-stu-id="05475-109">To accommodate the broad diversity of capabilities found in existing name services, the Windows Sockets 2 interface adopts the model described in the topics in this section.</span></span>

<span data-ttu-id="05475-110">В этом разделе описываются независимые от протокола возможности разрешения имен, доступные для разработчиков Winsock.</span><span class="sxs-lookup"><span data-stu-id="05475-110">This section describes protocol-independent name resolution capabilities available to Winsock developers.</span></span> <span data-ttu-id="05475-111">В следующем списке перечислены подразделы этого раздела.</span><span class="sxs-lookup"><span data-stu-id="05475-111">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="05475-112">Модель разрешения имен</span><span class="sxs-lookup"><span data-stu-id="05475-112">Name Resolution Model</span></span>](name-resolution-model-2.md)
-   [<span data-ttu-id="05475-113">Общие сведения о функциях разрешения имен</span><span class="sxs-lookup"><span data-stu-id="05475-113">Summary of Name Resolution Functions</span></span>](summary-of-name-resolution-functions-2.md)
-   [<span data-ttu-id="05475-114">Структуры данных разрешения имен</span><span class="sxs-lookup"><span data-stu-id="05475-114">Name Resolution Data Structures</span></span>](name-resolution-data-structures-2.md)

## <a name="related-topics"></a><span data-ttu-id="05475-115">См. также</span><span class="sxs-lookup"><span data-stu-id="05475-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05475-116">Регистрация и разрешение имен</span><span class="sxs-lookup"><span data-stu-id="05475-116">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



