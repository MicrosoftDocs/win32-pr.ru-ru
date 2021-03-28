---
description: Можно запустить корневое представление точки соединения через файл ярлыка для этой точки соединения.
title: Открытие корневого представления точки соединения через файл ярлыка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb83a6628b0dcffdf7d3bad66a25fc671c1feea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264415"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a><span data-ttu-id="825a5-103">Открытие корневого представления точки соединения через файл ярлыка</span><span class="sxs-lookup"><span data-stu-id="825a5-103">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>

<span data-ttu-id="825a5-104">Можно запустить корневое представление точки соединения через [файл ярлыка](./links.md) для этой точки соединения.</span><span class="sxs-lookup"><span data-stu-id="825a5-104">You can launch a rooted view of a junction point through a [shortcut file](./links.md) to that junction point.</span></span>

## <a name="instructions"></a><span data-ttu-id="825a5-105">Инструкции</span><span class="sxs-lookup"><span data-stu-id="825a5-105">Instructions</span></span>


<span data-ttu-id="825a5-106">Задайте для целевой строки файла ярлыка Explorer.exe с флагом/root.</span><span class="sxs-lookup"><span data-stu-id="825a5-106">Set the shortcut file's Target line to Explorer.exe with a /root flag.</span></span> <span data-ttu-id="825a5-107">Точная форма команды зависит от расположения точки соединения:</span><span class="sxs-lookup"><span data-stu-id="825a5-107">The exact form of the command depends on the location of the junction point:</span></span>

-   <span data-ttu-id="825a5-108">Если точка соединения является вложенной папкой рабочего стола, используйте:</span><span class="sxs-lookup"><span data-stu-id="825a5-108">If the junction point is a subfolder of the Desktop, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   <span data-ttu-id="825a5-109">Если точка соединения является папкой файловой системы, используйте:</span><span class="sxs-lookup"><span data-stu-id="825a5-109">If the junction point is a file system folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   <span data-ttu-id="825a5-110">Если точка соединения является вложенной папкой системной виртуальной папки, используйте:</span><span class="sxs-lookup"><span data-stu-id="825a5-110">If the junction point is a subfolder of a system virtual folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    <span data-ttu-id="825a5-111">Системные виртуальные папки, которые могут содержать точки соединения, имеют следующие идентификаторы классов (CLSID):</span><span class="sxs-lookup"><span data-stu-id="825a5-111">The system virtual folders that can contain junction points have the following class identifiers (CLSIDs):</span></span>

    

    |                   |                                        |
    |-------------------|----------------------------------------|
    | <span data-ttu-id="825a5-112">Мой компьютер</span><span class="sxs-lookup"><span data-stu-id="825a5-112">My Computer</span></span>       | <span data-ttu-id="825a5-113">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="825a5-113">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span></span> |
    | <span data-ttu-id="825a5-114">Мое сетевое окружение</span><span class="sxs-lookup"><span data-stu-id="825a5-114">My Network Places</span></span> | <span data-ttu-id="825a5-115">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="825a5-115">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span></span> |
    | <span data-ttu-id="825a5-116">Панель управления</span><span class="sxs-lookup"><span data-stu-id="825a5-116">Control Panel</span></span>     | <span data-ttu-id="825a5-117">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="825a5-117">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span></span> |
    | <span data-ttu-id="825a5-118">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="825a5-118">Internet Explorer</span></span> | <span data-ttu-id="825a5-119">{871C5380-42A0-1069-A2EA-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="825a5-119">{871C5380-42A0-1069-A2EA-08002B30309D}</span></span> |

    

     

## <a name="related-topics"></a><span data-ttu-id="825a5-120">См. также</span><span class="sxs-lookup"><span data-stu-id="825a5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="825a5-121">Указание расположения расширения пространства имен</span><span class="sxs-lookup"><span data-stu-id="825a5-121">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="825a5-122">Открытие корневого представления точки соединения в реестре</span><span class="sxs-lookup"><span data-stu-id="825a5-122">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
