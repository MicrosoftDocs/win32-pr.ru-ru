---
description: Обработка входных и выходных файлов MFT кодека
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: Обработка входных и выходных файлов MFT кодека
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af3a16fa1855574f1b7618bc0d41bf85c15412f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263496"
---
# <a name="processing-codec-mft-input-and-output"></a><span data-ttu-id="7d3c7-103">Обработка входных и выходных файлов MFT кодека</span><span class="sxs-lookup"><span data-stu-id="7d3c7-103">Processing Codec MFT Input and Output</span></span>

<span data-ttu-id="7d3c7-104">После настройки типа входных данных и типа выходных данных для MFT можно начать обработку образцов данных.</span><span class="sxs-lookup"><span data-stu-id="7d3c7-104">When you have configured the input type and output type for an MFT, you can begin processing data samples.</span></span> <span data-ttu-id="7d3c7-105">Передайте образцы в таблицу MFT для обработки с помощью метода [**имфтрансформ::P роцессинпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) , а затем извлеките обработанный пример, вызвав [**Имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="7d3c7-105">You pass samples to the MFT for processing by using the [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method, and then retrieve the processed sample by calling [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="7d3c7-106">Необходимо задать точные метки времени и длительности для всех пройденных выборок.</span><span class="sxs-lookup"><span data-stu-id="7d3c7-106">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="7d3c7-107">Метки времени не являются строго необходимыми, но помогают поддерживать синхронизацию аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="7d3c7-107">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="7d3c7-108">Если у вас нет меток времени для выборки, лучше оставить их, не используя неопределенные значения.</span><span class="sxs-lookup"><span data-stu-id="7d3c7-108">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d3c7-109">См. также</span><span class="sxs-lookup"><span data-stu-id="7d3c7-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d3c7-110">Работа с кодеками МФТС</span><span class="sxs-lookup"><span data-stu-id="7d3c7-110">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



