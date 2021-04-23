---
title: Устойчивая файловая система
description: Устойчивая файловая система
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba011dcdd3cd39280e0a79d0b325f9e75d6b64
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "104070799"
---
# <a name="resilient-file-system"></a><span data-ttu-id="a09da-103">Устойчивая файловая система</span><span class="sxs-lookup"><span data-stu-id="a09da-103">Resilient file system</span></span>

## <a name="platform"></a><span data-ttu-id="a09da-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="a09da-104">Platform</span></span>

<span data-ttu-id="a09da-105">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a09da-105">**Servers** – Windows Server 2012</span></span> 

## <a name="description"></a><span data-ttu-id="a09da-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a09da-106">Description</span></span>

<span data-ttu-id="a09da-107">Отказоустойчивая файловая система (ReFS) — это новая локальная файловая система.</span><span class="sxs-lookup"><span data-stu-id="a09da-107">Resilient File System (ReFS) is a new local file system.</span></span> <span data-ttu-id="a09da-108">Это позволяет максимально повысить доступность данных, несмотря на ошибки, которые могут привести к потере данных или простою.</span><span class="sxs-lookup"><span data-stu-id="a09da-108">It maximizes data availability, despite errors that would historically cause data loss or downtime.</span></span> <span data-ttu-id="a09da-109">Целостность данных гарантирует, что критически важные для бизнеса данные защищаются от ошибок и доступны при необходимости.</span><span class="sxs-lookup"><span data-stu-id="a09da-109">Data integrity ensures that business critical data is protected from errors and available when needed.</span></span> <span data-ttu-id="a09da-110">Его архитектура разработана для обеспечения масштабируемости и производительности в эпоху постоянно увеличивающихся размеров наборов данных и динамических рабочих нагрузок.</span><span class="sxs-lookup"><span data-stu-id="a09da-110">Its architecture is designed to provide scalability and performance in an era of constantly growing data set sizes and dynamic workloads.</span></span>

<span data-ttu-id="a09da-111">Основные функции ReFS:</span><span class="sxs-lookup"><span data-stu-id="a09da-111">The key features of ReFS are:</span></span>

-   <span data-ttu-id="a09da-112">**Целостность**: ReFS хранит данные, чтобы защитить их от многих распространенных ошибок, которые могут привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="a09da-112">**Integrity**: ReFS stores data so that it is protected from many of the common errors that can cause data loss.</span></span> <span data-ttu-id="a09da-113">Метаданные файловой системы всегда защищены.</span><span class="sxs-lookup"><span data-stu-id="a09da-113">File system metadata is always protected.</span></span> <span data-ttu-id="a09da-114">При необходимости данные пользователя могут быть защищены отдельно для каждого тома, каталога или каждого файла.</span><span class="sxs-lookup"><span data-stu-id="a09da-114">Optionally, user data can be protected on a per-volume, per-directory, or per-file basis.</span></span> <span data-ttu-id="a09da-115">Если происходит повреждение, ReFS может обнаруживать и при настройке с помощью дисковых пространств автоматически исправлять повреждение.</span><span class="sxs-lookup"><span data-stu-id="a09da-115">If corruption occurs, ReFS can detect and, when configured with Storage Spaces, automatically correct the corruption.</span></span> <span data-ttu-id="a09da-116">В случае системной ошибки ссылки на ReFS предназначены для быстрого восстановления после этой ошибки без потери пользовательских данных.</span><span class="sxs-lookup"><span data-stu-id="a09da-116">In the event of a system error, ReFS is designed to recover from that error rapidly, with no loss of user data.</span></span>
-   <span data-ttu-id="a09da-117">**Доступность**. ReFS предназначена для определения приоритета доступности данных.</span><span class="sxs-lookup"><span data-stu-id="a09da-117">**Availability**: ReFS is designed to prioritize the availability of data.</span></span> <span data-ttu-id="a09da-118">Если в ReFS возникает повреждение и его не удается исправить автоматически, оперативный процесс восстановления локализуется в области повреждения, что не требует какого-либо времени.</span><span class="sxs-lookup"><span data-stu-id="a09da-118">With ReFS, if corruption occurs, and it cannot be repaired automatically, the online salvage process is localized to the area of corruption, requiring no volume down-time.</span></span> <span data-ttu-id="a09da-119">Вкратце, если происходит повреждение, ReFS будет оставаться в сети.</span><span class="sxs-lookup"><span data-stu-id="a09da-119">In short, if corruption occurs, ReFS will stay online.</span></span>
-   <span data-ttu-id="a09da-120">**Масштабируемость**. ReFS разработана для наборов данных на сегодняшний день и размеров набора данных завтра; Она оптимизирована для обеспечения высокой масштабируемости.</span><span class="sxs-lookup"><span data-stu-id="a09da-120">**Scalability**: ReFS is designed for the data set sizes of today and the data set sizes of tomorrow; it’s optimized for high scalability.</span></span>
-   <span data-ttu-id="a09da-121">**Совместимость приложений**. чтобы развернуть AppCompat, ReFS поддерживает набор функций NTFS и интерфейсов API Win32, которые широко приняты.</span><span class="sxs-lookup"><span data-stu-id="a09da-121">**App Compatibility**: To maximize AppCompat, ReFS supports a subset of NTFS features plus Win32 APIs that are widely adopted.</span></span>
-   <span data-ttu-id="a09da-122">**Упреждающий код ошибки**. возможности целостности ReFS используются средством проверки целостности данных ("средство очистки"), которое периодически проверяет том, пытается определить скрытые повреждения, а затем заблаговременно запускает восстановление поврежденных данных.</span><span class="sxs-lookup"><span data-stu-id="a09da-122">**Proactive Error Identification**: The integrity capabilities of ReFS are leveraged by a data integrity scanner (a “scrubber”) that periodically scans the volume, attempts to identify latent corruption, and then proactively triggers a repair of that corrupt data.</span></span>

## <a name="resources"></a><span data-ttu-id="a09da-123">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="a09da-123">Resources</span></span>

-   [<span data-ttu-id="a09da-124">Создание записи в блоге по Windows 8 — Создание файловой системы следующего поколения для Windows: ReFS</span><span class="sxs-lookup"><span data-stu-id="a09da-124">Building Windows 8 Blog Post – Building the next generation file system for Windows: ReFS</span></span>](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [<span data-ttu-id="a09da-125">Совместимость приложений и ReFS</span><span class="sxs-lookup"><span data-stu-id="a09da-125">Application Compatibility and ReFS</span></span>](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 