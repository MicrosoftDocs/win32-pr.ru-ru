---
description: Функции установки обработают ящики внутренним образом. Чтобы явно перечислить и извлечь файлы из CAB-файла, можно вызвать функцию Сетупитератекабинет.
ms.assetid: 14bd925a-e7fe-48a3-9ed6-4e42ce796290
title: Использование CAB-файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03467f6591b4503cb13935cca550f8c1ba1dff81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664195"
---
# <a name="using-cabinet-files"></a><span data-ttu-id="d3328-104">Использование CAB-файлов</span><span class="sxs-lookup"><span data-stu-id="d3328-104">Using Cabinet Files</span></span>

<span data-ttu-id="d3328-105">Функции установки обработают ящики внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="d3328-105">The setup functions handle cabinets internally.</span></span> <span data-ttu-id="d3328-106">Чтобы явно перечислить и извлечь файлы из CAB-файла, можно вызвать функцию [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .</span><span class="sxs-lookup"><span data-stu-id="d3328-106">To explicitly enumerate and extract files from a cabinet, you can call the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function.</span></span>

<span data-ttu-id="d3328-107">В следующем разделе описывается внутренняя обработка CAB-файла для функций установки и использование [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="d3328-107">The following topic describes the cabinet processing internal to the setup functions and how to use [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="d3328-108">Также обсуждаются уведомления, отправленные **сетупитератекабинет** , и необходимый формат подпрограммы обратного вызова CAB-файла для обработки этих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d3328-108">Also discussed are the notifications sent by **SetupIterateCabinet** and the required format of a cabinet callback routine to process those notifications.</span></span>

-   [<span data-ttu-id="d3328-109">Извлечение файлов из ящиков</span><span class="sxs-lookup"><span data-stu-id="d3328-109">Extracting Files From Cabinets</span></span>](extracting-files-from-cabinets.md)
-   [<span data-ttu-id="d3328-110">Создание подпрограммы обратного вызова CAB-файла</span><span class="sxs-lookup"><span data-stu-id="d3328-110">Creating a Cabinet Callback Routine</span></span>](creating-a-cabinet-callback-routine.md)

 

 



