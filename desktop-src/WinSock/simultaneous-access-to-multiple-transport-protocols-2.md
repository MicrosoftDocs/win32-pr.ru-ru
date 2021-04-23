---
description: Транспортный протокол должен быть правильно установлен в системе и зарегистрирован с помощью сокетов Windows, чтобы быть доступным для приложения.
ms.assetid: 45b20f66-4e12-44df-b64b-c96cd5b24cd4
title: Одновременный доступ к нескольким транспортным протоколам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e4b9d97743691bc527c455881cd0da5803b62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702009"
---
# <a name="simultaneous-access-to-multiple-transport-protocols"></a><span data-ttu-id="995be-103">Одновременный доступ к нескольким транспортным протоколам</span><span class="sxs-lookup"><span data-stu-id="995be-103">Simultaneous Access to Multiple Transport Protocols</span></span>

<span data-ttu-id="995be-104">Транспортный протокол должен быть правильно установлен в системе и зарегистрирован с помощью сокетов Windows, чтобы быть доступным для приложения.</span><span class="sxs-lookup"><span data-stu-id="995be-104">A transport protocol must be properly installed on the system and registered with Windows Sockets to be accessible to an application.</span></span> <span data-ttu-id="995be-105">\_Библиотека32.dll Ws2 экспортирует набор функций для упрощения процесса регистрации.</span><span class="sxs-lookup"><span data-stu-id="995be-105">The Ws2\_32.dll library exports a set of functions to facilitate the registration process.</span></span> <span data-ttu-id="995be-106">Сюда входит создание новой регистрации и удаление существующей.</span><span class="sxs-lookup"><span data-stu-id="995be-106">This includes creating a new registration and removing an existing one.</span></span>

<span data-ttu-id="995be-107">При создании новых регистраций вызывающий объект (то есть сценарий установки поставщика стека) предоставляет одну или несколько заполненных структур сведений о [**всапротокол \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) , содержащих полный набор сведений о протоколе.</span><span class="sxs-lookup"><span data-stu-id="995be-107">When new registrations are created, the caller (that is, the stack vendor's installation script) supplies one or more filled in [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structures containing a complete set of information about the protocol.</span></span> <span data-ttu-id="995be-108">Дополнительные сведения см. в разделе [SPI Windows Sockets 2](about-the-winsock-spi.md).</span><span class="sxs-lookup"><span data-stu-id="995be-108">For more information, see [Windows Sockets 2 SPI](about-the-winsock-spi.md).</span></span> <span data-ttu-id="995be-109">Любой транспортный стек, установленный таким образом, называется поставщиком службы Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="995be-109">Any transport stack installed in this manner is referred to as a Windows Sockets service provider.</span></span>

<span data-ttu-id="995be-110">В Windows XP с пакетом обновления 2 (SP2), Windows Server 2003 с пакетом обновления 1 (SP1) и Windows Vista и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="995be-110">On Windows XP with Service Pack 2 (SP2), Windows Server 2003 with Service Pack 1 (SP1), and Windows Vista and later.</span></span> <span data-ttu-id="995be-111">каталог Winsock, содержащий список установленных поставщиков транспорта и пространств имен, можно отобразить в командной строке с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="995be-111">the Winsock catalog that contains a list of installed transport and namespace providers can be displayed in a command prompt with the following command:</span></span>

<span data-ttu-id="995be-112">**Netsh Winsock показывать каталог**</span><span class="sxs-lookup"><span data-stu-id="995be-112">**netsh winsock show catalog**</span></span>

<span data-ttu-id="995be-113">Пакет средств разработки программного обеспечения (SDK) для Microsoft Windows включает *Sporder.exe*, позволяющий пользователю просматривать и изменять порядок перечисления поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="995be-113">The Microsoft Windows Software Development Kit (SDK) includes *Sporder.exe*, which enables the user to view and modify the order in which service providers are enumerated.</span></span> <span data-ttu-id="995be-114">Используя *Sporder.exe*, пользователь может вручную установить определенный стек протокола TCP/IP в качестве поставщика TCP/IP по умолчанию, если имеется более одного такого стека.</span><span class="sxs-lookup"><span data-stu-id="995be-114">Using *Sporder.exe*, a user can manually establish a particular TCP/IP protocol stack as the default TCP/IP provider if more than one such stack is present.</span></span>

<span data-ttu-id="995be-115">Приложение *Sporder.exe* использует экспортированные функции из *Sporder.dll* для переупорядочивания поставщиков служб.</span><span class="sxs-lookup"><span data-stu-id="995be-115">The *Sporder.exe* application uses exported functions from *Sporder.dll* to reorder the service providers.</span></span> <span data-ttu-id="995be-116">В результате приложения установки могут использовать интерфейс, предоставленный *Sporder.dll* , для программного переупорядочивания поставщиков служб.</span><span class="sxs-lookup"><span data-stu-id="995be-116">As a result, installation applications can use the interface provided by *Sporder.dll* to programmatically reorder service providers.</span></span>

-   [<span data-ttu-id="995be-117">Многоуровневые протоколы и цепочки протоколов</span><span class="sxs-lookup"><span data-stu-id="995be-117">Layered Protocols and Protocol Chains</span></span>](layered-protocols-and-protocol-chains-2.md)
-   [<span data-ttu-id="995be-118">Использование нескольких протоколов</span><span class="sxs-lookup"><span data-stu-id="995be-118">Using Multiple Protocols</span></span>](using-multiple-protocols-2.md)
-   [<span data-ttu-id="995be-119">Множественные ограничения поставщика для Select</span><span class="sxs-lookup"><span data-stu-id="995be-119">Multiple Provider Restrictions on Select</span></span>](multiple-provider-restrictions-on-select-2.md)

 

 
