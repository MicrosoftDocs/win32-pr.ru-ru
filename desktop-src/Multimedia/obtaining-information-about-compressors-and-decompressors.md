---
title: Получение сведений об упаковщиках и декомпрессорах
description: Получение сведений об упаковщиках и декомпрессорах
ms.assetid: 2f1edfd0-dd30-42ea-a5ae-24265d3f8af3
keywords:
- Диспетчер сжатия видео (ВКМ), получение сведений об компрессорах
- ВКМ (диспетчер сжатия видео), получение сведений об компрессорах
- Функция Икжетинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874793233ef0aec4de5b372573fb8dcd79f5d875
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410731"
---
# <a name="obtaining-information-about-compressors-and-decompressors"></a><span data-ttu-id="d83e4-106">Получение сведений об упаковщиках и декомпрессорах</span><span class="sxs-lookup"><span data-stu-id="d83e4-106">Obtaining Information About Compressors and Decompressors</span></span>

<span data-ttu-id="d83e4-107">В следующем примере функция [**икжетинфо**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) используется для получения сведений об упаковщике или декомпрессоре.</span><span class="sxs-lookup"><span data-stu-id="d83e4-107">The following example uses the [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) function to obtain information about a compressor or decompressor.</span></span>


```C++
ICINFO ICInfo; 
ICGetInfo(hIC, &ICInfo, sizeof(ICInfo)); 
 
```



<span data-ttu-id="d83e4-108">В следующем примере для получения значений по умолчанию используются макросы [**икжетдефаулткэйфрамерате**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) и [**икжетдефаулткуалити**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) .</span><span class="sxs-lookup"><span data-stu-id="d83e4-108">The following example uses the [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) and [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macros to obtain the default values.</span></span>


```C++
DWORD dwKeyFrameRate, dwQuality; 
dwKeyFrameRate = ICGetDefaultKeyFrameRate(hIC); 
dwQuality = ICGetDefaultQuality(hIC); 
 
```



<span data-ttu-id="d83e4-109">В следующем примере используются макросы [**иккуерябаут**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) и [**икабаут**](/windows/desktop/api/Vfw/nf-vfw-icabout) для вывода диалогового окна о программе для сжатия или распаковки, если диалоговое окно существует.</span><span class="sxs-lookup"><span data-stu-id="d83e4-109">The following example uses the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) and [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macros to display an About dialog box for the compressor or decompressor, if the dialog box exists.</span></span>


```C++
// If the compressor has an About dialog box, display it.

if ( ICQueryAbout(hIC)) ICAbout(hIC, hwndApp); 
 
```



 

 




