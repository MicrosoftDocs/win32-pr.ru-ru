---
title: Изменение размера диалогового окна "приобретение лицензий"
description: Изменение размера диалогового окна "приобретение лицензий"
ms.assetid: e091d981-1574-4ffc-bdc4-b92f74396cb7
keywords:
- Проигрыватель Windows Media, диалоговое окно "изменение размера приобретения лицензии"
- Проигрыватель Windows Media, диалоговое окно "получение лицензии"
- Проигрыватель Windows Media, DRM_LicenseAcqURL атрибут
- диалоговое окно "изменение размера приобретения лицензии"
- Диалоговое окно "получение лицензии"
- DRM_LicenseAcqURL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440683ce65417653251bbed58d59c4d9a34dbc57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411150"
---
# <a name="resizing-the-license-acquisition-dialog-box"></a><span data-ttu-id="b8242-109">Изменение размера диалогового окна "приобретение лицензий"</span><span class="sxs-lookup"><span data-stu-id="b8242-109">Resizing the License Acquisition Dialog Box</span></span>

<span data-ttu-id="b8242-110">Можно добавить параметры строки запроса к URL-адресу, указанному для атрибута **DRM \_ лиценсеаккурл** , чтобы указать размер для диалогового окна Windows Media Player 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b8242-110">You can append query string parameters to the URL you provide for the **DRM\_LicenseAcqURL** attribute to specify a size for the Windows Media Player 10 or later license acquisition dialog box.</span></span> <span data-ttu-id="b8242-111">В следующей таблице перечислены параметры.</span><span class="sxs-lookup"><span data-stu-id="b8242-111">The following table lists the parameters.</span></span>



| <span data-ttu-id="b8242-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="b8242-112">Parameter</span></span> | <span data-ttu-id="b8242-113">Описание</span><span class="sxs-lookup"><span data-stu-id="b8242-113">Description</span></span>                                        |
|-----------|----------------------------------------------------|
| <span data-ttu-id="b8242-114">*длгкс*</span><span class="sxs-lookup"><span data-stu-id="b8242-114">*DlgX*</span></span>    | <span data-ttu-id="b8242-115">Задает ширину диалогового окна в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b8242-115">Specifies the width of the dialog box, in pixels.</span></span>  |
| <span data-ttu-id="b8242-116">*длги*</span><span class="sxs-lookup"><span data-stu-id="b8242-116">*DlgY*</span></span>    | <span data-ttu-id="b8242-117">Задает высоту диалогового окна в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b8242-117">Specifies the height of the dialog box, in pixels.</span></span> |



 

<span data-ttu-id="b8242-118">Например, следующий URL-адрес приобретения лицензии приведет к тому, что диалоговое окно "получение лицензии" будет открываться с размером 800 на 600 пикселей:</span><span class="sxs-lookup"><span data-stu-id="b8242-118">For example, the following license acquisition URL would cause the license acquisition dialog box to open with a size of 800 by 600 pixels:</span></span>


```C++
https://www.proseware.com/license/lic_acq.htm?DlgX=800&DlgY=600

```



<span data-ttu-id="b8242-119">Максимальный размер диалогового окна никогда не превысит размеры текущего экрана минус 20 пикселей.</span><span class="sxs-lookup"><span data-stu-id="b8242-119">The maximum size for the dialog box will never exceed the current screen dimensions minus 20 pixels.</span></span> <span data-ttu-id="b8242-120">Минимальный размер — 333 x 210 пикселей (размер по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="b8242-120">The minimum size is 333 x 210 pixels (the default size).</span></span>

<span data-ttu-id="b8242-121">Для этого компонента требуется проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b8242-121">This feature requires Windows Media Player 10 or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8242-122">См. также</span><span class="sxs-lookup"><span data-stu-id="b8242-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8242-123">**Проигрыватель Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b8242-123">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




