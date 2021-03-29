---
title: Примеры и средства BITS
description: Примеры и средства BITS
ms.assetid: e449da0d-46da-44f9-85f3-4f0e17887bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b651ec8d4a2c3b61381dda488293ff6a3b9f2c90
ms.sourcegitcommit: dc13cc13522097188392392d85f99de48a213984
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "105654271"
---
# <a name="bits-samples-and-tools"></a><span data-ttu-id="5cab0-103">Примеры и средства BITS</span><span class="sxs-lookup"><span data-stu-id="5cab0-103">BITS Samples and Tools</span></span>

<span data-ttu-id="5cab0-104">В следующем разделе приведены пошаговые примеры C++ для фоновая интеллектуальная служба передачи (BITS).</span><span class="sxs-lookup"><span data-stu-id="5cab0-104">The following section contains step-by-step C++ examples for Background Intelligent Transfer Service (BITS).</span></span>



| <span data-ttu-id="5cab0-105">Section</span><span class="sxs-lookup"><span data-stu-id="5cab0-105">Section</span></span>                                                            | <span data-ttu-id="5cab0-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="5cab0-106">Purpose</span></span>                                                                                      |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5cab0-107">Примеры приложений на C++ BITS</span><span class="sxs-lookup"><span data-stu-id="5cab0-107">BITS C++ Application Examples</span></span>](bits-c---application-examples.md) | <span data-ttu-id="5cab0-108">Примеры C++, демонстрирующие ряд задач, которые можно выполнить с помощью функций службы BITS.</span><span class="sxs-lookup"><span data-stu-id="5cab0-108">C++ examples that demonstrate a range of tasks that can be completed by using BITS features.</span></span> |



 

<span data-ttu-id="5cab0-109">Кроме того, службы BITS включают в Windows SDK следующие примеры.</span><span class="sxs-lookup"><span data-stu-id="5cab0-109">In addition, BITS includes the following samples in Windows SDK.</span></span> <span data-ttu-id="5cab0-110">Примеры находятся в разделе *InstallDirectory* \\ Samples \\ Web.</span><span class="sxs-lookup"><span data-stu-id="5cab0-110">The samples are located under *InstallDirectory*\\Samples\\Web.</span></span> <span data-ttu-id="5cab0-111">Каждый пример включает файл Readme.txt, в котором объясняется, как установить и запустить пример.</span><span class="sxs-lookup"><span data-stu-id="5cab0-111">Each sample includes a Readme.txt file that explains how to install and run the sample.</span></span> <span data-ttu-id="5cab0-112">Можно загрузить Windows SDK из пакета средств [разработки программного обеспечения Microsoft Windows](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5cab0-112">You can download the Windows SDK from [Microsoft Windows Software Development Kit](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="5cab0-113">Службы BITS входят в состав пакета SDK для Core.</span><span class="sxs-lookup"><span data-stu-id="5cab0-113">BITS is included in the Core SDK.</span></span>

> [!Note]  
> <span data-ttu-id="5cab0-114">Windows Vista. примеры на этой странице включены в [Microsoft Windows SDK для Windows Vista](https://www.microsoft.com/download/details.aspx?id=30998).</span><span class="sxs-lookup"><span data-stu-id="5cab0-114">Windows Vista: The samples on this page are included in the [Microsoft Windows SDK for Windows Vista](https://www.microsoft.com/download/details.aspx?id=30998).</span></span> <span data-ttu-id="5cab0-115">Однако образец Клиентцерт не включается.</span><span class="sxs-lookup"><span data-stu-id="5cab0-115">However, the ClientCert sample is not included.</span></span>

 



| <span data-ttu-id="5cab0-116">Образец</span><span class="sxs-lookup"><span data-stu-id="5cab0-116">Sample</span></span>       | <span data-ttu-id="5cab0-117">Назначение</span><span class="sxs-lookup"><span data-stu-id="5cab0-117">Purpose</span></span>                                                                                                                                                                                                                                  |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cab0-118">\_Internet Explorer BITS</span><span class="sxs-lookup"><span data-stu-id="5cab0-118">BITS\_IE</span></span>     | <span data-ttu-id="5cab0-119">Показывает, как использовать [интерфейсы](bits-interfaces.md) BITS для загрузки файлов с сервера.</span><span class="sxs-lookup"><span data-stu-id="5cab0-119">Shows how to use the BITS [interfaces](bits-interfaces.md) to download files from a server.</span></span>                                                                                                                                             |
| <span data-ttu-id="5cab0-120">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="5cab0-120">Controls</span></span>     | <span data-ttu-id="5cab0-121">Показывает, как использовать [интерфейсы](bits-interfaces.md) BITS для управления и настройки параметров BITS, в том числе с помощью некоторых методов администрирования однорангового кэша.</span><span class="sxs-lookup"><span data-stu-id="5cab0-121">Shows how to use the BITS [interfaces](bits-interfaces.md) to control and configure BITS options, including using some of the peer cache administration methods.</span></span><br/> <span data-ttu-id="5cab0-122">**BITS 4,0:** Пример элементов управления является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="5cab0-122">**BITS 4.0:** The Controls sample is deprecated.</span></span><br/> |
| <span data-ttu-id="5cab0-123">Скачиваемые файлы</span><span class="sxs-lookup"><span data-stu-id="5cab0-123">Downloads</span></span>    | <span data-ttu-id="5cab0-124">Показывает, как использовать [интерфейсы](bits-interfaces.md) BITS для загрузки файлов с сервера.</span><span class="sxs-lookup"><span data-stu-id="5cab0-124">Shows how to use the BITS [interfaces](bits-interfaces.md) to download files from a server.</span></span>                                                                                                                                             |
| <span data-ttu-id="5cab0-125">хттфеадерс</span><span class="sxs-lookup"><span data-stu-id="5cab0-125">HTTPHeaders</span></span>  | <span data-ttu-id="5cab0-126">Показывает, как использовать [интерфейсы](bits-interfaces.md) BITS для изменения заголовков HTTP.</span><span class="sxs-lookup"><span data-stu-id="5cab0-126">Shows how to use the BITS [interfaces](bits-interfaces.md) to modify HTTP headers.</span></span>                                                                                                                                                      |
| <span data-ttu-id="5cab0-127">BITS</span><span class="sxs-lookup"><span data-stu-id="5cab0-127">PeerCaching</span></span>  | <span data-ttu-id="5cab0-128">Показывает, как использовать [интерфейсы](bits-interfaces.md) BITS, чтобы разрешить скачивание задания с однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="5cab0-128">Shows how to use the BITS [interfaces](bits-interfaces.md) to enable a job to download from a peer.</span></span><br/> <span data-ttu-id="5cab0-129">**BITS 4,0:** Пример с кэшированием одноранговых членов не рекомендуется использовать.</span><span class="sxs-lookup"><span data-stu-id="5cab0-129">**BITS 4.0:** The PeerCaching sample is deprecated.</span></span><br/>                                                           |
| <span data-ttu-id="5cab0-130">Отправляет</span><span class="sxs-lookup"><span data-stu-id="5cab0-130">Uploads</span></span>      | <span data-ttu-id="5cab0-131">Показывает, как использовать [интерфейсы](bits-interfaces.md) BITS для передачи файла.</span><span class="sxs-lookup"><span data-stu-id="5cab0-131">Shows how to use the BITS [interfaces](bits-interfaces.md) to upload a file.</span></span>                                                                                                                                                            |
| <span data-ttu-id="5cab0-132">уплоадсампле</span><span class="sxs-lookup"><span data-stu-id="5cab0-132">UploadSample</span></span> | <span data-ttu-id="5cab0-133">Показывает, как использовать [интерфейсы](bits-interfaces.md) BITS для передачи файла на сервер и получения ответа.</span><span class="sxs-lookup"><span data-stu-id="5cab0-133">Shows how to use the BITS [interfaces](bits-interfaces.md) to upload a file to a server and receive a reply.</span></span>                                                                                                                            |



 

<span data-ttu-id="5cab0-134">Служба BITS предоставляет следующее средство.</span><span class="sxs-lookup"><span data-stu-id="5cab0-134">BITS provides the following tool.</span></span>



| <span data-ttu-id="5cab0-135">Инструмент</span><span class="sxs-lookup"><span data-stu-id="5cab0-135">Tool</span></span>                            | <span data-ttu-id="5cab0-136">Назначение</span><span class="sxs-lookup"><span data-stu-id="5cab0-136">Purpose</span></span>                                                                         |
|---------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="5cab0-137">битсадмин</span><span class="sxs-lookup"><span data-stu-id="5cab0-137">BITSAdmin</span></span>](bitsadmin-tool.md) | <span data-ttu-id="5cab0-138">Программа командной строки для создания заданий скачивания или отправки и отслеживания хода их выполнения.</span><span class="sxs-lookup"><span data-stu-id="5cab0-138">Command-line tool to create download or upload jobs and monitor their progress.</span></span> |



 

## <a name="additional-information"></a><span data-ttu-id="5cab0-139">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="5cab0-139">Additional Information</span></span>

<span data-ttu-id="5cab0-140">Если требуются дополнительные сведения, можно задать вопрос в группе новостей BITS Microsoft. Windows. public. баккграундтрансфер.</span><span class="sxs-lookup"><span data-stu-id="5cab0-140">If you need additional information, consider asking questions in the BITS newsgroup microsoft.windows.public.backgroundtransfer.</span></span>

<span data-ttu-id="5cab0-141">Сервер группы новостей — msnews.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="5cab0-141">The newsgroup server is msnews.microsoft.com.</span></span>

 

 





