---
title: Поиск по времени с помощью синхронного модуля чтения
description: Поиск по времени с помощью синхронного модуля чтения
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- Расширенный формат систем (ASF), поиск по времени
- ASF (Расширенный системный формат), поиск по времени
- Расширенный формат систем (ASF), синхронные средства чтения
- ASF (Расширенный системный формат), синхронные средства чтения
- синхронные читатели, поиск по времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a43e914a6fc0d320860db61f4747cbee3033e9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788809"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a><span data-ttu-id="f8923-108">Поиск по времени с помощью синхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="f8923-108">To Seek By Time Using the Synchronous Reader</span></span>

<span data-ttu-id="f8923-109">Чтобы найти данные с помощью синхронного модуля чтения, укажите диапазон для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="f8923-109">To seek for data using the synchronous reader, you specify a range for playback.</span></span> <span data-ttu-id="f8923-110">Диапазон определяется начальным временем презентации и длительностью (в 100-наносекундных единицах).</span><span class="sxs-lookup"><span data-stu-id="f8923-110">A range is defined by a starting presentation time and a duration, both in 100-nanosecond units.</span></span>

<span data-ttu-id="f8923-111">Чтобы найти данные в файле ASF с помощью синхронного модуля чтения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f8923-111">To seek data in an ASF file by presentation time using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="f8923-112">Укажите время и длительность выполнения образца доставки, вызвав [**ивмсинкреадер:: SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange).</span><span class="sxs-lookup"><span data-stu-id="f8923-112">Specify a starting time and duration for sample delivery by calling [**IWMSyncReader::SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange).</span></span> <span data-ttu-id="f8923-113">Этот метод не требует указания номера потока, так как время представления каждого потока должно быть уже синхронизировано.</span><span class="sxs-lookup"><span data-stu-id="f8923-113">This method does not require you to specify a stream number because the presentation times of each stream should already be synchronized.</span></span>
2.  <span data-ttu-id="f8923-114">Начало извлечения образцов с вызовами метода [**ивмсинкреадер:: жетнекстсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="f8923-114">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="f8923-115">Продолжайте работу, как обычно с синхронным модулем чтения.</span><span class="sxs-lookup"><span data-stu-id="f8923-115">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8923-116">См. также</span><span class="sxs-lookup"><span data-stu-id="f8923-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8923-117">**Интерфейс Ивмсинкреадер**</span><span class="sxs-lookup"><span data-stu-id="f8923-117">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="f8923-118">**Чтение файлов с помощью синхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="f8923-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




