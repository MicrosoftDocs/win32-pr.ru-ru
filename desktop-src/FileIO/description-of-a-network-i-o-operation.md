---
description: Описывает процесс сетевой операции ввода-вывода в Windows.
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: Описание сетевой операции ввода-вывода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371b72389554f1c3fa2ec43180b1a6e4c76dc012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345802"
---
# <a name="description-of-a-network-io-operation"></a><span data-ttu-id="866ed-103">Описание сетевой операции ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="866ed-103">Description of a Network I/O Operation</span></span>

<span data-ttu-id="866ed-104">На следующем рисунке показан процесс сетевой операции ввода-вывода в Windows.</span><span class="sxs-lookup"><span data-stu-id="866ed-104">The following figure illustrates the process of a network I/O operation under Windows.</span></span>

![сетевая операция ввода-вывода в Windows](images/fig4.png)

<span data-ttu-id="866ed-106">Когда приложение вызывает функцию файлового ввода-вывода для доступа к файлу на удаленном компьютере, происходят следующие события.</span><span class="sxs-lookup"><span data-stu-id="866ed-106">When an application calls a file I/O function to access a file on a remote computer, the following events occur:</span></span>

-   <span data-ttu-id="866ed-107">Запрос ввода-вывода перехватывается [сетевым перенаправительм](network-redirectors.md), также называемым просто перенаправитель на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="866ed-107">The I/O request is intercepted by a [network redirector](network-redirectors.md), also referred to simply as a redirector, on the local computer.</span></span> <span data-ttu-id="866ed-108">Это показано на предыдущем рисунке с помощью сплошной стрелки между приложением и перенаправитель клиента.</span><span class="sxs-lookup"><span data-stu-id="866ed-108">This is depicted in the preceding figure by the solid arrow between the application and the client redirector.</span></span>
-   <span data-ttu-id="866ed-109">Перенаправитель конструирует пакет данных, содержащий всю информацию о запросе, и отправляет его на сервер, где расположен файл.</span><span class="sxs-lookup"><span data-stu-id="866ed-109">The redirector constructs a data packet containing all of the information about the request, and sends it to the server where the file is located.</span></span> <span data-ttu-id="866ed-110">Это показано на предыдущем рисунке с помощью сплошной стрелки между перенаправительм клиента и перенаправитель сервера.</span><span class="sxs-lookup"><span data-stu-id="866ed-110">This is depicted in the preceding figure by the solid arrow between the client redirector and the server redirector.</span></span>
-   <span data-ttu-id="866ed-111">Перенаправитель на сервере получает пакет от клиента, проверяет подлинность доступа к файлу, требуемому для запроса ввода-вывода, и, если он прошел проверку подлинности, выполняет запрос от имени клиента.</span><span class="sxs-lookup"><span data-stu-id="866ed-111">The redirector on the server receives the packet from the client, authenticates the access to the file required by the I/O request, and, if authenticated, executes the request on behalf of the client.</span></span> <span data-ttu-id="866ed-112">В противном случае возвращается код ошибки для перенаправителя на клиенте.</span><span class="sxs-lookup"><span data-stu-id="866ed-112">If not, it returns an error code to the redirector on the client.</span></span> <span data-ttu-id="866ed-113">Это показано на предыдущем рисунке на изогнутой сплошной стрелке между перенаправительм сервера и файлом.</span><span class="sxs-lookup"><span data-stu-id="866ed-113">This is depicted in the preceding figure by the curved solid arrow between the server redirector and the file.</span></span>
-   <span data-ttu-id="866ed-114">После выполнения запроса перенаправитель на сервере отправляет все данные, полученные в результате запроса ввода-вывода в перенаправитель на клиенте, а также уведомление об успешном выполнении.</span><span class="sxs-lookup"><span data-stu-id="866ed-114">When the request has been executed, the redirector on the server sends any data resulting from the I/O request to the redirector on the client along with a success notification.</span></span> <span data-ttu-id="866ed-115">На рисунке выше показана Пунктирная стрелка между сервером и перенаправитель клиента.</span><span class="sxs-lookup"><span data-stu-id="866ed-115">This is depicted in the preceding figure by the dotted arrow between the server and the client redirector.</span></span>
-   <span data-ttu-id="866ed-116">Перенаправитель на клиенте получает пакет от сервера и передает данные пакета в приложение вместе с уведомлением об успешном выполнении.</span><span class="sxs-lookup"><span data-stu-id="866ed-116">The redirector on the client receives the packet from the server and passes the data in the packet to the application along with a success notification.</span></span> <span data-ttu-id="866ed-117">На рисунке выше показана Пунктирная стрелка между перенаправлением клиента и приложением.</span><span class="sxs-lookup"><span data-stu-id="866ed-117">This is depicted in the preceding figure by the dotted arrow between the client redirector and the application.</span></span>

<span data-ttu-id="866ed-118">Windows может использовать различные сетевые протоколы для выполнения операций ввода-вывода в сети, в том числе [протокол SMB Microsoft и общие сведения о протоколе CIFS](microsoft-smb-protocol-and-cifs-protocol-overview.md) и NFS.</span><span class="sxs-lookup"><span data-stu-id="866ed-118">Windows can use a variety of networking protocols to perform a network I/O operation, including [Microsoft SMB Protocol and CIFS Protocol Overview](microsoft-smb-protocol-and-cifs-protocol-overview.md) and NFS.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="866ed-119">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="866ed-119">In this section</span></span>



| <span data-ttu-id="866ed-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="866ed-120">Topic</span></span>                                                                                       | <span data-ttu-id="866ed-121">Описание</span><span class="sxs-lookup"><span data-stu-id="866ed-121">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="866ed-122">Различия в локальных и сетевых операциях ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="866ed-122">Differences in Local and Network I/O</span></span>](differences-in-local-and-network-i-o.md)<br/> | <span data-ttu-id="866ed-123">Различия между локальными операциями ввода-вывода и сетевыми операциями ввода-вывода в Windows.</span><span class="sxs-lookup"><span data-stu-id="866ed-123">Differences between local I/O and network I/O on Windows.</span></span><br/> |
| [<span data-ttu-id="866ed-124">Сетевые перенаправителя</span><span class="sxs-lookup"><span data-stu-id="866ed-124">Network Redirectors</span></span>](network-redirectors.md)<br/>                                   | <span data-ttu-id="866ed-125">Описание функциональных возможностей перенаправителя сети.</span><span class="sxs-lookup"><span data-stu-id="866ed-125">Describes the functionality of a network redirector.</span></span><br/>      |



 

 

 




