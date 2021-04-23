---
description: После создания INF-файла обычно создается исходный код для приложения установки. Вы вызываете функции установки из приложения установки для выполнения множества операций установки.
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: Создание приложений установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3aaca2b1d509795f625e67c18c13131d7e502b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663790"
---
# <a name="creating-setup-applications"></a><span data-ttu-id="f8141-104">Создание приложений установки</span><span class="sxs-lookup"><span data-stu-id="f8141-104">Creating Setup Applications</span></span>

<span data-ttu-id="f8141-105">После создания INF-файла обычно создается исходный код для приложения установки.</span><span class="sxs-lookup"><span data-stu-id="f8141-105">After you create an INF file, you will typically write the source code for your setup application.</span></span> <span data-ttu-id="f8141-106">Вы вызываете функции установки из приложения установки для выполнения множества операций установки.</span><span class="sxs-lookup"><span data-stu-id="f8141-106">You call the setup functions from your setup application to perform many installation operations.</span></span>

<span data-ttu-id="f8141-107">Следующие шаги охватывают один из способов использования функций установки для создания приложения установки.</span><span class="sxs-lookup"><span data-stu-id="f8141-107">The following steps cover one way to use the setup functions to create a setup application.</span></span> <span data-ttu-id="f8141-108">Этот пример можно использовать в качестве отправной точки или разработать собственный алгоритм установки.</span><span class="sxs-lookup"><span data-stu-id="f8141-108">You can use this example as a starting point, or develop your own installation algorithm.</span></span>

<span data-ttu-id="f8141-109">**Инициализация**</span><span class="sxs-lookup"><span data-stu-id="f8141-109">**Initialization**</span></span>

-   [<span data-ttu-id="f8141-110">Откройте INF-файл и при необходимости добавьте другие INF-файлы.</span><span class="sxs-lookup"><span data-stu-id="f8141-110">Open the INF and, if appropriate, append other INF files.</span></span>](opening-the-inf-file.md)
-   [<span data-ttu-id="f8141-111">Извлеките сведения о файле из INF-файла.</span><span class="sxs-lookup"><span data-stu-id="f8141-111">Extract file information from the INF file.</span></span>](extracting-file-information-from-the-inf-file.md)
-   [<span data-ttu-id="f8141-112">Сбор сведений о настройке пользователя.</span><span class="sxs-lookup"><span data-stu-id="f8141-112">Gather setup information from the user.</span></span>](gathering-setup-information-from-the-user.md)
-   [<span data-ttu-id="f8141-113">Создайте очередь.</span><span class="sxs-lookup"><span data-stu-id="f8141-113">Create a queue.</span></span>](creating-a-queue-and-queuing-file-operations.md)

<span data-ttu-id="f8141-114">**Установка файлов**</span><span class="sxs-lookup"><span data-stu-id="f8141-114">**Install files**</span></span>

-   [<span data-ttu-id="f8141-115">Зафиксируйте очередь, указав подпрограммы обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f8141-115">Commit the queue, specifying a callback routine.</span></span>](committing-the-queue.md)
-   [<span data-ttu-id="f8141-116">Обновление сведений реестра.</span><span class="sxs-lookup"><span data-stu-id="f8141-116">Update registry information.</span></span>](updating-registry-information.md)

<span data-ttu-id="f8141-117">**Очистка**</span><span class="sxs-lookup"><span data-stu-id="f8141-117">**Clean up**</span></span>

-   [<span data-ttu-id="f8141-118">Закройте очередь файлов и INF-файл.</span><span class="sxs-lookup"><span data-stu-id="f8141-118">Close the file queue and INF.</span></span>](closing-the-file-queue-and-inf-file.md)
-   [<span data-ttu-id="f8141-119">Освободите другие системные ресурсы и завершите программу.</span><span class="sxs-lookup"><span data-stu-id="f8141-119">Release any other system resources and end the program.</span></span>](releasing-other-system-resources.md)

 

 



