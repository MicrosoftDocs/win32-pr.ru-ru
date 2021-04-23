---
description: Обработка входных и выходных данных в коде DMO
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: Обработка входных и выходных данных в коде DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c6781d877f4c863161537fcc5b6a746691cfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344412"
---
# <a name="processing-codec-dmo-input-and-output"></a><span data-ttu-id="bae75-103">Обработка входных и выходных данных в коде DMO</span><span class="sxs-lookup"><span data-stu-id="bae75-103">Processing Codec DMO Input and Output</span></span>

<span data-ttu-id="bae75-104">После настройки входного типа и типа выходных данных для DMO можно начать обработку образцов данных.</span><span class="sxs-lookup"><span data-stu-id="bae75-104">When you have configured the input type and output type for a DMO, you can begin processing data samples.</span></span> <span data-ttu-id="bae75-105">Передайте примеры в DMO для обработки с помощью метода **имедиаобжект::P роцессинпут** , а затем извлеките обработанный пример, вызвав **Имедиаобжект::P роцессаутпут**.</span><span class="sxs-lookup"><span data-stu-id="bae75-105">You pass samples to the DMO for processing using the **IMediaObject::ProcessInput** method, and then retrieve the processed sample by calling **IMediaObject::ProcessOutput**.</span></span> <span data-ttu-id="bae75-106">Необходимо задать точные метки времени и длительности для всех пройденных выборок.</span><span class="sxs-lookup"><span data-stu-id="bae75-106">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="bae75-107">Метки времени не являются строго необходимыми, но помогают поддерживать синхронизацию аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="bae75-107">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="bae75-108">Если у вас нет меток времени для выборки, лучше оставить их, не используя неопределенные значения.</span><span class="sxs-lookup"><span data-stu-id="bae75-108">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bae75-109">См. также</span><span class="sxs-lookup"><span data-stu-id="bae75-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bae75-110">Работа с кодеками дмос</span><span class="sxs-lookup"><span data-stu-id="bae75-110">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 



