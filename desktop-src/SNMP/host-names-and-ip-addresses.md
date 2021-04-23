---
title: Имена узлов и IP-адреса
description: Для сетей TCP/IP имена узлов должны быть разрешены на IP-адреса, прежде чем можно будет использовать сведения об адресе для создания соединения.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- Имена узлов и IP-адреса SNMP
- Имена узлов, разрешение SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f711be9e1fda5dc936db6628cccc21093aa09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775116"
---
# <a name="host-names-and-ip-addresses"></a><span data-ttu-id="ea599-105">Имена узлов и IP-адреса</span><span class="sxs-lookup"><span data-stu-id="ea599-105">Host Names and IP Addresses</span></span>

<span data-ttu-id="ea599-106">Для сетей TCP/IP имена узлов должны быть разрешены на IP-адреса, прежде чем можно будет использовать сведения об адресе для создания соединения.</span><span class="sxs-lookup"><span data-stu-id="ea599-106">TCP/IP networks require host names to be resolved to IP addresses before the address information can be used to create a connection.</span></span> <span data-ttu-id="ea599-107">Компьютеры, работающие в операционной системе Windows, используют файл узла, который для этой цели сопоставляет имена узлов с IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="ea599-107">Computers running on the Windows operating system use a host file that, for this purpose, maps host names to IP addresses.</span></span>

<span data-ttu-id="ea599-108">Файл узла — это текстовый файл, в котором перечислены явные имена узлов и IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ea599-108">The host file is a text file that lists explicit host names and IP addresses.</span></span> <span data-ttu-id="ea599-109">Файл узла автоматически загружается в память при запуске и обращается в систему, когда требуется разрешение имени узла.</span><span class="sxs-lookup"><span data-stu-id="ea599-109">The host file is automatically loaded into memory on startup and consulted when a host name requires resolution.</span></span> <span data-ttu-id="ea599-110">Если файл узла не содержит сведений о сопоставлении, необходимых для разрешения определенного имени узла в IP-адрес, выполняется запрос на разрешение для DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="ea599-110">If the host file does not contain the mapping information that is required to resolve a specific host name to its IP address, a resolution query is made to a DNS server.</span></span>

<span data-ttu-id="ea599-111">Протокол SNMP использует Windows Internet Служба именования (WINS) для разрешения имен узлов.</span><span class="sxs-lookup"><span data-stu-id="ea599-111">SNMP uses the Windows Internet Naming Service (WINS) for host name resolution.</span></span> <span data-ttu-id="ea599-112">Служба WINS позволяет сопоставлять имена NetBIOS, или имена компьютеров, с IP-адресами в сетях TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="ea599-112">WINS makes it possible to map NetBIOS names, or machine names, to IP addresses on TCP/IP networks.</span></span> <span data-ttu-id="ea599-113">Если компьютеру не удается получить доступ к WINS-серверу, служба SNMP использует файл узла для разрешения имен узлов в IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ea599-113">If the computer cannot access a WINS server, the SNMP service uses the host file to resolve host names to IP addresses.</span></span>

<span data-ttu-id="ea599-114">Служба SNMP поддерживает использование как имен узлов, так и IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="ea599-114">The SNMP service supports the use of both host names and IP addresses.</span></span> <span data-ttu-id="ea599-115">Однако при наличии выбора между использованием имен узлов или IP-адресов для обнаружения сетевых расположений в приложениях управления SNMP должны использоваться имена узлов.</span><span class="sxs-lookup"><span data-stu-id="ea599-115">However, when you have a choice between using host names or IP addresses to identify network locations, your SNMP management applications should use host names.</span></span> <span data-ttu-id="ea599-116">При использовании имен узлов добавьте все сопоставления имен узлов и IP-адресов участвующих систем в файл узла.</span><span class="sxs-lookup"><span data-stu-id="ea599-116">If you use host names, add all host name and IP address mappings of the participating systems to the host file.</span></span>

 

 




