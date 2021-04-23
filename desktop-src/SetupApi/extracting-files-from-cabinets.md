---
description: Извлечь файлы из CAB-файла можно двумя способами. Первый и самый простой способ — воспользоваться преимуществами автоматической обработки CAB-файлов, встроенными в функции установки.
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: Извлечение файлов из ящиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94f413b4ad0ee1511dde21af747cd2665a4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662552"
---
# <a name="extracting-files-from-cabinets"></a><span data-ttu-id="a7881-104">Извлечение файлов из ящиков</span><span class="sxs-lookup"><span data-stu-id="a7881-104">Extracting Files from Cabinets</span></span>

<span data-ttu-id="a7881-105">Извлечь файлы из CAB-файла можно двумя способами.</span><span class="sxs-lookup"><span data-stu-id="a7881-105">You can extract files from a cabinet in two ways.</span></span> <span data-ttu-id="a7881-106">Первый и самый простой способ — воспользоваться преимуществами автоматической обработки CAB-файлов, встроенными в функции установки.</span><span class="sxs-lookup"><span data-stu-id="a7881-106">The first and simplest way is to take advantage of the automatic cabinet processing built into the setup functions.</span></span>

<span data-ttu-id="a7881-107">Функции установки, такие как [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**сетупинсталлфиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)и [**сетупинсталлфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), проверяют сжатие каждого файла.</span><span class="sxs-lookup"><span data-stu-id="a7881-107">The installation functions, such as [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), and [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), check the compression on each file.</span></span> <span data-ttu-id="a7881-108">Если файл находится в CAB-файле, функции сначала выполняют поиск файла с этим именем за пределами CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="a7881-108">If the file is in a cabinet, the functions first search for a file of that name outside the cabinet.</span></span> <span data-ttu-id="a7881-109">При обнаружении функции устанавливают внешний файл, игнорируя файл внутри CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="a7881-109">If found, the functions install the external file, ignoring the file inside the cabinet.</span></span> <span data-ttu-id="a7881-110">Это позволяет обновить отдельный файл в CAB-файле без перестроения CAB.</span><span class="sxs-lookup"><span data-stu-id="a7881-110">This enables you to update a single file inside the cabinet without rebuilding the cabinet.</span></span>

<span data-ttu-id="a7881-111">Функция установки также следит за тем, какие файлы в CAB-файле были извлечены, чтобы файл был извлечен только один раз, даже если он был установлен несколько раз.</span><span class="sxs-lookup"><span data-stu-id="a7881-111">The setup functions also track which files in a cabinet have been retrieved, so that a file is extracted only once, even if it is installed several times.</span></span>

<span data-ttu-id="a7881-112">Второй способ извлечения файлов из CAB-файла — с помощью [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="a7881-112">The second way to extract files from a cabinet is by using [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="a7881-113">Эта функция выполняет итерацию каждого файла в CAB-файле, отправляя уведомление в подпрограммы обратного вызова для каждого найденного файла.</span><span class="sxs-lookup"><span data-stu-id="a7881-113">This function iterates through each file in a cabinet, sending a notification to a callback routine for each file found.</span></span> <span data-ttu-id="a7881-114">Затем подпрограммы обратного вызова возвращают значение, указывающее, должен ли файл быть извлечен или пропущен.</span><span class="sxs-lookup"><span data-stu-id="a7881-114">The callback routine then returns a value that indicates whether the file should be extracted or skipped.</span></span>

> [!Note]  
> <span data-ttu-id="a7881-115">API установки не предоставляет подпрограмму обратного вызова по умолчанию для управления уведомлениями CAB.</span><span class="sxs-lookup"><span data-stu-id="a7881-115">The Setup API does not supply a default callback routine to handle cabinet notifications.</span></span> <span data-ttu-id="a7881-116">При явном вызове [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) необходимо предоставить подпрограммы обратного вызова для обработки уведомлений о CAB-файле, возвращаемых функцией.</span><span class="sxs-lookup"><span data-stu-id="a7881-116">If you call [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) explicitly, you must supply a callback routine to process the cabinet notifications that the function returns.</span></span>

 

 

 



