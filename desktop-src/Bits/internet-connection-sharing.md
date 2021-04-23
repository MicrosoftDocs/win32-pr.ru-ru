---
title: Общий доступ к подключению Интернета
description: Служба BITS может принудительно установить коммутируемое подключение для домашних сетей, использующих общий доступ к подключению к Интернету, если подключение к подключению настроено для удаленного доступа, когда компьютеры в сети обращаются к Интернету.
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f92538f0317ac1b198b69069c4041c562ce368c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773376"
---
# <a name="internet-connection-sharing"></a><span data-ttu-id="082e8-103">Общий доступ к подключению Интернета</span><span class="sxs-lookup"><span data-stu-id="082e8-103">Internet Connection Sharing</span></span>

<span data-ttu-id="082e8-104">Служба BITS может принудительно установить коммутируемое подключение для домашних сетей, использующих общий доступ к подключению к Интернету, если подключение к подключению настроено для удаленного доступа, когда компьютеры в сети обращаются к Интернету.</span><span class="sxs-lookup"><span data-stu-id="082e8-104">BITS can force a dial-up connection for home networks that use Microsoft Internet Connection Sharing if Connection Sharing is configured to dial out when computers on the network access the Internet.</span></span> <span data-ttu-id="082e8-105">Чтобы предотвратить принудительное коммутируемое подключение, отключите флажок **установить коммутируемое подключение, когда компьютер в сети пытается получить доступ к Интернету** на главном компьютере, который использует подключение к Интернету.</span><span class="sxs-lookup"><span data-stu-id="082e8-105">To prevent a forced dial-up connection, disable the **Establish a dial-up connection whenever a computer on my network attempts to access the Internet** option on the Connection Sharing host computer that shares its Internet connection.</span></span>

<span data-ttu-id="082e8-106">Компьютеры, подключенные к главному компьютеру общего доступа, предполагают, что они имеют сетевое подключение, поэтому служба BITS попытается передавать файлы.</span><span class="sxs-lookup"><span data-stu-id="082e8-106">Computers connected to the Connection Sharing host computer assume they have a network connection, so BITS will try to transfer files.</span></span> <span data-ttu-id="082e8-107">Если параметр коммутируемого подключения на главном компьютере отключен, а на главном компьютере нет активного подключения, то передача данных завершится с временной ошибкой.</span><span class="sxs-lookup"><span data-stu-id="082e8-107">If the dial-up option is disabled on the host computer and the host computer does not have an active connection, the transfers will fail with a transient error.</span></span> <span data-ttu-id="082e8-108">BITS будет периодически повторять передачу.</span><span class="sxs-lookup"><span data-stu-id="082e8-108">BITS will retry the transfers periodically.</span></span>

 

 




