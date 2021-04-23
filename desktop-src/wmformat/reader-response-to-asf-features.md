---
title: Ответ читателя на функции ASF
description: Ответ читателя на функции ASF
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- Windows Media Format SDK, средства чтения, отклики на функции ASF
- Расширенный системный формат (ASF), ответы читателей на функции
- ASF (Расширенный системный формат), ответы читателей на функции
- ответы читателя на функции ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291752d2d011fbc8b0a3e5211c5d8926f94b1cbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700555"
---
# <a name="reader-response-to-asf-features"></a><span data-ttu-id="70a75-107">Ответ читателя на функции ASF</span><span class="sxs-lookup"><span data-stu-id="70a75-107">Reader Response to ASF Features</span></span>

<span data-ttu-id="70a75-108">Большинство специальных возможностей файлов ASF можно задать в файлах, чтобы взаимодействовать с пользовательскими воспроизводимыми приложениями, предназначенными для их решения.</span><span class="sxs-lookup"><span data-stu-id="70a75-108">Most of the special ASF file features can be set in files to interact with custom playing applications designed to handle them.</span></span> <span data-ttu-id="70a75-109">Однако некоторые функции имеют встроенную поддержку в объекте Reader.</span><span class="sxs-lookup"><span data-stu-id="70a75-109">However, some of the features have built-in support in the reader object.</span></span>

<span data-ttu-id="70a75-110">Объект модуля чтения автоматически выбирает потоки из наборов, которые являются взаимоисключающими по скорости.</span><span class="sxs-lookup"><span data-stu-id="70a75-110">The reader object will automatically select streams from sets that are mutually exclusive by bit rate.</span></span> <span data-ttu-id="70a75-111">Этот особый случай называется несколькими битовыми частотами (MBR).</span><span class="sxs-lookup"><span data-stu-id="70a75-111">This special case is referred to as multiple bit rate (MBR).</span></span> <span data-ttu-id="70a75-112">Поток, выбираемый средством чтения, основан на скорости потока.</span><span class="sxs-lookup"><span data-stu-id="70a75-112">The stream the reader selects is based on the bit rate of the stream.</span></span> <span data-ttu-id="70a75-113">Номер потока и порядок, в котором он был добавлен в объект взаимного исключения, не имеют значения для автоматического выбора.</span><span class="sxs-lookup"><span data-stu-id="70a75-113">The stream number and the order in which it was added to the mutual exclusion object are irrelevant to the automatic selection.</span></span> <span data-ttu-id="70a75-114">Если файл содержит более одного набора потоков, взаимоисключающих с интенсивностью битов, средство чтения выберет потоки на основе вычисления наилучшего использования доступной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="70a75-114">If a file includes more than one set of streams mutually exclusive by bit rate, the reader will select streams based on calculating the best use of the available bandwidth.</span></span>

<span data-ttu-id="70a75-115">Взаимное исключение на основе языка задается с помощью параметра OUTPUT перед воспроизведением.</span><span class="sxs-lookup"><span data-stu-id="70a75-115">Language-based mutual exclusion is set using an output setting, before playback.</span></span> <span data-ttu-id="70a75-116">Если вы объединяете взаимное исключение на основе языка и поразрядной скорости, следует сгруппировать взаимоисключающие потоки с побитовой скоростью в зависимости от языка, а затем сделать группы взаимоисключающими по языку.</span><span class="sxs-lookup"><span data-stu-id="70a75-116">If you combine both language and bit-rate-based mutual exclusion, you should group the bit-rate-based mutually exclusive streams by language and then make the groups mutually exclusive by language.</span></span> <span data-ttu-id="70a75-117">Модуль чтения сначала проверяет язык, а затем определяет, какую скорость использовать.</span><span class="sxs-lookup"><span data-stu-id="70a75-117">The reader will check the language first, and then determine which bit rate to use.</span></span>

<span data-ttu-id="70a75-118">Определение приоритетов потоков задается с помощью массива записей.</span><span class="sxs-lookup"><span data-stu-id="70a75-118">Stream prioritization is set using an array of records.</span></span> <span data-ttu-id="70a75-119">Записи в массиве находятся в порядке убывания приоритета.</span><span class="sxs-lookup"><span data-stu-id="70a75-119">The records in the array are in descending order of priority.</span></span> <span data-ttu-id="70a75-120">Последний поток в массиве является первым, который будет удален модулем чтения.</span><span class="sxs-lookup"><span data-stu-id="70a75-120">The last stream in the array is the first that will be dropped by the reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70a75-121">См. также</span><span class="sxs-lookup"><span data-stu-id="70a75-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70a75-122">**Функции файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="70a75-122">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="70a75-123">**Взаимное исключение**</span><span class="sxs-lookup"><span data-stu-id="70a75-123">**Mutual Exclusion**</span></span>](mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="70a75-124">**Определение приоритетов потоков**</span><span class="sxs-lookup"><span data-stu-id="70a75-124">**Stream Prioritization**</span></span>](stream-prioritization.md)
</dt> </dl>

 

 




