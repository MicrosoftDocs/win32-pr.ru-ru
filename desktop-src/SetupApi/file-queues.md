---
description: Функции установки включают в себя функции очереди файлов.
ms.assetid: 628850ab-eb66-4b60-9298-1a44a7f6a390
title: Очереди файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7177e0bb267167ce5b37cf5213ea942c972ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998871"
---
# <a name="file-queues"></a><span data-ttu-id="97ae4-103">Очереди файлов</span><span class="sxs-lookup"><span data-stu-id="97ae4-103">File Queues</span></span>

<span data-ttu-id="97ae4-104">Функции установки включают в себя функции очереди файлов.</span><span class="sxs-lookup"><span data-stu-id="97ae4-104">The setup functions include file queue functionality.</span></span> <span data-ttu-id="97ae4-105">Очередь файлов — это список операций копирования, переименования и удаления файлов.</span><span class="sxs-lookup"><span data-stu-id="97ae4-105">A file queue is a list of file copying, renaming, and deletion operations.</span></span> <span data-ttu-id="97ae4-106">Эти операции могут быть отправлены в очередь в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="97ae4-106">These operations can be sent to the queue in any order.</span></span> <span data-ttu-id="97ae4-107">При фиксации очереди эти операции обрабатываются в виде пакета в порядке, определенном типом операции.</span><span class="sxs-lookup"><span data-stu-id="97ae4-107">When the queue is committed, these operations are processed as a batch, in order of the operation type.</span></span>

<span data-ttu-id="97ae4-108">В следующих разделах объясняется, что такое очередь и как ее использовать при создании приложения установки.</span><span class="sxs-lookup"><span data-stu-id="97ae4-108">The following sections explain what a queue is and how to use it when creating a setup application.</span></span> <span data-ttu-id="97ae4-109">Также рассматривается порядок обработки файловых операций в очереди в качестве фиксаций и то, какие уведомления очередь отправляет в подпрограммы обратного вызова на каждом этапе.</span><span class="sxs-lookup"><span data-stu-id="97ae4-109">Also discussed is the order in which the enqueued file operations are processed as the queue commits and what notifications the queue sends to a callback routine at each stage.</span></span>

-   [<span data-ttu-id="97ae4-110">О файловых очередях</span><span class="sxs-lookup"><span data-stu-id="97ae4-110">About File Queues</span></span>](about-file-queues.md)
-   [<span data-ttu-id="97ae4-111">Использование очередей файлов</span><span class="sxs-lookup"><span data-stu-id="97ae4-111">Using File Queues</span></span>](using-file-queues.md)
-   [<span data-ttu-id="97ae4-112">Справочник по очереди файлов</span><span class="sxs-lookup"><span data-stu-id="97ae4-112">File Queue Reference</span></span>](file-queue-reference.md)

 

 



