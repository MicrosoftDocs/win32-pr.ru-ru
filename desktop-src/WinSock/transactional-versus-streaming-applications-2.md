---
description: 'Существует два фундаментальных типа сетевых приложений: транзакционная и потоковая передача. Эти типы приложений также называются интерактивными и пакетной обработкой типов приложений соответственно.'
ms.assetid: 85795cdd-5a4f-4199-98bd-b5ce2299338b
title: Транзакционные и потоковые приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a000f3aa9c52fe6ce60622a613d6f4b9689b8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701497"
---
# <a name="transactional-versus-streaming-applications"></a><span data-ttu-id="68c2a-104">Транзакционные и потоковые приложения</span><span class="sxs-lookup"><span data-stu-id="68c2a-104">Transactional versus Streaming Applications</span></span>

<span data-ttu-id="68c2a-105">Существует два фундаментальных типа сетевых приложений: *транзакционная* и *потоковая передача*.</span><span class="sxs-lookup"><span data-stu-id="68c2a-105">There are two fundamental types of network applications: *transactional* and *streaming*.</span></span> <span data-ttu-id="68c2a-106">Эти типы приложений также называются *интерактивными* и *пакетной обработкой* типов приложений соответственно.</span><span class="sxs-lookup"><span data-stu-id="68c2a-106">These application types are also called *interactive* and *batch processing* application types, respectively.</span></span>

<span data-ttu-id="68c2a-107">Транзакционные приложения — это приложения с остановкой и Go.</span><span class="sxs-lookup"><span data-stu-id="68c2a-107">Transactional applications are stop-and-go applications.</span></span> <span data-ttu-id="68c2a-108">Обычно они выполняют операции "запрос-ответ", которые часто упорядочиваются.</span><span class="sxs-lookup"><span data-stu-id="68c2a-108">They usually perform request/reply operations, often ordered.</span></span> <span data-ttu-id="68c2a-109">Примеры транзакционных приложений включают синхронный удаленный вызов процедур (RPC), а также некоторые реализации HTTP и системы доменных имен (DNS).</span><span class="sxs-lookup"><span data-stu-id="68c2a-109">Examples of transactional applications include synchronous remote procedure call (RPC), as well as some HTTP and Domain Name System (DNS) implementations.</span></span>

<span data-ttu-id="68c2a-110">Потоковые приложения перемещают данные.</span><span class="sxs-lookup"><span data-stu-id="68c2a-110">Streaming applications move data.</span></span> <span data-ttu-id="68c2a-111">Чтобы описать приложения потоковой передачи с параллельным выражением, потоковые приложения придерживаются к философским принципам передачи данных, обычно с минимальными требованиями к упорядочению данных.</span><span class="sxs-lookup"><span data-stu-id="68c2a-111">To describe streaming applications with a parallel term, streaming applications adhere to a pedal-to-the-metal data transmission philosophy, usually with little concern for data ordering.</span></span> <span data-ttu-id="68c2a-112">Примеры приложений потоковой передачи включают в себя сетевую архивацию и протокол передачи файлов (FTP).</span><span class="sxs-lookup"><span data-stu-id="68c2a-112">Examples of streaming applications include network backup and file transfer protocol (FTP).</span></span>

<span data-ttu-id="68c2a-113">После определения типа приложения также определяются его характеристики сети и протокола.</span><span class="sxs-lookup"><span data-stu-id="68c2a-113">Once the application type is determined, its network and protocol characteristics are determined as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68c2a-114">См. также</span><span class="sxs-lookup"><span data-stu-id="68c2a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68c2a-115">Высокопроизводительные приложения Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="68c2a-115">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="68c2a-116">Измерения производительности</span><span class="sxs-lookup"><span data-stu-id="68c2a-116">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



