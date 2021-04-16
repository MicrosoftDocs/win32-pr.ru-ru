---
description: Тип данных Анипас — это текстовая строка, содержащая либо полный путь, либо относительный путь.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: анипас
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ab6265874616bb0bb1a2f61098cdbabfa8ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650731"
---
# <a name="anypath"></a><span data-ttu-id="5830d-103">анипас</span><span class="sxs-lookup"><span data-stu-id="5830d-103">AnyPath</span></span>

<span data-ttu-id="5830d-104">Тип данных Анипас — это текстовая строка, содержащая либо полный путь, либо относительный путь.</span><span class="sxs-lookup"><span data-stu-id="5830d-104">The AnyPath data type is a text string containing either a full path or a relative path.</span></span> <span data-ttu-id="5830d-105">При указании относительного пути можно добавить длинное имя файла с коротким именем файла, разделив короткие и длинные имена с помощью вертикальной черты ( \| ).</span><span class="sxs-lookup"><span data-stu-id="5830d-105">When specifying a relative path, you can include a long file name with the short file name by separating the short and long names with a vertical bar (\|).</span></span> <span data-ttu-id="5830d-106">Обратите внимание, что таким образом нельзя указать несколько уровней каталога или полных путей.</span><span class="sxs-lookup"><span data-stu-id="5830d-106">Note that you cannot specify multiple levels of a directory or fully qualified paths in this way.</span></span> <span data-ttu-id="5830d-107">Путь может содержать свойства, заключенные в квадратные скобки ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="5830d-107">The path may contain properties enclosed within square brackets (\[ \]).</span></span>

<span data-ttu-id="5830d-108">Примеры допустимых данных Анипас:</span><span class="sxs-lookup"><span data-stu-id="5830d-108">Examples of valid AnyPath data:</span></span>

-   <span data-ttu-id="5830d-109">\\\\\\Общая папка сервера \\ TEMP</span><span class="sxs-lookup"><span data-stu-id="5830d-109">\\\\server\\share\\temp</span></span>
-   <span data-ttu-id="5830d-110">c: \\ TEMP</span><span class="sxs-lookup"><span data-stu-id="5830d-110">c:\\temp</span></span>
-   <span data-ttu-id="5830d-111">\\Каталог</span><span class="sxs-lookup"><span data-stu-id="5830d-111">\\temp</span></span>
-   <span data-ttu-id="5830d-112">пакета ISPAC ~ 1 \| состояние проекта</span><span class="sxs-lookup"><span data-stu-id="5830d-112">projec~1\|Project Status</span></span>

<span data-ttu-id="5830d-113">Примеры недопустимых данных Анипас:</span><span class="sxs-lookup"><span data-stu-id="5830d-113">Examples of invalid AnyPath data:</span></span>

-   <span data-ttu-id="5830d-114">c: \\ temp \\ пакета ISPAC ~ 1 \| c: \\ состояние temp одного \\ проекта</span><span class="sxs-lookup"><span data-stu-id="5830d-114">c:\\temp\\projec~1\|c:\\temp one\\Project Status</span></span>
-   <span data-ttu-id="5830d-115">\\Временная \\ пакета ISPAC ~ 1 \| \\ временное \\ состояние одного проекта</span><span class="sxs-lookup"><span data-stu-id="5830d-115">\\temp\\projec~1\|\\temp one\\Project Status</span></span>

 

 



