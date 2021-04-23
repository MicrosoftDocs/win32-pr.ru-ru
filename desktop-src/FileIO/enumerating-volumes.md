---
description: Чтобы создать полный список томов на компьютере или управлять каждым томом, можно перечислить тома.
ms.assetid: 5adcd59a-48b7-4373-a10b-c352962f715a
title: Перечисление томов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc294d72fa3fad24536b175ee7e5e023066586c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683700"
---
# <a name="enumerating-volumes"></a><span data-ttu-id="0213d-103">Перечисление томов</span><span class="sxs-lookup"><span data-stu-id="0213d-103">Enumerating Volumes</span></span>

<span data-ttu-id="0213d-104">Чтобы создать полный список томов на компьютере или управлять каждым томом, можно перечислить тома.</span><span class="sxs-lookup"><span data-stu-id="0213d-104">To make a complete list of the volumes on a computer, or to manipulate each volume in turn, you can enumerate volumes.</span></span> <span data-ttu-id="0213d-105">В томе можно [проверить наличие подключенных папок](enumerating-volume-mount-points.md) или других объектов в томе.</span><span class="sxs-lookup"><span data-stu-id="0213d-105">Within a volume, you can [scan for mounted folders](enumerating-volume-mount-points.md) or other objects on the volume.</span></span>

<span data-ttu-id="0213d-106">Три функции позволяют приложению перечислять тома на компьютере:</span><span class="sxs-lookup"><span data-stu-id="0213d-106">Three functions allow an application to enumerate volumes on a computer:</span></span>

-   [<span data-ttu-id="0213d-107">**финдфирстволуме**</span><span class="sxs-lookup"><span data-stu-id="0213d-107">**FindFirstVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [<span data-ttu-id="0213d-108">**финднекстволуме**</span><span class="sxs-lookup"><span data-stu-id="0213d-108">**FindNextVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [<span data-ttu-id="0213d-109">**финдволумеклосе**</span><span class="sxs-lookup"><span data-stu-id="0213d-109">**FindVolumeClose**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)

<span data-ttu-id="0213d-110">Эти три функции работают так же, как функции [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)и [**финдклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="0213d-110">These three functions operate in a manner very similar to the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span>

<span data-ttu-id="0213d-111">Начните поиск томов с помощью [**финдфирстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span><span class="sxs-lookup"><span data-stu-id="0213d-111">Begin a search for volumes with [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span></span> <span data-ttu-id="0213d-112">Если поиск прошел успешно, обработайте результаты в соответствии со структурой приложения.</span><span class="sxs-lookup"><span data-stu-id="0213d-112">If the search is successful, process the results according to the design of your application.</span></span> <span data-ttu-id="0213d-113">Затем используйте [**финднекстволуме**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) в цикле для нахождения и обработки каждого последующего тома.</span><span class="sxs-lookup"><span data-stu-id="0213d-113">Then use [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) in a loop to locate and process each subsequent volume.</span></span> <span data-ttu-id="0213d-114">Когда предоставление томов будет исчерпано, закройте Поиск с помощью [**финдволумеклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).</span><span class="sxs-lookup"><span data-stu-id="0213d-114">When the supply of volumes is exhausted, close the search with [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).</span></span>

<span data-ttu-id="0213d-115">Не следует рассчитывать на корреляцию между порядком томов, возвращаемых этими функциями, и порядком томов, возвращаемых другими функциями или инструментами.</span><span class="sxs-lookup"><span data-stu-id="0213d-115">You should not assume any correlation between the order of the volumes that are returned by these functions and the order of the volumes that are returned by other functions or tools.</span></span> <span data-ttu-id="0213d-116">В частности, не следует рассчитывать на корреляцию между порядком использования томов и буквами дисков, назначенными BIOS (при наличии) или администратором дисков.</span><span class="sxs-lookup"><span data-stu-id="0213d-116">In particular, do not assume any correlation between volume order and drive letters as assigned by the BIOS (if any) or the Disk Administrator.</span></span>

<span data-ttu-id="0213d-117">Пример перечисления томов на компьютере см. в разделе [примеры подключенной папки](volume-mount-point-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="0213d-117">See [Mounted Folder Examples](volume-mount-point-examples.md) for an example of how to enumerate the volumes on a computer.</span></span>

 

 



