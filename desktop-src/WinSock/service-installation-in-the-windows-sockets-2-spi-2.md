---
description: Установка службы в Windows Sockets 2 (Winsock) SPI.
ms.assetid: a303fbcf-9122-422a-9b12-d00a5df0fc0f
title: Установка службы в списке SPI Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9028f35c21cc7055e8b8dde060c1c178dbf76715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692836"
---
# <a name="service-installation-in-the-windows-sockets-2-spi"></a><span data-ttu-id="b14d6-103">Установка службы в списке SPI Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="b14d6-103">Service Installation in the Windows Sockets 2 SPI</span></span>

-   [<span data-ttu-id="b14d6-104">**нспинсталлсервицекласс**</span><span class="sxs-lookup"><span data-stu-id="b14d6-104">**NSPInstallServiceClass**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [<span data-ttu-id="b14d6-105">**нспремовесервицекласс**</span><span class="sxs-lookup"><span data-stu-id="b14d6-105">**NSPRemoveServiceClass**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [<span data-ttu-id="b14d6-106">**нспсетсервице**</span><span class="sxs-lookup"><span data-stu-id="b14d6-106">**NSPSetService**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

<span data-ttu-id="b14d6-107">Если требуемый класс службы еще не существует, клиент SPI пространства имен использует [**нспинсталлсервицекласс**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) для установки нового класса службы путем указания имени класса службы, идентификатора GUID для идентификатора класса службы и ряда структур [**всансклассинфо**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) .</span><span class="sxs-lookup"><span data-stu-id="b14d6-107">When the required service class does not already exist, a namespace SPI client uses [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) to install a new service class by supplying a service class name, a GUID for the service class identifier, and a series of [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) structures.</span></span> <span data-ttu-id="b14d6-108">Эти структуры зависят от конкретного пространства имен и предоставляют общие значения, такие как Рекомендуемые номера TCP-портов или идентификаторы NetWare SAP.</span><span class="sxs-lookup"><span data-stu-id="b14d6-108">These structures are each specific to a particular namespace, and supply common values such as recommended TCP port numbers or NetWare SAP Identifiers.</span></span> <span data-ttu-id="b14d6-109">Класс службы можно удалить путем вызова [**нспремовесервицекласс**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) и указания идентификатора GUID, соответствующего идентификатору класса.</span><span class="sxs-lookup"><span data-stu-id="b14d6-109">A service class can be removed by calling [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) and supplying the GUID corresponding to the class identifier.</span></span>

<span data-ttu-id="b14d6-110">После существования класса службы определенные экземпляры службы могут быть установлены или удалены через [**нспсетсервице**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice).</span><span class="sxs-lookup"><span data-stu-id="b14d6-110">Once a service class exists, specific instances of a service can be installed or removed via [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice).</span></span> <span data-ttu-id="b14d6-111">Эта функция принимает структуру [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) в качестве входного параметра вместе с кодом операции и флагами операций.</span><span class="sxs-lookup"><span data-stu-id="b14d6-111">This function takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as an input parameter along with an operation code and operation flags.</span></span> <span data-ttu-id="b14d6-112">Код операции указывает, выполняется ли установка или удаление службы.</span><span class="sxs-lookup"><span data-stu-id="b14d6-112">The operation code indicates whether the service is being installed or removed.</span></span> <span data-ttu-id="b14d6-113">Структура **всакуерисет** предоставляет все необходимые сведения о службе, включая идентификатор класса службы, имя службы (для этого экземпляра), применимый идентификатор пространства имен и сведения о протоколе, а также набор транспортных адресов, на который прослушивается служба.</span><span class="sxs-lookup"><span data-stu-id="b14d6-113">The **WSAQUERYSET** structure provides all of the relevant information about the service including service class identifier, service name (for this instance), applicable namespace identifier and protocol information, and a set of transport addresses to which the service listens.</span></span>

 

 



