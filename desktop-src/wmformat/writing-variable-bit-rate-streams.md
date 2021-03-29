---
title: Запись потоков переменной скорости
description: Запись потоков переменной скорости
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- Расширенный системный формат (ASF), написание потоков VBR
- ASF (Расширенный системный формат), написание потоков VBR
- Переменная скорость (VBR), запись потоков
- VBR (переменная скорость), запись потоков
- потоки, запись VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981cbae04085c4bf4f771d9dd29e30752427cdc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788683"
---
# <a name="writing-variable-bit-rate-streams"></a><span data-ttu-id="5317d-108">Запись потоков переменной скорости</span><span class="sxs-lookup"><span data-stu-id="5317d-108">Writing Variable Bit Rate Streams</span></span>

<span data-ttu-id="5317d-109">Потоки с переменной скоростью (VBR) записываются так же, как потоки с постоянным битом потока (CBR).</span><span class="sxs-lookup"><span data-stu-id="5317d-109">Variable bit rate (VBR) streams are written the same way as constant bit rate (CBR) streams.</span></span> <span data-ttu-id="5317d-110">Единственное отличие заключается в обработке, выполняемой внутри модуля записи и кодеках.</span><span class="sxs-lookup"><span data-stu-id="5317d-110">The only difference is in the processing performed internally by the writer and the codecs.</span></span> <span data-ttu-id="5317d-111">Однако скорость потока, основанная на скорости (как с ограниченными, так и с неограниченными), требует передачи предварительной обработки в модуль записи.</span><span class="sxs-lookup"><span data-stu-id="5317d-111">However, bit rate based VBR (both constrained and unconstrained) requires a preprocessing pass in the writer.</span></span>

<span data-ttu-id="5317d-112">Необходимо проверить возвращаемое значение для первого вызова, внесенного в [**ивмвритер:: вритесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="5317d-112">You should check the return value for the first call you make to [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) for each stream.</span></span> <span data-ttu-id="5317d-113">Если возвращен код ошибки NS \_ E \_ недопустимое \_ число \_ проходов, поток требует передачи предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="5317d-113">If the error code returned is NS\_E\_INVALID\_NUM\_PASSES, the stream requires a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5317d-114">См. также</span><span class="sxs-lookup"><span data-stu-id="5317d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5317d-115">**Использование кодировки Two-Pass**</span><span class="sxs-lookup"><span data-stu-id="5317d-115">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="5317d-116">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="5317d-116">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




