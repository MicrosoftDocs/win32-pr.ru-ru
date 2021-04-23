---
description: Как Microsoft DVD Navigator выбирает регион DVD
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Как Microsoft DVD Navigator выбирает регион DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a2898725ad187946b50e567f7daa7e72a9886
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672947"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a><span data-ttu-id="bb565-103">Как Microsoft DVD Navigator выбирает регион DVD</span><span class="sxs-lookup"><span data-stu-id="bb565-103">How Microsoft DVD Navigator Selects the DVD Region</span></span>

<span data-ttu-id="bb565-104">Microsoft DVD Navigator использует следующий алгоритм для определения соответствия региона при воспроизведении DVD-дисков на ПК:</span><span class="sxs-lookup"><span data-stu-id="bb565-104">The Microsoft DVD Navigator uses the following algorithm to determine region match while playing DVD discs on a PC:</span></span>

1.  <span data-ttu-id="bb565-105">Навигатор DVD получает регион диска, регион и регион декодера.</span><span class="sxs-lookup"><span data-stu-id="bb565-105">The DVD Navigator gets the disc region, drive region, and decoder region.</span></span>
2.  <span data-ttu-id="bb565-106">Если регион диска — "все регионы", DVD-навигатор воспроизводит диск.</span><span class="sxs-lookup"><span data-stu-id="bb565-106">If the disc region is "all regions," the DVD Navigator plays the disc.</span></span>
3.  <span data-ttu-id="bb565-107">Если диск не отмечен для всех регионов, Навигатор DVD проверяет, есть ли у декодера предустановленный регион.</span><span class="sxs-lookup"><span data-stu-id="bb565-107">If the disc is not marked for all regions, the DVD Navigator checks whether the decoder has a preset region.</span></span>
4.  <span data-ttu-id="bb565-108">Если у декодера есть предустановленный регион, который не соответствует региону диска, Навигатор DVD возвращает ошибку, указывающую на то, что не удается воспроизвести диск в текущей конфигурации DVD.</span><span class="sxs-lookup"><span data-stu-id="bb565-108">If the decoder has a preset region and it does not match the disc region, the DVD Navigator returns an error indicating that it cannot play the disc on the current DVD configuration.</span></span> <span data-ttu-id="bb565-109">Выполняет</span><span class="sxs-lookup"><span data-stu-id="bb565-109">(Exit)</span></span>
5.  <span data-ttu-id="bb565-110">Если область декодера не задана или совпадает с регионом диска, Навигатор DVD проверяет, совпадает ли регион диска с регионом диска.</span><span class="sxs-lookup"><span data-stu-id="bb565-110">If the decoder region is not set, or is the same as the disc region, the DVD Navigator checks whether the drive region is the same as the disc region.</span></span>
6.  <span data-ttu-id="bb565-111">Если регион диска соответствует региону диска, Навигатор DVD воспроизводит его.</span><span class="sxs-lookup"><span data-stu-id="bb565-111">If the drive region matches the disc region, the DVD Navigator plays the title.</span></span>
7.  <span data-ttu-id="bb565-112">В противном случае, если регион драйвера не соответствует региону диска, Навигатор DVD вызывает код для изменения региона диска.</span><span class="sxs-lookup"><span data-stu-id="bb565-112">Otherwise, if the driver region does not match the disc region, the DVD Navigator invokes the code to change the drive's region.</span></span> <span data-ttu-id="bb565-113">Если разрешенное число изменений региона исчерпано, попытка изменения региона завершится неудачей, и заголовок невозможно будет воспроизвести в этой системе.</span><span class="sxs-lookup"><span data-stu-id="bb565-113">If the allowed number of region changes has been exhausted, the region change attempt fails and the title cannot be played on that system.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb565-114">См. также</span><span class="sxs-lookup"><span data-stu-id="bb565-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb565-115">Поддержка смены региона DVD в Windows</span><span class="sxs-lookup"><span data-stu-id="bb565-115">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



