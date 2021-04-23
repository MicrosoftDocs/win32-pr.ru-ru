---
title: Циклическое воспроизведение для МЦивнд
description: Циклическое воспроизведение (МЦивнд)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d6a22e917cf764b37444bcaf4afb0393e1c1b
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106188009"
---
# <a name="looping-playback-for-mciwnd"></a><span data-ttu-id="cad38-103">Циклическое воспроизведение для МЦивнд</span><span class="sxs-lookup"><span data-stu-id="cad38-103">Looping Playback for MCIWnd</span></span>

<span data-ttu-id="cad38-104">МЦивнд поддерживает воспроизведение в виде непрерывного цикла.</span><span class="sxs-lookup"><span data-stu-id="cad38-104">MCIWnd supports playback as a continuous loop.</span></span> <span data-ttu-id="cad38-105">Вы можете воспроизвести содержимое файла или устройства несколько раз в цикле с помощью макроса [**мЦивндсетрепеат**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) в сочетании с кнопкой **Воспроизведение** на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="cad38-105">You can play the content of a file or device repeatedly as a loop by using the [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) macro in combination with the **Play** button on the toolbar.</span></span> <span data-ttu-id="cad38-106">Устройство воспроизведения видео, МЦИАВИ, поддерживает циклы воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="cad38-106">The video playback device, MCIAVI, supports playback loops.</span></span> <span data-ttu-id="cad38-107">Чтобы определить, активировано ли непрерывное воспроизведение, используйте макрос [**мЦивнджетрепеат**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .</span><span class="sxs-lookup"><span data-stu-id="cad38-107">To determine if continuous playback has been activated, use the [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) macro.</span></span>

 

 




