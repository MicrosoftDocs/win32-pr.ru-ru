---
description: Общие ресурсы DDE — это ресурсы компьютера.
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: Общие ресурсы DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 012c219897187c9e68b5b9e662b93678b77974c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910208"
---
# <a name="dde-shares"></a><span data-ttu-id="85626-103">Общие ресурсы DDE</span><span class="sxs-lookup"><span data-stu-id="85626-103">DDE Shares</span></span>

<span data-ttu-id="85626-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="85626-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="85626-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="85626-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="85626-106">Общие ресурсы DDE — это ресурсы компьютера.</span><span class="sxs-lookup"><span data-stu-id="85626-106">DDE shares are a machine resource.</span></span> <span data-ttu-id="85626-107">Они похожи на общие файловые ресурсы, так как они используются для управления доступом к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="85626-107">They are similar to file shares because they are used to control access to a resource.</span></span> <span data-ttu-id="85626-108">При использовании файловых ресурсов ресурс является файлом.</span><span class="sxs-lookup"><span data-stu-id="85626-108">With file shares, the resource is a file.</span></span> <span data-ttu-id="85626-109">При использовании общих ресурсов DDE ресурс динамически обменивается данными.</span><span class="sxs-lookup"><span data-stu-id="85626-109">With DDE shares, the resource is dynamically exchanged data.</span></span> <span data-ttu-id="85626-110">Тип обмена данными определяется серверным приложением, предоставляющим данные, и клиентским приложением, которое запрашивает данные.</span><span class="sxs-lookup"><span data-stu-id="85626-110">The type of data exchanged is determined by the server application that supplies the data and the client application that requests the data.</span></span>

<span data-ttu-id="85626-111">Сервер вызывает функцию [**нддешареадд**](nddeshareadd.md) для создания общего ресурса DDE, который хранится в диспетчере общей базы данных DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="85626-111">The server calls the [**NDdeShareAdd**](nddeshareadd.md) function to create the DDE share, which is stored in the DDE share database manager (DSDM).</span></span>

<span data-ttu-id="85626-112">Клиент запускает сеанс DDE, подключаясь к общему ресурсу DDE.</span><span class="sxs-lookup"><span data-stu-id="85626-112">The client starts the DDE conversation by connecting to the DDE share.</span></span> <span data-ttu-id="85626-113">Клиент должен вызвать функцию [**ддеинитиализе**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) для инициализации ддемл и вызвать функцию [**ддеконнект**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) для подключения к общему ресурсу DDE.</span><span class="sxs-lookup"><span data-stu-id="85626-113">The client must call the [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) function to initialize DDEML and call the [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) function to connect to the DDE share.</span></span> <span data-ttu-id="85626-114">В вызове **ддеконнект** клиент указывает имя службы следующим образом:</span><span class="sxs-lookup"><span data-stu-id="85626-114">In the **DdeConnect** call, the client specifies the service name as follows:</span></span>

<span data-ttu-id="85626-115">\\\\*Имя компьютера* \\ НДДЕ $</span><span class="sxs-lookup"><span data-stu-id="85626-115">\\\\*ComputerName*\\NDDE$</span></span>

<span data-ttu-id="85626-116">где *ComputerName* — имя компьютера, на котором работает серверное приложение.</span><span class="sxs-lookup"><span data-stu-id="85626-116">where *ComputerName* is the name of the computer running the server application.</span></span> <span data-ttu-id="85626-117">НДДЕ $ указывает, что в разделе [**ддеконнект**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) указано имя общего ресурса DDE на удаленном компьютере с именем *ComputerName*.</span><span class="sxs-lookup"><span data-stu-id="85626-117">The NDDE$ indicates that the topic provided to [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) is the DDE share name on the remote computer named *ComputerName*.</span></span>

<span data-ttu-id="85626-118">Существует три типа общих ресурсов DDE: старый стиль, новый стиль и статический.</span><span class="sxs-lookup"><span data-stu-id="85626-118">There are three types of DDE shares: old style, new style, and static.</span></span> <span data-ttu-id="85626-119">Обычно поддерживается только статический тип.</span><span class="sxs-lookup"><span data-stu-id="85626-119">It is typical to support only the static type.</span></span> <span data-ttu-id="85626-120">Имена статических общих ресурсов используют следующее соглашение: *ShareName*$.</span><span class="sxs-lookup"><span data-stu-id="85626-120">The names of static shares use the following convention: *ShareName*$.</span></span>

 

 
